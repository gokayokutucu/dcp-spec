# Dynamic Contract Protocol (DCP)

Dynamic Contract Protocol (DCP) enables clients to define API behavior dynamically through JSON or Protobuf contracts. Servers interpret these contracts to generate secure, validated, and isolated API layers on the fly. The protocol is built around flexibility, security, scalability, and verifiability.

---

## ✨ Features

- ✅ Dynamic API generation (REST, GraphQL, OData support)
- ✅ JSON & Protobuf contract support
- ✅ Secure JWT and API Key-based authorization
- ✅ Regional data localization & compliance
- ✅ Auto-generated tests and deployment automation
- ✅ Lite mode for resource-constrained environments
- ✅ AI-powered schema and backend generation

---

## 📦 Basic Usage

### 1. Inline `ContractMessage` Example
```json
{
  "type": "ContractMessage",
  "protocol_version": "1.0",
  "contract": {
    "resources": [
      {
        "name": "Product",
        "operations": ["get", "list"],
        "fields": ["id", "name", "price"],
        "filters": ["price > 100"]
      }
    ],
    "response_formats": ["json"]
  }
}
```

### 2. `DataRequest` Example
```json
{
  "type": "DataRequest",
  "resource": "Product",
  "operation": "list",
  "parameters": {
    "filters": ["price < 200"],
    "page": 1
  }
}
```

### 3. `DataResponse` Example
```json
{
  "type": "DataResponse",
  "data": [
    { "id": 1, "name": "Phone", "price": 199 }
  ],
  "metadata": {
    "total_records": 1,
    "current_page": 1
  }
}
```

---

## 📚 Documentation

| Topic | Description |
|-------|-------------|
| [Specification](./docs/dcp-spec-v1.0.md) | Full protocol definition |
| [Examples](./docs/examples) | Sample contracts and requests |
| [Schemas](./schemas) | JSON Schema validators |
| [Validator SDK](./tools/dcp-client-validator) | Client-side filter validator |

---

## 🧪 Getting Started

```bash
git clone https://github.com/gokayokutucu/dcp-spec.git
cd dynamic-contract-protocol
```

> You can read the spec directly or build tooling using the provided schemas and SDKs.

---

## 🧠 Contributing

Want to contribute?

1. Fork this repository
2. Create a new branch (`feature/my-feature`)
3. Make your changes and commit them
4. Open a Pull Request

See [CONTRIBUTING.md](./CONTRIBUTING.md) for full guidelines.

---

## 🗓 Versioning

| Version | Highlights |
|---------|------------|
| v1.0    | Initial stable version: ContractMessage, DataRequest, Lite Profile, AI Engine, GraphQL, OData |
| v1.1    | (Planned) gRPC support, cross-contract joins |
| v2.0    | (Planned) Quantum-safe encryption, decentralized contract marketplace |

Full changelog is available in [CHANGELOG.md](./CHANGELOG.md).

---

## 🔒 License

This project is licensed under the [Apache 2.0 License](./LICENSE).

---

## 🌍 Who is it for?

- Startups: Rapid prototyping and delivery
- Enterprises: Regulated data environments
- API providers: Dynamic interface provisioning with policy enforcement

---

## 📫 Contact

For questions or support, open an issue via [GitHub Issues](https://github.com/gokayokutucu/dcp-spec/issues).
