# CreditKit

This extension connects the CreditKit MCP server (https://mcp.creditkit.dev), which sets up credits, a paywall and Stripe checkout in the developer's own AI app. The first time a CreditKit tool runs, sign in with `/mcp auth creditkit`.

When the user asks to charge credits for a feature, add a paywall or credit packs, or set up or debug CreditKit, follow the `creditkit-setup` skill. Everything runs in Test Mode; live keys and Stripe stay in the CreditKit console.
