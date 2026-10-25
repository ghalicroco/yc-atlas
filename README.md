# YC Atlas v2 — Startup Intelligence & Idea Lab

A shareable static website MVP for exploring publicly listed Y Combinator companies and turning a problem statement into an initial research brief.

## What works
- Live loading from the public `yc-oss/api` JSON endpoint
- Company search, sector/batch/location filters and sort
- Company cards, logo/favicons, company detail modal and source links
- Save favourites in browser local storage
- CSV export of filtered companies
- **Startup Idea Lab**: enter a problem, geography and business type; the page creates a structured validation brief and finds keyword-related YC companies
- Copy brief to clipboard

## Honest limits
The Idea Lab is an MVP, not a true semantic search or LLM research agent. It uses transparent keyword matching against public company records. Its “opportunity” prompts are hypotheses to validate, not evidence that a market is open. Geography is a user-supplied context and is not used to verify local competitors. Company summaries are source descriptions rather than independently verified company research.

## Run locally
```bash
python3 -m http.server 8000
```
Visit http://localhost:8000. If direct file opening blocks the data fetch, use the local server.

## Publish and share
1. Create a public GitHub repo named `yc-atlas`.
2. Upload `index.html` and this `README.md`.
3. In **Settings → Pages**, choose deployment from `main` and `/ (root)`.
4. Share the generated GitHub Pages URL.
You can also deploy as a static site on Netlify or Vercel.

## Data sources
- Dataset JSON: https://yc-oss.github.io/api/companies/all.json
- API repository: https://github.com/yc-oss/api
- Official YC directory: https://www.ycombinator.com/companies/

## Roadmap beyond this MVP
1. Add a backend ingestion job and versioned dataset snapshots.
2. Add semantic embeddings for problem/solution retrieval.
3. Enrich selected company profiles with AI-generated summaries and per-claim citations.
4. Track source dates, product status, pricing, customers and competitors.
5. Build sector trends, batch cohort comparisons and Europe-specific competitor research.
6. Add a persistent user account and shareable saved lists.
