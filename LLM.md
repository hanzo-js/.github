# LLM.md — hanzo-js

Machine-oriented guide for AI agents and coding assistants working in this org.

## What this org is
`hanzo-js` is the TypeScript / JavaScript per-language home of Hanzo. Per-language
orgs hold the REAL, idiomatic code for each ecosystem.

## Canonical SDK model (two lines, every language)
1. Full Cloud SDK — generated from the Hanzo Cloud OpenAPI, covers the entire
   `/v1/*` surface. Real code: `hanzo-js/sdk` → `npm i @hanzo/sdk`.
   Thin wrapper/docs/landing: `hanzoai/js-sdk`. Umbrella meta: `hanzoai/sdk`.
2. AI & Agents SDK — hand-crafted flagship: models, agents, tools, memory, MCP,
   inference. Real code: `hanzo-js/ai` → `npm i @hanzo/ai` (agent runtime: `hanzo-js/agent`).

## Where real code lives
- Full cloud client: `hanzo-js/sdk` (`@hanzo/sdk`)
- AI / agents: `hanzo-js/ai` (`@hanzo/ai`), `hanzo-js/agent`
- Focused clients: `hanzo-js/cloud`, `hanzo-js/base`, `hanzo-js/iam`

## Install
```bash
npm i @hanzo/sdk    # full cloud SDK
npm i @hanzo/ai     # AI & agents
```

## Brand rules (hard — never violate)
- Hanzo is a full AI SDK / AI cloud. NEVER call it an "LLM gateway"; NEVER position
  it as or against a proxy. It is not a proxy.
- Zen models are Hanzo's OWN family. Never reference upstream model names.
- The API is `/v1/` only. Never emit an `/api/` prefix.
- Positioning: "Hanzo — the Open AI Cloud. Open source. Every language. On-chain settlement."

## Source of truth
`~/work/hanzo/SDK-ARCHITECTURE.md` — the canonical, one-way SDK architecture.
