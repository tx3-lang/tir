# tir

The canonical home for the **Transaction Intermediate Representation (TIR)** — both the
specification and the reference Rust implementation.

A TIR artefact is a machine-readable, deterministic template for a transaction. It
encapsulates the structural and semantic shape of a transaction without binding it to
specific input UTxOs or argument values; an on-chain transaction is produced by applying
arguments to a TIR template and resolving its inputs against the current chain state.

TIR is serialised as CBOR and travels across the wire inside the `TirEnvelope` shape
referenced by the [TII](https://github.com/tx3-lang/tii) and
[TRP](https://github.com/tx3-lang/trp) specs.

## Layout

- `crates/tx3-tir/` — the reference implementation (`tx3-tir` on
  [crates.io](https://crates.io/crates/tx3-tir)). Modules: `compile`, `encoding`, `model`,
  `reduce`.
- `specs/` — the formal TIR wire-format specs (see `specs/README.md`).

## Supported encoding versions

- `v1beta0` — current.
- `v1alpha8` — deprecated.

## License

Apache-2.0. See [`LICENSE`](./LICENSE).
