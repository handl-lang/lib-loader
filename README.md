# lib-loader

The pure-handl module loader (`loader.hnl`), vendored by
`plugin-lib-handl`.

The package surface is pure `.hnl`: consumers copy `pkg.hnl` +
`src/**/*.hnl` via `handl-pkg-vendor` into `OUT_DIR` and embed them with
`include_str!` at their own build time (`plugin-lib-handl` does this —
the `handl-lib-loader` crate's `LOADER_HNL` const is no longer
consumed, and the crate shim is deleted).

## Layout

```text
src/index.hnl           the .hnl source (pure handl)
pkg.hnl                 package manifest — modules, deps, license
scripts/hnl-gate.sh     the gate
workflows/gate.yaml                   bupha entry (handl-gates)
```

## Gate

```bash
HNL=../host-cli/target/debug/hnl scripts/hnl-gate.sh
```

## License

MIT.

## Documentation

<https://handl-lang.github.io/docs/lib-loader/>
