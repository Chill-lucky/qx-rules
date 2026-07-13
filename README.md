# QX Rules

Quantumult X rule lists.

## IBKR / thinkorswim direct routing

Subscription URL:

```text
https://raw.githubusercontent.com/Chill-lucky/qx-rules/main/ibkr-trading.list
```

This list is optimized for mainland China users who want IBKR / thinkorswim / Schwab related traffic to bypass proxy rules.

Policy used by this list:

- `DIRECT`

## OpenAI Codex / ChatGPT / Gemini proxy routing

Subscription URL:

```text
https://raw.githubusercontent.com/Chill-lucky/qx-rules/main/openai-codex.list
```

Recommended Quantumult X `[filter_remote]` entry:

```text
https://raw.githubusercontent.com/Chill-lucky/qx-rules/main/openai-codex.list, tag=🤖 OpenAI & Gemini, force-policy=OpenAI, update-interval=86400, opt-parser=true, enabled=true
```

This list keeps Codex model streaming, secure WebSocket traffic, authentication,
static assets, uploads, Google Gemini, and required shared dependencies on the
same proxy path.
It is intended for profiles that already define an `OpenAI` policy group.
It includes OpenAI's current published network destinations plus dedicated
legacy, CAPTCHA, CDN, asset, and LiveKit compatibility hosts. It intentionally
excludes volatile IP/ASN rules and broad shared-service suffixes that could
reroute unrelated apps.

This list can replace existing generic OpenAI and Gemini remote filters. After
updating remote resources, disable the old filters, restart ChatGPT/Codex and
Gemini, and verify sign-in, model streaming, file uploads, and voice before
removing the old entries.

Policy used by this list:

- `OpenAI`
