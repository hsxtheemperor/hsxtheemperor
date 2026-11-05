# GLSC-AI

GLSC-AI is a C/Cython/Python project for data acquisition, setup-metadata generation, shell-driven orchestration, and binary payload persistence. It is proprietary to GLSC Ltd.

## Architecture

The current runtime is organized around these layers:

1. The shell parses commands and resolves domains.
2. The fetch runtime normalizes a domain and routes the requested action.
3. Family backends perform the data work; the Polymarket path is currently the most coherent.
4. Shared runtime headers and generated metadata define the data contract.
5. Broker and analysis layers validate and interpret runtime results rather than owning the canonical payload layout.

Setup metadata generation, fetch operations, shell dispatch, and payload structure have distinct responsibilities. In particular, binary-layout headers remain the authority for the payload contract.

## Status

The shell command dispatch and fetch-runtime routing are present, including domain alias normalization. The project is still in a migration phase: Finance and Economics backend declarations/contracts need alignment, some family paths and generated metadata remain in transition, and older documentation may describe previous architecture assumptions.

The project should therefore be described as a working shell/runtime with partially completed family backends—not as a fully ready multi-domain pipeline.

## License

Proprietary to GLSC Ltd. This profile summary does not grant permission to use or redistribute the project.
