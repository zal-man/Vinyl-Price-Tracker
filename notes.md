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
- Where Popsike fits vs live marketplaces
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