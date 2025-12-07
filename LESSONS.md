# Lessons Learned

Reference for future AI sessions. Learn from past mistakes.

---

## GitHub Markdown Line Breaks

> Source: Session 7 Dec 2025

### Problem
GitHub markdown does NOT render line breaks from plain text.

### What doesn't work

```markdown
❌ Plain text (renders as one line)
**Date**: 7 Dec
**Time**: 14:50

❌ Blockquote (renders as one line)
> Line 1
> Line 2
```

### What works

```markdown
✅ Bullet list (RECOMMENDED)
- **Date**: 7 Dec
- **Time**: 14:50

✅ Table
| Key | Value |
|-----|-------|
| Date | 7 Dec |

✅ HTML <br>
**Date**: 7 Dec<br>
**Time**: 14:50
```

### Rule
> Need multiple lines in GitHub markdown? → **Use bullet list first**

---

## GitHub Issues

> Source: Session 7 Dec 2025

### Problem
Long issues don't get read.

### Guidelines
- Keep it short
- Use user's language (Thai user → write Thai)
- Enough context, but not an essay
- Use checklist for tracking

### Good structure

```markdown
## Summary
1-2 sentences

## Changes
- Item 1
- Item 2

## Checklist
- [ ] Task 1
- [ ] Task 2
```

---

## Working with Users

> Source: Session 7 Dec 2025

### For AI
- **Ask requirements upfront** - Git? Issues? What language?
- **Know platform limitations** - e.g., GitHub markdown quirks
- **Preview before commit** - if unsure

### What good users do (learn from Nat)
- Give feedback immediately
- Be direct - AI handles direct feedback well
- Know what they want

---

---

## Timestamps

> Source: Session 7 Dec 2025

### Rule
Always include **time + timezone** when writing timestamps.

### How to get Bangkok time
```bash
TZ='Asia/Bangkok' date '+%Y-%m-%d %H:%M:%S %Z'
```

### Good format
```
*Generated: 7 Dec 2025 · 15:43 (GMT+7 Bangkok)*
```

### Bad format
```
*Generated: 7 Dec 2025*  ← missing time!
```

---

---

## macOS Text-to-Speech

> Source: Session 7 Dec 2025

### Voices
- **Thai**: `Kanya` (ผู้หญิง, ใช้ "ค่ะ" ไม่ใช่ "ครับ")
- **English**: `Samantha`

### Usage
```bash
# Thai (background)
say -v "Kanya" -r 280 "สวัสดีค่ะ" &

# English (background)
say -v "Samantha" -r 220 "Hello!" &
```

**Always use `&`** - runs in background, don't wait for speech to finish.

### Speed
- `-r 200` = normal fast
- `-r 280` = faster

---

*Last updated: 7 Dec 2025 · 16:15 (GMT+7 Bangkok)*
