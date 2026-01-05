# Max AI Prompt Templates

**Usage:** Copy these templates and fill in the bracketed placeholders with your specific details.

**Structure:** Context + Intent + Constraints = Good Prompt

---

## 1. GitHub-Notion Sync

### Basic Sync
```
Max, sync the latest commits from [repo-name] to my [Notion-page-name].
```

### Detailed Sync with Analysis
```
Max, check [GitHub-repo] for new commits since [date].
Update [Notion-page-URL] with:
- Commit messages
- Files changed
- Key achievements
Highlight any concerning patterns.
```

### Weekly Progress Update
```
Max, update Joe's learning progress.
[This triggers: pull github-learning-journal commits → update Notion COO Learning Progress page]
```

---

## 2. Project Status Generation

### Quick Status Check
```
Max, what's the current status of [project-name]?
Include: last update, blockers, next action.
```

### Full Project Report
```
Max, generate a status report for [project-name] from Master Projects DB.
Format: 3-bullet summary (What/Why/Next)
Include: timeline, owner, department, recent changes.
```

### Department Rollup
```
Max, summarize all active projects in [Department-name].
Show: project names, status, owners, blockers.
Format as markdown table.
```

---

## 3. GitHub PR Review (Manager View)

### Basic Review
```
Max, review this PR from a manager perspective: [PR-URL]
Assess:
- Scope (what changed)
- Risk level (high/medium/low)
- Communication quality
Flag any red flags.
```

### Detailed Risk Assessment
```
Max, analyze PR #[number] in [repo-name].
Focus on:
- Files changed in high-risk zones
- Breaking changes
- Missing documentation
- Review comments
Provide manager-friendly summary.
```

---

## 4. Notion Page Creation

### Create Page from Brief
```
Max, create a Notion page in [parent-page/database-name] with:
Title: [page-title]
Content:
- [section 1 details]
- [section 2 details]
- [section 3 details]
Use proper markdown formatting.
```

### Update Existing Page
```
Max, update [Notion-page-URL].
Change [section-name] to:
[new-content]
Keep everything else unchanged.
```

---

## 5. Documentation Generation

### README Creation
```
Max, create a README.md for [repo-name].
Include:
- Project overview
- Setup instructions
- Usage examples
- License
Tone: professional but friendly.
```

### Checklist Generation
```
Max, create a checklist for [task/process-name].
Format: markdown, actionable items, grouped logically.
Include common pitfalls to avoid.
```

---

## 6. Decision Support

### Should I Use Max?
```
Max, is this task suitable for AI assistance: [describe-task]?
Explain why or why not.
If yes, give me the optimal prompt.
```

### Technical Translation
```
Max, translate this technical concept for operational understanding:
[technical-term/description]
ELI5 style, focus on business impact.
```

---

## 7. Automation Workflows

### Custom Workflow Creation
```
Max, help me automate [repetitive-task].
Current process:
1. [step 1]
2. [step 2]
3. [step 3]
What can you automate? Give me the workflow.
```

### Time Savings Estimate
```
Max, estimate time savings if we automate [task-name].
Current time: [X minutes/hours per week]
Describe the automated workflow.
```

---

## 8. Troubleshooting

### Unclear AI Response
```
Max, your last response was unclear.
I need: [specific-information]
Context: [additional-context]
Format: [preferred-format]
```

### Error Diagnosis
```
Max, help troubleshoot this error:
[error-message/description]
Context: [what-I-was-doing]
What should I check?
```

---

## 9. Learning Support

### Concept Clarification
```
Max, explain [concept] in the context of DeDynamics operations.
Why does it matter for a COO?
Give 1 real example from our projects.
```

### Progress Check
```
Max, assess my progress on [learning-goal].
What have I accomplished?
What should I focus on next?
```

---

## 10. Escalation

### When to Ask Humans
```
Max, I need to decide: [decision-description].
Give me:
- Pros/cons analysis
- Risk assessment
- Your recommendation
- Flag if this needs Aleks approval
```

### Budget/Strategic Decisions
```
Max, gather information for this decision: [decision-details].
Provide:
- Relevant data from Notion/GitHub
- Similar past decisions
- Key considerations
Note: Final decision requires Aleks approval.
```

---

## Best Practices

### Good Prompt Anatomy
```
Max, [specific action] for [target].
[Context or constraints]
[Desired format or output]
[Any special requirements]
```

### Example - Good vs Bad

❌ **Bad:**
"Update the thing"

✅ **Good:**
"Max, update the DeDynamics Main Website project status in Master Projects DB. Set status to 'Active' and add next action: 'Deploy to Cloudflare Pages'."

---

## Tips for Effective Prompting

1. **Be specific:** Include URLs, names, exact details
2. **Add context:** Why you need this, what you'll do with it
3. **Set constraints:** Format, length, tone preferences
4. **Iterate:** Refine prompt if response isn't quite right
5. **Verify:** Always double-check AI outputs for accuracy
6. **Save winners:** Bookmark prompts that work well

---

## ADHD-Friendly Format

For maximum clarity, use this structure:

```
Max, [action]:
- [detail 1]
- [detail 2]
- [detail 3]

Output: [expected format]
```

Example:
```
Max, create project status update:
- Project: DSS Website
- Pull from: Master Projects DB
- Include: status, blockers, next action

Output: 3-bullet summary (What/Why/Next)
```
