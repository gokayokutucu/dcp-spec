# DCP Roadmap

## Q2 2025 – Foundational Work
- Define `ContractMessage` & `Acknowledgment` structures
- Publish initial DCP specification
- Draft runtime contract negotiation flow
- Publish “Why DCP Matters” and “Philosophy” docs

## Q3 2025 – Developer Experience
- Build CLI to simulate DCP negotiation
- Create DCP Mock Server for testing
- Write SDKs for Java, .NET, and Go (backend integration)
- Minimal web UI to inspect contracts/responses

## Q4 2025 – Adoption & Interoperability
- OpenAPI to DCP translation tool
- Example integration with API gateways (e.g., Kong, APIGW, Envoy)
- CLI scaffolding for DCP-compatible services
- GitHub Actions for contract validation

## Q1 2026 – Registry & Ecosystem
- Launch DCP Registry alpha
- Create a searchable contract catalog
- Support versioning, signatures, and auditing for contracts
- Public test suites and compliance harness

## Q2 2026 – Contract-as-a-Service (CaaS)
- Enable remote contract hosting and resolution
- Contracts served from decentralized or cloud registries
- Policy-based access to contract metadata
- Pluggable contract lifecycle events (pre-negotiation hooks, validation callbacks)

## Beyond
- DCP Lite spec for limited-resource clients
- UI tooling: Live contract visualizer
- gRPC/AsyncAPI support

## Future Versions

| Version | Target Features                         |
|---------|------------------------------------------|
| v1.1    | gRPC support                             |
| v1.2    | Cross-contract joins                     |
| v2.0    | Quantum-safe encryption                  |
| v3.0    | Decentralized contract marketplace       |