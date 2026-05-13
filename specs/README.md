# TIR specs

This directory is the canonical home for the **Tx3 Transaction Intermediate Representation
(TIR)** wire-format specification.

## Status

The specs in this directory are a placeholder. The format is currently defined implicitly
by the reference implementation in [`../crates/tx3-tir/`](../crates/tx3-tir/):

- CBOR is the serialisation format (see `crates/tx3-tir/src/encoding.rs`).
- The AST shape is given by the Rust types in `crates/tx3-tir/src/model/`.
- Two encoding versions exist today:
  - `v1beta0` — current.
  - `v1alpha8` — deprecated.

The `TirEnvelope` shape (`{ encoding, content, version }`) is already referenced by sibling
specs in [`trp`](https://github.com/tx3-lang/trp) and [`tii`](https://github.com/tx3-lang/tii).

## Planned layout

Formal artefacts will land here under per-version directories, mirroring the convention
established in `trp/v1beta0/` and `tii/v1beta0/`:

```
specs/
├── v1beta0/
│   ├── README.md       # prose description of the encoding
│   ├── envelope.cddl   # CDDL for TirEnvelope
│   └── ...             # additional schemas (full AST, etc.)
└── v1alpha8/           # legacy, deprecated
```

Contributions defining these artefacts are welcome.
