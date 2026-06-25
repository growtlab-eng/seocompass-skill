# Quick-wins scoring method

The point of scoring (vs just listing) is to spend effort where the *expected
click gain per unit of work* is highest. Three inputs.

## 1. CTR-by-position curve

Use this as the expected organic CTR for a position (desktop+mobile blend; it's
an estimate, not gospel — directional is enough):

| Position | ~CTR | Position | ~CTR |
|---|---|---|---|
| 1 | 28% | 6 | 4.5% |
| 2 | 15% | 7 | 3.5% |
| 3 | 10% | 8 | 3.0% |
| 4 | 7% | 9 | 2.5% |
| 5 | 5.5% | 10 | 2.2% |
| 11–15 | ~1.5% | 16–20 | ~0.8% |

## 2. Traffic upside

For a query at current position `p` with monthly impressions `I`:

```
upside_clicks = I × (CTR(target_p) − CTR(p))
```

Pick a realistic `target_p` — usually 3–5 positions better, not "position 1".
A query at position 12 → realistic target 6–8, not 1.

**CTR-gap variant:** if the query's *actual* CTR is well below `CTR(p)` (e.g.
position 6 but 1.2% CTR vs expected 4.5%), the upside is closing that gap with a
better title/meta — no ranking change needed. These are the cheapest wins.

## 3. Winnability (0–1)

How reachable the target move is:

```
winnability = position_factor × difficulty_factor
position_factor   = closer to page 1 = higher (a move from 8→5 beats 45→5)
difficulty_factor = lower keyword difficulty / stronger relative authority = higher
```

If you don't have keyword difficulty (no DataForSEO key), approximate
winnability from position alone and note the lower confidence.

## 4. Opportunity score

```
score = upside_clicks × winnability × effort_factor
effort_factor = title/meta-only fix → 1.0 ; on-page content → 0.6 ; new page → 0.3
```

Rank descending. The top of the list is "biggest realistic click gain for the
least work" — that's where to start.

> The SEOcompass app uses a refined version of this (per-row SERP-shape
> inference, authority proxy from real backlink data, decay curves) and runs it
> across the whole site automatically.
