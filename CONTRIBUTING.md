# Contributing to DeepRead

Thank you for helping make evidence-first reading more useful and trustworthy.

## Good contributions

- A reproducible bug report with a small source document or public URL.
- A focused fix with a regression test.
- Improvements to evidence tracing, PDF extraction, accessibility, or cross-host compatibility.
- A real output example generated from a public source, with provenance and reproduction steps.
- Documentation corrections that keep the portable Agent Skill and the full DSH plugin clearly separated.

Use [GitHub Discussions](https://github.com/xiehuan123/dsh-deepread/discussions) for usage questions and workflow ideas. Use an Issue for a reproducible defect or a scoped proposal.

## Before changing code

1. Read `AGENTS.md` and `docs/deepseek-harness-integration.md`.
2. Confirm whether the change belongs to the Node Host (`src/index.ts`, `src/host/`) or browser client (`src/client/`).
3. Do not edit generated files under `lib/types/` or `lib/client.js` directly.
4. Keep the npm id `dsh-deepread`, Cordis/tool name `deepread`, and patch row id `deepread` distinct.
5. Preserve optional-service behavior: the Host tool must still activate without Web, storage, or jobs services.

For a larger change, open an Issue first so the interface and compatibility impact can be agreed before implementation.

## Development setup

DeepRead requires Node.js `^22.19 || >=24`.

```sh
npm install
npm run typecheck:host
npm run typecheck:browser
npm test
```

After browser-source changes, run `npm run build:client` and include the matching generated `lib/client.js` change.

## Pull requests

- Keep the change focused and explain the user-visible outcome.
- Link the originating Issue when one exists.
- Add or update tests for behavioral and packaging changes.
- Include screenshots for browser UI changes in both light and dark themes.
- Note which commands you ran and any verification you could not perform.
- Preserve unrelated working-tree changes and generated/source ownership rules.

By participating, you agree to follow the [Code of Conduct](CODE_OF_CONDUCT.md).
