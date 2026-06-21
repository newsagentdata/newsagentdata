<div align="center">

<img src="https://newsagentdata.com/logo.png" alt="NewsAgent Data" width="420">

### Real-time, ML-enriched news intelligence — as an API

[![Website](https://img.shields.io/badge/Website-newsagentdata.com-3b82f6?style=flat-square)](https://newsagentdata.com/)
[![Docs](https://img.shields.io/badge/Docs-API_Reference-3b82f6?style=flat-square)](https://newsagentdata.com/documentation/)
[![Pricing](https://img.shields.io/badge/Pricing-Free_tier_%2B_from_%2429-3b82f6?style=flat-square)](https://newsagentdata.com/pricing/)
[![MCP](https://img.shields.io/badge/AI_Agents-MCP_Server-1e293b?style=flat-square)](https://newsagentdata.com/mcp/)
[![Status](https://img.shields.io/badge/Status-Live-22c55e?style=flat-square)](https://services.newsagentdata.com/)

</div>

---

Most news APIs hand you **raw articles**. NewsAgent Data hands you **structured intelligence**: every article arrives already labeled with an urgency score, political lean, topic and event classification, and cross-source clustering — so you can build on signal instead of parsing noise.

Global coverage with a Russian & English core, drawn from **RSS + Telegram** sources that most providers don't touch.

## Why NewsAgent Data

- **Enrichment on every article** — urgency score (1–10), breaking detection, political-lean classification, event clustering & de-duplication, topic tags, country tags, audience tags, language, and event type.
- **Coverage at scale** — 750K+ articles and growing ~1,800/hour, across **190+ countries** and **35+ languages**, from **7,000+ sources**.
- **Sources others miss** — RSS **and** Telegram, a major edge for OSINT, geopolitics, and breaking-news use cases.
- **Built for AI & automation** — a native **MCP server** for LLM agents, plus REST, Server-Sent Events streaming, JSONL bulk export, and HMAC-signed webhooks.
- **Real-time breaking pipeline** — urgency-scored detection with push delivery, not just a search index.
- **Bilingual depth** — true RU + EN with native-language enrichment (urgency scoring works *in* the source language, not only English).
- **Developer-friendly economics** — a free tier, paid entry at **$29/mo**, and transparent pricing.

## Quick start

Grab a free API key at **[newsagentdata.com/signup](https://newsagentdata.com/signup/)**, then:

```bash
curl -H "X-API-Key: YOUR_KEY" \
  "https://api.newsagentdata.com/v1/feed?lang=en&min_score=7&days=1"
```

Every record comes back enriched:

```json
{
  "title": "...",
  "source": "Cadena 3 Argentina",
  "link": "https://...",
  "urgency_score": 7,
  "urgency_label": "breaking",
  "political_lean": "neutral",
  "language": "es",
  "country_tags": "bo",
  "topic_tags": ["accident"],
  "event_type": "disaster",
  "audience_tags": "media",
  "cluster_id": 1782068387,
  "fetched_at": "2026-06-21 18:59:40"
}
```

## Endpoints

| Endpoint | Purpose |
|---|---|
| `GET /v1/feed` | Main feed — filter by language, score, days, country, political lean, topic, audience |
| `GET /v1/breaking` | High-urgency articles (score ≥ 7) |
| `GET /v1/search?q=` | Keyword search |
| `GET /v1/audience/{audience}` | Audience-targeted feed (trading, media, academic, security, tech, politics) |
| `GET /v1/stream` | Live Server-Sent Events stream |
| `GET /v1/export/jsonl` | Bulk JSONL export |
| `POST /v1/webhook` | Register an HMAC-signed webhook for breaking news |

Full reference: **[API documentation](https://newsagentdata.com/documentation/)** · interactive Swagger at **[/docs](https://api.newsagentdata.com/docs)**.

## For AI agents (MCP)

A ready-to-use **Model Context Protocol** server lets LLM agents query the feed, search, fetch breaking news, and read coverage stats as native tools.

→ **[MCP setup & download](https://newsagentdata.com/mcp/)**

## Use cases

Trading & market signals · OSINT and geopolitical monitoring · media monitoring & PR · academic and policy research · grounding data for AI/LLM applications · real-time alerting.

## Pricing

Free tier to start, then **Developer ($29/mo)**, Starter, Standard, Pro, and Enterprise.
Details: **[newsagentdata.com/pricing](https://newsagentdata.com/pricing/)**

## Links

🌐 [Website](https://newsagentdata.com/) · 📚 [Docs](https://newsagentdata.com/documentation/) · 🗺️ [Coverage](https://newsagentdata.com/coverage/) · 💬 [Telegram](https://t.me/n3wsagent) · ✉️ support@newsagentdata.com
