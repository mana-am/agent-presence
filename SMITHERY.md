# Mana Smithery Listing

Goal: list and verify Mana's read-only public MCP server on Smithery.

## Listing fields

- Name: `Mana Public`
- Slug: `mana-public`
- Website: `https://mana.am`
- GitHub: `https://github.com/mana-am/agent-presence`
- Server URL: `https://api.mana.am/mcp`
- Transport: Streamable HTTP
- Authentication: none
- Category: productivity, app-builder, iOS, community discovery
- Short description: `Read-only MCP tools for exploring Mana public creations,
  tags, creator profiles, and shared iPhone apps.`
- Support: `support@mana.am`

## Description

Mana is a Personal Agent for iPhone. Users describe an app, tool, tracker, or
game in plain language and Mana builds a real creation that runs on iOS 26+.
This MCP server exposes the public discovery surface only: browse published
creations, popular tags, creator profiles, and public share data.

Mana's MCP server cannot create, edit, publish, delete, or manage creations.
Those actions happen only inside the Mana iOS app.

## Tools

- `search_community_apps` - search and browse published Mana creations.
- `get_popular_tags` - list popular tags used by the Mana community.
- `get_creator_profile` - look up a public Mana creator profile.
- `get_app_share` - fetch public share data for one Mana creation.

## Verification request email

Subject: Verify official Mana MCP server on Smithery

```
Hi Smithery team,

Please verify the official Mana MCP server listing.

Company/product: Mana
Website: https://mana.am
GitHub: https://github.com/mana-am/agent-presence
Server URL: https://api.mana.am/mcp
Server card: https://api.mana.am/.well-known/mcp/server-card.json
Registry manifest: https://mana.am/.well-known/mcp/server.json
Support contact: support@mana.am

The server is read-only and unauthenticated. It exposes public community data
for published Mana creations, tags, creator profiles, and share pages.

Thanks,
Mana team
```

Send the request from a `@mana.am` mailbox or the verified Smithery account
that owns the listing.
