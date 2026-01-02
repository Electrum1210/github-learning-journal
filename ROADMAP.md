# \# Learning Roadmap

# 

# Journal and roadmap for my GitHub + GitHub Desktop learning as a non-developer manager, based on DeDaydreamer/thedaydreamverse-site.

# 

# ---

# 

# \## Week 1 – Foundations + Markdown basics

# ## Safe vs risky changes (manager view)

| Type of change                     | Why it feels safe or risky (manager view)           |
|------------------------------------|-----------------------------------------------------|
| Tiny README wording tweak          | Low blast radius, easy to review, easy to roll back |
| New feature touching many files    | Higher risk: more moving parts and dependencies     |
| Config change for production       | Potentially high risk: can break deployment         |
| Cosmetic UI text change only       | Usually safe, but still needs clear commit message  |


# Focus:

# \- Get comfortable with GitHub in the browser and GitHub Desktop.

# \- Understand forks, clones, and commits as "snapshots with explanations".

# \- Use Markdown for simple, clear text in this journal.

# 

# Git / GitHub goals:

# \- Star, Watch, and Fork DeDaydreamer/thedaydreamverse-site.

# \- Clone Electrum1210/thedaydreamverse-site and github-learning-journal with GitHub Desktop.

# \- Make small non-code changes (markdown edits, simple text files), commit, and push.

# 

# Markdown goals:

# \- Use `#` and `##` headings in README.md and ROADMAP.md.

# \- Write paragraphs with blank lines between them.

# \- Create bullet lists with `-` and numbered lists with `1.`.

# \- Use \*\*bold\*\* and \*italic\* for emphasis with `\\\*\\\*` and `\\\*`.

# 

# Manager angle:

# \- Treat Markdown as the layout language for decisions, notes, and learning logs, not as code.

# 

# ---

# 

# \## Week 2 – Structure, history, and Markdown for organization

# 

# Focus:

# \- Read the folder/file structure of DeDaydreamer/thedaydreamverse-site and your fork.

# \- Open commit history and see it as a sequence of decisions and risks.

# 

# Git / GitHub goals:

# \- View commit history for:

#   - DeDaydreamer/thedaydreamverse-site (upstream).

#   - Electrum1210/thedaydreamverse-site (your fork).

# \- Open individual commits and read messages for clarity and scope.

# \- Notice patterns like "feat:", "fix:", "chore:", "docs:" if present.

# 

# Markdown goals:

# \- Improve ROADMAP.md using:

#   - Nested lists to break down lessons.

#   - Links: `\\\[text](URL)` to reference your fork and important pages.

#   - A simple table (e.g., safe vs risky changes from a manager’s view).

# 

# Manager angle:

# \- Connect clear structure in files and docs to clear structure in the organization.

# \- Use Markdown structure to reflect how you group and prioritize work.

# 

# ---

# 

# \## Week 3 – Forks, upstream, and Markdown in communication

# 

# Focus:

# \- Understand forks vs upstream and how changes flow back using pull requests.

# \- Think about changes as proposals and conversations, not just code edits.

# 

# Git / GitHub goals:

# \- Compare your fork’s branches/commits to upstream for divergence.

# \- Learn the concept of a pull request (PR) as "a formal proposal to merge changes".

# \- Practice opening a draft PR from your fork to your fork (no real production impact).

# 

# Markdown goals:

# \- Draft PR descriptions using:

#   - Headings like "Context", "Changes", "Risk".

#   - Bullet lists for scope and impact.

#   - Task lists with `- \\\[ ]` as lightweight checklists.

# 

# Manager angle:

# \- Use Markdown in PRs and issues to communicate expectations, scope, and risk clearly.

# \- Treat PR descriptions as decision briefs a stakeholder can quickly understand.

# 

# ---

# 

# \## Week 4+ – Quality signals, reviews, and Markdown playbook

# 

# Focus:

# \- Spot red flags and good signals in repos, commits, and PRs.

# \- Develop your own manager review checklist.

# 

# Git / GitHub goals:

# \- Inspect branches, tags, releases (if any) in thedaydreamverse-site.

# \- Identify whether releases or tags exist and what they might represent.

# \- Review real commits and (later) PRs like a manager: scope, risk, communication quality.

# 

# Markdown goals:

# \- Create CHECKLIST.md or REVIEW-GUIDE.md in this journal with:

#   - Sections for "Repo structure", "Commit messages", "Release readiness", etc.

#   - Checklists and tables for "good signals vs red flags".

#   - Links to specific commits or PRs as examples.

# 

# Manager angle:

# \- Use Markdown documents as your persistent decision records and review templates.

# \- Aim for communication that another manager could pick up and use without you.

# 

# ---

# 

# \## Progress Log Pattern

# 

# Use this structure in separate journal files (for example, /journal/2025-01-15.md):

# 

# \- What I did today (specific actions).

# \- What I learned (in manager language).

# \- Questions to ask Aleks or another developer.

# \- Last completed marker to update in README.md or at the top of ROADMAP.md.

## Repo map – thedaydreamverse-site (manager view)

Core / app code

functions/ – likely where the actual site/app behaviour lives.

tests/ – code that checks the behaviour of functions/ (quality and safety net).

Configuration and build

package.json – declares dependencies, scripts, and basic metadata for how the project runs/builds.

.github/ – holds automation and workflow config (CI, issue templates, etc.), if present.

Documentation and communication

README.md – main entry point for understanding what this project is and how to work with it.

about, articles, contact, index, posts, sitemap, robots – all look like content or content‑layout parts of the site and, from a manager view, are communication surface with users and search engines.

## What to look for in README and key config (manager view)

In `README.md`, I want to quickly see:
- What this project is (1–3 sentences, plain language).
- How to run it locally (basic command or steps).
- How it is deployed or used in production (at least a short note).
- Who owns it / who to ask when something breaks.
- Any major risks or constraints (environments, data sensitivity, external services).

In `package.json` or similar config, I look for:
- `"scripts"` that hint at how to run, build, test, and deploy.
- Dependencies that might signal big external commitments (frameworks, cloud SDKs, etc.).
- Signs of testing (`"test"` scripts) as a basic quality signal.
- Anything that looks dangerous to change without a plan (e.g. deploy-related scripts).

### thedaydreamverse-site – current signals

- README: [Project purpose and usage are explained clearly; run/deploy, ownership, and basic risks are all covered well enough for a manager to understand the system at a glance.]
- package.json: [Run and test scripts are present, giving a clear way to start and validate the app; dependencies look modest, with no obvious high‑risk platform commitments at this stage].

## Branches/tags/releases – risk markers (manager view)

| Name | Type | What decision it represents | Risk level (manager view) |
|------|------|-----------------------------|---------------------------|
| main | branch | Current source of truth | Low (if tested) |
| [No other branches]
| [No other tags/releases]

## Pull request checklist (manager view)

Good PRs have:
- **Clear title** with type prefix (docs:, feat:, fix:) + short summary.
- **Structured description**:
  - Context: Why this change?
  - Changes: What files/scope?
  - Risk: Blast radius?
- **Narrow scope** (ideally 1 clear decision).
- **Draft status** for work-in-progress.

My draft PR example: [https://github.com/DeDaydreamer/thedaydreamverse-site/pull/1]

## Repo map – thedaydreamverse-site (UPDATED Week 2)

**High manager attention (risky changes):**
- `functions/` – behaviour logic; changes here need clear explanation [all listed are one folder - api]

**Medium attention (config/deploy):**
- `package.json` – run/build scripts
- `.github/` – automation/workflows (not listed here)

**Low attention (content/docs):**
- `posts/`, `about/`, etc. – content files
- `README.md` – project overview

## Commit patterns observed (Week 2 Lesson 2)

| Commit message                                                     | Files changed                                | Risk level | Manager notes                                          |
|--------------------------------------------------------------------|----------------------------------------------|------------|--------------------------------------------------------|
| Update clear-mornings.html                                         | posts/updates (1 html)                       | Low        | Content only                                           |
| CSS                                                                | .gitignore, assets/styles.css (2 files)      | Medium     | Config + styling; limited but not zero risk           |
| Hero image mod                                                     | welcome-to.png                               | High       | Affects key visual asset; check impact on layout/UX    |
| Track posts/first-post.html: allow local draft and update .gitignore | .gitignore, posts/first-post.html          | Medium     | Config + content; .gitignore change needs attention   |
| Update about.html                                                  | about.html                                   | Low        | Small content change                                  |
| build: pull private vault content during deploy                    | tools/pull-vault.sh                          | High       | Build/deploy behaviour; needs strong review/testing   |
| Initial commit: thedaydreamverse site (vault content excluded)     | ~36 files (.config, api, etc.)              | High       | Many files incl. config/api; foundational, broad risk |

## Safe vs risky changes (manager view) – updated with commit examples

| Type of change                                 | Why it feels safe or risky (manager view)           |
|-----------------------------------------------|-----------------------------------------------------|
| Tiny README wording tweak                      | Low blast radius, easy to review, easy to roll back |
| New feature touching many files                | Higher risk: more moving parts and dependencies     |
| Config change for production or deploy script  | High risk: can break deployment or environments     |
| Cosmetic UI or content text change only        | Usually safe, but still needs clear commit message  |
| Single function/api behaviour change           | High risk: behaviour changes; requires strong review |

## Week 3 Lesson 1 – Fork vs upstream divergence

Current state:
- My fork (Electrum1210/thedaydreamverse-site) is 1 commit ahead of upstream main.
- My additional commit(s) are:
  - Docs: add manager learning note to README.

Manager interpretation:
- Ahead commits = decisions made in my sandbox that are not yet in the source-of-truth.
- Even for docs-only changes, a PR should clearly explain Context / Changes / Risk before merge.

## Week 3 – PR review checklist (manager view)

For each pull request, I will check:

- **Title**
  - Uses a clear prefix (feat:, fix:, docs:, chore:) and plain-language summary.
- **Context**
  - Explains why the change is needed (problem, goal, or background).
- **Changes**
  - Lists main files/areas touched and the scope (small doc tweak vs many modules).
- **Risk**
  - States expected impact and risk level (low/medium/high) in non-technical terms.
  - Mentions if tests, checks, or manual verification were done.
- **Fit with repo risk map**
  - Notes whether the change is in high-risk areas (functions/api, deploy scripts) or low-risk (content/docs).

Example PR: https://github.com/DeDaydreamer/thedaydreamverse-site/pull/1

## Week 3 – PR feedback template (manager voice)

When reviewing a PR, I will aim to comment like this:

**1. Summary (what I see)**
- “This PR changes [area/files] and appears [low/medium/high] risk because [reason].”

**2. Questions (clarity and risk)**
- “Can you clarify [context/impact]?”
- “What testing or checks have you done?”
- “What could go wrong if we merge this as-is?”

**3. Decision**
- Approve: “I’m comfortable approving this because [reason: scope, tests, low risk].”
- Request changes: “Before approving, I need [specific change or clarification].”
- Block (rare): “I can’t approve this in its current form because [major risk/uncertainty].”

Example (for PR #1):
- Summary: Docs-only change to README; very low risk.
- Question: Will this note be relevant to other contributors?
- Decision: Approve once wording is confirmed.

## Week 4 – Repo quality checklist (manager view)

For any repo (including thedaydreamverse-site), I will look at:

**Structure**
- Clear top-level folders (core code, config, docs, content).
- A README that explains purpose, how to run, and who owns it.

**History**
- Reasonable commit sizes and messages (not all huge, not all “fix stuff”).
- Mix of content/config/behaviour changes that match the project’s goals.

**Collaboration**
- Issues and PRs used (or explicitly not needed) and kept up to date.
- Draft PRs for work in progress; clear, reviewed PRs for changes to main.

**Releases / stability**
- Tags or releases marking shipped points (if production).
- If none: treat project as early/experimental.

Initial notes for thedaydreamverse-site:
- README explains the project and its goal in clear, simple language.

- The live website link is prominently provided near the start.

- The contents of the repository are described so a reader understands what lives where.

- Deployment and usage instructions are documented clearly enough to follow.

- Ownership and who to contact for issues are explicitly stated.

- No major risks or constraints are called out at this development stage.

- The Issues tab currently shows no open issues.

- There is one pull request, which is my draft manager learning note.

- No automated workflows or Actions are visible for this repository.

- No immediate actions are required; the draft PR remains open for future review.

