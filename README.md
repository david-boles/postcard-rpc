# Postcard RPC

> **Fork note (branch `embassy-executor-0.10`):** this is upstream release
> [`v0.12.1`](https://github.com/jamesmunns/postcard-rpc/releases/tag/v0.12.1)
> plus only the changes needed to use `embassy-executor` 0.10. It contains no
> other unreleased upstream work. Changes relative to `v0.12.1`:
>
> - `embassy-executor` dependency `0.9` -> `0.10`, and `embassy_spawn` now takes
>   the `Result<SpawnToken, SpawnError>` returned by `#[task]` functions in
>   executor 0.10 (net library diff of upstream PR #167, `d30141f`).
> - `host_client/webusb.rs`: two-line fix from upstream `eeb2e05` so the
>   `webusb` feature compiles with `js-sys`/`web-sys` >= 0.3.95 (typed arrays).
>   Unmodified `v0.12.1` fails to compile with current versions of those crates.
> - `example/esp32c6-serial` taken from upstream `2469ebc` (esp-hal ~1.2,
>   esp-rtos 0.4, embassy-executor 0.10). Other examples are not updated.

A host (PC) and client (MCU) library for handling RPC-style request-response types.

See [overview.md](./docs/overview.md) for documentation.

See the [`postcard-rpc` book](https://onevariable.com/postcard-rpc-book/) for a walk-through example.

You can also watch James' [RustNL talk](https://www.youtube.com/live/XLefuzE-ABU?t=24300) for a video explainer of what this crate does.

## License

Licensed under either of

- Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE) or
  <http://www.apache.org/licenses/LICENSE-2.0>)
- MIT license ([LICENSE-MIT](LICENSE-MIT) or <http://opensource.org/licenses/MIT>)

at your option.

### Contribution

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in the work by you, as defined in the Apache-2.0 license, shall be
dual licensed as above, without any additional terms or conditions.
