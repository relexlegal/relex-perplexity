# Submission — Perplexity

> Prepared 2026-10-28 on branch `directory-review-2026-10`. Nothing has been
> submitted, pushed or deployed. Before any submission: deploy the backend branch
> `directory-review-2026-10` (neutral server instructions, data-only responses),
> then merge and push this repo.

Hosted server: `https://relex.legal/api/mcp` (streamable HTTP, OAuth 2.1 with
PKCE and dynamic client registration). Twelve tools: `list_matters`,
`read_matter_context`, `diagnose_matter_sources`, `read_matter_source`,
`save_matter_work_product`, `correct_matter_ontology`, `conclude_matter_session`,
`find_legal_professionals`, `read_legal_professional`,
`prepare_professional_request`, `search`, `execute`.

Perplexity has two paths: (1) any user can add Relex now as a custom remote
connector; (2) a curated Connector Marketplace listing is by partnership
proposal (form on perplexity.ai or connectors@perplexity.ai).

## Done in this branch / backend
- [x] Plugin 0.1.6; SECURITY.md reading default corrected; skills audited.
- [x] Backend: the OAuth consent screen now names "Perplexity" when the redirect goes to `www.perplexity.ai` / `enterprise.perplexity.ai` (`functions/src/oauth.py` VERIFIED_REDIRECT_HOSTS, test in `test_oauth_pkce.py`). Redirect `https://www.perplexity.ai/rest/connections/oauth_callback` is accepted (any https redirect is).
- [x] Logo `plugin/assets/logo.png` is 28 KB (limit 128 KB).

## User must do
- [ ] Custom connector check: Perplexity → Settings → Connectors/Plugins → Add custom → Remote, URL `https://relex.legal/api/mcp`, OAuth (discovery + DCR). Sign in and run "List my Relex matters".
- [ ] github.com/relexlegal/relex-perplexity returns 404 publicly (private or not created). Make it public if you want to link it.
- [ ] Send the marketplace proposal (draft in the parent report; not sent).
