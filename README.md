# 🤖 JSON AI Tool Router & Validator

A practical Python + Jupyter Notebook project that turns **JSON, JSON Schema, AI tool definitions, parameters, and tool registries** into a working mini **AI Tool Router**.

**JSON Request → Schema Validation → Tool Registry → Router → Python Tool → Structured JSON Result** 🚀

![Architecture](architecture.svg)

## 🎯 Objective

This project moves beyond simply reading JSON tool schemas and demonstrates an executable tool layer using deterministic mock tools.

It covers:

* 🧩 JSON tool metadata
* 📐 JSON Schema concepts
* 📚 Tool registry
* 🚦 Tool routing
* 🔧 Python tool execution
* 🛡️ Argument validation
* 📦 Structured JSON results

## 🏗️ Architecture

![Tool Router Architecture](architecture.svg)

```text
JSON Request
     ↓
Tool Registry
     ↓
JSON Schema Validator
     ↓
Tool Router
     ↓
Python Tool
     ↓
Structured JSON Result
```

## 🧪 Example Tool

```json
{
  "name": "get_order_status",
  "description": "Get the current status of an order.",
  "parameters": {
    "type": "object",
    "properties": {
      "order_id": { "type": "string" }
    },
    "required": ["order_id"],
    "additionalProperties": false
  }
}
```

## 🔄 What Happens During Execution?

1. 📥 Receive a JSON tool request
2. 🔎 Find the requested tool
3. 📐 Read its parameter schema
4. ✅ Validate required fields and types
5. 🚫 Reject unexpected fields
6. 🔧 Execute the mapped Python function
7. 📤 Return a structured JSON result

## 🚫 Validation Tests

The notebook demonstrates:

* Missing required parameters
* Incorrect parameter types
* Unexpected properties
* Unknown tools

## 🛠️ Technology Stack

| Technology              | Purpose                          |
| ----------------------- | -------------------------------- |
| 🐍 Python               | Tool implementations and routing |
| 📓 Jupyter Notebook     | Interactive learning             |
| 🧩 JSON                 | Tool definitions and requests    |
| 📐 JSON Schema concepts | Validation                       |
| 🚦 Tool Router          | Dispatching                      |

## ▶️ Getting Started

```bash
git clone https://github.com/<your-username>/json-ai-tool-router-validator.git
cd json-ai-tool-router-validator
pip install notebook
jupyter notebook
```

Open:

```text
JSON_AI_Tool_Router_Validator.ipynb
```

## 🚀 Final Challenge

Add:

```text
refund_order(order_id, reason)
```

Then define its JSON schema, implementation, registry entry, successful request, and invalid-request tests.

## 🔮 Future Enhancements

* 🤖 Connect an LLM that generates tool calls
* 🔐 Add authentication and authorization
* 🧱 Use Pydantic for stronger validation
* 📡 Expose tools through FastAPI
* 🗄️ Connect database-backed tools
* 🧠 Integrate LangChain or LangGraph
* 🔌 Expose tools through MCP
* 🧪 Add automated tests
* 📊 Add execution logging and monitoring

## 📂 Repository Structure

```text
json-ai-tool-router-validator/
├── 📓 JSON_AI_Tool_Router_Validator.ipynb
├── 🖼️ architecture.svg
├── 📄 README.md
└── 📜 LICENSE
```

## 💡 Key Takeaway

> **The schema defines the contract, the registry connects the contract to code, and the router validates and dispatches the request.**

```text
JSON Schema
    ↓
Validation
    ↓
Tool Registry
    ↓
Routing
    ↓
Execution
    ↓
JSON Result
```

⭐ A useful stepping stone from **JSON AI tool schemas** to real **LLM agent/tool-calling systems**.
