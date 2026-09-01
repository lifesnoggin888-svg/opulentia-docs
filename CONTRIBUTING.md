# Contributing to Opulentia Docs

This repo documents [Opulentia Digital Core Horizon](https://opulentia-digital.vercel.app) (RC-9802444) — architecture, deployment, and process notes for the platform. It's not the application source; that lives in [opulentia-digital-core-horizon](https://github.com/jayblast-spec/opulentia-digital-core-horizon).

## What belongs here

- Architecture decisions and how the live pages/data flows actually work (`ARCHITECTURE.md`)
- Deployment process and verification steps (`DEPLOYMENT.md`)
- Anything a new contributor would otherwise have to reverse-engineer from the codebase

## Ground rules

- **No fabricated numbers.** `ARCHITECTURE.md` already documents the correction made after an early draft shipped placeholder stats. Keep it that way — no invented metrics, no unverifiable claims, anywhere in these docs.
- **Docs follow reality, not the other way around.** If a doc describes a page, flow, or pipeline step, it should match what's actually deployed. If you change the app in a way that makes a doc wrong, update the doc in the same PR.
- **Deployment claims need evidence.** Per `DEPLOYMENT.md`: a `git push` or `vercel --prod` completing without error is not proof the site is live and correct. If you're documenting a deploy step, document the verification step next to it.

## How to contribute

1. Fork this repo, branch off `main`.
2. Make your change. Keep PRs scoped to one doc/topic where possible.
3. Open a PR describing what changed and why.
4. If your change affects deployment or architecture claims, note how you verified it's accurate.

Small, accurate fixes (typos, broken links, missing steps) are welcome without prior discussion. Larger additions (new sections, restructuring) — open an issue first so we're aligned before you write it.
