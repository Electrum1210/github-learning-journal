# Decision Tree: When to Use Max vs Escalate

**Purpose:** Clear framework for deciding when to use AI vs when to involve humans.

---

## Quick Reference

| Task Category | Use Max? | Escalate? | Why |
|---------------|----------|-----------|-----|
| **Read-only info gathering** | ✅ Yes | ❌ No | Max can fetch data from Notion/GitHub |
| **Routine updates** | ✅ Yes | ❌ No | Updating project status, syncing data |
| **Documentation** | ✅ Yes | ⚠️ Review | Max generates, human verifies |
| **Technical translation** | ✅ Yes | ❌ No | Max explains tech concepts |
| **Budget decisions** | ❌ No | ✅ Yes | Requires human approval |
| **Strategic direction** | ❌ No | ✅ Yes | Requires founder judgment |
| **Hiring/firing** | ❌ No | ✅ Yes | Human-only decision |
| **Client communication** | ⚠️ Draft only | ✅ Yes | Max drafts, human sends |
| **PR reviews** | ✅ Yes | ⚠️ Verify | Max gives manager view, human decides |
| **Workflow design** | ✅ Yes | ⚠️ Validate | Max proposes, human validates |

---

## Detailed Decision Flow

### Step 1: Can Max Access Required Data?

**Max has access to:**
- ✅ Notion workspace (all pages, databases)
- ✅ GitHub repos (DeDynamics, DSS, related orgs)
- ✅ Uploaded files (PDFs, images, documents)
- ✅ Web search (current information)
- ✅ Conversation history (this Space)

**Max does NOT have access to:**
- ❌ Bank accounts / financial systems
- ❌ Email inbox
- ❌ Private client communications
- ❌ Calendar (unless explicitly shared)
- ❌ Password managers
- ❌ Social media accounts

**→ If Max can't access required data, escalate or provide data manually**

---

### Step 2: Does Task Require Approval/Budget?

**Tasks requiring human approval:**
- Spending money (any amount)
- Committing to client deliverables
- Changing strategic direction
- Hiring or firing decisions
- Publishing content externally
- Legal/compliance matters

**→ If yes, use Max to gather info, but escalate decision to Aleks**

**Tasks Max can handle:**
- Internal documentation
- Project status updates
- Data analysis and summaries
- Workflow proposals
- Learning progress tracking

**→ If no approval needed, Max can execute**

---

### Step 3: Is Speed or Accuracy More Critical?

**Use Max when:**
- Speed matters (quick status check, rapid prototyping)
- Task is repetitive (syncing, updating, formatting)
- You need multiple options to evaluate
- Research phase (gathering information)

**Escalate when:**
- Accuracy is critical (client-facing, legal, financial)
- High stakes decision (strategic, hiring, large budget)
- Political sensitivity (internal conflicts, negotiations)
- First-time process (no template exists)

---

### Step 4: Can You Verify the Output?

**Max is good for tasks where you can verify:**
- ✅ Notion page updates (you can see the change)
- ✅ GitHub syncs (compare commits to Notion)
- ✅ Documentation (review before publishing)
- ✅ Data summaries (check against source)
- ✅ Workflow proposals (test before implementing)

**Escalate if you can't verify:**
- ❌ Technical code changes (beyond your review capability)
- ❌ Complex financial calculations (need expert validation)
- ❌ Legal language (requires lawyer review)

---

## Common Scenarios

### ✅ USE MAX

**Scenario 1: Weekly project update**
```
Task: Update all DeDynamics projects with latest status
Why Max: Routine, repeatable, verifiable
Prompt: "Max, update all Active projects in Master Projects DB with current status"
```

**Scenario 2: GitHub activity summary**
```
Task: See what happened in repos this week
Why Max: Read-only, informational, no decisions
Prompt: "Max, summarize commits across DeDynamics repos from Dec 16-23"
```

**Scenario 3: Create meeting notes page**
```
Task: Set up structured page for team sync
Why Max: Template-based, internal, non-critical
Prompt: "Max, create meeting notes page in DeDynamics PM HQ for Dec 24 sync"
```

---

### ⚠️ USE MAX + VERIFY

**Scenario 4: PR risk assessment**
```
Task: Review PR before Joe approves merge
Why Max + Verify: Max provides manager view, Joe makes final call
Prompt: "Max, review this PR for risk: [URL]. I'll decide on merge after."
```

**Scenario 5: Client proposal draft**
```
Task: Draft scope document for DSS client
Why Max + Verify: Max generates structure, Aleks reviews before sending
Prompt: "Max, draft DSS client proposal for [project]. Aleks will review before sending."
```

**Scenario 6: New workflow design**
```
Task: Automate monthly reporting
Why Max + Verify: Max proposes workflow, team validates before implementing
Prompt: "Max, design workflow for monthly department reports. We'll test before rolling out."
```

---

### ❌ ESCALATE TO HUMAN

**Scenario 7: Hire contractor decision**
```
Task: Decide if we should hire photographer for DSS
Why Escalate: Budget + strategic decision
Action: Ask Max to gather data (rates, portfolio, availability), then discuss with Aleks
```

**Scenario 8: Client conflict resolution**
```
Task: Unhappy client wants refund
Why Escalate: High stakes, relationship management, financial impact
Action: Escalate immediately to Aleks, don't use Max
```

**Scenario 9: Change product strategy**
```
Task: Pivot DSS from portraits to commercial
Why Escalate: Strategic direction, affects entire business model
Action: Use Max to analyze market data, but decision is founder-only
```

---

## Red Flags: When to STOP and Escalate

🚩 **Max suggests spending money** → Escalate to Aleks

🚩 **Max can't access required data** → Escalate or provide data manually

🚩 **Task affects client relationships** → Escalate to Aleks

🚩 **You don't understand Max's reasoning** → Ask Max to explain, if still unclear, escalate

🚩 **Output looks wrong but you can't verify** → Escalate to subject matter expert

🚩 **Legal or compliance implications** → Escalate immediately

🚩 **Max says "I don't have access" or "I can't do that"** → Escalate or adjust approach

---

## Escalation Protocol

### When to Tag Aleks

**Immediate escalation (< 1 hour):**
- Client emergencies
- Budget/spending decisions
- Strategic pivots
- Legal/compliance issues

**Same-day escalation (< 24 hours):**
- Workflow design validation
- Technical decisions beyond your expertise
- Cross-department coordination
- Hiring/contractor decisions

**Weekly sync escalation:**
- Process improvement ideas
- Learning blockers
- Tool/system feedback
- Nice-to-have features

### How to Escalate

**In Notion:**
```
@Aleks - [Brief description]
Context: [1-2 sentences]
Urgency: [Immediate / Same-day / Weekly sync]
What I need: [Specific ask]
```

**Via Max:**
```
Max, I need to escalate this to Aleks: [description]
Prepare a summary with:
- Situation
- Options considered
- Your recommendation
- Why it needs human decision
```

---

## Practice Exercise

For each scenario, decide: Use Max, Max + Verify, or Escalate?

1. Update Joe's learning progress after new GitHub commits
2. Decide if we should migrate to a new hosting provider
3. Create a new project page in Master Projects DB
4. Respond to client asking about timeline
5. Generate weekly activity report for all departments
6. Approve contractor invoice for $500
7. Review PR that changes authentication system
8. Set up automated reminder for weekly syncs

**Answers:**
1. Use Max ✅
2. Escalate ❌ (strategic + budget)
3. Use Max ✅
4. Max + Verify ⚠️ (draft response, human sends)
5. Use Max ✅
6. Escalate ❌ (budget approval required)
7. Max + Verify ⚠️ (high risk area)
8. Use Max ✅

---

## Key Principles

1. **Default to Max for routine, repeatable, verifiable tasks**
2. **Always verify AI outputs before acting on them**
3. **Escalate budget, strategic, and client-facing decisions**
4. **Use Max to gather info, human to make final call on high-stakes decisions**
5. **If unsure, ask Max: "Should I escalate this?"**
6. **Document successful workflows for future reuse**
7. **Learn from mistakes: if Max gets it wrong, update this decision tree**

---

## Evolution

This decision tree will evolve as you gain experience:
- Week 5-6: Follow strictly
- Week 7-8: Start making judgment calls
- Month 2+: Intuitive understanding of boundaries
- Quarter 2: Propose updates to this framework

**Your goal:** Become confident in knowing when to use Max vs when to involve humans, without needing to reference this document.
