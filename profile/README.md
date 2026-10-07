# SoroWorks

**Open-source Go tooling for shipping and maintaining Soroban smart contracts on Stellar.**

Three tools that cover a contract's lifecycle — each useful alone, and wired together into one pipeline:

| | Tool | What it does |
|---|---|---|
| 🚀 | **[SoroForge](https://github.com/soroworks/soroforge)** | Deploy and upgrade contracts with a recorded history in Postgres, dry runs that are safe against mainnet, and drift detection that checks the record against the chain. |
| 📚 | **[SoroVault](https://github.com/soroworks/sorovault)** | An interface (ABI) registry: decodes a deployed contract's spec, versions it by WASM hash, makes it searchable by function and type name, and generates typed TypeScript clients. |
| 🔍 | **[SoroProbe](https://github.com/soroworks/soroprobe)** | Read-only simulation and health checks: decoded results, resource costs, and how close each ledger entry is to expiring — with exit codes made for CI. |

```
 soroforge deploy ──registers──▶ SoroVault ◀──types arguments── soroprobe check
   (records history)          (decodes & versions the ABI)        (gates CI on health)
```

## Get started

- Download a [release](https://github.com/soroworks/soroforge/releases/latest), or `go install github.com/soroworks/<tool>/cmd/<tool>@latest`
- Read the **[documentation](https://github.com/soroworks/docs)**, starting with [Using the tools together](https://github.com/soroworks/docs/blob/main/workflow.md)

## Contribute

Issues labelled [`good first issue`](https://github.com/search?q=org%3Asoroworks+label%3A%22good+first+issue%22+state%3Aopen&type=issues) are small and self-contained; every issue carries a `complexity:` label and lists the files involved and its acceptance criteria. Tests never need a network or a database, and `make check` runs everything CI does.

All SoroWorks tools are Apache-2.0 licensed. SoroWorks is an independent community project, not affiliated with the Stellar Development Foundation.
