# tir

The canonical home for the **Tx3 Transaction Intermediate Representation (TIR)** — both the
specification and the reference Rust implementation.

TIR is the compiled, reduced AST that the Tx3 compiler emits and that resolvers consume to
build chain-specific transactions. It is serialised as CBOR and travels across the wire
inside the `TirEnvelope` shape referenced by the [TII](https://github.com/tx3-lang/tii) and
[TRP](https://github.com/tx3-lang/trp) specs.

## Layout

- `crates/tx3-tir/` — the reference implementation (`tx3-tir` on
  [crates.io](https://crates.io/crates/tx3-tir)). Modules: `compile`, `encoding`, `model`,
  `reduce`.
- `specs/` — placeholder for the formal TIR wire-format specs (see `specs/README.md`).

## Supported encoding versions

- `v1beta0` — current.
- `v1alpha8` — deprecated.

## Where this fits

This repo is one of the submodules in the
[`tx3-lang/lang-factory`](https://github.com/tx3-lang/lang-factory) aggregator. It is
consumed from crates.io by both `tx3` (the language) and `trix` (the toolchain).

## License

Apache-2.0. See [`LICENSE`](./LICENSE).
