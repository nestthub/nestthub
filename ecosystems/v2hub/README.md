<div align="center">

<h1>V2Hub Ecosystem</h1>
<h3>VPN Subscription Management Platform</h3>

<p>API server, client library, CLI, admin library, Telegram bot, and web panel as a single ecosystem.</p>

</div>

<br>

## Repositories

<div align="center">

<a href="https://github.com/nestthub/v2hub-api"><img src="https://github-readme-stats-eight-theta.vercel.app/api/pin/?username=nestthub&repo=v2hub-api&theme=dark&bg_color=0D1117&border_color=2ECC71&hide_border=false" /></a> <a href="https://github.com/nestthub/v2hub-panel"><img src="https://github-readme-stats-eight-theta.vercel.app/api/pin/?username=nestthub&repo=v2hub-panel&theme=dark&bg_color=0D1117&border_color=2ECC71&hide_border=false" /></a>

<a href="https://github.com/nestthub/v2hub-cli"><img src="https://github-readme-stats-eight-theta.vercel.app/api/pin/?username=nestthub&repo=v2hub-cli&theme=dark&bg_color=0D1117&border_color=2ECC71&hide_border=false" /></a> <a href="https://github.com/nestthub/v2hub-admin"><img src="https://github-readme-stats-eight-theta.vercel.app/api/pin/?username=nestthub&repo=v2hub-admin&theme=dark&bg_color=0D1117&border_color=2ECC71&hide_border=false" /></a>

<a href="https://github.com/nestthub/v2hub-bot"><img src="https://github-readme-stats-eight-theta.vercel.app/api/pin/?username=nestthub&repo=v2hub-bot&theme=dark&bg_color=0D1117&border_color=2ECC71&hide_border=false" /></a> <a href="https://github.com/nestthub/v2hub-core"><img src="https://github-readme-stats-eight-theta.vercel.app/api/pin/?username=nestthub&repo=v2hub-core&theme=dark&bg_color=0D1117&border_color=2ECC71&hide_border=false" /></a>

</div>

| Repository      | Status | Description                                                                                                                                                                                |
| --------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **v2hub-api**   | Public | Main V2Hub repository containing the complete server-side implementation — API, database, caching, background tasks, subscription processing, administration endpoints, and observability. |
| **v2hub-core**  | Public | Main client library for working with the V2Hub API. Provides shared models, API clients, and reusable components for building V2Hub integrations.                                          |
| **v2hub-admin** | Public | Administration library for **v2hub-api**. Used when deploying and operating your own V2Hub server.                                                                                         |
| **v2hub-cli**   | Public | Convenient command-line client for working with **v2hub-api**, built around **v2hub-core**.                                                                                                |
| **v2hub-bot**   | Public | Telegram bot for self-service subscription management — issues access tokens, provides access to the web panel, and allows users to manage tokens and providers.                           |
| **v2hub-panel** | Public | Web panel for managing subscriptions and providers, built around **v2hub-core**.                                                                                                           |

<br>

## Highlights

### **v2hub-api — V2Hub Server**

The main repository of the V2Hub ecosystem. It contains the complete server-side implementation of the platform: FastAPI application, SQLAlchemy 2.0 with asyncpg, PostgreSQL, Redis, Celery background tasks, subscription processing, provider aggregation, caching, administration endpoints, and observability.

The server supports multi-source aggregation and recursive subscription resolution with circular-reference detection and configurable nesting depth. It also provides HMAC-SHA256 signed administration endpoints, IP whitelisting, Redis-backed rate limiting, automatic IP banning, and a full observability stack with Prometheus, Loki, Grafana, and Alloy.

### **v2hub-core — Client Library**

The main library for working with the V2Hub API.

It provides the API client, models, and reusable components required to build applications and integrations on top of **v2hub-api**.

Other V2Hub applications can use **v2hub-core** instead of implementing API communication and common functionality from scratch.

### **v2hub-admin — Administration Library**

Administration library for **v2hub-api**.

It provides the functionality required to administer your own V2Hub server, including administrative operations and access control.

**v2hub-admin is intended for self-hosted V2Hub deployments.**

### **v2hub-cli — Command-Line Client**

A convenient terminal client for working with **v2hub-api**.

The CLI is built around **v2hub-core**, providing a convenient command-line interface for managing subscriptions, providers, tokens, and administrative operations.

### **v2hub-bot — Telegram Bot**

A Telegram bot for convenient self-service management of V2Hub subscriptions.

The bot can issue access tokens, provide users with access to the web panel, and allow them to manage their tokens and providers directly through Telegram.

### **v2hub-panel — Web Panel**

A web interface for managing V2Hub subscriptions and providers.

The panel is built around **v2hub-core** and provides a convenient browser-based interface for users to manage their subscriptions and configured providers.

<br>

## Architecture

```text
                         ┌─────────────────────┐
                         │     v2hub-api       │
                         │    V2Hub Server      │
                         │                     │
                         │ FastAPI             │
                         │ PostgreSQL          │
                         │ Redis               │
                         │ Celery              │
                         └──────────┬──────────┘
                                    │
                       V2Hub API    │
                                    │
                         ┌──────────▼──────────┐
                         │     v2hub-core      │
                         │    Client Library   │
                         └─────┬────────┬──────┘
                               │        │
                     ┌─────────┘        └─────────┐
                     │                            │
              ┌──────▼──────┐              ┌──────▼──────┐
              │  v2hub-cli  │              │ v2hub-panel │
              │     CLI     │              │  Web Panel  │
              └─────────────┘              └─────────────┘

                         ┌─────────────────────┐
                         │    v2hub-admin      │
                         │  Admin Library for  │
                         │     v2hub-api       │
                         └─────────────────────┘

                         ┌─────────────────────┐
                         │      v2hub-bot      │
                         │   Telegram Bot      │
                         └─────────────────────┘
```

<br>

<div align="center">

[← Back to profile](../../README.md)

</div>
