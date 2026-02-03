---
name: adhd-daily-planner
version: 1.0.0
description: Bullet journal style daily planner for ADHD brains. Time-blindness friendly with migration support, rapid logging, and dopamine-friendly design.
homepage: https://adhd-founder.com
author: ADHD-founder.com
license: MIT
keywords: [adhd, planner, bullet-journal, daily, productivity, time-blindness, bujo]
metadata:
  clawdbot:
    emoji: "📝🧠"
    tags: ["adhd", "planner", "bullet-journal", "daily", "productivity", "time-blindness"]
    category: productivity
    requires: {}
    optional:
      persistence: "For task migration and history"
      notifications: "For time reminders"
    examples:
      - "/adhd-planner today"
      - "/adhd-planner plan"
      - "/adhd-planner reflect"
      - "/adhd-planner migrate"
    related_skills: ["adhd-body-doubling"]
---

# ADHD Daily Planner 📝🧠

**Bullet Journal Style Planning for the ADHD Brain**  
*"Time-blindness friendly. Migration supported. Dopamine optimized."*

---

## What This Skill Does

Provides a bullet journal (BuJo) style daily planning system specifically designed for ADHD brains:
- 📝 **Rapid logging** with ADHD-friendly symbols
- ⏰ **Time-blindness protection** (relative times, not absolute)
- 🔄 **Task migration** (carry unfinished tasks forward)
- 🎯 **Daily intent** (morning: "What ONE thing must happen?")
- 🌙 **Evening reflection** ("What worked? What didn't?")
- 🏊 **Swim lane organization** (context-based, not time-based)
- 🧠 **Dopamine Menu** integration (built-in rewards)

---

## Core Philosophy

**"Plans are hypotheses, not promises"**  
**"Migration is success, not failure"**  
**"Relative time > Absolute time"**  
**"Intent > Schedule"**  
**"Swim lanes, not time blocks"**

---

## Why Bullet Journal for ADHD?

Traditional planners fail ADHD brains because:
- ✗ Rigid time slots (we're time-blind)
- ✗ Fixed layouts (we need flexibility)
- ✗ No migration (unfinished = failure)
- ✗ All tasks equal (we can't prioritize)
- ✗ No reflection (we don't learn)

**Bullet Journal works because:**
- ✓ Rapid logging (capture fast, organize later)
- ✓ Symbols (quick visual processing)
- ✓ Migration (unfinished tasks live on)
- ✓ Collections (group by context, not time)
- ✓ Reflection (build self-awareness)

---

## Commands

| Command | Description |
|---------|-------------|
| `/adhd-planner today` | View today's swim lanes and tasks |
| `/adhd-planner plan` | Morning intent setting + rapid log |
| `/adhd-planner reflect` | Evening reflection + what worked |
| `/adhd-planner migrate` | Carry unfinished tasks forward |
| `/adhd-planner log [task]` | Quick add to today's log |
| `/adhd-planner done [task]` | Mark task complete |
| `/adhd-planner dopamine` | Show dopamine menu for rewards |

---

## Bullet Journal Symbols (ADHD-Adapted)

### Core Symbols
| Symbol | Meaning | Usage |
|--------|---------|-------|
| `•` | Task | Anything that needs doing |
| `×` | Completed | Task is DONE (celebrate!) |
| `>` | Migrated | Moved to future (not failure!) |
| `<` | Scheduled | Moved to specific date |
| `–` | Note | Information, not actionable |
| `○` | Event | Happening (meeting, deadline) |
| `★` | Priority | Must happen today |
| `☆` | If-Energy | Nice to have, energy permitting |
| `!` | Urgent | Time-sensitive, do first |
| `?` | Waiting | Blocked, waiting on someone |

### Signifiers (Add to left of symbol)
| Signifier | Meaning |
|-----------|---------|
| `*` | Inspiration/idea worth capturing |
| `!` | Urgent/priority |
| `@` | Location-based (errands, specific place) |
| `$` | Money/revenue impact |
| `💀` | Dread task (needs extra support) |

---

## The Swim Lane System 🏊

Instead of time blocks (which ADHD brains ignore), we use **context-based swim lanes:**

### Default Swim Lanes
```
🎯 MUST HAPPEN (Today's ONE thing)
🔥 HIGH ENERGY (Deep work, creative)
💧 MEDIUM ENERGY (Standard tasks)
❄️ LOW ENERGY (Admin, easy wins)
🚫 NOT TODAY (Captured but deferred)
```

### Custom Swim Lanes You Can Create
- `@calls` - All phone calls
- `@computer` - Desk work only
- `@errands` - Out of house
- `$revenue` - Money-generating activities
- `💀dread` - Tasks you're avoiding

### How Swim Lanes Work
1. **No time slots** - Work in the lane that matches your CURRENT energy
2. **Fluid movement** - Tasks can move between lanes
3. **Context grouping** - Do all calls together, all errands together
4. **Energy matching** - Pick the lane that fits how you feel RIGHT NOW

---

## Daily Workflow

### Morning: `/adhd-planner plan`

```
🌅 DAILY INTENT - [Date]

═══════════════════════════════════════════════════════
🎯 TODAY'S ONE THING
"What ONE thing must happen for today to be a success?"

[User answers - this becomes the ★ priority task]

═══════════════════════════════════════════════════════
🧠 ENERGY CHECK
"How's your energy right now? (1-10)"
"What type of work matches this energy?"

[Suggest swim lane based on energy]

═══════════════════════════════════════════════════════
📝 RAPID LOG - Capture everything:

[User brain dumps everything on their mind]

═══════════════════════════════════════════════════════
🏊 SORT INTO SWIM LANES:

🎯 MUST HAPPEN: ★ [The ONE thing]

🔥 HIGH ENERGY:
  • [Deep work task]
  • [Creative task]

💧 MEDIUM ENERGY:
  • [Standard task]
  • [Another task]

❄️ LOW ENERGY:
  • [Admin task]
  • [Easy email]

🚫 NOT TODAY:
  > [Deferred task]
  > [Future task]

═══════════════════════════════════════════════════════
⚡ DOPAMINE MENU (Today's Rewards):
"What will you do when you complete the ONE thing?"
[Select from dopamine menu]
```

### During Day: `/adhd-planner today`

```
📋 TODAY'S SWIM LANES - [Date]

🎯 MUST HAPPEN: ★ [The ONE thing]
   Status: [In progress / Not started / Blocked]
   Next micro-step: _________

🔥 HIGH ENERGY (Pick if you're feeling sharp):
  • Task A
  • Task B

💧 MEDIUM ENERGY (Default lane):
  • Task C  [○ Event at 2pm]
  • Task D

❄️ LOW ENERGY (For when you're drained):
  • Task E
  • Task F

📊 PROGRESS:
  Completed: X tasks
  Remaining: Y tasks  
  Migrated: Z tasks (not failure!)

═══════════════════════════════════════════════════════
💡 SUGGESTION:
"Your energy is [high/medium/low]. Try the [lane] lane."
"Next micro-step: [specific actionable thing]"
```

### Evening: `/adhd-planner reflect`

```
🌙 EVENING REFLECTION - [Date]

═══════════════════════════════════════════════════════
✅ TODAY'S WINS (List everything completed):
  × [Task 1]
  × [Task 2]
  × [The ONE thing - YES!]

═══════════════════════════════════════════════════════
📊 WHAT WORKED?
"What helped you today?"
  • [Technique/condition 1]
  • [Technique/condition 2]

═══════════════════════════════════════════════════════
📊 WHAT DIDN'T?
"What got in the way?"
  • [Distraction/blocker 1]
  • [Distraction/blocker 2]

═══════════════════════════════════════════════════════
🔄 MIGRATION CHECK:
"Any tasks to carry forward?"

Incomplete tasks:
  • [Task A] → Move to tomorrow? (>) / Future? (<) / Drop? (Delete)
  • [Task B] → Move to tomorrow? (>) / Future? (<) / Drop? (Delete)

═══════════════════════════════════════════════════════
🧠 PATTERN NOTE:
"You completed X/Y tasks. [Pattern observation]"
"Best energy time: [morning/afternoon/evening]"

═══════════════════════════════════════════════════════
🌟 ONE THING FOR TOMORROW:
"What's one thing you'll do differently?"
[Capture for tomorrow's planning]
```

---

## Migration System 🔄

**Migration is not failure. It's adaptation.**

### Daily Migration (Evening)
At day's end, review incomplete tasks:
- `>` Migrated to tomorrow (still relevant, not urgent)
- `<` Scheduled for specific future date
- `×` Completed (during review!)
- ~~strikethrough~~ Dropped (no longer relevant)

### Weekly Migration (Sunday/Monday)
Review the week's migrated tasks:
- Some become this week's priorities
- Some get scheduled to specific days
- Some get dropped (if they're not happening, admit it)

### Monthly Migration
Review month's unfinished items:
- What keeps migrating? (System issue or avoidance?)
- What patterns emerge?
- What swim lanes work best?

### Migration Mindset
```
❌ "I failed to finish this task"
✅ "I'm strategically deferring based on priorities"

❌ "I have too many unfinished tasks"
✅ "I'm maintaining a trusted capture system"

❌ "Migration is procrastination"  
✅ "Migration is intentional prioritization"
```

---

## Time-Blindness Friendly Design ⏰

### No Absolute Times
Instead of: "Email at 9am, Meeting at 10am"  
We use: "Email (morning block), Meeting (when alert)"

### Relative Time Markers
- `🌅 Morning` - First thing
- `☕ Mid-morning` - After coffee/settled
- `🌞 Midday` - Lunch-adjacent
- `🌤️ Afternoon` - Post-lunch energy
- `🌙 Evening` - Winding down
- `🦉 Night` - Night owls only

### Duration Estimates (not timestamps)
- `⚡ 5 min` - Quick win
- `⏱️ 15 min` - Short task
- `🕐 30 min` - Medium task
- `⏳ 60+ min` - Deep work block

### Transition Buffers
```
⚠️ BETWEEN TASKS:
• 5-min buffer (ADHD time blindness needs this)
• "What am I doing next?" reminder
• Location/context check
```

---

## Dopamine Menu Integration 🧠⚡

Built into the planner - not an afterthought:

### Morning: Pick Your Rewards
```
🎁 TODAY'S DOPAMINE MENU:

When I complete the ONE thing:
□ [Reward from user's personal menu]

When I finish a swim lane:
□ [Smaller reward]

If I have a perfect migration day:
□ [Celebration reward]
```

### Default Dopamine Menu
1. **Movement** - Walk, stretch, dance to one song
2. **Sensory** - Coffee, snack, comfy blanket
3. **Social** - Text a friend, check social (timed!)
4. **Creation** - Doodle, play music, organize something
5. **Nature** - Step outside, look at plants/sky
6. **Novelty** - Read something new, watch a short video
7. **Completion** - Check off list (the dopamine of done!)

---

## Monthly Log (Collection)

```
📅 MONTHLY OVERVIEW - [Month Year]

═══════════════════════════════════════════════════════
🎯 MONTHLY THEME/INTENT:
"This month is about: _________"

═══════════════════════════════════════════════════════
📊 PATTERN TRACKING:
| Week | ONE Thing | Completed | Energy | What Worked |
|------|-----------|-----------|--------|-------------|
| W1   |           |           |        |             |
| W2   |           |           |        |             |
| W3   |           |           |        |             |
| W4   |           |           |        |             |

═══════════════════════════════════════════════════════
🔄 RECURRING MIGRATIONS:
Tasks that keep migrating - system issue?
• [Task] - Migrated X times - [Analysis]

═══════════════════════════════════════════════════════
🏆 WINS THIS MONTH:
• [Big accomplishment]
• [Learned something]
• [System improvement]
```

---

## Collections (Custom Lists)

Create custom collections for recurring themes:

### Suggested Collections
- `💀 Dread Tasks` - Things you're avoiding (with micro-steps)
- `💡 Ideas` - Capture without action pressure
- `📚 Reading/Watching` - Media queue
- `🛒 Errands` - Location-based batching
- `$ Revenue Ideas` - Business opportunities
- `🎁 Dopamine Menu` - Personal reward options
- `🤝 Waiting On` - Delegated/outstanding items
- `🧠 Brain Dumps` - Uncategorized capture

---

## File Structure

```
~/.openclaw/skills/adhd-daily-planner/
├── daily/
│   ├── 2026-02-03.md
│   ├── 2026-02-04.md
│   └── ...
├── monthly/
│   ├── 2026-01.md
│   ├── 2026-02.md
│   └── ...
├── collections/
│   ├── dread-tasks.md
│   ├── ideas.md
│   ├── dopamine-menu.md
│   └── ...
├── templates/
│   ├── daily.md
│   ├── monthly.md
│   └── reflection.md
└── history.json (patterns, stats)
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
8. **Weekly review** - Migrate intentionally, not by default

---

## Integration with Body Doubling

Use together for maximum ADHD support:

```
Morning:
  /adhd-planner plan → Get your ONE thing
  
During day:
  /body-doubling start 50 → Work on ONE thing
  
Stuck?
  /body-doubling stuck → Micro-task breakdown
  
Evening:
  /body-doubling done → Session autopsy
  /adhd-planner reflect → Daily reflection
  /adhd-planner migrate → Carry forward
```

---

## The ADHD-Planner Promise

> "This planner adapts to your brain, not the other way around. Migration is strategy, not failure. Your ONE thing matters more than your todo list."

**No rigid schedules. No time-shaming. Just flexible, dopamine-friendly planning.**

---

*Part of the ADHD-founder.com ecosystem - German Engineering for the ADHD Brain*
