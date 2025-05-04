---
layout: default
title: Dynamic Contract Protocol (DCP)
description: Contract-first, dynamic API protocol for AI-powered apps
---

# Dynamic Contract Protocol (DCP)

A contract-first, dynamic API protocol for AI-driven applications.

## Why DCP?

DCP eliminates the need for static documentation like Swagger or Postman by enabling contract-driven API interactions. It supports REST, GraphQL, OData, and Protobuf with JWT-based authorization and regional data compliance.

## Features

- ✅ Dynamic API generation
- ✅ JSON & Protobuf support
- ✅ JWT and API Key authorization
- ✅ AI-powered schema generation
- ✅ Lite mode for edge devices

## Usage Journey

1. Client sends a `ContractMessage` describing needed data.
2. Server responds with a `ContractAcknowledgement` if accepted.
3. Client sends a `DataRequest` using the agreed structure.
4. Server replies with a `DataResponse` containing results.

### ContractMessage Example

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

### ContractAcknowledgement Example

```json
{
  "type": "ContractAcknowledgement",
  "status": "accepted",
  "endpoints": {
    "rest": "/dcp/client_123/products"
  },
  "expires_at": "2025-03-25T00:00:00Z"
}
```

### DataRequest Example

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

### DataResponse Example

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

## Contract Schema Discovery

```json
{
  "schemas": {
    "ContractMessage": "/schemas/contract.schema.json",
    "DataRequest": "/schemas/data-request.schema.json"
  }
}
```

## OPA Policy Example

```json
{
  "contract": {
    "resources": [
      {
        "name": "products",
        "operations": ["get", "list"],
        "fields": ["id", "name", "price", "stock"],
        "filters": ["price > 100", "stock > 0"]
      }
    ],
    "policies": [
      {
        "name": "read_only_policy",
        "source": "package dcp.read\nallow { input.method == \"GET\" }"
      }
    ]
  }
}
```

## Contributing

We welcome contributions!

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/my-feature`
3. Commit your changes
4. Open a pull request

See [CONTRIBUTING.md](https://github.com/gokayokutucu/dcp-spec/blob/main/CONTRIBUTING.md) for guidelines.

## License

This project is licensed under the [Apache 2.0 License](https://github.com/gokayokutucu/dcp-spec/blob/main/LICENSE).