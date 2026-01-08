# Questions for Aleks (COO consolidated)

## thedaydreamverse-site

* What's the deployment process for functions/api changes?
* ans: Cloudflare Pages handles automatic deployment. When you push to the main branch (or merge a PR), Cloudflare detects the change and rebuilds the site. For functions/api specifically, those are Cloudflare Workers functions — they deploy as part of the Pages build. No separate manual step required. If a function breaks, the build fails, and you'll see errors in the Cloudflare dashboard.
​
* Why so few commits in functions/api? Stable or not touched?
* Stable. The API layer was designed once, tested, and hasn't required changes since initial deployment. Most active work happens in content files (Markdown pages, assets, config). Functions/api commits would only appear if business logic changes — like adding a new endpoint or modifying how data flows.

* How much fork divergence is acceptable before we worry?
* Depends on intent. If the fork is for experimentation (like Joe's practice repo), divergence is fine — it's a sandbox. If the fork is meant to contribute back upstream via PRs, you want to stay close (sync every 1-2 weeks). If divergence grows beyond 20-30 commits or multiple months without sync, merging becomes risky — conflicts multiply. For DeDynamics forks used in production, we treat them as independent codebases unless explicitly maintaining upstream sync.

## ddpro-joer-businesscard-site

* Are there plans for automated deployment (vs manual file://)?
* Yes. Joe's business card site should move to Cloudflare Pages for automated deployment. Current file:// setup is a local-only prototype. Next step: connect the GitHub repo to Cloudflare Pages, configure build settings, and enable automatic deploys on push. This removes manual file handling and gives Joe a live URL to share.

* Any SEO/accessibility checks for assets/img changes?
* Not automated yet, but should be added. For SEO, image alt text and proper heading structure matter most. For accessibility, contrast ratios, keyboard navigation, and semantic HTML. Recommendation: add a pre-commit checklist in the repo (like Joe's REVIEW-GUIDE) that flags missing alt text or oversized images before pushing. We can also integrate Lighthouse CI into Cloudflare Pages builds to auto-check accessibility scores. But this is something to worry about after you learnd DDprOS

## General

* When do we start requiring PR Context/Changes/Risk sections?
* Now — for medium and high-risk changes. Define "risk" by blast radius:
​Low risk: README updates, new documentation, asset swaps (no review template required, but good practice)
Medium risk: Config changes, new features, API modifications (require Context/Changes/Risk in PR description)
High risk: Database schema changes, authentication logic, deployment pipeline edits (require full review template + second approver)


* What extra review steps for medium/high-risk changes?
Second reviewer required — never merge high-risk alone
Staging deployment test — deploy to preview environment first (Cloudflare Pages provides this automatically)​
Rollback plan documented — state how to undo if it breaks
Manual QA checklist — test affected workflows before merge
Post-merge monitoring — check logs/analytics for 24 hours after deploy
For high-risk only, add: Cloudflare Workers preview testing and explicit approval from me or you before merge.

*Last updated: 2026-01-08*

