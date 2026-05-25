# Mana

> Your Personal Agent for iPhone. Describe what you want in plain language and
> Mana turns it into a real, runnable creation on your iPhone — apps, trackers,
> two-player games, and shared albums — with a real backend wired in.
> **Create · Play · Remix.**

- Website: https://mana.am
- App Store: https://apps.apple.com/app/id6757949329
- Platform: iOS 26+

This repository is Mana's **public agent & developer presence**: machine-readable
docs, an agent skill, and instructions for how AI agents and AI coding tools
should understand and interact with Mana. The product itself (the iOS app and
its backend) is closed-source; this repo exists so agents can discover Mana at a
predictable, public location.

## How Mana works

1. **Start with a sentence** — describe what you want, like telling a friend.
2. **Mana writes the code** — files, logic, and UI, generated and checked.
3. **It runs on your iPhone** — no install, no TestFlight, instant.
4. **Share with one tap** — every creation gets a `{handle}.mana.am` link; it
   can be remixed by anyone.

Native iOS surfaces (Dynamic Island, widgets, Siri, Shortcuts, sensors) and a
real backend (database, file storage, push, email, realtime, 500+ integrations)
are baked into every creation.

## Public read API

Base URL `https://api.mana.am`. No authentication; read-only; fair-use.

| Endpoint | Description |
| --- | --- |
| `GET /public/share/community` | Paginated, sortable, searchable community feed |
| `GET /public/share/tags` | Globally popular tags with counts |
| `GET /public/share/user/{handle}` | Public creator profile + their public apps |
| `GET /public/share/app/{handle}/{slug}` | Public data for one creation |

Full schema: **[OpenAPI 3.1](https://mana.am/openapi.json)**. Responses use the
envelope `{ "code": 0, "data": ... }`.

```bash
curl "https://api.mana.am/public/share/community?sort=recent&limit=5"
```

There is **no** public write API, OAuth-for-agents flow, or MCP server —
building happens in the iOS app.

## For AI agents

- [`AGENTS.md`](./AGENTS.md) — how AI agents / coding tools should interact with Mana.
- [`SKILL.md`](./SKILL.md) — installable agent skill (also served at
  https://mana.am/.well-known/agent-skills/mana/SKILL.md).
- Context index: https://mana.am/llms.txt and https://mana.am/llms-full.txt
- Pricing: https://mana.am/pricing.md · Auth: https://mana.am/auth.md

## Links

- X / Twitter: https://x.com/try_mana_app
- Support: support@mana.am
