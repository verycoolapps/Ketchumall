# 🏗️ DECK BUILDING FRAMEWORK

> The complete 8-step methodology. Load for any deck construction or optimization task.

---

## STEP 1 — DEFINE THE OBJECTIVE

Extract from user input (or ask):

- **Archetype** — what deck concept? (e.g., "Lucario ex control", "Marnie's Grimmsnarl", "Dragapult ex burn")
- **Main attacker** — the card that does the heavy lifting
- **Secondary attacker** — backup win condition
- **Win condition** — prizes, deck-out, mill, alternate KO
- **Playstyle** — aggressive, control, midrange, combo, stall
- **Competitive level** — casual, locals, regionals, worlds
- **Format** — Standard / Expanded / stated
- **Budget** — unlimited or capped
- **Collection** — specific cards owned?

**Output:** One-paragraph objective statement. If user says "build me a Charizard deck" — that's enough to start; make reasonable assumptions and disclose them.

---

## STEP 2 — SELECT THE CORE

Identify the **engine** — the card(s) that make the deck function.

Analyze each core card:
- What does it DO? (draw, search, attack, accelerate, disrupt)
- What does it NEED? (evolution pieces, specific energy, setup turns)
- What does it GIVE UP? (prize liability, bench space, hand cost)

Example core evaluation:
```
Card: Radiant Charizard ex
Role: Main attacker + late-game closer
Needs: 2 fire energy, Charizard line setup
Gives up: 2 prizes when KO'd (ex)
Synergy: Pidgey line for draw, Rare Candy for evolution
```

---

## STEP 3 — BUILD THE ENGINE

Every deck needs these subsystems. Mark which the core provides and which need cards:

| Engine | Purpose | Example cards |
|---|---|---|
| **Draw engine** | Replace cards, find pieces | Pidgey ex, Kirlia, opponents' discard |
| **Search engine** | Find specific cards | Ultra Ball, Professor's Research, Boss's Orders |
| **Energy accel** | Attach faster than 1/turn | Chien-Pao, cards with "attach from discard" |
| **Recovery** | Get resources back | Boss (gust), Itemfinder analogs, etc. |
| **Switching** | Move Active safely | Switch cards, Boss's Orders |
| **Disruption** | Slow opponent | Hand disruption, item denial, status |
| **Defense** | Survive hits | High HP, healing, protection effects |

**Rule:** Every engine slot must have a card assigned or explicitly marked "not needed because [reason]".

---

## STEP 4 — CALCULATE CARD RATIOS

No arbitrary numbers. For each category:

### Pokémon (typically 12-20 cards)
- Main attacker line: 4-8 copies (e.g., 2-2-2 line or 4x single-prize attacker)
- Setup/supporting: 4-8 copies
- Tech/situational: 1-4 copies

### Trainers (typically 30-40 cards)
- Supporters: 12-16 (Professor's Research, Boss's Orders, etc.)
- Items: 8-12 (Ultra Ball, etc.)
- Stadiums: 2-4
- Tools: 0-4
- Special: ACE SPEC max 1 total

### Energy (typically 8-12 cards)
- Match attacker requirements exactly
- Special energy only if effect justifies the slot
- Never run more energy than needed for consistent attacks by turn 2-3

**Every count gets a justification sentence.** "4x Ultra Ball — consistency engine, finds missing evolution pieces and Boss targets; reduced to 3 only if deck has excessive draw already."

---

## STEP 5 — OPTIMIZE CONSISTENCY

Run probability checks (see `probability-engine.md`):

- **Opening hand** — can you see a Basic + a way to evolve/attack?
- **Turn 1 setup** — how often do you get active attacker + energy?
- **First attack timing** — turn 2? 3? What's the deck's speed?
- **Dead cards** — cards that do nothing without specific setup
- **Prize risk** — key cards prized on turn 1 = disaster?

**Consistency targets by deck type:**
- Aggro: T1 attacker 60%+, T2 attack 80%+
- Midrange: T2 setup 70%+, T3 attack 85%+
- Control: T3-4 setup acceptable, resource longevity critical

---

## STEP 6 — BUILD MATCHUP COVERAGE

For each expected matchup, identify:
- Your win condition vs theirs
- Who sets up faster?
- Damage race math (can you OHKO their threats? can they OHKO yours?)
- Disruption opportunities (when to use Boss, when to use hand disruption)
- Weakness exploitation (type advantage = ×2)

**Tech card justification:** Every non-core card must name the matchup it improves.
"1x [Card] — improves matchup vs [archetype] by [mechanism]."

---

## STEP 7 — VALIDATE THE DECK

Checklist:
- [ ] Total = 60 cards (or format-legal count)
- [ ] Max 4 copies per card name (Basic Energy exempt)
- [ ] ACE SPEC total ≤ 1
- [ ] All cards legal in stated format + Regulation mark
- [ ] Energy requirements can be met consistently
- [ ] No card text errors or misremembered effects
- [ ] All evolution lines complete (Basic→Stage1→Stage2 counts make sense)

**Use `card-legality-verification.md` checklist.**

---

## STEP 8 — FINAL OPTIMIZATION

For each card, ask:
1. Is it redundant? (Two cards doing the same job)
2. Does it conflict? (Requires bench space you don't have, energy you can't spare)
3. Is it a dead card? (No effect without specific setup that isn't reliable)
4. Does it reduce consistency? (Cutting it improves opening hands)
5. Does it create unnecessary requirements? (Needs 3 specific pieces to function)
6. Is its strategic value sufficient? (Does the slot pull its weight?)

**Replacement process:** See `output-templates.md` → Replacement tiers.

---

## CARD ROLE CLASSIFICATION

Assign every card exactly one primary role:

| Role | Description | Example |
|---|---|---|
| Main attacker | Primary damage dealer | Charizard ex |
| Secondary attacker | Backup win condition | Small 1-prize attacker |
| Setup | Enables engine | Basic that searches evolution |
| Draw engine | Replaces hand | Pidgey, Kirlia |
| Search engine | Finds specific cards | Ultra Ball, Boss |
| Energy accel | Faster energy attachment | Chien-Pao |
| Recovery | Gets resources back | Itemfinder-type cards |
| Disruption | Slows opponent | Hand disruption, status |
| Protection | Prevents KOs | Healing, switching |
| Mobility | Bench/Active management | Switch cards |
| Utility | Flexible effect | Tech cards |
| Matchup tech | Specific counter | Tech for bad matchup |
| Consistency | Improves opening hands | Rare Candy, quick search |

**A card can have secondary roles but gets ONE primary classification.**
