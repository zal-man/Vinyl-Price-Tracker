# Notes (Work in Progress)

These are rough research notes, repo comparisons, and open questions.
They are intentionally incomplete and may change or be removed.

## Ideas

- Track prices for specific albums (version-agnostic at first)
- Possible sources:
  - Discogs wantlist export
  - Retailers (Rough Trade, Amazon, local shops)
  - Reddit / deal feeds

## Next Questions
- What signals matter more than sources?
- How to normalize price without versioning?
- Where Popsike and/or Discogs fits vs live marketplaces
- What already exists?
- What’s easiest to build first?
- What would *I* actually use?

### Repo: HowLucky

- What it tracks:
  Discogs-based vinyl price history, supply, and trends with SQL storage and interactive visualizations.

- How it identifies records:
  Discogs release-level IDs (version-specific). Strong dependency on Discogs API, OAuth, and schema.

- Strengths:
  Thoughtful data modeling, nice exploratory visuals, clearly a serious analytics project.

- Biggest limitations:
  Overly Discogs-centric; no abstraction for artist/album-level tracking.
  Optimized for analysis, not for “alerts” or casual collectors.
  UI appears partially aspirational / demo-level.

### Repo: vinyl-tracker
- Scraper-focused system pulling prices into a DB
- Strong example of scraping stack (Python, BS4, lxml, Supabase)
- Weak product layer — unclear user workflow
- Heavy maintenance burden if sources change

## My Angle (Early Hypothesis)

- I do NOT want to track:
- I DO want to track:
- My first constraint:

## What This Is *Not*
- This is not a collector optimization tool.
- This is not about chasing the “best” pressing.
- This is not anti-Discogs or anti-knowledge.
- This is about reducing decision fatigue for people who just want good records at sane prices.

## Signals I Trust (Early Thinking)

These are plain-English signals I already use (often subconsciously) when deciding whether to buy a record now, wait, or pass.

- If a record keeps showing up “on sale” across Amazon, Target, or Walmart, the list price is probably inflated.
- If eBay listings sit unsold at the same price for weeks, that price isn’t real — it’s aspirational.
- If Discogs has dozens of versions but most sales cluster in a tight price band, versioning matters less than sellers think.
- If Reddit deal threads light up repeatedly for the same title, waiting usually pays off (members love posting “hold” memes/GIFs in the comments).
- If a title is widely available new, panic buying is almost never justified.
- If a record disappears briefly and then reappears at retail, scarcity was artificial.
- If prices spike around an anniversary or reissue rumor, they often settle back down.
- Some limited editions or special re-pressings (e.g., unique colors) *do* appreciate as a band breaks into the mainstream (Slomosa, for example).
- If a record quietly restocks at multiple retailers after being “sold out,” initial scarcity was marketing-driven.
- For common titles, condition matters more than pressing — a clean copy at a fair price beats a hyped version in rough shape.
- If a recent retail sale (e.g., Amazon) cleared copies at ~$15 but secondary listings remain ~$30+, the market hasn’t adjusted yet — waiting or offering below ask is usually rational. This acknowledges that sales reset reality, explains why the market feels “wrong” afterward. and it gives guidance without pretending to be precise. This is not anti-seller — it’s anti-delusion.
- When recent sold prices are materially lower than current Buy-It-Now listings, the market is in a standoff — sellers are anchored to peaks, buyers to history. In these cases, offers (or patience) outperform panic buying. This might mean that the buy-It-Now ≠ market truth, that timing/time matters, and that offers are a strategy, not an insult.

## First Worked Verdict (Draft)

### Album: Bone Thugs-N-Harmony — *E. 1999 Eternal* (VMP Repress)

**Verdict:** Inflated / Hold or Offer Below Ask

**Context:**
- Out-of-print VMP repress (2023); original pressings exist but are not the primary market reference for most buyers.
- Album is culturally significant, which amplifies emotional pricing.

**Signals Observed:**
- Discogs sold prices ranged ~$75–$120 over the past year.
- Current Buy-It-Now listings cluster ~$175–$200 with limited movement.
- eBay listings sit unsold at higher price points, some with Buy It Now
- Private offers exist below public listings, suggesting softness beneath the surface.

**Interpretation:**
Sellers appear anchored to peak scarcity pricing, while buyers remain anchored to historical sales. This has created a pricing standoff where listings do not reflect clearing prices.

**Guidance:**
Unless ownership is time-sensitive, waiting or making offers materially below ask is rational. This is not a “deal” environment — it is a negotiation environment.

## Possible Verdict Systems (Draft 1.0)
- Buy Now (Mispriced / Lagging)
- Fair Price (Market Rate)
- Inflated (Wait or Offer)
- Artificial Scarcity (Ignore)
- True Scarcity (Pay if you must)

## Poassible Verdict System (Draft 1.1)

- **Deal** — materially below recent clearing prices
- **Fair** — aligned with market reality
- **Inflated** — anchored to peaks or list prices, not sales
- **Artificially Scarce** — supply manipulation or marketing-driven
- **Grail** — truly out-of-print, emotional pricing applies

## Verdict System (Draft 2.0)

- **Unmissable Deal**  Mispriced relative to recent reality. Buy immediately.

- **Good Deal**  Below typical market expectations. Worth buying if you want it.

- **Market Price**  Fair, boring, stable. Buy if you’re ready; no urgency.

- **Inflated**  Anchored to peaks, list prices, or hype. Wait or make offers.

- **Negotiation Zone**  Listings don’t reflect clearing prices. Patience or offers outperform panic.

- **True Scarcity**  Genuinely out-of-print or structurally limited. Grails fall into this category. Price reflects reality — decide emotionally, not rationally.

