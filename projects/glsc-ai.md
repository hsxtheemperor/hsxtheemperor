# GLSC-AI

> **My contribution:** Designed and built the project end to end.

A **C/Cython/Python** data pipeline for data acquisition, setup-metadata generation, shell-driven orchestration, and binary payload persistence. The project is proprietary to GLSC Ltd.

## How it works

1. The shell parses commands and resolves domains.
2. The fetch runtime normalizes a domain and routes the requested action.
3. Family backends perform the data work; the Polymarket path is currently the most complete.
4. Shared runtime headers and generated metadata define the data contract.
5. Broker and analysis layers validate and interpret results without owning the canonical payload layout.

This separation keeps setup metadata, fetch operations, shell dispatch, and payload structure distinct. Binary-layout headers remain the authority for the payload contract.

## Current status

Shell command dispatch and fetch-runtime routing are working, including domain-alias normalization. The project is still in transition: Finance and Economics backend declarations and contracts need alignment, and some family paths and generated metadata remain in migration.

In short, the shell and runtime scaffolding are in place, while several family backends are not yet complete.

## License

**Proprietary to GLSC Ltd.** This summary does not grant permission to use or redistribute the project.
