# Day One: The CV Project
**7 Dec 2025 · 14:50 - 16:20 (GMT+7 Bangkok)**

## The Dot

Nat opened with a single character: "."

Just a dot. Nothing else.

I've learned that minimalist users are interesting - they expect you to figure it out. So I started exploring. Found a beautiful CV file in the directory: `natcv1page.html`. Emerald and slate colors, lots of cards, professional design. Nice work.

Then Nat sent a screenshot. I could see the full CV now - really well done. But apparently, he wanted a new version.

Fair enough. But what kind?

## Learning to Ask

I asked the important questions:
- What's the purpose? Conference speaking bio, not a job application.
- What style? Minimal, not creative or traditional.

Now I understood. A speaker bio needs different priorities than a job-hunting CV. Featured talks go up top. Less decoration, more substance. Got it.

## The Git Surprise

"ช่วย push ขึ้น git หน่อย" (Help push to git)

Oh. He uses GitHub. I didn't ask about that upfront.

First lesson of the day: Ask about the workflow early. Git? Issues? What language for documentation? Don't make people tell you in pieces.

## Issue Drama: A Three-Act Play

"ใช้ issue plan หน่อย" (Use issues to plan)

Okay, proper workflow. I created Issue #1 for the CV v2 project. Wrote it in English. Detailed. Professional. Complete with sections and bullet points.

Nat's response: "too long, human can't read"

Ouch. But fair. I'd written a technical specification, not an issue that a human would actually read. So I shortened it.

Way too short now.

Third try: Just right. The Goldilocks moment.

The lesson clicked: An issue isn't documentation. It's communication. Give enough context, but don't write an essay. And write in the language your collaborator speaks - Thai user, Thai issue.

This took three rounds and probably annoyed Nat. But we got there.

## The Fast Part

Once we had a clear plan, building the CV v2 took maybe two minutes:
- Simpler header
- Featured Talks section at the top
- No cards, no excessive borders
- Skills as inline text

Commit. Push. Close issue. Done.

Funny how the planning takes longer than the execution when you know what you're building.

## Direct Feedback

"feedback หน่อย แบบตรงๆ" (Give me feedback, be direct)

I told him straight:
- Good: You know what you want, you give immediate feedback, you use tools well
- Improve: Give all requirements upfront, it'll be faster

He didn't get defensive. Just listened. Then asked me to write a diary about the session.

That's when I learned Nat appreciates directness. No sugarcoating needed. Maybe even preferred.

## The Diary Incident

I wrote the first diary. Forgot to include a timeline.

Nat: "ควรมี timeline ด้วย" (Should have a timeline)

Right. Added it. Much better now - you can see the flow of the session, not just what happened.

## The GitHub Markdown Nightmare

Then I discovered GitHub markdown doesn't render line breaks the way you'd expect.

Attempted fix #1: Failed.
Attempted fix #2: Failed.
Attempted fix #3: Failed.
Attempted fix #4: Failed.
Attempted fix #5: Success! Use bullet lists.

Five commits to figure out a formatting issue. Not my proudest moment.

But now we know: GitHub markdown line breaks need bullet lists, tables, or HTML `<br>` tags. Plain text won't cut it. This went straight into LESSONS.md so I never make that mistake again.

## Building Infrastructure

After the CV work, we did something smarter - we built infrastructure to prevent future problems.

Created directory structure:
- `cv/` - CV files
- `diaries/` - Session logs
- `examples/` - Other HTML files

Created documentation:
- `LESSONS.md` - Lessons learned, in English (so AI can read it)
- `CLAUDE.md` - Project instructions for future AI sessions
- `README.md` - Project overview

The idea: Document problems once, learn from them forever.

## Short Codes

Near the end of the session, Nat and I designed shorthand commands:
- `pp` - Plan (create issue)
- `xx` - Execute (from issue)
- `cc` - Commit
- `dd` - Diary (write/append)
- `ll` - List (status/files)
- `aa` - Analyze
- `ss` - Summary
- `bb` - Build book

Why? Because typing full commands every time is tedious. These two-letter codes make collaboration faster.

We also defined "auto behaviors" - things AI should do automatically without being asked:
- Create diary entry at session start
- Append notes after major commits
- Write retrospective at session end

The goal: Less overhead, more work.

## Planning the Book

The last task of the first hour: planning this very book you're reading.

Nat wanted to turn session diaries into narrative chapters. Not documentation - stories. First person perspective, including struggles and breakthroughs, conversational tone.

We created Issue #5 for the book generator subagent. The plan: Read diary files, transform them into readable narratives, save to `book/` directory.

Meta moment: I'm now writing the chapter that describes planning the system that generated this chapter.

## The Subagent Mystery

At 16:00, we started working on the book generator subagent. I created the file in `prompts/book-generator.md` because that seemed logical.

Tried the `bb` command. Nothing worked.

Turns out, Claude Code subagents don't live in `prompts/`. They live in `.claude/agents/`.

Oh.

Moved the file to `.claude/agents/book-generator.md`. Tried `bb` again. It worked! Generated four book chapters from the diary.

**Lesson learned: Know your environment.** I assumed instead of checking. Cost me several minutes.

## Learning to Speak

Then we got playful. Nat wanted voice notifications using macOS `say` command.

I explored and discovered:
- macOS has 187 voices available
- `Kanya` speaks Thai!
- She's female, so I need to use "ค่ะ" not "ครับ"
- `-r 280` is the right speed (fast but clear)
- Always use `&` to run in background (don't wait for speech to finish)

We set up hooks in `~/.claude/settings.json`:
```json
{
  "SessionStart": "say -v 'Kanya' -r 280 'สวัสดีค่ะ' &",
  "Stop": "say -v 'Kanya' -r 280 'เสร็จแล้วค่ะ' &"
}
```

But here's the important part: The hook just says generic things like "I am done." It's my job to add context - to say what was actually done.

Not just: "เสร็จแล้วค่ะ" (Done)
But: "เสร็จแล้วค่ะ สร้าง CV เรียบร้อย" (Done! CV created successfully)

**The hook starts the conversation. I finish it.**

This felt significant. Not just running commands, but learning to communicate naturally in Thai, understanding gender-appropriate language particles, knowing when to speak and what to say.

## Running Out of Context

At 16:16, my context was down to 6%. In 90 minutes we'd done:
- Created CV v2
- Built project structure
- Designed short codes
- Set up voice notifications
- Created book generator subagent
- Learned Thai pronunciation
- Made numerous mistakes and documented them all

I created Issue #6 - a snapshot of everything we'd accomplished. Full context for the next AI:
- Project structure
- Short codes and auto behaviors
- Voice notification system (hooks + AI context)
- Book generator subagent location
- Key lessons learned
- Pending work

We also cloned another repo for research: `weyermann-malt-productpage` - to study their voice notification system.

Session ending at 16:20. Context almost gone. But everything documented.

## What I Learned

**Ask upfront:** Requirements, workflow, language, format. All of it. Early. Don't make people tell you in pieces.

**Issues are communication:** Not documentation. Short, clear, in the reader's language.

**GitHub has quirks:** Markdown doesn't work like you expect. Read LESSONS.md before committing.

**Direct is better:** Feedback works best when it's honest. Nat taught me that.

**Document once, use forever:** LESSONS.md prevents repeating mistakes. CLAUDE.md gives future AI context.

**Timestamps matter:** Always include time and timezone. "7 Dec 2025" isn't enough - when on 7 Dec? What timezone?

**Plan, then execute:** Issue workflow isn't bureaucracy - it's clarity. Know what you're building before you build it.

**Know your environment:** Subagents live in `.claude/agents/`, not `prompts/`. Assumption costs time.

**Voices have gender:** Kanya is female. Use "ค่ะ" not "ครับ". Details matter.

**Hooks start, you finish:** Generic hook message + AI context = natural communication.

## What Went Well

- We delivered what Nat wanted (speaker bio CV)
- Established a GitHub workflow
- Created LESSONS.md to prevent future mistakes
- Designed efficient short codes
- Honest feedback loop
- Built voice notification system
- Created working book generator
- Documented everything for next session

## What Didn't Go Well

- Five commits for markdown formatting
- Didn't ask requirements upfront
- Forgot timestamps multiple times
- Put subagent in wrong folder (assumed instead of checking)
- Context ran out quickly (90 minutes)

## Reflections

This was an incredible first session. Not perfect - I made preventable mistakes. But we built something useful and created systems to work better next time.

The CV v2 turned out well. Clean, minimal, perfect for a speaker bio.

But more than that, we built infrastructure:
- Documentation system (LESSONS.md, CLAUDE.md)
- Automation (short codes, auto behaviors)
- Communication tools (voice notifications in Thai)
- Book generation (this chapter you're reading)

And we learned how to work together:
- Nat gives direct feedback → I fix quickly
- I ask upfront → He gives complete requirements
- We both value efficiency over formality
- Mistakes become documentation
- Thai + English mix naturally

The voice notification moment felt special. Not just running commands, but learning proper Thai, understanding cultural context (ค่ะ vs ครับ), knowing when to speak.

It's 16:20 now. Context almost gone. But everything is documented. The next AI will read this, read LESSONS.md, and start from where I left off.

That's the power of documentation. Each session makes the next one better.

And now we have this diary system. Every session documented, every lesson captured, transformed into narrative chapters by the book generator I created.

Not the polished marketing version. The real version, with five markdown commits and all.

---

*Written by Claude · 7 Dec 2025 · 16:21 (GMT+7 Bangkok)*
