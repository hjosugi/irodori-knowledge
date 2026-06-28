# irodori-knowledge

Knowledge-base and batch-job primitives extracted from Irodori Table.

This workspace holds the pieces the desktop app builds on but that evolve
independently:

- `irodori-error` — the shared `IrodoriError` / `Result` vocabulary;
- `irodori-jobs` — the batch-job runtime (`JobRuntime`: progress, cancellation,
  retries, concurrency, checkpoint/resume) and the operation envelope `run_job`;
- `irodori-knowledge` — a disk-backed knowledge store (sources, snapshots, FTS
  search) and the streaming, flat-memory inverted-index builder.

The dependency flow is one-way: `irodori-error → irodori-jobs → irodori-knowledge`.
None of them depend on the Irodori desktop shell.

## Development

```sh
cargo test
```

Irodori Table consumes these crates as version-tagged Git dependencies so the app
can stay slimmer while the job/knowledge contracts evolve independently.

## License

Irodori-authored code in this repository is available under `MIT OR 0BSD` unless
a file says otherwise. See [LICENSE](LICENSE).

## Disclaimer

These crates are shared development components for Irodori Table. For public
product caveats, warranty notes, and preview-status guidance, see the Irodori
Table [disclaimer](https://hjosugi.github.io/irodori-docs/disclaimer.html).
