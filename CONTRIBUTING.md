# Contributing to DCP Spec

🎉 **Thank you for your interest in contributing to the Dynamic Contract Protocol (DCP)!**  
This project welcomes both specification writers and software developers to collaborate on building a robust, extensible, and machine-executable protocol.

---

## 📚 About This Project

DCP (Dynamic Contract Protocol) aims to define contracts for APIs that support:
- dynamic schema generation
- validation and testing
- policy enforcement
- client-side form generation
- machine learning-driven schema evolution (future roadmap)

We maintain two major tracks in this repository:
- `spec/`: Specification files and schema definitions
- `impl/`: Implementation details and upcoming CLI tools, validators, runners, etc.

---

## 💡 How You Can Contribute

### 📐 Specification Contributions

We welcome:
- New contract types
- Profile definitions (e.g., Lite, OData, GraphQL, gRPC)
- Validation rule proposals
- Use case examples

Use the template under `spec/contracts/_template/` to create a new contract spec.

#### 🔖 Tagging Suggestions
We use the following GitHub labels:
- `good first issue`: Suitable for newcomers
- `discussion-needed`: Requires community decision
- `specification`: Pure spec changes
- `implementation`: Changes in implementation tooling or logic

---

### ⚙️ Implementation Contributions (Coming Soon)

We are building the following components under the `impl/` directory:
- `dcp-cli`: A command-line tool for validating and generating contracts
- `dcp-validator`: A reusable validation core
- `dcp-ui`: Optional browser-based visual editor and tester (planned)
- `qwen-finetune`: Experiments on fine-tuning Qwen with contract patterns

Please watch this repository for updates. We will mark issues accordingly when components are open to contributions.

#### 🧪 Automated Tests

- All implementation modules will include unit and integration tests.
- We use `pytest` (Python) and `dotnet test` (C#) depending on the module.
- CI/CD will validate that all PRs pass tests before merge.
- For spec-related changes, test fixtures under `test-fixtures/` will be used to simulate contract execution.

---

## 🧼 Code Style & Tools

- **Python modules** must follow `black` format and use type hints.
- **.NET components** must use `C# 13` and respect `StyleCop` rules.
- Include docstrings and comments in English.

---

## 🧠 Contribution Process

1. **Fork this repo**
2. Create a new branch: `feature/your-feature-name` or `spec/new-contract-type`
3. Make your changes
4. Write or update tests (if applicable)
5. Create a PR and describe your change clearly

---

## 🙋‍♀️ Need Help?

Feel free to [open a discussion](https://github.com/gokayokutucu/dcp-spec/discussions) if:
- you're unsure how to get started
- want to propose a major change
- need clarification on any part of the project

---

Thanks for helping us build the future of dynamic API contracts!  
— _The DCP Spec Team_