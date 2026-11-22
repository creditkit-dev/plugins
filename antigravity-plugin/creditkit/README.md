# CreditKit for Antigravity

Add prepaid credits, a drop-in paywall, and Stripe checkout to your AI app directly from Antigravity.

Ask Antigravity something like:

> Add CreditKit to this app. Charge 5 credits each time a user generates an image, give new users 20 free credits, and sell a 100-credit pack for $5. Then check the setup until every step is done.

Antigravity creates (or selects) your CreditKit project, configures action costs and packs, wires the SDK for your stack and auth library, and runs `check_setup` until every required step passes.

## What's included

- **CreditKit MCP server** (`https://mcp.creditkit.dev` via `mcp_config.json`): OAuth sign-in with your CreditKit account on first tool call.
- **`creditkit-setup` skill**: step-by-step onboarding workflow for configuring and verifying CreditKit in your codebase.

## Safety boundary

Everything over MCP runs in **Test Mode**: purchases are simulated and no money moves. Live keys (`sk_live_...`), Stripe Connect onboarding, domain allowlists, and plan changes stay in the CreditKit console at https://creditkit.dev/dashboard.

## Links

- Docs: https://creditkit.dev/docs/mcp
- Privacy policy: https://creditkit.dev/privacy
- Terms: https://creditkit.dev/terms
- Support: https://creditkit.dev/support
