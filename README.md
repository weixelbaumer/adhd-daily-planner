# ADHD Daily Planner 📝🧠

**Bullet Journal Style Planning for the ADHD Brain**  
*"Time-blindness friendly. Migration supported. Dopamine optimized."*

## What This Does

A BuJo-style planner designed specifically for ADHD brains:
- 📝 **Rapid logging** with visual symbols
- ⏰ **No absolute times** - relative time markers only
- 🔄 **Task migration** - unfinished tasks carry forward (not failure!)
- 🎯 **Daily ONE thing** - morning intent setting
- 🌙 **Evening reflection** - learn what works
- 🏊 **Swim lanes** - context-based, not time-based
- 🧠 **Dopamine Menu** - built-in rewards

## Quick Start

```bash
./scripts/plan.sh today    # View today's swim lanes
./scripts/plan.sh plan     # Morning planning
./scripts/plan.sh reflect  # Evening reflection
./scripts/plan.sh migrate  # Carry tasks forward
```

## Commands

| Command | Description |
|---------|-------------|
| `/adhd-planner today` | View today's swim lanes |
| `/adhd-planner plan` | Morning intent + rapid log |
| `/adhd-planner reflect` | Evening reflection |
| `/adhd-planner migrate` | Migrate unfinished tasks |
| `/adhd-planner log [task]` | Quick add task |
| `/adhd-planner done [task]` | Mark complete |

## Key Symbols

| Symbol | Meaning |
|--------|---------|
| `•` | Task |
| `×` | Completed |
| `>` | Migrated (tomorrow) |
| `<` | Scheduled (future date) |
| `★` | Today's ONE thing |
| `☆` | If-energy (nice to have) |
| `💀` | Dread task |

## Swim Lanes (Not Time Blocks!)

```
🎯 MUST HAPPEN - Today's ONE thing
🔥 HIGH ENERGY - Deep work, creative
💧 MEDIUM ENERGY - Standard tasks  
❄️ LOW ENERGY - Admin, easy wins
🚫 NOT TODAY - Deferred
```

## Migration = Success

Moving tasks forward is **strategy, not failure**.

- `>` Moved to tomorrow
- `<` Scheduled for specific date
- ~~struck through~~ Dropped (not happening)

## Daily Workflow

1. **Morning** `/adhd-planner plan`
   - Set ONE thing that must happen
   - Rapid log everything
   - Sort into swim lanes
   - Pick dopamine rewards

2. **Day** `/adhd-planner today`
   - Work from appropriate swim lane
   - No rigid times - match your energy
   - Use body doubling for hard tasks

3. **Evening** `/adhd-planner reflect`
   - List wins
   - Note what worked/didn't
   - Migrate unfinished tasks
   - One lesson for tomorrow

## Integration

Works great with `adhd-body-doubling`:
```
/plan → Get your ONE thing
/body-doubling start 50 → Work on it
/reflect → Learn from the day
```

## File Structure

```
~/.openclaw/skills/adhd-daily-planner/
├── daily/YYYY-MM-DD.md
├── monthly/YYYY-MM.md
├── collections/
└── templates/
```

---

*Part of ADHD-founder.com - German Engineering for the ADHD Brain*
