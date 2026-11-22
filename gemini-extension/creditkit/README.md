# CreditKit for Gemini CLI

Add credits, a paywall and Stripe checkout to your AI app from the terminal.

Connect the hosted MCP server directly:

```bash
gemini mcp add --transport http creditkit https://mcp.creditkit.dev
```

Or install the full extension (MCP server + `creditkit-setup` skill + `GEMINI.md` context) from a local checkout of this bundle:

```bash
gemini extensions install ./integrations/gemini-extension/creditkit
```

Then ask: "Add CreditKit to this app and charge 5 credits per generated image." Sign in to CreditKit the first time a tool runs (`/mcp auth creditkit`).

Everything runs in Test Mode; live keys and Stripe stay in the CreditKit console. Docs: https://creditkit.dev/docs/mcp · Privacy: https://creditkit.dev/privacy
