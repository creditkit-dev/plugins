# CreditKit Plugins & MCP Skills

Official plugins and agent skills for **[CreditKit](https://creditkit.dev)** — add prepaid usage credits, crash-proof holds, a branded paywall, and Stripe checkout to any AI app directly from your coding agent.

All plugins connect to the hosted OAuth 2.1 MCP server at **`https://mcp.creditkit.dev`**.

## Included Plugins

| Client | Path | What's Inside |
| :--- | :--- | :--- |
| **Claude Code** | [`claude-plugin/creditkit`](./claude-plugin/creditkit) | `.claude-plugin/plugin.json`, `.mcp.json`, `creditkit-setup` skill |
| **Cursor** | [`cursor-plugin/creditkit`](./cursor-plugin/creditkit) | `.cursor-plugin/plugin.json`, `mcp.json`, `creditkit-setup` skill |
| **Antigravity** | [`antigravity-plugin/creditkit`](./antigravity-plugin/creditkit) | `plugin.json`, `mcp_config.json`, `creditkit-setup` skill |
| **Gemini CLI** | [`gemini-extension/creditkit`](./gemini-extension/creditkit) | `gemini-extension.json`, `GEMINI.md`, `creditkit-setup` skill |

## Direct MCP Connection

Most MCP-compatible clients (Cursor, Claude Code, VS Code, Codex, Windsurf, Lovable, v0, Bolt, Replit) can also connect directly with zero install:

- **Server URL:** `https://mcp.creditkit.dev`
- **Transport:** Streamable HTTP (`OAuth 2.1` with PKCE)
- **Setup guides for every client:** [creditkit.dev/docs/mcp](https://creditkit.dev/docs/mcp)

## Safety Boundary

Everything over MCP runs in **Test Mode** — purchases are simulated and no real money moves. Live secret keys (`sk_live_...`), Stripe Connect onboarding, production domains, and billing plans remain exclusively in the [CreditKit Console](https://creditkit.dev/dashboard).

## Links

- **Homepage:** [https://creditkit.dev](https://creditkit.dev)
- **MCP Docs:** [https://creditkit.dev/docs/mcp](https://creditkit.dev/docs/mcp)
- **LLM Reference:** [https://creditkit.dev/llms-full.txt](https://creditkit.dev/llms-full.txt)
- **Support:** [https://creditkit.dev/support](https://creditkit.dev/support)
- **Privacy Policy:** [https://creditkit.dev/privacy](https://creditkit.dev/privacy)
- **Terms of Service:** [https://creditkit.dev/terms](https://creditkit.dev/terms)

## License

MIT — see [LICENSE](./LICENSE).
