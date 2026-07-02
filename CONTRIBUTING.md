# Contributing

`irodori-knowledge` contains shared error, job, and knowledge-store crates used
by Irodori Table and sibling Rust hosts.

## Clean-Room Rules

Follow the Irodori clean-room policy before using reference products, source
code, snippets, generated assets, official docs snapshots, or database-client
behavior notes:

<https://hjosugi.github.io/irodori-docs/clean-room.html>

Project-authored code uses `MIT OR 0BSD` unless a file states otherwise.

## Local Checks

```sh
cargo fmt --all -- --check
cargo test --workspace
```

Knowledge-source and generated-doc changes should be made from source data or
generators in the owning repository, not by hand-editing generated snapshots.
