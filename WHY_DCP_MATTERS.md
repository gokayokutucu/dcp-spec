# Why DCP Matters

## 🚧 The Problem

Modern APIs often rely on static specifications like OpenAPI, RAML, or Postman collections. While useful, they fall short in environments where:

- Schemas change frequently
- Multiple clients integrate with differing permissions or needs
- Onboarding involves manual coordination and human-readable docs
- Dynamic systems (e.g. AI agents, low-code tools) consume APIs

These workflows often introduce drift, misalignment, and unnecessary delay.

## 💡 Our Insight

What if contracts came first — and the API behavior emerged from them?

DCP rethinks the role of API specifications by introducing a **contract-driven protocol** where:

- Clients declare what they need (`ContractMessage`)
- Servers validate, provision, and respond with tailored access (`Acknowledgment`)
- The interaction schema is derived, not predefined
- Tests, auth, and documentation become runtime artifacts

## 🛠️ Philosophy

- **Contract as truth**: Everything starts from the contract — no pre-generated client SDKs required.
- **Dynamic by design**: Endpoints, schemas, and policies are constructed at runtime, not baked in.
- **Declarative over imperative**: Clients declare their needs; servers decide how to serve.
- **Pluggable security**: Authorization is decoupled from endpoint structure via OPA-based policies.
- **Zero-friction onboarding**: New clients don’t wait for docs — they get a contract, send it, and start.

## 🌍 Who Needs This?

- **Enterprises** managing multi-tenant APIs
- **Startups** building zero-config backends
- **AI Agents** needing programmable discovery and access
- **API Providers** offering dynamic endpoints to diverse clients
- **DevOps** teams aiming for test automation and validation on first contact

## 🔭 The Vision

We want to build toward:

- A world where API integrations begin with a contract, not an email
- A system where API changes are validated, negotiated, and versioned automatically
- A lightweight runtime that reflects the evolving shape of a client’s intent