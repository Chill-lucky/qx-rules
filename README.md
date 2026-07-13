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

## OpenAI Codex / ChatGPT proxy routing

Subscription URL:

```text
https://raw.githubusercontent.com/Chill-lucky/qx-rules/main/openai-codex.list
```

Recommended Quantumult X `[filter_remote]` entry:

```text
https://raw.githubusercontent.com/Chill-lucky/qx-rules/main/openai-codex.list, tag=🤖 Codex & OpenAI, force-policy=OpenAI, update-interval=86400, opt-parser=true, enabled=true
```

This list keeps Codex model streaming, secure WebSocket traffic, authentication,
static assets, uploads, and required shared dependencies on the same proxy path.
It is intended for profiles that already define an `OpenAI` policy group.

Policy used by this list:

- `OpenAI`
