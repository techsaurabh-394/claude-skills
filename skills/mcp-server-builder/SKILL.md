---
name: mcp-server-builder
description: Scaffold a Model Context Protocol (MCP) server in TypeScript with typed tools, input validation and a test checklist. Use when the user wants to expose an API, database or internal tool to an AI assistant through MCP.
---

# MCP Server Builder

## Process
1. Clarify the system being exposed and list 3-7 **tools** (verbs the model can call). For each tool: name, one-line purpose, input schema, output shape, side effects (read-only vs writes).
2. Prefer small, single-purpose tools with explicit descriptions. Descriptions are what the model reads to choose a tool.
3. Validate every input with a schema. Return errors as readable text, never stack traces.
4. Mark destructive tools clearly in the description and require explicit parameters (no implicit "delete all").
5. Keep responses compact; return only the fields the model needs.

## Starter (TypeScript, `@modelcontextprotocol/sdk` + `zod`)
```ts
import { McpServer } from "@modelcontextprotocol/sdk/server/mcp.js";
import { StdioServerTransport } from "@modelcontextprotocol/sdk/server/stdio.js";
import { z } from "zod";

const server = new McpServer({ name: "example-server", version: "1.0.0" });

server.tool(
  "add_numbers",
  "Add two numbers and return the sum.",
  { a: z.number(), b: z.number() },
  async ({ a, b }) => ({ content: [{ type: "text", text: String(a + b) }] })
);

await server.connect(new StdioServerTransport());
```
Check the current SDK documentation before finalising; the API evolves.

## Deliverables
- Project layout (`src/index.ts`, `src/tools/*.ts`, `package.json`, `tsconfig.json`)
- Tool table (name, inputs, outputs, side effects)
- Claude Desktop / client config snippet to register the server
- Test checklist: each tool with valid input, invalid input, empty result, upstream failure
- Security notes: secrets via env vars, least-privilege credentials, no arbitrary shell or SQL execution
