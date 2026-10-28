# Submission — Perplexity

> Prepared 2026-10-28; updated the same day for MCP server version 1.1.0
> (branch `docs/read-api-1.1.0`). Nothing has been submitted. The backend with
> neutral server instructions, data-only responses and the `read_api` tool is
> on `master` (5a5d7b9) and deployed as revision `relex-backend-00192`.

Hosted server: `https://relex.legal/api/mcp` (streamable HTTP, OAuth 2.1 with
PKCE and dynamic client registration). Thirteen tools: `list_matters`,
`read_matter_context`, `diagnose_matter_sources`, `read_matter_source`,
`save_matter_work_product`, `correct_matter_ontology`, `conclude_matter_session`,
`find_legal_professionals`, `read_legal_professional`,
`prepare_professional_request`, `search`, `read_api`, `execute`.

Server version 1.1.0. `read_api` reads one GET endpoint (read-only; parameters
`path` and optional `query`). `execute` creates, updates or deletes through one
endpoint (POST/PUT/PATCH/DELETE); DELETE and other irreversible routes are not
applied by the tool and return a Relex deep link where the user confirms the
change.

Perplexity has two paths: (1) any user can add Relex now as a custom remote
connector; (2) a curated Connector Marketplace listing is by partnership
proposal (form on perplexity.ai or connectors@perplexity.ai).

## Done in this branch / backend
- [x] Plugin 0.1.7; SECURITY.md reading default corrected; skills audited.
- [x] Backend: the OAuth consent screen now names "Perplexity" when the redirect goes to `www.perplexity.ai` / `enterprise.perplexity.ai` (`functions/src/oauth.py` VERIFIED_REDIRECT_HOSTS, test in `test_oauth_pkce.py`). Redirect `https://www.perplexity.ai/rest/connections/oauth_callback` is accepted (any https redirect is).
- [x] Logo `plugin/assets/logo.png` is 28 KB (limit 128 KB).

## User must do
- [ ] Custom connector check: Perplexity → Settings → Connectors/Plugins → Add custom → Remote, URL `https://relex.legal/api/mcp`, OAuth (discovery + DCR). Sign in and run "List my Relex matters".
- [ ] github.com/relexlegal/relex-perplexity returns 404 publicly (private or not created). Make it public if you want to link it.
- [ ] Send the marketplace proposal (draft in the parent report; not sent).
