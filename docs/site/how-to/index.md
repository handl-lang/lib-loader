# How-to guides

Task recipes. Each assumes sibling checkouts of this repo and of the platform
repos it patches.

## Follow an import

Trace the loader's resolution for a concrete path — a resolution surprise is almost always a name mapping, not a missing file.

## Change resolution rules

Edit `loader.hnl` and rerun the plugin's tests; the loader is data the runtime evaluates, so no Rust rebuild of the loader is needed.
