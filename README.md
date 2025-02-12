# C-KZG-4844

This is a minimal library for EIP-4844 that implements the [Polynomial
Commitments](https://github.com/ethereum/consensus-specs/blob/dev/specs/deneb/polynomial-commitments.md)
API. It was originally a stripped-down copy of
[C-KZG](https://github.com/benjaminion/c-kzg), but it has been heavily modified
since then.

## Interface functions

There are functions for KZG operations:

- `blob_to_kzg_commitment`
- `compute_kzg_proof`
- `compute_blob_kzg_proof`
- `verify_kzg_proof`
- `verify_blob_kzg_proof`
- `verify_blob_kzg_proof_batch`

There are functions for loading/freeing the trusted setup:

- `load_trusted_setup`
- `load_trusted_setup_file`
- `free_trusted_setup`

## Bindings

There are bindings for the following languages:

| Language | Link                                 |
|----------|--------------------------------------|
| C#       | [README](bindings/csharp/README.md)  |
| Go       | [README](bindings/go/README.md)      |
| Java     | [README](bindings/java/README.md)    |
| Node.js  | [README](bindings/node.js/README.md) |
| Python   | [README](bindings/python/README.md)  |
| Rust     | [README](bindings/rust/README.md)    |

## Installation

Initialize the blst submodule:

```
git submodule update --init
```

Build the blst library:

```
cd src
make blst
```

Build/test the C-KZG-4844 library:

```
cd src
make
```
