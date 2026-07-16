# Connect Relex in Perplexity

**You need:** a Perplexity plan that allows custom connectors (typically Pro / Max / Enterprise), and a free Relex account at [relex.you](https://relex.you).

## Personal account

1. Open **Account settings → [Connectors](https://www.perplexity.ai/account/connectors)**
2. Click **+ Custom connector**
3. Select **Remote**
4. Fill in:
   - **Name:** Relex  
   - **MCP Server URL:** `https://relex.you/api/mcp`  
   - **Auth:** OAuth (recommended)  
   - Transport: Streamable HTTP if asked  
5. Confirm any risk acknowledgement → **Add**
6. Click **Connect** on Relex and sign in with Google or Apple
7. Start a chat and ask to set up your practice workflow with Relex

## Team / organisation

1. **Admin:** add the custom connector once (same URL) if members cannot add their own  
2. **Each member:** Connectors → find Relex → **Connect** → own Relex login  

## Fallback

If OAuth is unavailable in your UI, create an API key in Relex **Settings → API Keys** and choose API key auth on the connector (advanced). Prefer OAuth when possible.

## Safety

Client names and documents stay encrypted in the browser. Perplexity only works with labels like `[Party 1]`.
