# GitHub 收录与曝光审计（2026-08-30）

审计对象：[xiehuan123/dsh-deepread](https://github.com/xiehuan123/dsh-deepread)

本报告优先使用 `gh`、GitHub REST/GraphQL API、GitHub Code Search、相关仓库的 PR/Issue 和目录数据文件。GitHub Code Search 只代表当前可检索的默认分支内容，可能存在索引延迟；Traffic 数据只有仓库管理员可见，API 返回窗口截至 2026-08-27。

## 结论摘要

- GitHub 用户收藏口径：**41 Stars、3 Forks、0 Watchers**。
- 外部收录口径：GitHub Code Search 找到 **21 个外部仓库**含项目 URL 或包名引用；其中 **14 个**可归类为公开目录、注册表、商店或技能集合，其余 7 个主要是趋势历史、监控、摘要或隐藏候选，不能都算有效曝光。
- 另有 [Oh-My-DSH #21](https://github.com/like-study1/Oh-My-DSH/issues/21) 由维护者明确确认已收录，但其机器索引未出现在本次精确代码搜索结果中。因此按“当前代码可检索目录”是 14 个，按“加上维护者确认”是 **至少 15 个外部收录/集合**。
- 仍有 **10 个独立渠道待审**，另有 1 个隐藏候选；不应把它们计为已收录。
- 仓库自身目前 **0 个开放 Issue、0 个开放 PR**；历史共 3 个 Issue（全部关闭）和 2 个 PR（1 merged、1 closed）。
- 作者对外共提交 21 个相关 PR：**14 merged、5 open、2 closed**，覆盖 16 个外部仓库。另有一个机器人创建的 Agent Plugins PR 仍开放。
- GitHub Traffic 窗口内有 **2,631 views / 1,140 unique visitors**，以及 **590 clones / 323 unique cloners**。曝光已经形成，但首周峰值后明显回落。

## 审计后已执行动作

截至 2026-08-30，本轮审计已经转化为以下实际改进：

- GitHub 仓库已启用 Discussions；Homepage 已从 npm 改为项目 GitHub Pages；简介与 Topics 已补充 `fact-checking`、`pdf-analysis`、`research-tools` 等可发现关键词。
- README 中英文首屏已强化「观点—证据—原文位置」差异化表达，加入真实 Web 面板和真实输出案例；官网增加公众号入口和 **Appoint 实验室**关注区块。
- 已新增 CONTRIBUTING、Code of Conduct、Bug/Feature Issue 表单和 PR 模板，降低提问与贡献门槛。
- hidden candidate 已通过正式 [admission Issue #165](https://github.com/Ericwong5021/deepseek-plugin-store/issues/165) 获得 `gov:approved`，治理机器人已创建公开收录 [PR #166](https://github.com/Ericwong5021/deepseek-plugin-store/pull/166)，当前等待维护者合并。
- ranbot 的错误归属已通过 [awesome-skills PR #11](https://github.com/ranbot-ai/awesome-skills/pull/11) 从爬虫生成链路修正：保留 Antigravity 作为发现来源，但把 `repoUrl`、`skillUrl` 和作者回流指向 `xiehuan123/dsh-deepread`；当前 PR 可合并、等待维护者处理。
- 已生成 1280×640 的 GitHub Social Preview 素材；GitHub Settings 图片上传仍需在已登录的浏览器会话完成。

## 仓库与流量基线

| 指标 | 当前值 | 说明 |
| --- | ---: | --- |
| Stars | 41 | 最后一次新增 Star：2026-08-27 |
| Forks | 3 | 其中一个 Fork 有后续 push，一个 Fork 自身获得 1 Star |
| Watchers | 0 | 持续关注信号弱 |
| 自身 Issues | 3 closed / 0 open | 2 个功能反馈已在 1.0.0 处理；1 个目录邀请转交外部申请 |
| 自身 PRs | 1 merged / 1 closed / 0 open | 两个 PR 都由仓库所有者创建，尚无外部贡献者 PR |
| Releases | 3 | v0.3.1、v0.5.4、v1.0.0 |
| 最近 push | 2026-08-22 | 审计日距最近代码 push 8 天 |
| Community profile | 42% | 缺 CONTRIBUTING、Code of Conduct、Issue 模板、PR 模板 |
| Discussions | 未开启 | 缺少低门槛社区交流入口 |
| 自定义 Social Preview | 未设置 | 当前使用 GitHub 默认 Open Graph 图 |

来源：[仓库主页](https://github.com/xiehuan123/dsh-deepread)、[Issues](https://github.com/xiehuan123/dsh-deepread/issues?q=is%3Aissue+is%3Aclosed)、[Pull requests](https://github.com/xiehuan123/dsh-deepread/pulls?q=is%3Apr+is%3Aclosed)、[Releases](https://github.com/xiehuan123/dsh-deepread/releases)、[Traffic](https://github.com/xiehuan123/dsh-deepread/graphs/traffic)。

### 14 天 Traffic 窗口

| 指标 | 总量 | Unique |
| --- | ---: | ---: |
| Views | 2,631 | 1,140 |
| Clones | 590 | 323 |

方向性转化：`41 / 1,140 ≈ 3.6%` 的访客成为 Star，`323 / 1,140 ≈ 28.3%` 的访客产生 unique clone。两者不是严格同一 cohort，只适合做趋势判断。

- 浏览峰值：2026-08-18，406 views / 173 unique visitors。
- 窗口最后一天：2026-08-27，113 views / 62 unique visitors；较峰值分别下降约 72% 和 64%。
- Stars 主要集中在 8 月 16 日至 22 日：3 → 11 → 19 → 21 → 22 → 30 → 37；之后只在 8 月 24 日和 27 日各增加 2 个。
- 主要页面：仓库 Overview 1,482 views / 1,043 unique；中文 README 648 / 521。中文内容具有很强的实际需求。
- 主要引荐：github.com 511、项目 GitHub Pages 73、Bing 49、dsh-market.com 19、beancookie.github.io 19、dshfind.com 13、Google 12、npmjs.com 9、dshmarketplace.dev 9、plugin.dshdesk.com 6。

## 已收录与引用

### 代码搜索可确认的 14 个公开目录/集合

1. [ZeroPointRepo/awesome-dsh-plugins](https://github.com/ZeroPointRepo/awesome-dsh-plugins)
2. [imsai-sh/awesome-deepseek-harness-plugins](https://github.com/imsai-sh/awesome-deepseek-harness-plugins)
3. [star-power0/dsh-plugins](https://github.com/star-power0/dsh-plugins)
4. [unStone/dsh-xray](https://github.com/unStone/dsh-xray)
5. [yzfly/awesome-dsh-skills](https://github.com/yzfly/awesome-dsh-skills)
6. [beancookie/awesome-dsh-plugin](https://github.com/beancookie/awesome-dsh-plugin)
7. [davepoon/buildwithclaude](https://github.com/davepoon/buildwithclaude)
8. [fabioc-aloha/Alex_Skill_Mall](https://github.com/fabioc-aloha/Alex_Skill_Mall)
9. [fendouai/awesome-deepseek-harness](https://github.com/fendouai/awesome-deepseek-harness)
10. [neko233-com/dsh-desktop](https://github.com/neko233-com/dsh-desktop)
11. [ranbot-ai/awesome-skills](https://github.com/ranbot-ai/awesome-skills)
12. [ylwl1997/dshbase](https://github.com/ylwl1997/dshbase)
13. [zhu1090093659/dsh-web](https://github.com/zhu1090093659/dsh-web)
14. [znc15/dsh-web-plugins](https://github.com/znc15/dsh-web-plugins)

维护者另行确认：[Oh-My-DSH #21](https://github.com/like-study1/Oh-My-DSH/issues/21) 对应配置已由 [PR #27](https://github.com/like-study1/Oh-My-DSH/pull/27) 合并并写入机器索引。

### 不应算作有效公开收录的 7 类引用

这些引用来自趋势记录、历史快照、监控雷达、摘要或发现状态，例如 [github-trending](https://github.com/encoreshao/github-trending)、[upstream-radar](https://github.com/MicroMilo/upstream-radar)、[dsh-suite](https://github.com/whyihaveyou/dsh-suite)。它们证明项目被抓取或观察，不等于用户能通过目录发现并安装。

[deepseek-plugin-store 的候选记录](https://github.com/Ericwong5021/deepseek-plugin-store/blob/main/governance/state/candidates/95/xiehuan123-dsh-deepread.json)尤其明确标记为 `admission.status: candidate`、`visibility: hidden`，虽然 `admissionReady: true`，仍不能计为公开收录。

另一个需要修正的归属问题：[ranbot-ai/awesome-skills 的条目](https://github.com/ranbot-ai/awesome-skills/blob/main/data/skills/dsh-deepread.json)把 `repoUrl` 和 `skillUrl` 指向第三方再打包仓库 `sickn33/antigravity-awesome-skills`，而不是项目 canonical source。它能带来曝光，但会稀释来源归属和回流。

## 未收录、待审与失败项

### 10 个独立待审渠道

| 优先级 | 渠道 | 当前状态 | 建议 |
| --- | --- | --- | --- |
| P0 | [Agent Skill Exchange #44](https://github.com/agentskillexchange/skills/issues/44) | 维护者明确认可，但要求提交聚焦 `skills/dsh-deepread/SKILL.md` 的 PR；目前没有 PR | 立即按评论给出的 frontmatter 和验证命令提交 |
| P0 | [Agent Plugins PR #112](https://github.com/dmgrok/agent-plugins/pull/112) | 自动验证通过，PR open | 请求人工 review/merge，并更新版本描述到 1.0.0 |
| P0 | [Composio Awesome Codex Skills PR #235](https://github.com/composio-community/awesome-codex-skills/pull/235) | open | 已是 16k+ Stars 渠道，补充 1.0.0、真实输出和 canonical skill 路径后跟进一次 |
| P0 | [HelloGitHub #3553](https://github.com/521xueweihan/HelloGitHub/issues/3553) | open | 173k+ Stars，中文用户与现有流量高度匹配；用真实案例而非功能清单跟进 |
| P0 | [阮一峰周刊 #11210](https://github.com/ruanyf/weekly/issues/11210) | open | 101k+ Stars；突出“证据可追溯精读”与可复现示例 |
| P1 | [BehiSecc Awesome Claude Skills PR #577](https://github.com/BehiSecc/awesome-claude-skills/pull/577) | open | 10k+ Stars；更新到 1.0.0 后礼貌跟进一次 |
| P1 | [Composio Awesome Claude Plugins PR #417](https://github.com/composio-community/awesome-claude-plugins/pull/417) | open | 澄清 portable skill 与 DSH runtime plugin 的边界 |
| P1 | [Awesome Claude Code Toolkit PR #729](https://github.com/rohitg00/awesome-claude-code-toolkit/pull/729) | open | PR 自 8 月 16 日后无活动；确认仓库是否仍维护该目录 |
| P1 | [helloianneo Awesome Claude Code Skills PR #71](https://github.com/helloianneo/awesome-claude-code-skills/pull/71) | open | 项目更新较慢，跟进一次后降低投入 |
| P2 | [DSH Plugin Directory #154](https://github.com/alexchenzl/dsh-plugin-directory/issues/154) | open、无回复 | 目录规模较小；补充 1.0.0 后等待，不再重复提交 |

### 明确未成功或需谨慎重投

- [github/awesome-copilot #2683](https://github.com/github/awesome-copilot/issues/2683)：自动规范、lint、安装 smoke 和版本检查全部通过，但维护者以 Copilot 已内置 `/research` 为由拒绝。除非重新定位出与内置 research 明显不同的、Copilot 特有工作流，否则不建议原样重投。
- [VoltAgent/awesome-agent-skills #913](https://github.com/VoltAgent/awesome-agent-skills/pull/913)：closed without merge，维护者未给原因。该仓库 33k+ Stars，价值高，但只应在先读最新贡献规范、做明显差异化定位后再提一次，避免重复投稿。
- [lmy414/dshregistry #1](https://github.com/lmy414/dshregistry/issues/1)：Issue 已关闭，但无维护者确认、无评论，本次 Code Search 也未找到当前条目，不能算已收录。
- [deepseek-plugin-store candidate](https://github.com/Ericwong5021/deepseek-plugin-store/blob/main/governance/state/candidates/95/xiehuan123-dsh-deepread.json)：检查通过但仍 hidden，需要维护者 admission，不是公开目录条目。

## PR / Issue 盘点

### 本仓库

- Issues：3 个，全部关闭。[#1](https://github.com/xiehuan123/dsh-deepread/issues/1) 和 [#2](https://github.com/xiehuan123/dsh-deepread/issues/2) 是真实产品反馈并已在 1.0.0 处理；[#3](https://github.com/xiehuan123/dsh-deepread/issues/3) 是目录邀请并已转外部申请。
- PRs：2 个；[#5](https://github.com/xiehuan123/dsh-deepread/pull/5) merged，[#4](https://github.com/xiehuan123/dsh-deepread/pull/4) closed。两者均由仓库所有者创建。
- 判断：维护响应速度好，但尚未形成外部贡献与公开讨论，社区参与面偏弱。

### 外部推广 PR / Issue

- 作者提交的相关外部 PR：21 个，14 merged、5 open、2 closed，覆盖 16 个仓库。
- 以项目 URL 搜索到的全部相关外部 PR：20 个，13 merged、6 open、1 closed，覆盖 18 个仓库；这里包含其他维护者或机器人发起的 PR，搜索口径与“作者提交”不同。
- 作者提交的外部收录 Issue：10 个，其中 5 open、5 closed。Agent Plugins 的 open Issue 与自动生成的 open PR 是同一渠道，不能重复算作两个待审渠道。

## 增长空间判断

项目有增长空间，而且空间不小，但已经从“缺目录曝光”转为“曝光转化与社区信任不足”。主要证据：

1. **首周传播有效。** 12 天左右获得 41 Stars、3 Forks，且 323 位 unique cloners，说明价值主张能驱动实际尝试。
2. **曝光正在衰减。** 浏览和 Star 都在 8 月 22 日后明显放缓，最近 push 也停在 8 月 22 日。
3. **目录数量已不少，目录流量却有限。** 可见目录引荐合计远低于 GitHub 本站和项目 Pages；继续广撒小目录的边际收益低。
4. **中文转化机会突出。** 中文 README 有 521 unique visitors，HelloGitHub 和阮一峰周刊是最契合的待审大渠道。
5. **社区信任信号不足。** 0 Watchers、无 Discussions、无外部 PR、Community profile 42%，会压低访问者长期关注和贡献意愿。
6. **展示转化仍可提升。** README 内容完整，但首屏主要是流程 SVG；仓库未设置自定义社交分享图，也缺少 20–30 秒真实 UI/输出演示。

## 建议执行顺序

### P0：先完成已有高价值待审，不再新增一批低质量投稿

1. 提交 Agent Skill Exchange 要求的 focused PR。
2. 跟进 Agent Plugins #112、Composio Codex #235、HelloGitHub #3553、阮一峰周刊 #11210。
3. 对仍开放的旧 PR 统一补一条简短 1.0.0 更新，包含 release、canonical skill 路径和一个真实输出链接；只跟进一次。
4. 修正 ranbot 条目的 canonical source；推动 hidden candidate 转 admission。

### P1：提高访问到 Star、试用和贡献的转化

1. 设置自定义 GitHub Social Preview，文案只讲一个结果：`PDF/文章 → 可追溯观点—证据—位置`。
2. README 首屏增加一张真实结果卡片截图或 20–30 秒 GIF，并在首屏放一个最短可复现示例。
3. 将仓库 Homepage 从 npm 页面改为已有 GitHub Pages 产品页；npm 继续保留 badge 和安装链接。
4. 补 CONTRIBUTING、Issue 模板、PR 模板、Code of Conduct；开启 Discussions，并准备 2–3 个 `good first issue`。
5. 在 README 加“Roadmap / What help is wanted”，把 0 open issue 转为可参与的公开工作面。

### P1：围绕已有中文需求做内容曝光

优先发布三个可复现案例，而不是再写一篇功能总览：

- 微信公众号文章：观点与证据核验；
- PDF/论文：页码级证据定位与关键数据表；
- 架构文档：决策、证据、限制条件与知识地图。

每个案例都使用同一结构：输入材料 → 普通摘要遗漏什么 → DeepRead 输出 → 可复现命令 → 真实文件链接。项目已有 GitHub Pages 引荐 73 次，可把 Pages 建成案例落地页，而不是只做 README 镜像。

### P2：建立可量化的两周增长实验

每个外部渠道使用可区分的落地页或查询参数，记录：referrer、unique visitors、Stars、clones、安装/问题反馈。两周目标建议：

- Stars：41 → 60；
- Watchers：0 → 3；
- 外部贡献者 PR：0 → 1；
- Community profile：42% → 80% 以上；
- 完成至少 3 个 P0 待审渠道；
- 让非 GitHub/non-direct referrer 的有效访问占比提升。

如果两周后目录跟进没有带来可测流量，应停止继续铺目录，把精力转向真实案例、短演示和集成合作。

## 可复现的主要 `gh` 查询口径

```sh
gh repo view xiehuan123/dsh-deepread --json stargazerCount,forkCount,watchers,issues,pullRequests,createdAt,pushedAt
gh issue list --repo xiehuan123/dsh-deepread --state all
gh pr list --repo xiehuan123/dsh-deepread --state all
gh search code '"xiehuan123/dsh-deepread"' --limit 100
gh search code '"dsh-deepread"' --limit 100
gh search prs 'dsh-deepread author:xiehuan123' --limit 100
gh search issues '"xiehuan123/dsh-deepread"' --limit 100
gh api repos/xiehuan123/dsh-deepread/traffic/views
gh api repos/xiehuan123/dsh-deepread/traffic/clones
gh api repos/xiehuan123/dsh-deepread/traffic/popular/referrers
gh api repos/xiehuan123/dsh-deepread/community/profile
```
