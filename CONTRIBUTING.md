# Contributing

Thanks for helping keep this list accurate! Pricing in this space changes
*monthly*, so corrections are as valuable as additions.

## What belongs here

This list catalogs **subscriptions and paid model-access plans for agentic
coding** — the thing you *pay for* to put an LLM behind a coding agent.

✅ In scope:

- First-party frontier subscriptions (Claude Max, ChatGPT Pro, Gemini, …)
- Bundled tool subscriptions where you buy a plan (Cursor, Copilot, Windsurf, …)
- Flat-rate coding plans (GLM Coding Plan, Kimi, MiniMax, …)
- Pay-as-you-go API access (DeepSeek, Qwen, OpenRouter, Groq, …)
- Routers / gateways / free tiers / cheap-access hidden gems

❌ Out of scope:

- The **harness** itself (Claude Code, Cline, Aider, Roo, Continue, Zed editor) —
  these are free clients; they belong only in the *integration* column.
- Pure local / self-host runtimes (Ollama, llama.cpp, vLLM) — the opposite of a
  subscription.

## How to add or fix an entry

1. Keep entries in the right section, sorted by **value**.
2. Use the badge legend: 💎 hidden gem · 🆓 free tier · ⭐ value rating · ✅ verified pricing.
3. **Cite a source** — link the official pricing page (and a community thread if
   the claim is about sentiment/value).
4. Use concrete numbers: exact price, exact limits, exact model names.
5. If you're correcting a price, note the date you verified it.
6. One change per pull request where possible. Run `npx awesome-lint` before
   submitting.

## Format for an entry

```
- **[Name](https://link)** — `$price/period`. Models: X, Y. Limits: Z.
  Integration: OpenAI-compat / Claude Code backend / etc. ⭐4 💎
  *Why it's here.* [pricing](url) · [community](url)
```

Disagreements about value ratings are welcome — open an issue with your
reasoning and benchmark/price evidence.
