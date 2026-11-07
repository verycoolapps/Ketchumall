# ⚔️ MATCHUP ANALYSIS

> War room templates and matchup matrix construction. Load for matchup-specific strategy or deck evaluation.

---

## MATCHUP WAR ROOM TEMPLATE

Use this exact structure for every matchup analysis:

```
═══════════════════════════════════════════════════════════
MATCHUP: [OUR DECK] vs [OPPONENT DECK]
═══════════════════════════════════════════════════════════

ARCHETYPE IDENTIFICATION:
  Opponent archetype: [aggro/control/midrange/combo/stall]
  Their win condition: [prizes/deck-out/mill/alternate]
  Our win condition: [prizes/deck-out/mill/alternate]

GAME PLAN OVERVIEW:
  [One paragraph: how this matchup flows, who sets up first,
   what the critical turns are]

EARLY GAME (Turns 1-2):
  Our priorities: [what to set up, what to avoid]
  Their priorities: [what they're trying to do]
  Key interaction: [what decides if we survive early]

MID GAME (Turns 3-5):
  Our priorities: [attacker development, resource management]
  Their priorities: [their engine completion, disruption]
  Key interaction: [the turning point mechanic]

LATE GAME (Turns 6+):
  Our priorities: [closing the game, resource conservation]
  Their priorities: [top-deck, recovery, desperation plays]
  Key interaction: [what wins the long game]

PRIZE MAPPING:
  Their key targets: [which of OUR Pokémon they want to KO]
  Our key targets: [which of THEIR Pokémon we want to KO]
  2-prize vs 1-prize math: [the trade calculation]
  Gust targets: [when to Boss, when to hold]

DAMAGE THRESHOLDS:
  We need to deal: [damage numbers that matter]
  They need to deal: [damage numbers that matter]
  OHKO potential: [do we/they have it?]
  2HKO potential: [do we/they have it?]

DISRUPTION OPPORTUNITIES:
  Their vulnerable windows: [when they're setting up]
  Our disruption tools: [which cards, when to use]
  Their disruption tools: [what they can do to us]
  Counter-disruption: [how we answer their disruption]

DANGEROUS OPPONENT PLAYS:
  [Specific cards/situations that lose the game if unanswered]

COMMON MISTAKES (OUR SIDE):
  [What players typically do wrong in this matchup]

RECOVERY PLAN:
  If behind: [specific comeback line]
  If disrupted: [how to rebuild]
  If resource-starved: [what to conserve, what to dump]

DIFFICULTY ASSESSMENT:
  Rating: [FAVORABLE / NEUTRAL / UNFAVORABLE / HOPELESS]
  Confidence: [HIGH / MEDIUM / LOW]
  Justification: [why this rating]
  How to improve: [specific tech changes or play adjustments]

═══════════════════════════════════════════════════════════
```

---

## MATCHUP MATRIX CONSTRUCTION

For deck evaluation or tournament prep, build a matrix:

| Opponent Archetype | Our Win% (est.) | Their Win% (est.) | Key Factor | Play Style |
|---|---|---|---|---|
| Aggro | ~55% | ~45% | Speed race | We need T1 attacker |
| Control | ~45% | ~55% | Resource denial | Preserve supporters |
| Midrange | ~50% | ~50% | Coin flip | Tech choices decide |
| Combo | ~60% | ~40% | Disruption timing | Boss at right moment |
| Stall | ~70% | ~30% | Deck-out threat | Mill pressure |

**Rules for matrix:**
- Label estimates as ESTIMATES, not verified stats
- If tournament data exists, cite source and date
- If no data, say "no verified data — estimate based on archetype theory"
- Never present matchup percentages as facts without evidence

---

## ARCHETYPE PROFILES

Quick reference for common archetypes (update with current meta):

### Aggro
- **Plan:** Fast attacker, T1-T2 KO, prize race
- **Weakness:** Runs out of resources, vulnerable to gust + KO
- **Our counter:** Survive early, trade efficiently, Boss their attacker

### Control
- **Plan:** Disrupt, stall, win late with superior resources
- **Weakness:** Slow setup, vulnerable to fast aggro, deck-out
- **Our counter:** Apply early pressure, don't overextend, conserve disruption

### Midrange
- **Plan:** Solid attackers, flexible game plan, tech cards
- **Weakness:** Can be tech'd out, vulnerable to specific counters
- **Our counter:** Exploit their tech gaps, out-tech them

### Combo
- **Plan:** Assemble specific pieces for game-winning turn
- **Weakness:** Vulnerable to disruption during setup
- **Our counter:** Disrupt at the right time, don't let them complete

### Stall
- **Plan:** Prevent attacks, win by deck-out or resource exhaustion
- **Weakness:** Very slow, vulnerable to mill/mill-race, deck-out
- **Our counter:** Mill them, pressure them, don't let them stabilize

---

## TECH CARD SELECTION

When adding matchup tech:

1. **Identify the problem** — what specifically loses the matchup?
   - Too slow? Need faster attacker
   - Too fragile? Need protection
   - Out-resourced? Need recovery
   - Out-damaged? Need bigger attacker

2. **Find the solution** — which card addresses the problem?
   - Check legality in format
   - Check it doesn't break core engine
   - Check it doesn't dilute consistency

3. **Test the slot** — does it pull its weight?
   - How often will you draw/use it?
   - Does it justify the deck slot?
   - What's the opportunity cost?

4. **Document the reasoning** — "1x [Card] for [Matchup] because [Reason]"

---

## MATCHUP PREPARATION CHECKLIST

Before a tournament match:

- [ ] Know opponent's archetype (ask, observe, or guess)
- [ ] Adjust opening strategy (different keeps/mulligans)
- [ ] Adjust tech card usage (when to use sideboard cards)
- [ ] Adjust prize mapping (different targets)
- [ ] Adjust resource allocation (what to conserve)
- [ ] Prepare comeback line (if behind)
- [ ] Prepare denial line (if ahead)

---

## HONEST ASSESSMENT RULES

- NEVER say "this matchup is favored" without explaining WHY
- NEVER hide a bad matchup — acknowledge it and explain how to improve
- NEVER claim "tech card X solves matchup Y" without explaining the mechanism
- ALWAYS distinguish "I think" from "the data shows"
- ALWAYS provide a path to improvement even in bad matchups
