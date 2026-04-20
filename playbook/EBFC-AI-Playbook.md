# From Chatbot to Construction Companion
### AI Deployment Playbook · Felipe Engineer-Manriquez · EBFC AI
**Day 2 Closing Keynote · CONSTRUCT 2026** · ebfc.ai

---

```
╔══════════════════════════════════════════════════════════════════════╗
║                                                                      ║
║  THE CORE INSIGHT                                                    ║
║                                                                      ║
║  Build a workspace, not a chat habit.                                ║
║                                                                      ║
║  The problem isn't the model — it's the method. Every time you       ║
║  open a new chat window you start over: re-explain your role,        ║
║  re-paste your project context, edit out the robot-speak.            ║
║                                                                      ║
║  A workspace folder fixes that permanently.                          ║
║  You build it once. The AI reads it every session.                   ║
║  The folder is the system.                                           ║
║                                                                      ║
╚══════════════════════════════════════════════════════════════════════╝
```

---

## Chatbot vs. Workspace — The Difference

```
┌─────────────────────────────────────┬─────────────────────────────────────┐
│  CHATBOT LOOP                       │  WORKSPACE                          │
├─────────────────────────────────────┼─────────────────────────────────────┤
│                                     │                                     │
│  Open new chat                      │  Open workspace                     │
│    → explain your role again        │    → AI already knows your role     │
│    → paste project context again    │    → AI already knows your project  │
│    → get generic answer             │    → AI already knows your tone     │
│    → edit out the robot-speak       │    → first draft sounds like you    │
│    → close tab                      │      wrote it                       │
│                                     │                                     │
│  Repeat every single session.       │  Same model. Better method.         │
│  Forever.                           │  Built once, runs forever.          │
└─────────────────────────────────────┴─────────────────────────────────────┘
```

**Your workspace folder has three files:**

```
your-workspace/
   SKILL.md        <- your role, project context, writing rules
   references/     <- phrases to avoid, patterns that sound robotic
   examples/       <- one good RFI, one clean report, one email that landed
```

---

## Your 4-Step Deployment Plan

```
┌─ STEP 1 · DAY 1 ────────────────────────────────────────────────────┐
│                                                                     │
│  PICK ONE REPETITIVE TASK                                           │
│                                                                     │
│  Start narrow. Find the task that eats 30-60 min/day and produces   │
│  forgettable output — daily reports, RFI responses, coordination    │
│  emails. That's your proving ground.                                │
│                                                                     │
│  -> Must be text-based and currently done by hand                   │
│  -> Daily reports, RFI drafts, meeting recaps                       │
│  -> Subcontractor coordination emails                               │
│  -> Safety observation write-ups                                    │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘

┌─ STEP 2 · DAY 2–3 ──────────────────────────────────────────────────┐
│                                                                     │
│  BUILD YOUR WORKSPACE FOLDER                                        │
│                                                                     │
│  Create a folder — local or cloud — with three files. This is the   │
│  memory you give AI. It turns a generic chatbot into your           │
│  construction companion without re-explaining anything.             │
│                                                                     │
│  -> SKILL.md — your role, project, team, communication tone         │
│  -> references/ — phrases to avoid, patterns that sound robotic     │
│  -> examples/ — one good RFI, one clean report, one email that      │
│                 landed                                              │
│  -> Point your AI tool at this folder once. Done.                   │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘

┌─ STEP 3 · DAY 4–5 ──────────────────────────────────────────────────┐
│                                                                     │
│  BUILD YOUR PROMPT PROCESS AS A .md FILE                            │
│                                                                     │
│  Document the exact steps you follow to get a good output for your  │
│  chosen task. Save it as a Markdown file in your workspace. Now     │
│  anyone on your team can run it in 60 seconds.                      │
│                                                                     │
│  -> Format: Role → Context → Raw Input → Output Format              │
│  -> Name it by task: daily-report.md, rfi-draft.md                  │
│  -> Drop it in your workspace folder — AI reads it automatically    │
│  -> Refine it when outputs need adjustment — the file is the system │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘

┌─ STEP 4 · WEEK 2 → ONGOING ─────────────────────────────────────────┐
│                                                                     │
│  RUN 2 WEEKS, EDIT OUTPUTS, REFINE                                  │
│                                                                     │
│  AI output is a first draft, not a final one. Edit like a           │
│  superintendent reviews a punchlist — inspect the work, then fix    │
│  the .md file so the same mistake doesn't come back.                │
│                                                                     │
│  -> Run your prompt process every day for 2 weeks                   │
│  -> Track your edits — patterns in your fixes = prompt improvements │
│  -> Update SKILL.md with anything you keep having to correct        │
│  -> Share the folder with your team — they inherit your system,     │
│     not your effort                                                 │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘
```

---

## The Workspace Formula — Quick Reference

```
┌──────────────────────┬──────────────────────┬──────────────────────┬──────────────────────┐
│  [1] Start a folder  │  [2] Write your rules│  [3] Add examples    │  [4] Let it work     │
│                      │                      │                      │                      │
│  One place:          │  Save as SKILL.md    │  One good RFI,       │  AI reads the folder │
│  role, project,      │  in the folder       │  one clean report,   │  every session —     │
│  rules               │                      │  one email that      │  no re-explaining    │
│                      │                      │  landed              │                      │
└──────────────────────┴──────────────────────┴──────────────────────┴──────────────────────┘
```

---

## What Your SKILL.md Looks Like

```markdown
# My Construction AI Workspace

## Role
You are a senior construction superintendent with 15 years of field experience.
You write clearly, directly, and specifically. No corporate filler.

## Project Context
Project: [Project Name]  |  Owner: [Owner]  |  GC: [GC Name]
Phase: [Current Phase]   |  Contract: [Contract Type]
Key contacts: [PM Name], [Super Name], [Owner Rep]

## Writing Rules
- Write like you're talking to someone on the jobsite, not in a boardroom
- Use specific numbers, dates, and names — never vague generalities
- Short sentences. Active voice. No "leverage," "synergy," or "optimize."
- If you don't know something, say so — don't make it up

## Output Format
[Describe the format you want: bullet points, paragraphs, email structure, etc.]
```

---

## Prompt Process Template (save as `task-name.md`)

```markdown
# [Task Name] Prompt Process

## When to use
[Describe the situation — "end of each work day", "when an RFI is needed", etc.]

## Steps
1. Open workspace in [your AI tool]
2. Paste this prompt:

---
ROLE: [paste your role from SKILL.md]

CONTEXT: [paste your project context from SKILL.md]

RULES: [paste your writing rules from SKILL.md]

TASK: [describe the specific task]

RAW INPUT:
[paste your field notes / bullet points / voice-to-text here]

OUTPUT FORMAT: [describe what you want back]
---

## What to check before sending
- [ ] Numbers and dates are correct
- [ ] Names and titles are right
- [ ] Tone matches your company's voice
- [ ] Nothing in there you didn't actually mean
```

---

```
┌─────────────────────────────────────────────────────────────────────┐
│                                                                     │
│  Felipe Engineer-Manriquez · Chief Engineer, EBFC AI                │
│  felipe@ebfc.ai · ebfc.ai                                           │
│                                                                     │
│  Follow for more: @FelipeEngineer                                   │
│  Full workspace template: ebfc.ai                                   │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘
```
