# lib-loader

The pure-handl module loader (`loader.hnl`), vendored by
`plugin-lib-handl`.

## Layout

| path | role |
| --- | --- |
| `src/index.hnl` | the .hnl source (pure handl) |
| `pkg.hnl` | package manifest — modules, deps, license |
| `docs/` | site docs (`site.yaml` + `site/`) |
| `scripts/hnl-gate.sh`, `ci.sh` | the gate / bupha entry |

## Contract

- Pure `.hnl` package surface: consumers copy `pkg.hnl` +
  `src/**/*.hnl` via `handl-pkg-vendor` into `OUT_DIR` and embed them
  with `include_str!` at their own build time (`plugin-lib-handl`
  does this). No Rust crate ships here.
- No `Cargo.toml` — the package is vendored source, not a crate.

## Verification

```bash
HNL=../host-cli/target/debug/hnl scripts/hnl-gate.sh
```

## License

MIT.

<!-- myco:agent-awareness -->

## Agent awareness

- Session start / any work discussion: run `myco status --prompt`
  before proposing next steps — know the board first.
- User describes new work → offer to capture it (`myco todo add`,
  `issue new`, `proposal new`). Don't wait to be asked.
- Picking up a task: `myco resume <ID>` is the briefing.
- Wrapping up: `myco handoff <ID>` anything resumable; keep statuses
  honest (claimed → in-progress → blocked/done).

<!-- /myco:agent-awareness -->
