<div align="center">

# Hanzo for TypeScript / JavaScript

**The Open AI Cloud — open source, every language, on-chain settlement.**

`hanzo-js` is the TypeScript / JavaScript home of [Hanzo](https://hanzo.ai). Real,
idiomatic code for the whole Hanzo Cloud — one typed client for every `/v1` service,
plus a first-class AI & agents library.

[hanzo.ai](https://hanzo.ai) · [Docs](https://docs.hanzo.ai) · [Umbrella org](https://github.com/hanzoai) · [JS wrapper & docs](https://github.com/hanzoai/js-sdk)

</div>

---

## Two SDK lines, one ecosystem

Every Hanzo language ships two SDKs. Here they are for Node and the browser:

### 1 · Full Cloud SDK — `@hanzo/sdk`

Typed client for the entire cloud surface (`/v1/*`: AI, agents, inference, compute,
data, network, security/IAM/KMS, platform, observe, web3, apps). Generated from the
Hanzo Cloud OpenAPI, so it never drifts. Real code lives here in [`hanzo-js/sdk`](https://github.com/hanzo-js/sdk).

```bash
npm i @hanzo/sdk
```

```ts
import { Hanzo } from '@hanzo/sdk'

const hanzo = new Hanzo({ apiKey: process.env.HANZO_API_KEY })

const models = await hanzo.models.list()
console.log(models.data.map((m) => m.id))
```

### 2 · AI & Agents — `@hanzo/ai`

The hand-crafted AI-first library: Zen models, agents, tools, memory, MCP, and
inference. Lives in [`hanzo-js/ai`](https://github.com/hanzo-js/ai), with the agent
runtime in [`hanzo-js/agent`](https://github.com/hanzo-js/agent).

```bash
npm i @hanzo/ai
```

```ts
import { Agent } from '@hanzo/ai'

const agent = new Agent({ model: 'zen-coder' })
const { output } = await agent.run('Summarize the last deploy and flag any regressions.')
console.log(output)
```

> Zen is Hanzo's own model family. The API is always `/v1/` — never `/api/`.

---

## Repositories

Typed clients and building blocks that make up the JS/TS stack:

| Repo | Package | What it is |
|------|---------|------------|
| [`sdk`](https://github.com/hanzo-js/sdk) | `@hanzo/sdk` | Full Cloud SDK — one typed client for every `/v1` service |
| [`ai`](https://github.com/hanzo-js/ai) | `@hanzo/ai` | AI SDK — Zen models, agents, tools, memory, MCP, inference |
| [`agent`](https://github.com/hanzo-js/agent) | `@hanzo/agent` | Agent runtime — planning, tool use, memory |
| [`cloud`](https://github.com/hanzo-js/cloud) | `@hanzo/cloud` | Focused `/v1` platform client — agents, sessions, machines |
| [`base`](https://github.com/hanzo-js/base) | `@hanzo/base` | Client for Hanzo Base, the reactive backend (IAM-native) |
| [`iam`](https://github.com/hanzo-js/iam) | `@hanzo/iam` | Hanzo IAM-native auth — OIDC + PKCE, one way |
| [`chat`](https://github.com/hanzo-js/chat) | `@hanzo/chat` | Composable React chat UI on `@hanzo/ai` + `@hanzo/gui` |
| [`commerce.js`](https://github.com/hanzo-js/commerce.js) | `@hanzo/commerce` | Commerce SDK |
| [`shop.js`](https://github.com/hanzo-js/shop.js) | `@hanzo/shop` | Storefront widget over `@hanzo/commerce` |
| [`checkout.js`](https://github.com/hanzo-js/checkout.js) | `@hanzo/checkout` | Checkout widget |
| [`coin.js`](https://github.com/hanzo-js/coin.js) | `@hanzo/coin` | Crypto payments & token-sale SDK |
| [`track.js`](https://github.com/hanzo-js/track.js) | `@hanzo/track` | First-party web analytics — identify & track |
| [`dash.js`](https://github.com/hanzo-js/dash.js) | `@hanzo/dash` | Reactive UI components for modular dashboards |
| [`hanzo.js`](https://github.com/hanzo-js/hanzo.js) | `@hanzo/hanzo` | Core JavaScript SDK |
| [`css`](https://github.com/hanzo-js/css) | `@hanzo/css` | Centralized CSS library |
| [`cowork`](https://github.com/hanzo-js/cowork) | — | Collaborative workspace toolkit |

<sub>Legacy / archived: `ui`, `cli`, `dash2`, `astley.js`, `hanzo-js.github.io`, `mobile-accounting`.</sub>

---

## Also available in

Every language gets the same two lines — full Cloud SDK plus AI & agents:

| Language | Org | Language | Org |
|----------|-----|----------|-----|
| Python (flagship AI) | [hanzo-py](https://github.com/hanzo-py) · [hanzoai/python-sdk](https://github.com/hanzoai/python-sdk) | Go | [hanzo-go](https://github.com/hanzo-go) |
| Rust | [hanzo-rs](https://github.com/hanzo-rs) | C++ | [hanzo-cpp](https://github.com/hanzo-cpp) |
| Swift | [hanzo-swift](https://github.com/hanzo-swift) | Kotlin | [hanzo-kt](https://github.com/hanzo-kt) |

Umbrella & meta: [`hanzoai/sdk`](https://github.com/hanzoai/sdk) — one install, every service, every language.

---

<div align="center">

**[Hanzo AI](https://hanzo.ai)** · the Open AI Cloud · [github.com/hanzoai](https://github.com/hanzoai)

</div>
