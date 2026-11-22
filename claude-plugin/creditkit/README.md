# CreditKit for Claude

Add credits, a paywall and Stripe checkout to your AI app without leaving Claude.

Ask Claude something like:

> Add CreditKit to this app. Charge 5 credits each time a user generates an image, give new users 20 free credits, and sell a 100-credit pack for $5. Then check the setup until every step is done.

Claude creates (or picks) your CreditKit project, sets what each action costs, adds the code for your stack and login library, and checks that charges and purchases work.

## What's included

- **CreditKit connector** (`https://mcp.creditkit.dev`): you sign in with your CreditKit account the first time it's used.
- **`creditkit-setup` skill**: the step-by-step setup Claude follows.

## What it can't do

Everything runs in Test Mode: purchases are simulated and no money moves. It can't see or use your live keys, connect Stripe, change your CreditKit plan, move money or delete projects. Those stay in the console at https://creditkit.dev/dashboard.

## Links

- Docs: https://creditkit.dev/docs/mcp
- Privacy policy: https://creditkit.dev/privacy
- Terms: https://creditkit.dev/terms
- Support: https://creditkit.dev/support
