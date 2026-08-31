# Architecture Notes

## Stack

- Next.js 16 (App Router, Turbopack), TypeScript, Tailwind CSS v4
- Hosted on Vercel

## Pages

- `/` — homepage: hero, live news ticker, product grid, positioning section
- `/about`, `/careers`, `/contact` — standard company pages
- `/services` + `/services/[slug]` — four product overview and detail pages
- `/news` — live Tech News Hub, sourced from the Hacker News Algolia API
- `/blog` + `/blog/[slug]` — company-authored Insights posts

## Live news data flow

`lib/news.ts` fetches from `hn.algolia.com/api/v1/search_by_date`, filtered
to `points>15`, sorted by recency. Results are revalidated every 5 minutes
via Next.js ISR and used both on the homepage ticker and the dedicated
News Hub page. Every headline links out to the original publisher.

## Content principle

No fabricated metrics or unverifiable claims anywhere on the site — this
was a deliberate correction after an early AI-generated draft included
placeholder stats ("$50B+", "1M+ users") that didn't reflect reality for
a brand-new company.
