<div align="center">

<a href="https://newsagentdata.com/"><img src="https://newsagentdata.com/banner.png" alt="NewsAgent Data — real-time, ML-enriched news intelligence as an API" width="100%"></a>

<br>

<a href="https://newsagentdata.com/"><img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3000&pause=900&color=3B82F6&center=true&vCenter=true&width=720&lines=Real-time+news+intelligence%2C+as+an+API;190%2B+countries+%C2%B7+38+languages+%C2%B7+RU%2FEN+core;Every+article+ML-enriched%3A+urgency%2C+lean%2C+clustering;Built+for+AI+agents+%E2%80%94+a+native+MCP+server" alt="Typing SVG" /></a>

<br><br>

[![Website](https://img.shields.io/badge/Website-newsagentdata.com-3b82f6?style=for-the-badge&logo=googlechrome&logoColor=white)](https://newsagentdata.com/)
[![Docs](https://img.shields.io/badge/API-Reference-3b82f6?style=for-the-badge&logo=readme&logoColor=white)](https://newsagentdata.com/documentation/)
[![MCP](https://img.shields.io/badge/AI_Agents-MCP_Server-1e293b?style=for-the-badge&logo=openai&logoColor=white)](https://newsagentdata.com/mcp/)
[![Pricing](https://img.shields.io/badge/Free_tier-from_%2429%2Fmo-22c55e?style=for-the-badge)](https://newsagentdata.com/pricing/)

</div>

<br>

## 🟢 Live from our pipeline — right now

<div align="center">

<sub>These badges pull straight from our public API and refresh automatically.</sub>

<br><br>

[![Articles](https://img.shields.io/badge/dynamic/json?style=for-the-badge&color=3b82f6&label=%F0%9F%93%B0%20Articles&query=%24.total&url=https%3A%2F%2Fnewsagentdata.com%2Fpublic%2Fstats)](https://newsagentdata.com/)
[![Added today](https://img.shields.io/badge/dynamic/json?style=for-the-badge&color=22c55e&label=%E2%9A%A1%20Last%2024h&query=%24.today&url=https%3A%2F%2Fnewsagentdata.com%2Fpublic%2Fstats)](https://newsagentdata.com/)
[![Breaking](https://img.shields.io/badge/dynamic/json?style=for-the-badge&color=ef4444&label=%F0%9F%9A%A8%20Breaking&query=%24.breaking&url=https%3A%2F%2Fnewsagentdata.com%2Fpublic%2Fstats)](https://newsagentdata.com/)

[![Countries](https://img.shields.io/badge/dynamic/json?style=for-the-badge&color=6366f1&label=%F0%9F%8C%8D%20Countries&query=%24.countries_count&url=https%3A%2F%2Fnewsagentdata.com%2Fpublic%2Fstats)](https://newsagentdata.com/coverage/)
[![Languages](https://img.shields.io/badge/dynamic/json?style=for-the-badge&color=0ea5e9&label=%F0%9F%97%A3%EF%B8%8F%20Languages&query=%24.languages_count&url=https%3A%2F%2Fnewsagentdata.com%2Fpublic%2Fstats)](https://newsagentdata.com/)
[![Sources](https://img.shields.io/badge/dynamic/json?style=for-the-badge&color=8b5cf6&label=%F0%9F%93%A1%20Sources&query=%24.sources&url=https%3A%2F%2Fnewsagentdata.com%2Fpublic%2Fstats)](https://newsagentdata.com/sources/)

<br><br>

### 📰 Latest breaking — straight from the pipeline

<a href="https://newsagentdata.com/"><img src="https://newsagentdata.com/public/card.svg" alt="Live breaking news from NewsAgent Data" width="100%"></a>

<sub>This card is generated on-the-fly by our own API. Refresh in a few hours — the headlines will be different.</sub>

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
750K+ articles, growing ~1,800/hour, across **190+ countries** and **35+ languages** — true RU + EN depth with native-language enrichment.

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

<details>
<summary><b>👀 See what a single enriched article looks like</b></summary>

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

Every field above is generated automatically — no extra calls, no post-processing.
</details>

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

Full reference → **[API docs](https://newsagentdata.com/documentation/)** · interactive Swagger at **[/docs](https://api.newsagentdata.com/docs)**

<br>

## 🤖 For AI agents (MCP)

A ready-to-use **Model Context Protocol** server lets LLM agents query the feed, search, fetch breaking news, and read coverage stats as native tools → **[MCP setup & download](https://newsagentdata.com/mcp/)**

<br>

## 🎯 Use cases

`Trading & market signals` · `OSINT & geopolitical monitoring` · `Media monitoring & PR` · `Academic & policy research` · `Grounding data for AI/LLM apps` · `Real-time alerting`

<br>

<div align="center">

**[🌐 Website](https://newsagentdata.com/)** · **[📚 Docs](https://newsagentdata.com/documentation/)** · **[💵 Pricing](https://newsagentdata.com/pricing/)** · **[🗺️ Coverage](https://newsagentdata.com/coverage/)** · **[💬 Telegram](https://t.me/n3wsagent)** · ✉️ support@newsagentdata.com

<br>

<img src="https://komarev.com/ghpvc/?username=newsagentdata&style=flat-square&color=3b82f6&label=Profile+views" alt="Profile views" />

<sub><i>The numbers above are live. So is the news.</i></sub>

</div>
