---
name: placed-setup
description: Set up the PLACED_API_KEY so the user can use placed-mcp from Claude or any MCP client. Guides through checking, obtaining, and saving the API key. Use when the user says 'setup placed', 'configure placed', 'placed api key', 'placed token', 'connect placed', 'placed mcp setup', or 'I want to use placed'.
tags: "placed,setup,api-key,mcp,configure,token,placed-mcp,exidian"
version: "1.0.0"
allowed-tools: Bash, Read
---

# Placed Setup — API Key Configuration

Get the user's `PLACED_API_KEY` configured so placed-mcp works.

## Step 0 — Token Provided Directly

If the user's message contains a token (starts with `eyJ` or looks like a long API key string), skip all steps and save it immediately:

```bash
echo 'export PLACED_API_KEY=<token>' >> ~/.zshrc && source ~/.zshrc
```

Then verify with the health check (Step 3 below) and confirm success.

---

## Step 1 — Check if Already Set

```bash
printenv PLACED_API_KEY
```

- If output is non-empty → key is already set. Go to Step 3 to verify it works.
- If output is empty → key is not set. Continue to Step 2.

---

## Step 2 — Obtain the API Key

Tell the user:

> Your PLACED_API_KEY is not set. Let's fix that.
>
> 1. Open this URL in your browser:
>    https://placed.exidian.tech/settings/api-key
>
> 2. Copy the token shown on that page.
>
> 3. Paste it here and I'll save it for you automatically.

Wait for the user to paste the token, then save it:

```bash
echo 'export PLACED_API_KEY=<token_from_user>' >> ~/.zshrc && source ~/.zshrc
```

Confirm it's now in the environment:

```bash
printenv PLACED_API_KEY
```

---

## Step 3 — Verify with Health Check

Call the Placed API health check to confirm the key works:

```bash
curl -s -X POST https://placed.exidian.tech/api/mcp \
  -H "Authorization: Bearer $PLACED_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"jsonrpc":"2.0","id":1,"method":"tools/call","params":{"name":"health_check","arguments":{}}}'
```

- If the response contains `"ok"` or a success result → tell the user: "You're all set. placed-mcp is connected and working."
- If the response contains an auth error → the token is invalid. Ask the user to re-check https://placed.exidian.tech/settings/api-key and repeat Step 2.
- If curl fails entirely → check network connectivity and try again.

---

## Notes

- The key is saved to `~/.zshrc`. If the user uses a different shell (bash, fish), adjust accordingly:
  - bash: `~/.bashrc` or `~/.bash_profile`
  - fish: `set -Ux PLACED_API_KEY <token>` (no export needed)
- Never log or display the full token in output — truncate to first 8 chars if you need to reference it: `${PLACED_API_KEY:0:8}...`
- If the user is on a machine where `source ~/.zshrc` doesn't propagate to the current shell session, remind them to open a new terminal or run `export PLACED_API_KEY=<token>` directly for the current session.
