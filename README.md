# Awesome AI Coding Subscriptions & APIs [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated, benchmarked list of the **best-value subscriptions and paid model-access plans for agentic coding** — what to actually *buy* to power Claude Code, Cursor, Cline, Aider, Roo/Kilo Code, OpenCode and friends, ranked by price ↔ power ↔ model count ↔ request limits ↔ integration.

This list catalogs the **plans you pay for** (subscriptions, flat-rate coding plans, pay-as-you-go APIs, routers, free tiers) — **not** the coding tools themselves. The harness (Claude Code, Cline, Aider…) is free; it's only the *integration target*. The interesting question is which cheap backend you put behind it.

**The one-line takeaway:** a $3–30/mo flat-rate plan from a Chinese open-weight lab (GLM / Kimi / DeepSeek / MiniMax / Qwen) pointed at a free CLI harness gets you ~78–80% SWE-bench coding for **7–15% of the price** of a $200 frontier subscription. Frontier subs still win the hardest 5–10% of tasks. Most pros in 2026 **stack both**: a frontier sub for hard reasoning + a cheap plan for high-volume agentic overflow.

> ⚠️ **Pricing in this space changes monthly.** Numbers reflect **~June 2026**. Always confirm on the official page before buying. Corrections welcome — see [Contributing](#contributing).

---

## Legend

| Badge | Meaning |
|-------|---------|
| 💎 | **Hidden gem** — punches above its price / under-the-radar |
| 🆓 | Has a genuinely usable **free tier** |
| ✅ | **Pricing fact-checked** against official source (June 2026) |
| ⭐ | Value rating (1–5), price-vs-power-vs-limits-vs-integration |
| 🇨🇳 | China-hosted (data-residency / latency caveat for some) |
| ⚠️ | Carries notable risk (ToS, reliability, longevity, reseller) |

**Integration shorthand:** `CC-native` = native Anthropic-compatible endpoint, drop-in Claude Code backend via `ANTHROPIC_BASE_URL`. `OpenAI-compat` = works in Cline/Roo/Kilo/Aider/Continue/OpenCode by base-URL swap (Claude Code needs a shim/router). `Native-only` = locked to the vendor's own editor/agent, not reusable as a backend.

---

## Contents

- [How to choose](#how-to-choose)
- [TL;DR — top picks by use-case](#tldr--top-picks-by-use-case)
- [Master comparison table](#master-comparison-table)
- [First-party frontier subscriptions](#first-party-frontier-subscriptions)
- [Bundled tool subscriptions (editor + model)](#bundled-tool-subscriptions-editor--model)
- [Flat-rate coding plans — the value champions 💎](#flat-rate-coding-plans--the-value-champions-)
- [Pay-as-you-go value APIs](#pay-as-you-go-value-apis)
- [Speed / fast-inference providers](#speed--fast-inference-providers)
- [Routers & gateways](#routers--gateways)
- [Free tiers 🆓](#free-tiers-)
- [Niche & specialty](#niche--specialty)
- [Hidden gems & reseller proxies ⚠️](#hidden-gems--reseller-proxies-)
- [Plugging cheap plans into your harness](#plugging-cheap-plans-into-your-harness)
- [Benchmark-per-dollar](#benchmark-per-dollar)
- [What the community actually says](#what-the-community-actually-says)
- [Caveats & disclaimer](#caveats--disclaimer)
- [Contributing](#contributing)

---

## How to choose

Score every plan on five axes:

1. **💵 Price** — sticker, and the *real* effective cost (credit ratios, peak multipliers, overage).
2. **🧠 Power** — model quality; the value tier clusters at ~78–80% SWE-bench Verified, frontier at 85–89%.
3. **🔢 Model count** — one plan that multiplexes many models (Qwen Coding Plan, OpenRouter) hedges churn.
4. **📊 Limits** — requests/tokens per 5h-window, weekly caps, concurrency. The hidden cost: one IDE "prompt" fans out to **5–30 model calls**, so advertised "prompts/5h" are softer than they look.
5. **🔌 Integration** — does it expose a **native Anthropic endpoint** (clean Claude Code drop-in) or only OpenAI-compat (needs a router)? Or is it native-only (no reuse)?

**Decision shortcut:**

- Want the **best agent, simplest path** → Claude Pro $20 → Max 5x $100.
- Want **most coding per dollar** → a flat-rate plan (GLM / MiniMax / Qwen / Kimi) on Claude Code.
- Want **$0** → Cerebras free + OpenRouter free (+$10 unlock) + NVIDIA NIM, escalate hard tasks to a paid model.
- Want **one key for everything** → OpenRouter.
- Want **privacy (no China-host)** → Synthetic.new (US, no-train, 14-day deletion) or first-party US subs.

---

## TL;DR — top picks by use-case

| Use-case | Pick | Why | ~Price |
|----------|------|-----|--------|
| 🏆 **Best overall value** | **GLM Coding Plan** 💎🇨🇳 | "3× Claude Max usage for ~$30/mo"; GLM-5.1 ~94% of Opus coding; native Claude Code | $10–30/mo |
| 🥇 **Best raw frontier** | **Claude Max 5x** | Unlocks Opus in Claude Code, the consensus #1 agent | $100/mo |
| 🪙 **Cheapest serious entry** | **GLM Lite** / **Qwen Standard** / **Trae Lite** 💎 | Real coding backend from ~$3–10/mo | $3–10/mo |
| 💸 **Cheapest per token** | **DeepSeek V4-Flash** 💎 | $0.14/M in, $0.0028/M cache-hit, 1M ctx, CC-native | pay-go |
| 🧪 **Best free** | **Cerebras free** 🆓 + **OpenRouter :free** 🆓 | 1M tok/day (fast) + Qwen3-Coder-480B free | $0 |
| ⚡ **Best fast+cheap** | **Groq** 💎🆓 / **Cerebras Code** | Native Anthropic endpoint (Groq); ~2000 tok/s flat-rate (Cerebras) | free / $50/mo |
| 🔀 **Best universal router** | **OpenRouter** | 315+ models, one key, Anthropic skin, no token markup | pay-go +5.5% |
| 🔒 **Best privacy (US-host)** | **Synthetic.new** 💎 | US infra, no-train, 14-day deletion, dual OpenAI+Anthropic compat | $20–60/mo |
| 🧰 **Best for big codebases** | **Augment Code** ✅ | Best-in-class Context Engine for monorepos | $20+/mo |
| 🏢 **Best team value** | **Claude Team Premium seat** 💎 | ≈ Max-5x usage + SSO/admin | $100/seat |

---

## Master comparison table

Sorted roughly by value. Prices ~June 2026; **verify before buying**.

| Plan | Type | Price | Models | Limits (coding) | Integration | ⭐ | Notes |
|------|------|-------|--------|-----------------|-------------|----|-------|
| [GLM Coding Plan](#glm-coding-plan-zai) | flat-rate | $10–30/mo (Lite/Pro, qtrly) | GLM-5.1/5/4.7 | Lite ~80, Pro ~400 prompts/5h | CC-native | ⭐5 | 💎🇨🇳✅ |
| [DeepSeek API](#deepseek) | pay-go API | V4-Pro $0.435/$0.87; Flash $0.14/$0.28 | V4-Pro/Flash | 1M ctx, 500–2500 concur | CC-native | ⭐5 | 💎🇨🇳✅ |
| [MiniMax Coding Plan](#minimax) | flat-rate | $10–50/mo | M2.7 (plan), M2.5/M3 (API) | Starter ~100, Max ~1000 prompts/5h | CC-native | ⭐5 | 💎🇨🇳 |
| [Kimi Code](#kimi-moonshot) | flat-rate+API | ~$19/mo + metered | K2.6 (1T) | ~300–1200 calls/5h, 30 concur | CC-native | ⭐5 | 💎🇨🇳 |
| [Qwen Cloud Coding Plan](#qwen-alibaba) | flat-rate | Pro $50/mo (Lite $10, closed) | Qwen3.5 + Kimi/GLM/MiniMax | Pro 6000 req/5h, 1M ctx | CC-native | ⭐4 | 💎🇨🇳✅ |
| [OpenRouter](#openrouter) | router | pay-go, +5.5% top-up | 315+ (all of them) | balance-bound; free models 50–1000/day | CC-native skin | ⭐5 | 🆓 |
| [Claude Pro](#anthropic-claude) | first-party | $20/mo | Sonnet 4.6 (no Opus) | ~40–45 msg/5h + weekly | CC-native | ⭐5 | best entry |
| [Claude Max 5x](#anthropic-claude) | first-party | $100/mo | + Opus 4.6/4.7 | ~50–225 prompts/5h | CC-native | ⭐5 | Opus unlocked |
| [Cerebras Code](#cerebras) | flat-rate speed | $50/$200 | GLM-4.7 (~2000 tok/s) | 24M–120M tok/day, 131k ctx | OpenAI-compat | ⭐5 | ✅ often sold out |
| [Synthetic.new](#synthetic) | flat-rate (US) | $20–60/mo | 16 open-weight (GLM/Kimi/Qwen/DS) | ~125–1250 req/5h | CC-native | ⭐5 | 💎🔒 |
| [Chutes](#chutes) | flat-rate ⚠️ | $3/$10/$20 | GLM-5/Kimi/DS/MiniMax/Qwen | 300/2000/5000 req/day | OpenAI-compat | ⭐5 | 💎⚠️ decentralized ✅ |
| [Grok Code Fast 1](#xai-grok) | pay-go API | $0.20/$1.50/M | grok-code-fast-1 | 256K ctx, ~92 tok/s | CC-native | ⭐5 | 💎 #1 on OpenRouter |
| [ChatGPT Plus](#openai-chatgpt--codex) | first-party | $20/mo | GPT-5.x-Codex | token-credit metered | Codex-native | ⭐4 | Codex #2 agent |
| [ChatGPT Pro](#openai-chatgpt--codex) | first-party | $100/$200 (5x/20x) | GPT-5.5-Codex | high; dedicated GPU | Codex-native | ⭐4 | |
| [Claude Max 20x](#anthropic-claude) | first-party | $200/mo | Opus 4.6/4.7 | ~200–900 prompts/5h | CC-native | ⭐4 | power tier |
| [Cursor Pro / Ultra](#cursor) | bundled | $20 / $200 | all frontier + Auto | $20 / $400 usage pool | Native-only | ⭐4 | Ultra = 2× credit ratio |
| [GitHub Copilot Pro](#github-copilot) | bundled | $10/mo | GPT-5/Claude/Gemini | $10 AI-credits (usage) | Native-only (+ACP) | ⭐4 | free completions 🆓 |
| [DeepInfra](#deepinfra) | speed/API | pay-go (cheapest OSS) | Kimi/DS/Qwen3-Coder/GLM | balance-bound | CC-native | ⭐5 | 💎✅ cheapest host |
| [Groq](#groq) | speed/API | pay-go + free | GPT-OSS/Qwen3/Kimi | free RPM/TPM caps | CC-native | ⭐4 | 💎🆓 |
| [Vercel AI Gateway](#vercel-ai-gateway) | router | $0 markup (even BYOK) | 100s incl. Claude | $5/mo free credits | CC-native | ⭐4 | 💎🆓✅ |
| [Requesty](#requesty) | router | +5% flat | Claude/GPT/Gemini/DS/Qwen | semantic cache ~40% off | OpenAI-compat | ⭐4 | 💎 team governance |
| [Mistral Le Chat Pro](#mistral) | first-party | $14.99/mo ($5.99 student) | Devstral 2 + Vibe CLI | ~25 free msg/day | Native-only | ⭐4 | 💎🆓🇪🇺 cheapest major sub |
| [Augment Code](#bundled-tool-subscriptions-editor--model) | bundled | $20–200/mo | Claude/Gemini/GPT | 40k–450k credits/mo | Native-only | ⭐4 | ✅ best big-repo context |
| [Zed Pro](#bundled-tool-subscriptions-editor--model) | bundled | $10/mo | any (BYO key/ACP) | $5 credits + usage | ACP + BYOK | ⭐4 | 💎 anti-lock-in |
| [Cerebras free](#free-tiers-) | free | $0 | Qwen3-Coder-480B, GPT-OSS-120B | 1M tok/day, 8K ctx cap | OpenAI-compat | ⭐5 | 💎🆓 fastest free |
| [Google AI Studio](#free-tiers-) | free | $0 | Gemini 2.5 Flash, Gemma 3 27B | Flash 250 RPD; Gemma 14.4k RPD | OpenAI-compat | ⭐4 | 🆓 biggest free ctx |

---

## First-party frontier subscriptions

The direct-from-vendor plans. A subscription authenticates the **vendor's own harness** (Claude Code, Codex CLI, Antigravity, Grok Build) via login — it does **not** give you a generic API key for third-party OpenAI-compat tools (that's separate per-token billing). Exception: xAI Grok models are OpenAI/Anthropic-compatible.

> Value pecking order for agentic coding (June 2026 consensus): **Claude > OpenAI Codex > Google Gemini > xAI Grok**. An independent 30-day test put Claude ~95% vs ChatGPT ~85% coding accuracy; vendor SWE-bench has GPT-5.5 (88.7%) ≈ Opus 4.7 (87.6%).

### Anthropic (Claude)
- **[Claude Pro](https://claude.com/pricing)** — `$20/mo` ($17 annual). Sonnet 4.6 in Claude Code (**no Opus**). ~40–45 msg/5h + weekly cap, shared with chat/Cowork. **Best value entry point to the #1 coding agent.** April 2026 doubled the 5h limits & removed peak throttling. ⭐5
- **[Claude Max 5x](https://support.claude.com/en/articles/11049741-what-is-the-max-plan)** — `$100/mo`. **Unlocks Opus 4.6/4.7** + 5× throughput (~50–225 prompts/5h). The pro sweet-spot; a $100 middle tier OpenAI/Google don't match as usefully. ⭐5
- **[Claude Max 20x](https://support.claude.com/en/articles/11049741-what-is-the-max-plan)** — `$200/mo`. ~200–900 prompts/5h. For all-day parallel agents; the **flat-rate-beats-API** math is decisive (90%+ of Claude Code tokens are cache-reads, free on subscription, billed on API — one dev's peak month = $5,623 at API ≈ 4.5 years of Max 5x). ⭐4
- **[Claude Team Premium seat](https://claude.com/pricing)** 💎 — `$100/seat` (annual). ≈ Max-5x usage **plus** SSO/admin/audit/enterprise-search. Quietly the best *team* coding value; Standard $20 seat also includes Claude Code. ⭐4

### OpenAI (ChatGPT / Codex)
- **[ChatGPT Plus](https://help.openai.com/en/articles/11369540-using-codex-with-your-chatgpt-plan)** — `$20/mo`. Codex CLI/IDE bundled (GPT-5.5/5.4/5.3-Codex). **Token-credit metered** since April 2026 (confusing). Codex = consensus #2 agent. Plus caps run out fast on heavy agentic work. ⭐4
- **[ChatGPT Pro](https://developers.openai.com/codex/pricing)** — `$100` (5x) / `$200` (20x). High throughput + dedicated GPU. Note the $100-tier "10x boost" promo **expired May 31 2026** (now 5x). The classic "$200 plan worth it?" debate = Claude Max 20x vs ChatGPT Pro 20x. ⭐4

### Google (Gemini)
- **[Gemini AI Pro / Ultra](https://gemini.google/subscriptions/)** — Ultra's bundled GCP credits ($40 at $100 / $100 at $200) materially offset cost if you use Google Cloud 💎. ⚠️ **Google is killing the open-source Gemini CLI June 18 2026**, forcing migration to the closed Antigravity CLI with far lower free quotas (~1000 → ~20 req/day) — the biggest community grievance of 2026.

### xAI (Grok)
- **[SuperGrok](https://x.ai/news/grok-code-fast-1)** — `$10` (Lite) / `$30` / `$300` (Heavy). Grok Build CLI runs **8 parallel sub-agents in isolated git worktrees** (novel). `grok-code-fast-1` has a cult following (cheap+fast) and was free in many partner IDEs. SWE-bench ~70.8% trails leaders. **For coding, buy the [xAI API](#xai-grok), not the SuperGrok app sub.** ⭐3 💎

---

## Bundled tool subscriptions (editor + model)

Here the plan *is* the product — you buy into the vendor's editor/agent. The 2026 trend: nearly all moved from fixed request counts to **credits / token-metering**, making costs *less* predictable (loud backlash).

### Cursor
- **[Cursor](https://cursor.com/pricing)** — Hobby free · **Pro `$20`** · **Pro+ `$60`** 💎 · **Ultra `$200`**. Since June 2025, your plan price = a usage pool at API rates. **Credit ratio improves up-tier**: Pro $20/$20 (1×), Pro+ $60/$70 (1.17×), Ultra $200/$400 (**2×, best**). `Auto` mode is the value key — effectively unlimited, doesn't drain the pool like pinning Claude/MAX does. ⚠️ The June-2025 switch caused a [pricing disaster](https://www.wearefounders.uk/cursors-pricing-disaster-the-full-timeline-of-how-an-ai-coding-darling-burned-its-most-loyal-users/) (HN user: "$350 overage in a week"); CEO apologized + refunded. **Native-only** — can't back Claude Code, and as of Jan 2026 you can't route a Claude sub *into* Cursor either. Best-in-class Tab/Apply. ⭐4

### GitHub Copilot
- **[GitHub Copilot](https://github.com/features/copilot/plans)** — Free 🆓 · **Pro `$10`** · Pro+ `$39` · Max `$100` · Business `$19` · Enterprise `$39`. ⚠️ **Moved to usage-based AI Credits June 1 2026** (1 credit = $0.01); each plan includes a credit pool (Pro=$15, Pro+=$70). **Code completions stay unlimited & free** — completion-only users unaffected. Backlash severe (TechTimes: agentic bills jumped 10×–50×). Best-in-class IDE completions + governance/IP-indemnity for orgs. **Native-only** (escape hatch: Copilot CLI speaks ACP). ⭐4

### Others
- **[Augment Code](https://www.augmentcode.com/pricing)** ✅ — Indie `$20`/40k credits · Standard `$60` · Max `$200`. **Best-in-class Context Engine** for large monorepos (tops context-recall comparisons). VS Code + JetBrains + Auggie CLI. Native-only. Credit burn on tool-heavy tasks is the gripe. ⭐4 💎
- **[Zed Pro](https://zed.dev/pricing)** 💎 — Free · **Pro `$10`** (only +10% markup) · Business `$30`. The **anti-lock-in** pick: open [ACP](https://zed.dev/docs/ai/) drives external agents (Claude Code, Codex, OpenCode) and BYO keys for any provider. Fastest native editor. ⭐4
- **[Kiro](https://kiro.dev/pricing/)** 💎 — Free · **Pro `$20`/1k credits** · Pro+ `$40` · Power `$200`. Best **spec-driven** agent (requirements→design→tasks), full Claude lineup incl. Opus 4.7, fractional 0.01-credit billing. **AWS Startups = 1 free year of Pro+.** ⭐4
- **[Trae](https://www.trae.ai/pricing)** 💎🇨🇳 — Free · **Lite `$3`** · Pro `$10` · Ultra `$100`. ByteDance VS Code fork; usage pool exceeds sticker (e.g. $20 usage for $10) = "the $3 Cursor alternative." ⚠️ ByteDance telemetry shared with affiliates — enterprise dealbreaker. ⭐4
- **[Sourcegraph Amp](https://sourcegraph.com/amp)** — Free to start ($10 credit; $40 for ex-Cody). Pure **consumption** (no monthly floor), runs Opus 4.8 in "smart" mode. Great for light use, uncapped-burn risk for heavy. Cody Free/Pro were retired into Amp. ⭐3
- **[JetBrains AI / Junie](https://www.jetbrains.com/ai-ides/buy/)** — beloved IDE integration, but Junie **burns credits fast** (Ultimate's 35 credits gone in ~4–5 days). Only if you live in JetBrains.
- **Overpriced / avoid:** **Tabnine** ($39 floor, no free tier, annual lock-in — only for on-prem/air-gap needs); **Windsurf Pro** (March 2026 swap to daily/weekly quotas is the year's most-complained-about change, post-Cognition trust low). **Supermaven** is dead as a standalone (folded into Cursor Tab Nov 2025).

---

## Flat-rate coding plans — the value champions 💎

The heart of this list. Fixed monthly/quarterly plans that put a frontier-ish open-weight model behind your harness, mostly from Chinese labs — **almost all expose a native Anthropic endpoint**, so they're true Claude Code drop-ins via `ANTHROPIC_BASE_URL`. Canonical endpoint reference: [Alorse/cc-compatible-models](https://github.com/Alorse/cc-compatible-models).

> Consensus pecking order: **GLM** (cheapest entry, community default) · **MiniMax** (best price/volume) · **Kimi** (best long-horizon agent) · **Qwen** (>262K context, multi-model). Claude Pro $20 is the quality benchmark they undercut.

<a name="glm-coding-plan-zai"></a>
### GLM Coding Plan — Z.ai (Zhipu AI) 💎🇨🇳 ✅
- `Lite ~$10/mo ($30/qtr)` · `Pro ~$30/mo ($90/qtr)` · `Max ~$80/mo ($240/qtr)`. Q2-2026 promo: $27/$81/$216/qtr. (The viral **$3/mo** promo ended Feb 11 2026; annual Lite ~$7/mo is the remaining cheap route.)
- Models: **GLM-5.1** (~94% of Opus 4.6 coding), GLM-5/5-Turbo, GLM-4.7, GLM-4.5-Air.
- Limits: Lite ~80, Pro ~400, Max ~1,600 prompts/5h + weekly. ⚠️ **Peak-hour 3× multiplier** (14:00–18:00 UTC+8) on GLM-5/5.1 quietly halves throughput.
- Integration: `ANTHROPIC_BASE_URL=https://api.z.ai/api/anthropic` — official Claude Code support + Cline/Roo/Kilo/OpenCode (20+ tools). **First-party** = no reseller ban risk.
- > *The single most-recommended budget coding plan of 2026.* "3× Claude Max usage for ~$30/mo." Backlash over the Feb price hike + ⅓ quota cut, still rated top value. ⭐5
- Sources: [z.ai/subscribe](https://z.ai/subscribe) · [pricing](https://docs.z.ai/guides/overview/pricing) · [GLM-5.1 review](https://serenitiesai.com/articles/glm-5-1-coding-plan-review-2026)

<a name="minimax"></a>
### MiniMax Coding / Token Plan 💎🇨🇳
- `Starter $10/mo` · `Plus $20` · `Max $50` (2 months free annual); High-Speed variants $40–150.
- Models: M2.7 / M2.7-Highspeed on the plan; **M2.5/M3** (1M ctx) via API. ⚠️ **Plan often serves an older model** (M2.1) than the benchmarked M2.5/M2.7.
- Limits: Starter ~100 → Max ~1,000 prompts/5h; ~50 TPS (100 high-speed).
- Integration: `ANTHROPIC_BASE_URL=https://api.minimax.io/anthropic` + OpenAI-compat.
- > "Cut my Claude Code bill in half." **Best raw price/volume** in the flat-rate bucket; M2.7 ~94% of GLM-5.1 at ~1/5 the input cost. ⭐5
- Sources: [coding plan](https://platform.minimax.io/subscribe/coding-plan) · [M2.5 pricing](https://www.verdent.ai/guides/minimax-m2-5-pricing)

<a name="kimi-moonshot"></a>
### Kimi Code — Moonshot AI 💎🇨🇳
- `~$19/mo membership` + metered API (K2.6 $0.60–0.95/M in, $2.50–4.00/M out, 75% cache discount). Tiered Moderato/Allegretto/Vivace.
- Models: **Kimi K2.6** (1T MoE, ~80.2% SWE-bench), K2.5.
- Limits: ~300–1,200 calls/5h, **30 concurrent** (generous for parallel agents).
- Integration: `ANTHROPIC_BASE_URL=https://api.moonshot.ai/anthropic` — true Claude Code drop-in; ships own Kimi CLI (6.4k★).
- > **Best long-horizon agent stability** (sustained 4,000+ tool calls over a 13-hour session). "Saving 88% coding costs." Priciest input-side of the open cohort. ⭐5
- Sources: [agent support](https://platform.kimi.ai/docs/guide/agent-support) · [Kimi Code guide](https://www.nxcode.io/resources/news/kimi-code-2026-plans-pricing-developer-guide)

<a name="qwen-alibaba"></a>
### Qwen Cloud Coding Plan — Alibaba 💎🇨🇳 ✅
- `Pro $50/mo` (Lite ~$10 **closed to new subs** since Mar 20 2026).
- Models: Qwen3.5-Plus, Qwen3-Coder-Next/Plus/480B + cross-model **Kimi/GLM/MiniMax** under one key. **1M-token context** (best in lane).
- Limits: Pro 6,000 req/5h + 45k/wk + 90k/mo (sliding window). Dedicated `sk-sp-` key (not interchangeable with pay-go).
- Integration: `ANTHROPIC_BASE_URL=https://coding-intl.dashscope.aliyuncs.com/apps/anthropic` + Qwen Code CLI.
- > Standout = **one plan multiplexes Qwen+Kimi+GLM+MiniMax** and the only credible 1M-context flat plan. ⭐4
- Sources: [Model Studio coding plan](https://www.alibabacloud.com/help/en/model-studio/coding-plan)

### Open-weight flat subs (privacy / US-host)
- **[Synthetic.new](https://synthetic.new/pricing)** 💎🔒 — `$20–60/mo`. ~16 always-on open-weight models (Kimi/GLM/Qwen3-Coder-480B/DeepSeek). **US infra, no-training, 14-day deletion.** **Dual OpenAI + Anthropic compat** = genuine Claude Code drop-in. The privacy-conscious alternative to China plans. ⭐5
- **[Cerebras Code](#cerebras)** — `$50`/`$200`, flat-rate speed (see [Speed](#speed--fast-inference-providers)).
- **[OpenCode Go (Zen)](https://opencode.ai/go)** 💎 — `$5` first month then `$10/mo` flat. ~12–14 Chinese open-weight models (GLM-5.1/Kimi/Qwen3.7/DeepSeek V4/MiniMax). First-class in OpenCode. No Claude/GPT. ⭐4

### Niche / cheap-tier flat plans 🇨🇳
- **[StepFun Step Plan](https://github.com/Alorse/cc-compatible-models)** — `$6.99`–`$99/mo`, 100–5,000 prompts/5h, CC-native. Price undercutter, models less battle-tested. ⭐3
- **MiMo (Xiaomi)** — `$6`–`$100/mo` credit-based (60M–1.6B), CC-native (`api.xiaomimimo.com`), incl. multimodal Omni. Barely benchmarked. ⭐3
- **Atlas Cloud** 💎 — `$10`/`$20`, 800k–1.8M credits/**day**, OpenAI-compat (Claude Code/Codex/OpenCode). Daily-credit model for autonomous agents. ⭐4
- **Factory Droid** 💎 — from `$20/mo` token-based, frontier models (Claude/GPT/Gemini), rolling 5h/7d/30d windows. Notable "I canceled two $200 Max plans for Droid" story. ⭐4

---

## Pay-as-you-go value APIs

Per-token access from the value labs. **Cache pricing is the real cost driver** for agent loops — design for cache hits over headline input price.

<a name="deepseek"></a>
### DeepSeek 💎🇨🇳 ✅
- **V4-Pro** `$0.435/M in · $0.0036/M cache-hit · $0.87/M out` (the **75% cut is now permanent**). **V4-Flash** `$0.14 / $0.0028 / $0.28`. 1M context, 384K max output.
- Integration: OpenAI-compat **+ native Anthropic** (`https://api.deepseek.com/anthropic`) — drop-in Claude Code (`ANTHROPIC_MODEL=deepseek-v4-pro[1m]`).
- > **The cost-per-token champion.** V4-Pro ~80.6% SWE-bench / 93.5% LiveCodeBench at <$1/M out. V4-Flash's $0.0028/M cache-hit is unbeatable for bulk loops. ⭐5
- Sources: [pricing](https://api-docs.deepseek.com/quick_start/pricing) · [Claude Code setup](https://api-docs.deepseek.com/quick_start/agent_integrations/claude_code)

### Others
- **[Alibaba Qwen3-Coder API](https://www.alibabacloud.com/help/en/model-studio/model-pricing)** 🇨🇳 — 480B `$0.22/$1.00`, Flash `$0.195/$0.975`, 30B-A3B `$0.07/$0.27`. **1M free tokens / 90 days** (Intl). CC-native. Strongest open-weight agentic coder. Use Singapore-region keys. ⭐4
- **[Moonshot Kimi API](https://platform.kimi.ai/docs/pricing)** 🇨🇳 — K2.6 `$0.95/$4.00` ($0.16 cached), K2.5 `$0.60/$3.00`. CC-native. Excellent tool-calling; output price is the grumble. $10 deposit removes daily cap. ⭐4
- **[Zhipu GLM API](https://docs.z.ai/guides/overview/pricing)** 🇨🇳 — GLM-5.1 `$1.40/$4.40`, GLM-4.7 `$0.60/$2.20`, FlashX `$0.07/$0.40`. CC-native. Most enthusiasts buy the cheaper [Coding Plan](#glm-coding-plan-zai) instead. ⭐4
- **[MiniMax API](https://platform.minimax.io/docs/guides/pricing-paygo)** 🇨🇳 ✅ — M3 `$0.30/$1.20` ($0.06 cache, **free cache writes**), M2.5 ~`$0.15/$1.15`. "20× cheaper than Opus." First-party Anthropic compat. ⭐4

---

## Speed / fast-inference providers

Per-token hosts of open-weight models, optimized for throughput. **Groq is the only one with a native Anthropic endpoint** (cleanest Claude Code drop-in); the rest are OpenAI-compat (need a shim/router for CC, native in Cline/Roo/OpenCode).

<a name="deepinfra"></a>
- **[DeepInfra](https://deepinfra.com/pricing)** 💎 ✅ — **the cheapest-per-token champion.** DeepSeek V3.2 ~$0.26/$0.38, Kimi K2.6 $0.75/$3.50, Qwen3-Coder-480B $0.30/$1.00. 90+ models, cached discounts, **native Anthropic endpoint**, no upfront cost. Speed good-not-elite. ⭐5
<a name="groq"></a>
- **[Groq](https://groq.com/pricing)** 💎🆓 — LPU speed (GPT-OSS-20B ~860 tok/s). GPT-OSS-120B `$0.15/$0.60`, Kimi K2 `$1.00/$3.00`. **Native Anthropic + OpenAI compat** + real free tier. Batch+cache stack to ~25%. No Qwen3-Coder-480B (ceiling is Qwen3-32B). ⭐4
<a name="cerebras"></a>
- **[Cerebras](https://www.cerebras.ai/pricing)** ✅ — **fastest** (~2,000–3,000 tok/s). **Code Pro `$50`** (24M tok/day) / **Max `$200`** (120M tok/day), GLM-4.7, 131k ctx. Pay-go GPT-OSS-120B `$0.35/$0.75`. ⚠️ Frequently **sold out**; 131k ctx (half native) + high TTFT blunt the speed in agent loops. ⭐5 flat-rate / ⭐4 pay-go
- **[Together AI](https://www.together.ai/pricing)** — broadest catalog (Qwen3-Coder-480B, Kimi, DeepSeek V4 Pro $2.10/$4.40 w/ $0.20 cached). Mid-pack price, ~89 tok/s. ⭐4
- **[Fireworks AI](https://fireworks.ai/pricing)** — production/enterprise lean, aggressive cache ($0.15/M), DeepSeek V4-Flash $0.14/$0.28, Azure Foundry path. ⭐4
- **[Novita](https://novita.ai/pricing)** 💎 — hosts the full Qwen3-Coder family at near-DeepInfra prices; under-the-radar OpenRouter route. ⭐4
- **[Hyperbolic](https://docs.hyperbolic.xyz/docs/hyperbolic-ai-inference-pricing)** 💎 — GPT-OSS-20B `$0.10/M` blended (among cheapest anywhere); hosts Qwen3-Coder-480B (FP8). ~13 models. ⭐3
- **SambaNova** — uniquely fast on giant 671B/405B models; forever-free + $5 credit 🆓 but 50 req/day cap = eval-only.

---

## Routers & gateways

One key across many providers. Pick a router as your **default access layer**.

<a name="openrouter"></a>
- **[OpenRouter](https://openrouter.ai/pricing)** 🆓 — **the consensus default.** 315+ models, one key, **Anthropic-compat "skin"** (`ANTHROPIC_BASE_URL=https://openrouter.ai/api` = true Claude Code drop-in), **no token-price markup** (only +5.5% on top-ups), free ZDR + spend caps, generous BYOK (1M free req/mo). Free models (Qwen3-Coder-480B, DeepSeek, Llama 4): 50 RPD → **1000 RPD forever after a one-time $10 deposit**. The 5.5% fee stings only above ~$5k/mo spend. ⭐5
<a name="requesty"></a>
- **[Requesty](https://www.requesty.ai/)** 💎 — **flat 5% markup**, all features incl. **semantic caching** (~40% savings, beats identical-only caches) + smart per-request routing + **per-agent model policies** (different model per classifier/synthesizer role) + SOC 2 Type II. The team-governance pick. OpenAI-compat. ⭐4
<a name="vercel-ai-gateway"></a>
- **[Vercel AI Gateway](https://vercel.com/docs/ai-gateway/pricing)** 💎🆓 ✅ — **zero markup, even on BYOK.** Native Anthropic-compat (`https://ai-gateway.vercel.sh`) = direct Claude Code + Claude Agent SDK + "Claude Code Max via Gateway". $5/mo free credits refresh indefinitely (stops once you top up). Best pure-economics pick, esp. in the Vercel ecosystem. ⭐4
- **[Helicone Gateway](https://helicone.ai/pricing)** 🆓 — observability-first (auto logging/tracing/cost), zero markup, free 10k req/mo; subs $79/$799. ⭐3
- **[CometAPI](https://www.cometapi.com/)** — 500+ models incl. latest proprietary, ~20–40% off official, **dual OpenAI+Anthropic compat**. Prepaid-credit middleman risk. ⭐4
- **[ElectronHub](https://www.electronhub.ai/pricing)** — 600+ models, weekly credits can exceed cash cost; tight 5–10 RPM on cheap tiers, reseller-trust caveat. ⭐3
- **[LiteLLM](https://docs.litellm.ai/)** — the OSS **self-host** standard (free, no markup) — see [integration tricks](#plugging-cheap-plans-into-your-harness). DIY infra, not turnkey. ⭐4

---

## Free tiers 🆓

Genuinely usable $0 access. **Consensus ranking** for real agent loops (June 2026):

1. **[Cerebras free](https://inference-docs.cerebras.ai/support/rate-limits)** 💎 — **1M tokens/day, no card, fastest** (2000+ tok/s), Qwen3-Coder-480B + GPT-OSS-120B. ⚠️ **8K context cap** kills whole-repo work. ⭐5
2. **[Google AI Studio](https://ai.google.dev/gemini-api/docs/rate-limits)** — **biggest free context** (Flash up to 1M) + Gemma 3 27B at **14,400 RPD**. ⚠️ Gemini 2.5 Pro no longer free (~April 2026); limits slashed Dec 2025; free data used for training. ⭐4
3. **[OpenRouter :free](https://openrouter.ai/models?max_price=0)** — best free coding model (Qwen3-Coder-480B) + DeepSeek/Llama/GLM, one key. **Spend the one-time $10 → 1000 RPD forever** (50 RPD otherwise). ⭐4
4. **[Groq free](https://console.groq.com/docs/rate-limits)** 💎 — fastest small-prompt loops; ⚠️ 6,000 TPM cap = many small steps, not big context. ⭐4
5. **[NVIDIA NIM](https://build.nvidia.com/)** 💎 — 1,000–5,000 credits, **no card/no expiry**, 40 RPM, frontier open models (MiniMax M2.x, Qwen3-Coder-480B, GLM-5, Kimi K2.5). Eval tier (credit-capped). ⭐4
6. **Mistral Experiment** — 1B tokens/month (!), ~1 req/sec + training opt-in.
- **Prototyping-only:** GitHub Models (50 RPD), Cloudflare Workers AI, Together ($1 default).
- **Durable free strategy:** route 60–80% of agent traffic to free Qwen3-Coder/GPT-OSS/DeepSeek (Cerebras + OpenRouter+$10 + NVIDIA NIM); escalate the hard 20% to a paid frontier model. ⚠️ Free quotas tightened hard in 2025–2026 — assume any can shrink without notice.

---

## Niche & specialty

- **[xAI Grok Code Fast 1 (API)](https://x.ai/news/grok-code-fast-1)** 💎 — `$0.20/$1.50/M` ($0.02 cached), 256K ctx, **OpenAI + Anthropic compat**. **#1 by usage on OpenRouter** — the textbook "good-enough + fast + cheap" implementer. $25 free signup credits; up to $175/mo via data-sharing. ⚠️ Over-edits without tight scope; escalate hard reasoning. ⭐5
- **[Mistral Le Chat Pro / Vibe](https://mistral.ai/pricing/)** 💎🆓🇪🇺 — `$14.99/mo` (**$5.99 student**). **Cheapest major coding sub**, includes the Vibe CLI terminal agent (Devstral 2). Free tier has real (limited) coding. ⭐4
- **[Mistral Codestral / Devstral 2 (API)](https://mistral.ai/news/codestral-2501/)** 🇪🇺 — Codestral `$0.30/$0.90` (32K) with a **free FIM endpoint** (Continue.dev's go-to autocomplete); Devstral 2 `$0.40/$2.00`, Devstral Small **free**. EU sovereignty. ⭐4
- **[Inception Mercury](https://www.inceptionlabs.ai/)** 💎 — diffusion dLLM, `$0.25/$0.75–1/M`, 128K, **5–10× faster** than Haiku/GPT-4o-mini, #1 speed on Copilot Arena small-model tier. Latency-sensitive autocomplete buy, not a frontier reasoner. ⭐4
- **[Morph Fast Apply](https://www.morphllm.com/pricing)** 💎 — the **"apply" layer**: ~10,500 tok/s, ~98% merge accuracy, cuts token cost 50–60% / latency 90%+. Free 200 req/mo, $20 starter. **MCP tool works in Claude Code & Cursor.** ⚠️ openly transitional category ("Fast Apply Models are Already Dead"). ⭐4
- **[Relace](https://relace.ai/pricing)** 💎 — Morph peer with **256K apply context** + bundled Search/Rank/Embed retrieval stack. Builder/infra buy. ⭐4
- **Cohere Command A** — `$2.50/$10` — the lane's *weakest* coding value (enterprise RAG/multilingual play, not an agentic-coding pick).

---

## Hidden gems & reseller proxies ⚠️

> **Squeezing frontier-ish coding out of <$10–30/mo.** Genuine bargains exist, but the reseller-proxy corner is risky and rising.

**Genuine bargains the community recommends:** [Chutes](https://chutes.ai/pricing) ($3/$10 for huge open-weight variety, decentralized) ✅ · [OpenCode Go](#niche--cheap-tier-flat-plans-) ($10 flat) · [Synthetic](#open-weight-flat-subs-privacy--us-host) ($20–30, reliable+private+CC-native) · [Z.ai GLM](#glm-coding-plan-zai) (first-party). Best neutral diaries: [patshead.com](https://blog.patshead.com/2026/01/squeezing-value-from-free-and-low-cost-ai-coding-subscriptions.html) + InfoWorld's "vibe code for free."

- **[Chutes](https://chutes.ai/pricing)** 💎⚠️ ✅ — Base `$3` (300 req/day) · Plus `$10` (2,000/day) · Pro `$20` (5,000/day). GLM-5/Kimi/DeepSeek/MiniMax/Qwen, OpenAI-compat, TEE privacy. ⚠️ **Decentralized (Bittensor)** = variable latency/quality between nodes, no SLA, quantization drift, frontier models gated to $10+. Treat as hobby/non-critical, keep a fallback. ⭐5
- **[NanoGPT](https://nano-gpt.com/pricing)** 💎 — true **pay-per-prompt** ($0.10 min, crypto-friendly), proprietary + open models. ⚠️ tool-call failures reported in coding agents (OpenCode). Better as chat/API than a hardcore coding backend. ⭐3
- **[AgentRouter](https://agentrouter.org)** ⚠️ — ~$200 free credits, routes Claude/GPT-5/DeepSeek/Zhipu, works as a Claude Code backend. A real free-credit **on-ramp**, but a non-profit with opaque long-term policy. Trials only, not proprietary code. ⭐3

### ⚠️ Reseller-proxy risk (read before depositing)
Relays like **PackyCode, YesCode, AnyRouter, EasyClaude, IKunCode, Cubence** reverse-proxy official Claude Max/Pro accounts (**ToS violation**) or aggregate keys. Hard data: Anthropic's 2025–2026 crackdown forced simultaneous price hikes across these, and **>60% of 2025 reverse-engineering relays died within 3 months**. AnyRouter is Scamadviser-flagged. The **universal community rule: only deposit what you need, never large sums** — balances evaporate when a relay dies, and Anthropic also bans the underlying-account users. Aggregator-routers (CometAPI, ElectronHub) are the safer middle (legitimately metered) but you still trust a middleman with your prompts.

---

## Plugging cheap plans into your harness

The harness (Claude Code, Cline, Aider, OpenCode) is **free** — you only pay for the plan behind it. How to wire a cheap plan into a premium harness:

**1. Two-env-var trick (no proxy)** 💎 — simplest cost cut. Any provider with a native Anthropic endpoint:
```bash
export ANTHROPIC_BASE_URL=https://api.deepseek.com/anthropic   # or api.z.ai/api/anthropic, api.moonshot.ai/anthropic, api.minimax.io/anthropic
export ANTHROPIC_AUTH_TOKEN=<provider-key>
export ANTHROPIC_DEFAULT_SONNET_MODEL=deepseek-v4-pro[1m]      # map sonnet/opus/haiku to provider models
claude
```
*Single backend only — no per-task routing.*

**2. [claude-code-router (CCR)](https://github.com/musistudio/claude-code-router)** ⭐5 — the canonical way to **mix subscriptions per task**. Runs a local proxy on `:3456`; route keys `default / background / think / longContext / webSearch` to different models — cheap/local for edits, frontier for planning, big-context for long files. Fallback chains (GLM → free OpenRouter → local). All Claude Code features keep working.

**3. [LiteLLM proxy](https://docs.litellm.ai/docs/tutorials/claude_non_anthropic_models)** — the **team** choice. Single stable Anthropic `/v1/messages` passthrough endpoint, per-key budgets, spend tracking, audit logs, load-balancing + fallback across 100+ providers. Switching Opus→DeepSeek cuts output cost ~95%. Heavier to stand up than CCR.

**4. [copilot-api bridge](https://github.com/ericc-ch/copilot-api)** ⚠️ — reuse a GitHub Copilot sub (esp. free edu/OSS) as a Claude Code backend. **Reverse-engineered → likely ToS violation / ban risk.** Use at your own risk.

**5. Native Anthropic levers (no provider switch)** 💎 — **prompt caching** gives up to 90% input savings (cache reads = 0.1× input), and the **Batch API** stacks another 50% off for async bulk jobs. Often overlooked while chasing third-party models. ⚠️ Default cache TTL regressed 1h→5m in March 2026.

> **Integration takeaway:** for Claude Code you want an **Anthropic-compatible** endpoint (GLM, Kimi, MiniMax, Qwen, DeepSeek, Groq, Synthetic, CometAPI, Vercel all offer one). OpenAI-compat-only services (Chutes, ElectronHub, Cerebras, GitHub Models) plug cleanly into **OpenCode/Cline/Roo** and need a shim for Claude Code. OpenCode is the favored harness in the budget lane for its easy multi-provider env-var routing.

---

## Benchmark-per-dollar

SWE-bench Verified (mostly vendor-reported; treat as directional — contamination concerns exist, SWE-bench Pro is the cleaner successor):

| Tier | Model | SWE-bench Verified | ~Cost behind it |
|------|-------|--------------------|-----------------|
| Frontier | Claude Opus 4.8 | **88.6%** | Max $100–200/mo |
| Frontier | GPT-5.3-Codex | 85% | ChatGPT Pro $100–200 |
| Frontier | GPT-5.2 | 80% | — |
| **Value 💎** | **DeepSeek V4-Pro** | **80.6%** (LiveCodeBench 93.5%) | $0.435/$0.87 per M |
| **Value 💎** | **MiniMax M2.5** | 80.2% | $0.15/$1.15 or $10/mo |
| **Value 💎** | **Kimi K2.6** | 80.2% | $0.95/$4.00 or $19/mo |
| Frontier | Claude Sonnet 4.6 | 79.6% | Pro $20 |
| **Value 💎** | **GLM-5.1** | 77.8% | $10–30/mo plan |
| Speed/cheap | Grok Code Fast 1 | 70.8% | $0.20/$1.50 per M |

> **The value lane exists to approximate Claude Code at 7–15% of its price.** Pay $10–30/mo for a flat plan that hits ~78–80%, reserve $100–200 frontier subs for the top 5–10 benchmark points you genuinely need.

---

## What the community actually says

Aggregated from r/LocalLLaMA, r/ChatGPTCoding, r/ClaudeAI, r/cursor, r/Anthropic, Hacker News, and neutral blogs (patshead, InfoWorld, serenitiesai, vibecoding, verdent, every.to).

- **#1 hidden gem & value pick:** **GLM Coding Plan** is the runaway favorite for "cheapest way to run Claude Code." "GLM-4.6 is ~80% as good as Claude Code for ~1/3 the price" gets quoted constantly.
- **The flat-rate-beats-API math:** for Claude itself, subscriptions win at scale because 90%+ of Claude Code tokens are cache-reads (free on sub, billed on API). The viral example: a $5,623 API month = 4.5 years of Max 5x.
- **The billing-nerf backlash:** Cursor (June 2025), GitHub Copilot (June 1 2026), Windsurf — all moved from request caps to usage credits. The loudest recurring complaint; Copilot's agentic bills jumped 10×–50× for power users.
- **The cost-stacking meta:** keep a frontier sub for hard work + a cheap open-weight plan for overflow. Most-repeated stack: **Claude Pro $20 + GLM Lite $10**.
- **"I canceled my $200 sub for X":** Factory's Droid is the notable concrete replacement story.
- **Contrarian / scam-watch:** Cerebras Code took heat for "2000 TPS / no weekly limits" marketing vs hidden daily token caps; avoid sketchy reseller-proxy Claude/GPT keys; China-hosted plans flagged for data-privacy; watch GLM's quarterly-billing surprise. OpenRouter is the "one key for everything" default, but flat-rate plans beat it for heavy daily coders.

---

## Caveats & disclaimer

- **Pricing volatility:** every number here can change within weeks. GLM doubled prices Feb 2026; Qwen Lite closed to new subs Mar 2026; Cerebras is perpetually sold out; Gemini 2.5 Pro stopped being free April 2026; models EOL constantly. **Confirm on the official page before buying.**
- **Vendor benchmarks:** SWE-bench numbers are largely self-reported and contamination-prone. Treat as directional.
- **Same model ≠ same quality:** an open-weight model performs differently across hosts (quantization + serving config). Test with short commitments; hedge across 2–3 plans.
- **China-hosting:** GLM/Kimi/DeepSeek/MiniMax/Qwen are China-hosted — a data-residency consideration for sensitive/enterprise code. US-host alternatives: Synthetic.new, first-party US subs.
- **ToS:** routing a consumer Claude/Copilot subscription into third-party tools, or using reseller relays, can violate provider ToS and risk an account ban. This list documents what exists; it doesn't endorse ToS violations.
- Not affiliated with or endorsed by any listed vendor. No referral links.

---

## Contributing

Corrections and additions welcome — pricing changes monthly, so fixes are as valuable as new entries. See [CONTRIBUTING.md](CONTRIBUTING.md). Keep entries in the right section, sorted by value, with a **source link** and concrete numbers.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](LICENSE)

To the extent possible under law, the contributors have waived all copyright and related rights to this work ([CC0 1.0](LICENSE)).
