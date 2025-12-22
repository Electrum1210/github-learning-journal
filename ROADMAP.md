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





