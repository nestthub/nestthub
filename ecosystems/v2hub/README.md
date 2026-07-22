<div align="center">

<h1>V2Hub Ecosystem</h1>
<h3>VPN Subscription Management Platform</h3>

<p>Server core, client SDK, CLI, admin module, and web panel as a single system.</p>

</div>

<br>

## Repositories

<div align="center">

<a href="https://github.com/nestthub/v2hub-core"><img src="https://github-readme-stats-eight-theta.vercel.app/api/pin/?username=nestthub&repo=v2hub-core&theme=dark&bg_color=0D1117&border_color=2ECC71&hide_border=false" /></a>
<a href="https://github.com/nestthub/v2hub-panel"><img src="https://github-readme-stats-eight-theta.vercel.app/api/pin/?username=nestthub&repo=v2hub-panel&theme=dark&bg_color=0D1117&border_color=2ECC71&hide_border=false" /></a>

<a href="https://github.com/nestthub/v2hub-cli"><img src="https://github-readme-stats-eight-theta.vercel.app/api/pin/?username=nestthub&repo=v2hub-cli&theme=dark&bg_color=0D1117&border_color=2ECC71&hide_border=false" /></a>
<a href="https://github.com/nestthub/v2hub-admin"><img src="https://github-readme-stats-eight-theta.vercel.app/api/pin/?username=nestthub&repo=v2hub-admin&theme=dark&bg_color=0D1117&border_color=2ECC71&hide_border=false" /></a>

<a href="https://github.com/nestthub/v2hub-bot"><img src="https://github-readme-stats-eight-theta.vercel.app/api/pin/?username=nestthub&repo=v2hub-bot&theme=dark&bg_color=0D1117&border_color=2ECC71&hide_border=false" /></a>

</div>

| Repository       | Status                           | Description                                                                                                                                                       |
| ---------------- | -------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **v2hub-server** | 🔒 Private — public release soon | Core API — FastAPI, PostgreSQL, Redis, Celery. Multi-source aggregation, recursive subscription resolution, HMAC-signed admin endpoints, full observability stack |
| **v2hub-core**   | Public                           | Shared business logic, API models, and reusable platform components                                                                                               |
| **v2hub-panel**  | Public                           | Web mini-app for managing subscriptions and sources — FastAPI + vanilla JS                                                                                        |
| **v2hub-cli**    | Public                           | Terminal client built on Typer and Rich for managing services from the command line                                                                               |
| **v2hub-admin**  | Public                           | Administration module — HMAC-SHA256 auth, user CRUD, IP filtering                                                                                                 |
| **v2hub-bot**    | Public                           | Telegram integration for self-service subscription management                                                                                                     |

<br>

## Highlights

**v2hub-server — VPN Subscription API**
FastAPI core with SQLAlchemy 2.0 (async) and asyncpg, PostgreSQL + Redis two-tier caching, Celery background refresh every 15 minutes. Recursive subscription resolution with circular-reference detection and configurable nesting depth. HMAC-SHA256 signed admin endpoints, IP whitelisting, Redis-backed rate limiting, automatic IP banning. Full observability stack — Prometheus, Loki, Grafana, Alloy. Currently private; scheduled for public release.

**v2hub-panel — Web Mini App**
FastAPI + vanilla JS, no build step. Rate limiting, IP-restricted Grafana access, HSTS, strict CORS.

**v2hub-cli**
Terminal client on Typer and Rich for managing subscriptions, sources, and admin operations from the command line.

**v2hub-admin**
HMAC-SHA256 signed requests, user CRUD, IP whitelisting and banning.

**v2hub-bot**
Telegram integration for self-service subscription management — config delivery, QR codes, and lifecycle automation.

<br>

<div align="center">

[← Back to profile](../../README.md)

</div>
