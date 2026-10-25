# Explanation

## Why this crate exists

A loader written in the language it loads keeps the module system inside the
same semantics as user code: resolution is evaluated, not special-cased in Rust.
Separating it into its own repo makes that surface small enough to review.

## Where it sits

This crate belongs to the `engine-*` family. Plugins, kits and hosts reach it
through the kit's operation slot, so the engine can be swapped without touching a
language definition.

See the [reference](/lib-loader/reference/) for the API and the
[how-to guides](/lib-loader/how-to/) for tasks.
