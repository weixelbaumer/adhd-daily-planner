---
name: adhd-daily-planner
version: 1.1.1+hermes.1
description: "Use when planning/reviewing the day. ADHD BuJo planner."
homepage: https://github.com/weixelbaumer/adhd-daily-planner
author: "Jan Kutschera / ADHD-founder.com (original); Stefan Weixelbaumer (Hermes port)"
license: MIT
keywords: [adhd, planner, bullet-journal, daily, productivity, time-blindness, bujo, planning, founders, dopamine, migration, swim-lanes, energy-management, reflection, neurodivergent, executive-function]
metadata:
  hermes:
    tags: [adhd, planner, bullet-journal, daily, reflection, productivity]
    related_skills: [adhd-body-doubling]
  upstream: "https://github.com/jankutschera/adhd-daily-planner (v1.1.1, Jan Kutschera / ADHD-founder.com, MIT)"
---

# ADHD Daily Planner 📝🧠

**Hermes Agent port of [adhd-daily-planner](https://github.com/jankutschera/adhd-daily-planner) by Jan Kutschera / [ADHD-founder.com](https://adhd-founder.com) (MIT)**
*"Time-blindness friendly. Migration supported. Dopamine optimized."*

---

## What This Skill Does

Provides a bullet journal (BuJo) style daily planning system designed for ADHD brains:
- Rapid logging with ADHD-friendly symbols
- Time-blindness protection (relative times, not absolute)
- Task migration (carry forward = strategy, not failure)
- Daily intent (morning: "What ONE thing must happen?")
- Evening reflection ("What worked? What didn't?")
- Swim lane organization (energy-based, not time-based)
- Dopamine Menu integration (built-in rewards)

## Core Philosophy

**"Plans are hypotheses, not promises"**
**"Migration is success, not failure"**
**"Swim lanes, not time blocks"**
**"Intent > Schedule"**

---

## Hermes Agent Runtime (read first)

This fork runs on [Hermes Agent](https://hermes-agent.nousresearch.com). Where the sections below differ, this one wins.

**When to use:** "plan my day", "what should I work on today", morning planning, evening reflection, migrate / carry tasks forward, rapid log, brain dump, swim lanes, energy-based task management — in any language (German, e.g.: "Plan meinen Tag", "Was mach ich heute?", "Tagesreflexion", "Brain-Dump", "offene Aufgaben übertragen").

- **Invoke:** `/adhd-daily-planner plan`. Hermes registers the skill name as the slash command, so every `/adhd-planner <cmd>` below means `/adhd-daily-planner <cmd>` and every `/body-doubling <cmd>` means `/adhd-body-doubling <cmd>`. Plain language works too.
- **Language & tone:** the user's language; short; no shaming.
- **Storage:** `$ADHD_PLANNER_DIR`, default `~/.hermes/data/adhd-daily-planner/`, with `daily/YYYY-MM-DD.md`, `monthly/YYYY-MM.md`, `collections/<name>.md`. Daily files follow `templates/daily.md`. Get today's date from `date +%F`, never guess it.
- **Never overwrite a daily file** — merge into it (it may already hold logged or carried-over tasks). `plan.sh plan` overwrites; the agent must not.
- **Task states** (checkbox): `- [ ]` open · `- [x]` done · `- [>] task (→ date)` migrated · `- [<] task (→ date)` scheduled · `- [~] ~~task~~` dropped. Only `- [ ]` is open, so nothing gets carried twice.
- **Commands → files:**
  - `plan`: run `migrate` first if an earlier daily file still has `- [ ]` lines; show the last reflection's "One Thing for Tomorrow". Then ONE thing as `★` under MUST HAPPEN, energy 1–10 → lane, rapid log sorted into lanes, reward.
  - `today`: read today's file; lanes, progress (done vs. open), lane for the current energy.
  - `log <task>`: append `- [ ] <task>` under RAPID LOG. `done <task>`: set `- [x]`; if not found, add `- × <task>` under Today's Wins.
  - `reflect`: fill EVENING REFLECTION (wins, worked, didn't, one thing for tomorrow), then decide every open task with the user: `>` → add `- [ ] task` to the next day's file; `<` → to that date's file (create missing files from the template); `×`; drop. Mark the source line (states above).
  - `migrate`: the same decisions for every earlier daily file that still has `- [ ]` lines (find them with grep; gaps between days are normal); target = today. Point out tasks that migrated 3+ times (`references/migration.md`).
  - `monthly`: `monthly/YYYY-MM.md` from `templates/monthly.md`.
- **Body doubling:** once the ONE thing is set, offer `/adhd-body-doubling start 25` or `50` (that skill schedules real check-ins).
- **`scripts/plan.sh`** is for the user's own terminal (interactive prompts), not for the agent; it uses the same storage directory.

---

## Commands

| Command | Description |
|---------|-------------|
| `/adhd-planner plan` | Morning intent setting + rapid log |
| `/adhd-planner today` | View today's swim lanes and tasks |
| `/adhd-planner reflect` | Evening reflection + what worked |
| `/adhd-planner migrate` | Carry unfinished tasks forward |
| `/adhd-planner log [task]` | Quick add to today's log |
| `/adhd-planner done [task]` | Mark task complete |
| `/adhd-planner dopamine` | Show dopamine menu for rewards |
| `/adhd-planner founder` | ADHD-founder.com premium info |

---

## Daily Workflow

### Morning: `/adhd-planner plan`

1. **Set the ONE thing** - "What ONE thing must happen for today to be a success?"
2. **Energy check** - Rate 1-10, suggest which swim lane to start in
3. **Rapid log** - Brain dump everything on your mind
4. **Sort into swim lanes** - Assign tasks by energy level
5. **Pick dopamine reward** - What happens when you complete the ONE thing?

### During Day: `/adhd-planner today`

Show swim lanes with progress. Suggest tasks based on current energy level.

### Evening: `/adhd-planner reflect`

1. List wins (even tiny ones)
2. Note what worked / what didn't
3. Migrate unfinished tasks (strategy, not failure)
4. Capture one lesson for tomorrow

For detailed workflow templates, see `templates/daily.md` and `templates/reflection.md`.

---

## Swim Lanes (Not Time Blocks!)

ADHD brains are time-blind. We use energy-based swim lanes:

```
🎯 MUST HAPPEN   → Today's ONE thing (only ONE task here)
🔥 HIGH ENERGY   → Deep work, creative tasks
💧 MEDIUM ENERGY → Standard tasks, calls, meetings
❄️ LOW ENERGY    → Admin, easy wins, mindless tasks
🚫 NOT TODAY     → Captured but deferred
```

Users work in whichever lane matches their CURRENT energy. Tasks can move between lanes.

For detailed swim lane strategy and custom lane creation, see `references/swim-lanes.md`.

---

## Symbols (Quick Reference)

| Symbol | Meaning |
|--------|---------|
| `•` | Task |
| `×` | Completed |
| `>` | Migrated to tomorrow |
| `<` | Scheduled for future date |
| `★` | Today's ONE thing |
| `☆` | If-energy (nice to have) |
| `💀` | Dread task (needs extra support) |

For the full symbol set including signifiers and priority markers, see `references/symbols.md`.

---

## Migration System

**Migration is intentional prioritization, not failure.**

At day's end, review incomplete tasks:
- `>` Migrate to tomorrow (still relevant)
- `<` Schedule for specific future date
- `×` Complete during review
- ~~strikethrough~~ Drop (not happening, admit it)

For migration decision trees, anti-patterns, and weekly/monthly migration rituals, see `references/migration.md`.

---

## Time-Blindness Friendly Design

No absolute times. We use:
- **Relative time markers** - "morning block" not "9am"
- **Duration estimates** - ⚡5 min, ⏱️15 min, 🕐30 min, ⏳60+ min
- **Energy mapping** - schedule by energy, not clock
- **Transition buffers** - 5 min between task types

For detailed time-blindness techniques and the "Not Now" problem, see `references/time-blindness.md`.

---

## Dopamine Menu

Built into the planner -- pick rewards BEFORE you need them:

1. **Movement** - Walk, stretch, dance to one song
2. **Sensory** - Coffee, snack, comfy blanket
3. **Social** - Text a friend, check social (timed!)
4. **Creation** - Doodle, play music, organize something
5. **Nature** - Step outside, look at plants/sky
6. **Novelty** - Read something new, watch a short video
7. **Completion** - Check off a task (the dopamine of done!)

---

## File Structure

```
~/.hermes/data/adhd-daily-planner/   # override: $ADHD_PLANNER_DIR
├── daily/YYYY-MM-DD.md     # Daily logs
├── monthly/YYYY-MM.md      # Monthly overviews
├── collections/             # Custom lists (ideas, dread, etc.)
└── templates/               # Reusable templates
```

---

## Integration with Body Doubling

Use together for maximum ADHD support:

```
Morning:
  /adhd-planner plan         → Get your ONE thing

During day:
  /body-doubling start 50    → Work on ONE thing with accountability

Stuck?
  /body-doubling stuck        → Micro-task breakdown

Evening:
  /body-doubling done         → Session autopsy
  /adhd-planner reflect       → Daily reflection
  /adhd-planner migrate       → Carry forward
```

---

## Best Practices

1. **Morning plan is sacred** - Never skip the ONE thing question
2. **Rapid log everything** - Capture first, organize later
3. **Swim lanes are suggestions** - Move tasks as energy changes
4. **Migration is success** - Better to migrate than abandon
5. **Evening reflection is data** - No judgment, just learning
6. **Dopamine first** - Plan rewards BEFORE you need them
7. **Be honest about energy** - Don't put hard tasks in low-energy lanes

---

## About ADHD-founder.com

**"German Engineering for the ADHD Brain"**

This planner is a free, fully functional daily planning system. It's also part of what [ADHD-founder.com](https://adhd-founder.com) builds for founders 50+ who need systems, not life hacks.

🎯 **Founder Circle Mastermind** - High-ticket accountability for serious founders
💼 **Executive Consulting** - Operational systems for ADHD entrepreneurs
📚 **Operating System Course** - Build your own ADHD business framework

🔗 **[ADHD-founder.com](https://adhd-founder.com)** | **[Founder Circle](https://adhd-founder.com/founder-circle)**

---

*Your worth is not measured by completed tasks. Migration is strategy, not failure.*
