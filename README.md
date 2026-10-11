# Relex × Perplexity

**Legal Workspace — One source of truth for any Agent — confidential by design**

Keep legal knowledge, matter context and saved progress in Relex, independently
of the assistant you use. Authorize another compatible agent to continue from
the same stored context, without rebuilding the background in another chat.

## Portable context, with your permission

1. Create or open the matter in Relex and add information through its protected
   intake and document workflows.
2. Connect a supported client to `https://relex.legal/api/mcp` and authorize
   your own Relex account. Installing a package does not authorize private data.
3. Ask the agent to read the permitted matter context before working and save
   its conclusions when finished. A second authorized client can then use that
   continuing record.

Portability covers information saved in Relex, not automatic import of private
chat histories or a model's internal memory. Client-side identity encryption,
de-identification and MCP access controls protect the supported workflows;
de-identified legal facts may still be sensitive. Review what you authorize.

## Workspace, SDK and Marketplace

Use **Legal Workspace** for persistent legal context; the **Legal SDK** for
building your firm's or legal department's own platform; and the
**Legal Marketplace** to discover published professional profiles or make an
AI-first law firm discoverable across specialties.

An agent may help find a professional and prepare a reference-only request.
The user must review and approve sharing in Relex. Discovery is not engagement,
a completed conflict check, payment or a guarantee of professional availability.

Client support depends on the host product, plan and administrator settings.
Gemini CLI support does not imply support in every Gemini web experience.
Harvey BYOMCP is a customer-admin connection path, not a claim of Harvey
Connector Library listing or approval. Check the current
[connector guides](https://relex.legal/docs/connectors) and
[portable-context guide](https://relex.legal/guides/portable-legal-context).
## Quick start (personal)

1. Open [Perplexity → Account settings → Connectors](https://www.perplexity.ai/account/connectors)
2. **+ Custom connector** → choose **Remote**
3. Name: **Relex**  
   MCP Server URL: `https://relex.legal/api/mcp`  
   Auth: **OAuth** (preferred)
4. Add → when asked, **Connect** and sign in to Relex (Google or Apple)
5. In a chat, use Relex tools / say: *Set up my practice workflow with Relex*

Full non-technical guide: **https://relex.legal/docs/connectors/perplexity**

## Team / Enterprise

| Who | What they do |
|-----|----------------|
| **Admin** | Adds the custom connector once for the organisation (if your plan restricts custom connectors to admins) |
| **Each member** | Opens Connectors, finds **Relex**, clicks **Connect**, signs into their own Relex account |

Admin install does **not** sign members in automatically.

## Package

```
plugin/
  .mcp.json          → https://relex.legal/api/mcp
  skills/            → PII-safe legal workflow skills
  commands/          → relex-setup, relex-connect
  agents/            → relex-guide
```

Same MCP server as Claude, ChatGPT, Grok, Gemini, and generic hosts.

## Sibling packages

- [relex-claude](https://github.com/relexlegal/relex-claude)
- [relex-gpt](https://github.com/relexlegal/relex-gpt)
- [relex-grok](https://github.com/relexlegal/relex-grok)
- [relex-gemini](https://github.com/relexlegal/relex-gemini)
- [relex-mcp](https://github.com/relexlegal/relex-mcp)

## License

AGPL-3.0-or-later — see [LICENSE](LICENSE).

## MCP tools (remote server)

The hosted connector at `https://relex.legal/api/mcp` exposes **twelve** tools:
`list_matters`, `read_matter_context`, `read_matter_source`, `diagnose_matter_sources`,
`save_matter_work_product`, `correct_matter_ontology`, `conclude_matter_session`,
`find_legal_professionals`, `read_legal_professional`, `prepare_professional_request`,
`search`, and `execute`. Auth is OAuth 2.1 + PKCE; connector scopes are
`relex.cases.read relex.cases.write relex.draft`.

Perplexity custom MCP / connector flows use the same remote URL and OAuth; follow Perplexity’s current connector settings.
