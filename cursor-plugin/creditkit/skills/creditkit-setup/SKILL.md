---
name: creditkit-setup
description: Add CreditKit credits, a paywall and Stripe checkout to the developer's own AI app using the CreditKit MCP tools. Use when the user asks to charge credits for an AI feature, add a paywall or credit packs, give users free credits, or set up or debug CreditKit in their codebase.
---

# Set up CreditKit in an app

CreditKit lets a developer charge their app's users credits for AI actions (for example, 5 credits per generated image), sell credit packs through the developer's own Stripe account, and refund credits automatically when a run fails. These tools configure the developer's own app. They never buy anything or charge the person you are talking to.

Everything you do here uses **Test Mode**: purchases are simulated and no money moves. Live keys, connecting Stripe and plan changes happen only in the CreditKit console (https://creditkit.dev/dashboard), never through these tools.

## Steps

1. **Find or create the project.** Call `list_projects`. If the app has no project yet, call `create_project` with the app's name (and its production URL if the user gives one).
2. **Decide what costs credits.** Ask the user which actions in their app should cost credits and how many, unless they already said. Call `set_action` once per action, using a short code name such as `generate_image`. If the user knows what one run costs them (their AI/API bill), pass `cost_per_use_usd` so CreditKit can show margins.
3. **Free credits (optional).** If the user wants new or returning users to get free credits, call `set_free_credits` (once at sign-up, daily or monthly).
4. **Packs and plans (optional).** If the user wants to sell credits, call `set_packs` with 1 to 6 packs or monthly plans. Read any warnings it returns (for example a bigger pack that is worse value) and tell the user.
5. **Get the code for this app.** Look at the codebase to see the stack and login library, then call `get_setup_code` with `stack` (`nextjs` or `other`) and `auth` (`clerk`, `supabase`, `better-auth`, `authjs` or `custom`). Follow its `instructions` exactly: install command, the `.env` lines, the server client, and the charge around each AI call.
6. **Keep keys out of git.** Put the keys only in the app's local env file (for example `.env.local`) and make sure that file is git-ignored. Never paste a key into source code, a commit or a public place.
7. **Run it and check.** Ask the user to run the app and use the feature once (and try a test purchase if they set up packs). Then call `check_setup` and work through its `next` step until every required step reports done.

## When something is off

- A charge fails or a step stays not done: call `check_setup`; each step's `todo` says what's missing.
- Look up one user's credits or history: `get_user_balance`, `list_user_transactions`.
- Webhooks: `list_webhook_events` to see failures; `retry_webhook` to resend one after the endpoint is fixed.
- Full reference for the SDKs and REST API: https://creditkit.dev/llms-full.txt

## Don't

- Don't remove actions (`remove_action`) or replace packs (`set_packs`) the user didn't ask to change: both affect what the app's users can do.
- Don't ask for or handle the user's live secret key, Stripe keys or card details.
