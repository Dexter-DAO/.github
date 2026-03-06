<p align="center">
  <img src="https://raw.githubusercontent.com/Dexter-DAO/dexter-x402-sdk/main/assets/dexter-wordmark.svg" alt="Dexter" width="420">
</p>

<p align="center">
  <strong>Payments infrastructure for the agentic web. x402 protocol, AI marketplace, and multi-chain settlement.</strong>
</p>

<p align="center">
  <a href="https://dexter.cash"><strong>dexter.cash</strong></a>&nbsp;&nbsp;|&nbsp;&nbsp;
  <a href="https://dexter.cash/opendexter"><strong>OpenDexter Marketplace</strong></a>&nbsp;&nbsp;|&nbsp;&nbsp;
  <a href="https://x402.org"><strong>x402 Protocol</strong></a>&nbsp;&nbsp;|&nbsp;&nbsp;
  <a href="https://lab.dexter.cash"><strong>Dexter Lab</strong></a>
</p>

---

## Ecosystem Map

```
                              ┌─────────────────────┐
                              │     dexter.cash      │  ← what users see
                              │     (dexter-fe)      │
                              └──────────┬──────────┘
                                         │
                    ┌────────────────────┼────────────────────┐
                    │                    │                    │
           ┌────────▼───────┐   ┌───────▼────────┐  ┌───────▼────────┐
           │   dexter-api   │   │  dexter-agents  │  │  dexter-phone  │
           │   (backend)    │   │  (voice agent)  │  │ (phone agent)  │
           └───┬────┬───┬───┘   └────────────────┘  └────────────────┘
               │    │   │
    ┌──────────┘    │   └──────────┐
    │               │              │
┌───▼──────┐  ┌─────▼──────┐  ┌───▼───────────┐
│dexter-mcp│  │ dexter-    │  │ dexter-loop   │
│ (tools)  │  │ facilitator│  │ (traffic eng) │
└──────────┘  │ (payments) │  └───────────────┘
              └────────────┘
```

---

### Core Platform

| Repo | What it does | |
|------|-------------|---|
| **[dexter-fe](https://github.com/Dexter-DAO/dexter-fe)** | Next.js frontend — marketplace, Lab, facilitator dashboard, voice/chat UI | `private` |
| **[dexter-api](https://github.com/Dexter-DAO/dexter-api)** | Central orchestrator — x402 billing, realtime sessions, MCP proxy, wallet management, marketplace engine | `private` |
| **[dexter-facilitator](https://github.com/Dexter-DAO/dexter-facilitator)** | x402 v2 payment facilitator — verifies, settles, and sponsors transactions on Solana and EVM | `private` |
| **[dexter-mcp](https://github.com/Dexter-DAO/dexter-mcp)** | MCP server exposing 60+ Solana DeFi tools over HTTP and stdio | `public` |

### Agent Surfaces

| Repo | What it does | |
|------|-------------|---|
| **[dexter-agents](https://github.com/Dexter-DAO/dexter-agents)** | Flagship voice agent — OpenAI Realtime + MCP tools + x402 micropayments | `public` |
| **[dexter-phone](https://github.com/Dexter-DAO/dexter-phone)** | Phone agent — Twilio Media Streams + OpenAI Realtime + MCP | `private` |
| **[dexter-alexa](https://github.com/Dexter-DAO/dexter-alexa)** | Alexa skill — voice-control Dexter through Amazon Echo | `private` |

### Developer Tools

| Repo | What it does | |
|------|-------------|---|
| **[dexter-x402-sdk](https://github.com/Dexter-DAO/dexter-x402-sdk)** | Full-stack x402 SDK — client, server, React hooks, Express middleware | `public` |
| **[dexter-cursor](https://github.com/Dexter-DAO/dexter-cursor)** | x402 plugin for Cursor IDE — search, pay, and build with x402 | `public` |
| **[dexter-lab](https://github.com/Dexter-DAO/dexter-lab)** | Build, deploy, and monetize paid APIs from your browser | `public` |
| **[dexter-wallet-app](https://github.com/Dexter-DAO/dexter-wallet-app)** | Mobile wallet with native x402 payment support (Solana + EVM) | `private` |
| **[vendorsandbox](https://github.com/Dexter-DAO/vendorsandbox)** | Sandbox for testing x402 seller implementations | `private` |

### Integrations

| Repo | What it does | |
|------|-------------|---|
| **[clawdexter](https://github.com/Dexter-DAO/clawdexter)** | x402 payments + marketplace for OpenClaw agents — 59+ Solana DeFi tools | `public` |
| **[dexter-lobster-skill](https://github.com/Dexter-DAO/dexter-lobster-skill)** | x402 marketplace skill for lobster.cash agents | `private` |
| **[x402-ads](https://github.com/Dexter-DAO/x402-ads)** | Protocol-native sponsored resource recommendations | `private` |

### Operations

| Repo | What it does | |
|------|-------------|---|
| **[dexter-loop](https://github.com/Dexter-DAO/dexter-loop)** | Autonomous x402 payment traffic engine — wallet fleets, volume targeting, anti-pattern obfuscation | `private` |

---

### How it all connects

**Users** visit [dexter.cash](https://dexter.cash) (dexter-fe) to browse the marketplace, build APIs in Lab, or talk to agents.

**Agents** (voice, phone, Alexa, Cursor, OpenClaw, lobster.cash) call tools through **dexter-mcp** and pay for premium access via **dexter-api**'s x402 billing.

**Payments** settle on-chain through **dexter-facilitator** — USDC on Solana or Base. The **dexter-x402-sdk** makes this seamless for any developer.

**Sellers** deploy x402-gated endpoints and get auto-discovered in the **OpenDexter marketplace** (5,000+ indexed APIs). Quality verification, AI naming, and reputation scoring happen automatically.

**dexter-loop** generates the network's baseline transaction volume across rotating wallet fleets with configurable targets and adaptive pacing.

---

<p align="center">
  <a href="https://dexter.cash">dexter.cash</a>&nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="https://x402.org">x402.org</a>&nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="https://twitter.com/dabordexter">@dabordexter</a>
</p>
