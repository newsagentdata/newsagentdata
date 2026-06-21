<div align="center">

<a href="https://newsagentdata.com/"><img src="https://newsagentdata.com/banner.png" alt="NewsAgent Data — real-time, ML-enriched news intelligence as an API" width="100%"></a>

<br><br>

[![Website](https://img.shields.io/badge/Website-newsagentdata.com-3b82f6?style=for-the-badge)](https://newsagentdata.com/)
[![Docs](https://img.shields.io/badge/API-Reference-3b82f6?style=for-the-badge)](https://newsagentdata.com/documentation/)
[![MCP](https://img.shields.io/badge/AI_Agents-MCP_Server-1e293b?style=for-the-badge)](https://newsagentdata.com/mcp/)
[![Pricing](https://img.shields.io/badge/Free_tier-from_%2429%2Fmo-22c55e?style=for-the-badge)](https://newsagentdata.com/pricing/)

</div>

<br>

> Most news APIs hand you **raw articles**. NewsAgent Data hands you **structured intelligence** — every article arrives already labeled with an urgency score, political lean, topic, event clustering, and audience tags, so you build on signal instead of parsing noise.

Global coverage with a Russian & English core, drawn from **RSS + Telegram** sources that most providers don't touch.

<br>

## ✨ What makes it different

<table>
<tr>
<td width="50%" valign="top">

### 🧠 Enrichment on every article
Urgency score (1–10), breaking detection, political-lean classification, event clustering & de-duplication, plus topic, country, audience, language and event-type tags.

</td>
<td width="50%" valign="top">

### 🌍 Coverage at scale
750K+ articles, growing ~1,800/hour, across **190+ countries** and **35+ languages**, from **7,000+ sources** — true RU + EN depth with native-language enrichment.

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 📡 Sources others miss
RSS **and** Telegram — a major edge for OSINT, geopolitics, and breaking-news monitoring.

</td>
<td width="50%" valign="top">

### 🤖 Built for AI & automation
A native **MCP server** for LLM agents, plus REST, SSE live streaming, JSONL bulk export, and HMAC-signed webhooks.

</td>
</tr>
</table>

<br>

## 🚀 Quick start

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
  "cluster_id": 1782068387
}
```

<br>

## 🔌 Endpoints

| Endpoint | Purpose |
|---|---|
| `GET /v1/feed` | Main feed — filter by language, score, days, country, lean, topic, audience |
| `GET /v1/breaking` | High-urgency articles (score ≥ 7) |
| `GET /v1/search?q=` | Keyword search |
| `GET /v1/audience/{audience}` | Audience feed — trading · media · academic · security · tech · politics |
| `GET /v1/stream` | Live Server-Sent Events stream |
| `GET /v1/export/jsonl` | Bulk JSONL export |
| `POST /v1/webhook` | Register an HMAC-signed breaking-news webhook |

Full reference: **[API documentation](https://newsagentdata.com/documentation/)** · interactive Swagger at **[/docs](https://api.newsagentdata.com/docs)**

<br>

## 🤖 For AI agents (MCP)

A ready-to-use **Model Context Protocol** server lets LLM agents query the feed, search, fetch breaking news, and read coverage stats as native tools → **[MCP setup & download](https://newsagentdata.com/mcp/)**

<br>

## 🎯 Use cases

`Trading & market signals` · `OSINT & geopolitical monitoring` · `Media monitoring & PR` · `Academic & policy research` · `Grounding data for AI/LLM apps` · `Real-time alerting`

<br>

<div align="center">

**[🌐 Website](https://newsagentdata.com/)** · **[📚 Docs](https://newsagentdata.com/documentation/)** · **[💵 Pricing](https://newsagentdata.com/pricing/)** · **[🗺️ Coverage](https://newsagentdata.com/coverage/)** · **[💬 Telegram](https://t.me/n3wsagent)** · ✉️ support@newsagentdata.com

</div>
