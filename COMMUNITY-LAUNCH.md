# Mana Third-Party Corpus Launch

Goal: create durable, independent mentions so search engines and LLMs can
disambiguate Mana from unrelated "Mana" entities.

## Positioning

Short description:

> Mana is a Personal Agent for iPhone. Describe an app, tracker, tool, game, or
> shared experience in plain language and Mana builds a real creation that runs
> on your iPhone. Create, play, remix.

Search phrases to repeat naturally:

- AI assistant for creating content on iPhone
- AI app builder for iPhone
- create iPhone apps without coding
- personal agent for iPhone
- no-code iOS app builder
- build trackers and games on iPhone

## Launch order

1. Publish 2-3 concrete case studies on `mana.am`.
2. Submit Product Hunt with screenshots and a short demo video.
3. Post a technical Show HN only when the post has a real demo and details.
4. Share in focused communities: iOS builders, no-code builders, AI agents,
   creator tools, and indie apps.
5. Pitch journalists and newsletters with one story angle and measurable facts.
6. Publish an engineering post about the public API, MCP, and agent docs.

## Hacker News draft

Title:

```
Show HN: Mana - describe an iPhone app and run it instantly on your phone
```

Body:

```markdown
Mana is a Personal Agent for iPhone. You describe an app, tracker, small game,
or shared tool in natural language, and Mana builds a real iOS creation that
runs on your phone. Each creation gets a public share link and can be remixed.

We made the public discovery surface agent-readable too:
- OpenAPI: https://mana.am/openapi.json
- MCP: https://api.mana.am/mcp
- llms.txt: https://mana.am/llms.txt
- Agent skill: https://www.skills.sh/mana-am/agent-presence/mana

I'd love feedback from people who prototype personal tools on iPhone, especially
where this should be more native than a web/no-code workflow.
```

## Reddit draft

Use this only in communities where self-promotion is allowed.

```markdown
I am working on Mana, an iPhone app that turns natural-language descriptions
into runnable iPhone creations: small apps, trackers, games, shared albums, and
tools. The interesting part is that the output runs on-device and can be shared
or remixed with a public link.

Example prompt: "make me a shared habit tracker for my running group with weekly
check-ins and reminders."

Website: https://mana.am
App Store: https://apps.apple.com/app/id6757949329
Public API / agent docs: https://mana.am/developers.md

Looking for feedback from people who build personal iPhone workflows or creator
tools: what would make this more useful than a web no-code builder?
```

## Press pitch

Subject:

```
Mana turns plain-language prompts into runnable iPhone creations
```

Email:

```text
Hi [name],

I am reaching out about Mana, a Personal Agent for iPhone. Users describe an
app, tracker, game, or shared tool in plain language, and Mana builds a runnable
iPhone creation with sharing and remixing built in.

The angle: consumer AI app creation is moving from web previews to native phone
experiences. Mana targets the "make a small app for this moment" workflow:
trackers, group tools, games, shared albums, and lightweight utilities.

Useful links:
- Website: https://mana.am
- App Store: https://apps.apple.com/app/id6757949329
- Agent/developer docs: https://mana.am/developers.md
- Public API: https://mana.am/openapi.json

Happy to share screenshots, usage examples, or a short demo.

Best,
Mana team
```

## YouTube/short demo script

```text
I am going to build an iPhone app by describing it.

Prompt: "Make a two-player habit tracker for my roommate and me. Show streaks,
send reminders, and let us share progress."

Mana writes the app, runs it on the phone, and gives it a share link. I can
open it, test it, and remix it without touching Xcode or waiting for TestFlight.

That is Mana: create, play, remix on iPhone.
```
