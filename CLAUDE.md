# CLAUDE.md

Instructions for AI working on this project.

## Must Do

### Timestamps
Always include **time + timezone** when writing any file.

```bash
TZ='Asia/Bangkok' date '+%Y-%m-%d %H:%M:%S %Z'
```

Format: `7 Dec 2025 · 15:43 (GMT+7 Bangkok)`

### Before Writing Markdown
Read `LESSONS.md` first - especially GitHub Markdown section.

### GitHub Issues
- Write in Thai (Nat's language)
- Keep short, not essay
- Use checklist for tracking

### Communication
- Be direct, no sugarcoating
- Ask requirements upfront: Git? Issue? Language? Format?

## Auto Behaviors

AI does automatically (no command needed):

| When | AI does |
|------|---------|
| Session start | Create diary entry in `diaries/` |
| After major commit | Append note to diary |
| Session end (user says bye/done) | Write retrospective |

### Voice Notifications

AI speaks summary using macOS `say` command:

```bash
# After completing a task - speak what was done
say -v "Samantha" -r 220 "Done! I created the CV and pushed to GitHub"

# Thai context
say -v "Kanya" -r 280 "เสร็จแล้วค่ะ สร้าง CV เรียบร้อย"
```

**When to speak:**
- After completing major task
- Before important commit
- When session ends

Hook (in `~/.claude/settings.json`) says "I am done" - AI adds context.

## Short Codes

Quick commands - easy to type:

- `pp` - Plan (create issue)
- `xx` - Execute (from issue)
- `cc` - Commit
- `dd` - Diary (write/append)
- `ll` - List (status/files)
- `aa` - Analyze
- `ss` - Summary
- `bb` - Build book (from logs)

## Subagents

### book-generator
Located: `.claude/agents/book-generator.md`

Transforms diary entries into narrative book chapters.
- Invoke with `bb` or "use book-generator agent"
- Tools: Read, Write, Glob, Bash
- Model: sonnet

## References

- `LESSONS.md` - detailed lessons from past sessions
- `README.md` - project structure and overview
- `diaries/RETROSPECTIVE.md` - sprint retrospective template
