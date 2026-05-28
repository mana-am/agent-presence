# Mana MCP Registry Submission

Mana has one canonical product MCP runtime plus separate docs surfaces:

- Product MCP: `https://api.mana.am/mcp`
- Product apex alias: `https://mana.am/api/mcp`
- Docs MCP: `https://mana.am/docs/mcp`
- Docs short alias: `https://mana.am/mcp`
- Registry manifest: `https://mana.am/.well-known/mcp/server.json`
- Product server card: `https://api.mana.am/.well-known/mcp/server-card.json`

The product MCP is read-only and unauthenticated. It exposes public community,
tag, creator-profile, and share-page lookup tools. It does not create, edit, or
publish Mana creations.

## Registry metadata

Use the deployed `server.json`:

```json
{
  "$schema": "https://static.modelcontextprotocol.io/schemas/2025-12-11/server.schema.json",
  "name": "am.mana/mana-public",
  "title": "Mana Public",
  "version": "1.0.0",
  "remotes": [
    {
      "type": "streamable-http",
      "url": "https://api.mana.am/mcp"
    }
  ]
}
```

Full manifest: https://mana.am/.well-known/mcp/server.json

## Submit

The official MCP Registry is in preview and uses `mcp-publisher`.

```bash
brew install mcp-publisher
mcp-publisher --help
```

Mana uses HTTP domain authentication so the proof can be hosted at
`https://mana.am/.well-known/mcp-registry-auth` without changing DNS records.

```bash
PRIVATE_KEY="$(openssl pkey -in ~/.config/mana/mcp-registry-ed25519.pem -noout -text | awk '/priv:/{flag=1;next}/pub:/{flag=0}flag' | tr -d ' :\n')"
mcp-publisher login http --domain mana.am --private-key "$PRIVATE_KEY"
mcp-publisher publish
```

If publishing from the standalone agent repo, download the deployed manifest:

```bash
curl -L https://mana.am/.well-known/mcp/server.json -o server.json
PRIVATE_KEY="$(openssl pkey -in ~/.config/mana/mcp-registry-ed25519.pem -noout -text | awk '/priv:/{flag=1;next}/pub:/{flag=0}flag' | tr -d ' :\n')"
mcp-publisher login http --domain mana.am --private-key "$PRIVATE_KEY"
mcp-publisher publish
```

## Ownership

- Preferred registry name: `am.mana/mana-public`
- Public GitHub repo: `https://github.com/mana-am/agent-presence`
- Official website: `https://mana.am`
- Support: `support@mana.am`

Use MCP Registry domain authentication for `mana.am`; the server name
`am.mana/mana-public` follows the reverse-DNS namespace for `mana.am`. The HTTP
proof file is `https://mana.am/.well-known/mcp-registry-auth`. If using GitHub
authentication instead, the name must change to the GitHub namespace format,
for example `io.github.mana-am/mana-public`.

## Verification checks

```bash
curl -L https://mana.am/.well-known/mcp/server.json | jq .
curl -L https://api.mana.am/.well-known/mcp/server-card.json | jq .
curl -X POST "https://api.mana.am/mcp" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json, text/event-stream" \
  -d '{"jsonrpc":"2.0","id":1,"method":"tools/list"}'
```
