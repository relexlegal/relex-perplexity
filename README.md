# Relex × Perplexity

Connect **Perplexity** to **Relex** so you can work legal cases with your
assistant — **without client names or documents ever leaving a sealed vault**.

> For lawyers and teams: simple Connectors setup. No code required.

## Quick start (personal)

1. Open [Perplexity → Account settings → Connectors](https://www.perplexity.ai/account/connectors)
2. **+ Custom connector** → choose **Remote**
3. Name: **Relex**  
   MCP Server URL: `https://relex.you/api/mcp`  
   Auth: **OAuth** (preferred)
4. Add → when asked, **Connect** and sign in to Relex (Google or Apple)
5. In a chat, use Relex tools / say: *Set up my practice workflow with Relex*

Full non-technical guide: **https://relex.you/docs/connectors/perplexity**

## Team / Enterprise

| Who | What they do |
|-----|----------------|
| **Admin** | Adds the custom connector once for the organisation (if your plan restricts custom connectors to admins) |
| **Each member** | Opens Connectors, finds **Relex**, clicks **Connect**, signs into their own Relex account |

Admin install does **not** sign members in automatically.

## Package

```
plugin/
  .mcp.json          → https://relex.you/api/mcp
  skills/            → PII-safe legal workflow skills
  commands/          → relex-setup, relex-connect
  agents/            → relex-guide
```

Same MCP server as Claude, ChatGPT, Grok, Gemini, and generic hosts.

## Sibling packages

- [relex-claude](https://github.com/relexyou/relex-claude)
- [relex-gpt](https://github.com/relexyou/relex-gpt)
- [relex-grok](https://github.com/relexyou/relex-grok)
- [relex-gemini](https://github.com/relexyou/relex-gemini)
- [relex-mcp](https://github.com/relexyou/relex-mcp)

## License

AGPL-3.0-or-later — see [LICENSE](LICENSE).
