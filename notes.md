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