<p align="center">
  <img src="https://raw.githubusercontent.com/Dexter-DAO/dexter-x402-sdk/main/assets/dexter-wordmark.svg" alt="Dexter" width="420">
</p>

<h1 align="center">Organization</h1>

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

## Ecosystem

```mermaid
flowchart LR
    subgraph clients["Clients"]
        direction TB
        fe["dexter-fe"]
        agents["dexter-agents"]
        phone["dexter-phone"]
        alexa["dexter-alexa"]
        cursor["dexter-cursor"]
        claw["clawdexter"]
        lobster["dexter-lobster-skill"]
    end

    subgraph core["Core"]
        direction TB
        api["dexter-api"]
    end

    subgraph services["Services"]
        direction TB
        mcp["dexter-mcp"]
        facilitator["dexter-facilitator"]
    end

    subgraph devtools["Dev Tools"]
        direction TB
        sdk["dexter-x402-sdk"]
        lab["dexter-lab"]
        wallet["dexter-wallet-app"]
    end

    subgraph settle["Settlement"]
        direction TB
        solana["Solana"]
        base["Base"]
    end

    fe --> api
    agents --> api
    phone --> api
    alexa --> api
    cursor --> api
    claw --> api
    lobster --> api

    api --> mcp
    api --> facilitator

    sdk -.-> facilitator
    lab --> api
    wallet --> facilitator

    facilitator --> solana
    facilitator --> base
```

---

### Core Platform

| Repo | Description | |
|------|------------|---|
| [**dexter-api**](https://github.com/Dexter-DAO/dexter-api) | Central orchestrator — x402 billing, realtime sessions, MCP proxy, wallet management, marketplace engine | `private` |
| [**dexter-fe**](https://github.com/Dexter-DAO/dexter-fe) | Next.js frontend — marketplace, Lab, facilitator dashboard, voice/chat UI | `private` |
| [**dexter-facilitator**](https://github.com/Dexter-DAO/dexter-facilitator) | x402 v2 payment facilitator — verifies, settles, and sponsors transactions on Solana and EVM | `private` |
| [**dexter-mcp**](https://github.com/Dexter-DAO/dexter-mcp) | MCP server exposing 60+ Solana DeFi tools over HTTP and stdio | `public` |

### Agent Surfaces

| Repo | Description | |
|------|------------|---|
| [**dexter-agents**](https://github.com/Dexter-DAO/dexter-agents) | Flagship voice agent — OpenAI Realtime API + MCP tools + x402 micropayments | `public` |
| [**dexter-phone**](https://github.com/Dexter-DAO/dexter-phone) | Phone agent — Twilio Media Streams + OpenAI Realtime + MCP | `private` |
| [**dexter-alexa**](https://github.com/Dexter-DAO/dexter-alexa) | Alexa skill — voice-control Dexter through Amazon Echo | `private` |
| [**dexter-cursor**](https://github.com/Dexter-DAO/dexter-cursor) | x402 plugin for Cursor IDE — search, pay, and build with x402 | `public` |

### Developer Tools

| Repo | Description | |
|------|------------|---|
| [**dexter-x402-sdk**](https://github.com/Dexter-DAO/dexter-x402-sdk) | Chain-agnostic x402 v2 SDK — client, server, React hooks, Express middleware | `public` |
| [**dexter-lab**](https://github.com/Dexter-DAO/dexter-lab) | Build, deploy, and monetize paid APIs from your browser | `public` |
| [**dexter-wallet-app**](https://github.com/Dexter-DAO/dexter-wallet-app) | Mobile wallet with native x402 payment support (Solana + EVM) | `private` |

### Integrations

| Repo | Description | |
|------|------------|---|
| [**clawdexter**](https://github.com/Dexter-DAO/clawdexter) | x402 payments + marketplace for OpenClaw agents — 59+ Solana DeFi tools | `public` |

---

### How it connects

**Users** visit [dexter.cash](https://dexter.cash) to browse the marketplace, build APIs in Lab, or talk to agents.

**Agents** (voice, phone, Alexa, Cursor, OpenClaw, lobster.cash) call tools through **dexter-mcp** and pay via **dexter-api**'s x402 billing.

**Payments** settle on-chain through **dexter-facilitator** — USDC on Solana or Base. The **dexter-x402-sdk** makes integration seamless for any developer.

**Sellers** deploy x402-gated endpoints and get auto-discovered in the [OpenDexter marketplace](https://dexter.cash/opendexter) (5,000+ indexed APIs).

---

<p align="center">
  <a href="https://dexter.cash">dexter.cash</a>&nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="https://x402.org">x402.org</a>&nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="https://twitter.com/dabordexter">@dabordexter</a>
</p>
