# BUGFIX — 1.0.2

## Bug：知识地图导出 FreeMind（.mm）时四类条目被静默丢弃

### 标题
map 模式下，`items` 中 type 为 `数据`、`隐含前提`、`反对意见`、`核心结论` 的条目在 Markdown 报告与 HTML 分节中正常出现，但在 FreeMind（.mm）导出（以及 HTML 报告末尾的思维导图树）中整组消失，无任何提示。

### 证据链（修复前）
- 提示词模式 `MAP_SCHEMA`（`src/host/plugin.ts`）规定 items 的 type 十选一：核心结论、分论点、原因或作用机制、事实、数据、案例、隐含前提、反对意见、限制条件、可执行建议；`sanitizeMap` 不过滤未知 type，十类都会进入结果数据。
- `renderMapMarkdown`（`src/host/export.ts`）逐条渲染全部 items；`buildHtml` 按十类分组渲染。
- 但 `buildMindTree` 的 map 分支只遍历六类：`['分论点', '原因或作用机制', '事实', '案例', '限制条件', '可执行建议']`，其余四类从未被访问。`buildFreeMind` 与 HTML 的思维导图树共用 `buildMindTree`，故两处同时丢数据。
- 最小复现（离线，mock `ctx.fs` 捕获 `attachExports(value, 'mm')` 写出的内容，样本含五类各一条）：
  - 修复前：`数据条目X markdown=true freemind=false`、`隐含前提条目Y markdown=true freemind=false`、`反对意见条目Z markdown=true freemind=false`，脚本 exit 1。
  - `git stash` 回退到上游基线复跑，输出逐字一致、exit 1，证明为上游既有缺陷，非本 fork 引入。

### 根因
`buildMindTree` 的分组类型清单是手写子集，与 MAP_SCHEMA 的十类枚举及 `buildHtml` 的十类清单脱节，新增/其余类型在导图构建时被静默跳过。

### 改动文件
- `src/host/export.ts`：`buildMindTree` map 分支的分组类型清单由六类补全为与 MAP_SCHEMA、`buildHtml` 一致的十类（保持 `buildHtml` 的顺序）；`lib/types/host/export.js` 为其构建产物（仓库约定提交构建产物）。
- 版本同步（1.0.1 → 1.0.2，仓库 AGENTS.md 要求六处版本源一致）：`package.json`、`package-lock.json`（根 + `packages['']`）、`dsh-plugin.json`、`plugin.json`、`.claude-plugin/plugin.json`、`.codex-plugin/plugin.json`；`package.json` 的 `repository.url` 改指本 fork 落点仓。
- `README.md` 顶部追加中文 fork 说明头，上游原文一字未删；新增 `UPSTREAM.md`、本文件。`LICENSE` 原样保留。
- 注意：`src/host/export.ts` 中 FreeMind 的 `<map version="1.0.1">` 是 FreeMind 文件格式版本，不是包版本，未改动。

### 复验结果
- 复现脚本：修复后五类条目在 .mm 中全部保留，exit 0。
- `npm run build`、`npm run typecheck:host`、`npm run typecheck:browser` 均通过。
- 仅含本修复（版本仍为 1.0.1）时 `npm test` 全量 exit 0，与上游基线（exit 0）逐项一致，零回归。

### 验证边界
- 版本升至 1.0.2 后，`test/release-docs-contract.mjs` 会失败：该测试把已发布的 1.0.1 钉死在断言中（包版本字面值、`docs/releases/1.0.1.md`、README/升级指南中的 1.0.1 安装口径），属于上游发版仪式门禁。本 fork 不伪造 1.0.2 的 release notes / 升级指南，故未迁就修改该测试与已发布文档；其余 29 个测试文件在 1.0.2 下逐个复跑全部通过；该文件实测失败点正是首条断言 `packageJson.version === '1.0.1'`（actual: '1.0.2'），六处版本源彼此仍一致。
- 未在真实 DeepSeek Harness 宿主中做端到端导出验证；复现走的是与宿主相同的 `createExportTools` + `attachExports` 代码路径（mock 文件服务捕获写出内容）。
