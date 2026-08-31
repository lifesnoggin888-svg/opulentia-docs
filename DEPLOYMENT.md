# Deployment Notes

## Live

- Production: https://opulentia-digital.vercel.app
- Source: https://github.com/jayblast-spec/opulentia-digital-core-horizon

## Pipeline

```bash
npm run build          # real production build, not just dev
vercel --prod           # deploy to production
```

Every deploy is verified with a direct `curl` against the live URL before
being reported as done — a git push or `vercel --prod` completing without
error is not itself proof the site is live and correct.

## Domain

The production Vercel deployment is not yet aliased to a custom domain.
Domain purchases are handled directly by the company, not automated here.
