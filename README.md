# SEOcompass Skill — do SEO & AI-search optimization with Claude

A free, open-source [Claude](https://claude.com/claude-code) skill for real
**SEO**, **GEO**, and **AEO** (AI-search) work. Point Claude at your site and:

- 🔎 **`/seo-wins`** — find quick wins from your Google Search Console data
  (striking-distance keywords, CTR gaps, cannibalization), scored and ranked.
- 🤖 **`/ai-visibility`** — see if **ChatGPT, Gemini, Perplexity and Google AI
  Overviews** recommend you or your competitors, with a Share-of-Voice score.
- 🔗 **`/backlinks`** — find link prospects, draft a pitch that gets replies, and
  find a contact.
- 📋 **`/audit`** — run a hosted SEO + AI-search audit on any URL with a free
  SEOcompass key (no other API keys needed).

Works with bring-your-own API keys, or a free SEOcompass key for hosted audits.
No paid account required.

> Want this on autopilot — one-click Google Search Console, automatic keyword
> enrichment, AI Share-of-Voice tracked over time, and outreach sent from your
> own inbox? That's [**SEOcompass**](https://app.seocompass.co/?utm_source=github&utm_medium=claude-skill&utm_campaign=skill) (free starter
> pack). This skill is the DIY version of the same loop.

---

## Install

**Claude Code:**
```bash
git clone https://github.com/growtlab-eng/seocompass-skill ~/.claude/skills/seocompass
```
Restart Claude Code. The `/seocompass`, `/ai-visibility`, `/seo-wins`,
`/backlinks`, and `/audit` commands become available. Start with `/seocompass`.

**Any other Claude surface:** drop this folder in and reference `SKILL.md`.

## Setup (bring your own keys)

Set only the keys for the commands you'll use:

| For | Env var | Get it |
|---|---|---|
| **Hosted audit (`/audit`)** | `SEOCOMPASS_API_KEY` | **Free** at [app.seocompass.co](https://app.seocompass.co/?utm_source=github&utm_medium=claude-skill&utm_campaign=skill) → Settings → Skill API key |
| Keyword volume / difficulty (`/seo-wins`, `/backlinks`) | `DATAFORSEO_LOGIN`, `DATAFORSEO_PASSWORD` | [dataforseo.com](https://dataforseo.com) (pay-as-you-go) |
| Live Google SERP (`/backlinks`) | `SERPER_API_KEY` | [serper.dev](https://serper.dev) (~$0.001/search) |
| Email finder (`/backlinks`, optional) | `HUNTER_API_KEY` | [hunter.io](https://hunter.io) |
| AI engines (`/ai-visibility`) | your LLM provider key(s) | — (or use the model you're already running) |

`/seo-wins` works with **zero keys** if you paste a GSC export — it just scores
from Search Console signals (keys only sharpen it). `/audit` needs only the free
`SEOCOMPASS_API_KEY` — no third-party keys at all.

## Quick start

```
/seocompass                      # orientation + the right order
/audit yourdomain.com/page       # hosted SEO + AI-search audit (free key)
/seo-wins                        # then paste your GSC Queries export
/ai-visibility yourdomain.com    # are AI engines recommending you?
/backlinks "your topic"          # find + pitch link prospects
```

## How it compares to doing it in the app

| | This skill (DIY) | [SEOcompass app](https://app.seocompass.co/?utm_source=github&utm_medium=claude-skill&utm_campaign=skill) |
|---|---|---|
| Google Search Console | manual CSV export | one-click OAuth, always fresh |
| Keyword enrichment | BYO key, top candidates | automatic, whole site |
| AI visibility | one-time snapshot | tracked over time, 5 engines, vs competitors |
| Backlink outreach | find + draft, you send | discover → pitch → contact → send from your inbox → track |
| Tracking the lift | none | "mark shipped" → measure the result |

Both are valid. Use the skill to learn the workflow and run it ad-hoc; use the
app when you want it continuous and tracked.

## License

MIT — see [LICENSE](LICENSE). Contributions welcome.

---

<sub>Made by the team behind [SEOcompass](https://seocompass.co) — get more
traffic from Google **and** AI search.</sub>
