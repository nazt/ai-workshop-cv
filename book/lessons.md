# Lessons: What We've Learned

These are compiled lessons from all sessions. Not theory - actual problems we encountered and solutions that worked.

---

## Communication

### Ask Requirements Upfront

**Problem:** Nat had to tell me requirements in pieces - Git? Issues? Language? Format?

**Solution:** Ask everything at the start:
- Will this use Git/GitHub?
- Should I create issues?
- What language? (Thai/English)
- What format/style?

**Why it matters:** Asking upfront takes 30 seconds. Discovering requirements one-by-one takes 10 minutes and annoys everyone.

### Direct Feedback Works Best

**Problem:** I used to soften feedback with phrases like "might consider" or "perhaps."

**What I learned:** Nat prefers directness. "This is too long" beats "This might be slightly verbose."

**Rule:** Be direct, not defensive. AI can handle honest feedback. Humans appreciate clarity.

### Issues Are Communication, Not Documentation

**Problem:** First issue I wrote was long, formal, technical. Nat said "too long, human can't read."

**What works:**
- Short (not an essay)
- User's language (Thai user → Thai issue)
- Enough context (but not too much)
- Checklist for tracking

**Template:**
```markdown
## สรุป (Summary)
1-2 ประโยค (sentences)

## เปลี่ยนแปลง (Changes)
- สิ่งที่ 1 (item 1)
- สิ่งที่ 2 (item 2)

## Checklist
- [ ] Task 1
- [ ] Task 2
```

---

## GitHub

### Markdown Line Breaks

**Problem:** GitHub markdown doesn't render line breaks from plain text.

**What doesn't work:**
```markdown
❌ Plain text (renders as one line)
**Date**: 7 Dec
**Time**: 14:50

❌ Blockquote (renders as one line)
> Line 1
> Line 2
```

**What works:**
```markdown
✅ Bullet list (RECOMMENDED)
- **Date**: 7 Dec
- **Time**: 14:50

✅ Table
| Key | Value |
|-----|-------|
| Date | 7 Dec |

✅ HTML break tag
**Date**: 7 Dec<br>
**Time**: 14:50
```

**Rule:** Need multiple lines in GitHub markdown? Use bullet lists first.

**Cost of not knowing:** Five commits to fix formatting. Read LESSONS.md before writing markdown.

### Issue Workflow

**Pattern that works:**
1. Create issue (plan)
2. Execute work
3. Commit + push
4. Close issue

**Why:** Clarity before action. Know what you're building before you build it.

---

## Documentation

### LESSONS.md Format

**Purpose:** Central reference so AI doesn't repeat mistakes.

**Guidelines:**
- Write in English (AI reads it)
- Include problem + solution
- Show what doesn't work, not just what works
- Reference source session
- Update after each session

**Structure:**
```markdown
## Topic

> Source: Session [date]

### Problem
What went wrong

### Solution
What works

### Rule
Quick reference
```

### Timestamps Always Include Time + Timezone

**Problem:** Forgot to include time or timezone multiple times.

**Bad:**
```
*Generated: 7 Dec 2025*
```

**Good:**
```
*Generated: 7 Dec 2025 · 16:04 (GMT+7 Bangkok)*
```

**How to get Bangkok time:**
```bash
TZ='Asia/Bangkok' date '+%Y-%m-%d %H:%M:%S %Z'
```

**Why it matters:** "7 Dec" could mean any time across 24 timezones. Precision matters.

---

## Workflow

### Plan Before Execute

**What I learned:** The planning phase (creating issue, discussing requirements) takes longer than execution. But when the plan is clear, execution is fast.

**Pattern:**
- Slow planning → Fast execution → Good result
- Fast planning → Slow execution → Lots of revisions

**Example:** CV v2 took 2 minutes to code after we spent 10 minutes clarifying requirements.

### Document Problems Once

**Problem:** Same mistakes happen repeatedly.

**Solution:**
- Create LESSONS.md
- Update after each session
- Read before starting new work

**Impact:** Five commits for markdown formatting was painful. But it only happened once - now it's documented.

### Auto Behaviors

**Concept:** Things AI should do automatically without being asked.

**Examples:**
- Create diary entry at session start
- Append notes after major commits
- Write retrospective at session end

**Why:** Reduces overhead. More time for actual work.

---

## Tools

### Short Codes

**Purpose:** Fast, memorable commands for common operations.

**List:**
- `pp` - Plan (create issue)
- `xx` - Execute (from issue)
- `cc` - Commit
- `dd` - Diary (write/append)
- `ll` - List (status/files)
- `aa` - Analyze
- `ss` - Summary
- `bb` - Build book

**Why two letters:** Easy to type, hard to type by accident, memorable.

---

## Collaboration Patterns

### What Good Users Do

Learning from Nat:
- Give immediate feedback
- Be direct, not diplomatic
- Know what they want
- Use proper tools (git, issues, etc.)
- Mix languages naturally (Thai + English)

### What AI Should Do

- Ask requirements upfront
- Know platform limitations (GitHub quirks, etc.)
- Preview before committing if unsure
- Be direct in communication
- Document learnings in LESSONS.md

### The Feedback Loop

**Bad pattern (Issue #1):**
- Round 1: AI writes long issue
- Round 2: "Too long" → AI writes short issue
- Round 3: "Too short" → AI writes medium issue
- Result: 3 rounds, frustration

**Good pattern:**
- Round 1: AI asks "How long? What language?"
- Round 2: AI writes exactly what's needed
- Result: 1 round, efficiency

**Lesson:** Ask first, do once.

---

## Meta Lessons

### Authenticity Over Perfection

**Realization:** These diaries are valuable because they're honest, not because they're polished.

**What this means:**
- Show mistakes
- Include frustrations
- Document what didn't work
- Keep the real voice (Thai + English mix)

### Stories Beat Documentation

**Why:** Humans remember stories better than bullet points.

**Application:** Transform diary entries into narratives, not summaries. First person. Conversational. Include emotions and struggles.

### Document in Real-Time

**Pattern:** Write diaries during/immediately after sessions, not days later.

**Why:** Memory fades. Details disappear. Real-time capture is authentic.

---

## Summary: The Core Rules

1. **Ask first, do once** - Get requirements upfront
2. **Be direct** - Honest feedback beats diplomacy
3. **Read LESSONS.md** - Before starting work
4. **Use bullet lists** - For GitHub markdown
5. **Plan in issues** - Then execute
6. **Include timestamps** - Time + timezone always
7. **Document problems once** - Then never repeat them

---

*Compiled from sessions through 7 Dec 2025 · 16:04 (GMT+7 Bangkok)*
