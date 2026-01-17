# Phase 2 Days 2-3: Max Capabilities & Effective Prompting

**Date**: January 16, 2026  
**Time**: 1:40 PM - 10:10 PM GMT (with breaks)  
**Duration**: ~2.5 hours active learning  
**Status**: ✅ Complete

---

## Day 2: Max Capabilities & Verification (1:40-2:58 PM)

### What I Learned

**Max's Access Scope**
- ✅ Full Notion workspace (search, fetch, create, update with approval)
- ✅ GitHub repos (commits, PRs, files, branches, issues)
- ✅ File uploads (via search_files_v2)
- ❌ Private credentials, local machine files, email/Slack (not connected)
- ❌ Strategic decisions, budget authorization, production changes without approval

**Verification Framework**
- ALWAYS verify: Operational state, before modifications, financial/legal data, client communication
- OPTIONAL verify: General knowledge, process guidance, learning content
- Red flags: "probably", "likely", "should be", specific numbers without source

**Live Demonstrations**
1. Fetched Notion workspace structure (Master Projects, Active Projects, client work)
2. Fetched GitHub commits (last 5 from learning journal)
3. Retrieved exact project status (Natalia Portfolio, Invoice Automation)
4. Demonstrated fetch-before-report pattern

### Exercises Completed

**Verification Test (Statements A, B, C)**
- Statement A: "Last commit 40 minutes ago" → ⚠️ VERIFY (specific operational data)
- Statement B: "Context/Changes/Risk format helps reviewers" → ✅ TRUST (documented process)
- Statement C: "Natalia probably waiting, ships next week" → 🚨 DANGER (hallucination triggers)

**Score**: 8/10 - Caught hallucinations, recognized verification needs

**Learning Page Fetch**
- Asked: "When was my learning progress page last updated?"
- Max response: ❗ Fetched → "Jan 16, 2026 @ 12:21 PM GMT"
- Pattern demonstrated: Ask → Fetch → Report exact data

### Key Takeaway
**Trust but verify**. Max must fetch before claiming operational state. Never accept "probably" or "likely" for client/project data.

---

## Day 3: Effective Prompting Framework (3:04-4:10 PM + 10:10 PM)

### What I Learned

**Core Prompt Structure: Context + Intent + Constraints**

**Context**: What Max needs to know (situation, background, why asking)
**Intent**: What you want done (specific action, desired outcome)
**Constraints**: Boundaries (what NOT to do, format, approval gates)

**ADHD-Friendly Alternative: 3-Bullet Format**
- **What**: Action in plain language
- **Why**: Reason (keeps context clear)
- **How**: Specific execution or constraint

### Examples Reviewed

**Bad Prompt**: "Update the project." (vague, missing details)

**Good Prompt**: 
```
Context: Just finished Day 2 of Phase 2 training
Intent: Update Notion learning progress page to show Day 2 complete
Constraints: Fetch first, show changes, get approval
```

**ADHD Format**:
```
What: Update GitHub learning journal with Phase 2 Days 1-2 progress
Why: Haven't documented Day 2 yet, need complete record
How: Create journal/phase-2-day-2.md with verification training content
```

### Exercises Completed

**Scenario 1: GitHub Commit Count** ✅
- **My prompt**: "Context: tell me commits in last 7 days / Intent: Fetch joe learning journal / Constraints: exact data, no guessing"
- **Result**: Max fetched → Found 4 commits (all Jan 16) → Zero commits Jan 9-15
- **Score**: 8.5/10 (excellent structure, minor redundancy in context)

**Scenario 2: New Notion Client Project** ⚠️
- **My prompt**: "Context: add client project / Intent: fill in fields / Constraints: DDprOS rules"
- **Problem**: Missing critical data (which client? what project? status? owner?)
- **Learning**: Prompts need EXECUTABLE DATA, not just intent
- **Max response**: Fetched Master Projects schema → showed required fields → asked for details

**Scenario 3: End-of-Day Report** ✅ (This prompt!)
- **My prompt**: "What: finish today's learning / Why: end of day / How: produce report, add to GitHub and Notion"
- **Result**: Max structured complete workflow with approval gates
- **Score**: Perfect application of What/Why/How format

### Prompt Templates I Can Use

**Template 1: Fetch and Report**
```
Context: [situation]
Intent: Fetch [source] and tell me [specific thing]
Constraints: Show exact data, no guessing
```

**Template 2: Execute with Approval**
```
Context: [background]
Intent: [specific action]
Constraints: Fetch first, show changes, get approval
```

**Template 3: ADHD Quick Hit**
```
What: [action]
Why: [reason]
How: [method/constraint]
```

### Key Takeaway
**Structured prompts = efficient execution**. Context/Intent/Constraints or What/Why/How prevents wasted rounds. Always include EXECUTABLE DATA for write operations.

---

## Skills Progression

**Phase 1** → Read GitHub, assess risk, review PRs (manager lens)  
**Phase 2 Days 1-3** → Understand Max capabilities, verify data, structure prompts

**Next** → GitHub-Notion sync, technical decision support, documentation automation

---

## Confidence Check (Self-Rating)

- Understanding when to use Max: **8/10** (clear on capabilities/limits)
- Structuring effective prompts: **8/10** (Context/Intent/Constraints solid, need more practice with edge cases)
- Trusting but verifying AI outputs: **9/10** (strong red flag recognition, good verification discipline)
- ADHD-friendly workflow: **9/10** (What/Why/How format feels natural)

---

## Next Actions

1. Ship this journal entry to GitHub (PR with Context/Changes/Risk)
2. Update Notion learning progress page
3. Resume Phase 2 Week 5 Day 4-5: GitHub-Notion sync workflows

---

**Artifacts Created**:
- This journal entry (phase-2-day-2-3.md)
- Verification framework notes
- Prompt templates collection
- End-of-day report workflow

**Time to Phase 2 completion**: ~4-5 more sessions (Days 4-7)
