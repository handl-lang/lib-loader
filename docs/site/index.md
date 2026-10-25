# lib-loader

The pure-handl module loader, embedded by `plugin-lib-handl`.

## What it is

`loader.hnl` resolves module imports at runtime — the module chain, import
splicing and name resolution — implemented in handl itself. Like the desugar
pass it is embedded by `plugin-lib-handl` rather than imported by users.

## Modules
- `src/index.hnl` — the loader: module discovery, import resolution, name binding


## Start here

- **Reference** — [public API](/lib-loader/reference/)
- **How-to** — [task recipes](/lib-loader/how-to/)
- **Explanation** — [design and rationale](/lib-loader/explanation/)

No tutorials: this repo is a building block used from Rust. End-to-end
walkthroughs live with the product that composes it — see the
[Handl platform](/handl/).
