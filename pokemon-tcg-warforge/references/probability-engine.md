# 📐 PROBABILITY ENGINE

> Mathematical reasoning for Pokémon TCG decisions. Load when calculating odds, consistency, or expected value.

---

## CORE FORMULA — Hypergeometric Distribution

For a deck of $N$ cards with $K$ "success" cards, drawing $n$ cards:

$$P(X = k) = \frac{\binom{K}{k} \binom{N-K}{n-k}}{\binom{N}{n}}$$

$$P(\text{at least one success}) = 1 - \frac{\binom{N-K}{n}}{\binom{N}{n}}$$

**Variables:**
- $N$ = total deck size (typically 60)
- $K$ = number of cards that count as "success"
- $n$ = number of cards observed (opening hand + mulligan considerations)
- $k$ = number of successes wanted

---

## WORKED EXAMPLES

### Example 1: Finding a Basic Pokémon

Deck: 60 cards. You run 8 Basic Pokémon that can start.
Opening hand: 7 cards.

$$P(\text{at least one Basic}) = 1 - \frac{\binom{60-8}{7}}{\binom{60}{7}} = 1 - \frac{\binom{52}{7}}{\binom{60}{7}}$$

$$\approx 1 - 0.352 = 0.648 \approx 65\%$$

**Interpretation:** ~65% chance of opening with at least one playable Basic. Mulligan if you have none (unless format allows bench-stall strategy).

### Example 2: Evolution Line Consistency

You run a 2-2-2 evolution line (2 Basic, 2 Stage 1, 2 Stage 2 = 6 total pieces).
After opening 7 cards, you draw 1 per turn.

- Turn 1: 8 cards seen
- Turn 2: 9 cards seen
- Turn 3: 10 cards seen
- Turn 4: 11 cards seen
- Turn 5: 12 cards seen

$$P(\text{at least one of each stage by turn 5})$$ — requires tracking hypergeometric for EACH stage separately, then combining.

**Simplified approach:** If you run 4 copies of each stage (12 total evolution pieces):
$$P(\text{at least one piece}) = 1 - \frac{\binom{48}{12}}{\binom{60}{12}} \approx 95\%$$

But getting the FULL line (Basic + Stage1 + Stage2) is much harder — typically 40-60% by turn 5 without search assistance.

### Example 3: Energy Accessibility

You run 10 Fire Energy in a 60-card deck.
Need 2 energy on your attacker by turn 2.

- Opening hand: 7 cards → ~1.2 energy expected
- Draw 1 per turn → ~2.2 energy by turn 2
- Attach 1 per turn → 2 energy by turn 3 realistically

$$P(\text{at least 2 energy in opening 7}) = 1 - \frac{\binom{50}{7}}{\binom{60}{7}} - \frac{\binom{10}{1}\binom{50}{6}}{\binom{60}{7}}$$

**Wait — prizes reduce draw.** 6 prizes face-down mean your deck effectively has ~54 unknown cards for draw purposes. Adjust N accordingly.

---

## CRITICAL CAVEATS

### Prize Cards = Hidden Information
6 cards are set aside face-down. You don't know what they are. This means:
- Your effective "unknown deck" is 54 cards, not 60
- Prize cards taken by EITHER player reduce remaining unknowns
- You cannot calculate exact probabilities without knowing prize contents

**Rule:** Always state whether calculation assumes prizes are random or accounts for known prize contents.

### Mulligans & Search Effects
- Mulligan redraws change effective hand size
- Search effects (Ultra Ball, Professor's Research) let you CHOOSE what to keep — this is NOT random draw
- Conditional probabilities apply: "given I found X, probability of Y changes"

**Rule:** Never apply simple hypergeometric when search/draw effects are involved without modeling the selection.

### Draw vs Search
- **Draw** (Pidgey, draw supporters) = random from deck → hypergeometric applies
- **Search** (Ultra Ball, Boss) = you see and choose → NOT hypergeometric; use combinatorics of "how many ways to find what I need"

### Opponent Interaction
- Opponent's deck disruption (discard, mill) changes YOUR probabilities
- Their search/draw affects THEIR consistency, not yours
- Track both when calculating matchup odds

---

## EXPECTED VALUE (EV) FRAMEWORK

For decisions with probabilistic outcomes:

$$EV = \sum_{i=1}^{n} P(\text{outcome}_i) \times \text{value}(\text{outcome}_i)$$

**Example:** Boss's Orders to gust a 2-prize Pokemon vs attacking into their wall.
- P(they KO back and take your attacker) = ~40%
- Value of 2 prizes = high
- P(they don't KO back) = ~60%
- Value of favorable trade = moderate

Compare EV of Boss play vs alternative line. Show the math.

---

## CONSISTENCY TARGETS BY DECK TYPE

| Deck Type | T1 Setup | T2 Attack | T3+ Stability |
|---|---|---|---|
| Hyper-aggro | 70%+ | 85%+ | N/A (game over) |
| Aggro-control | 60%+ | 75%+ | 80%+ |
| Midrange | 50%+ | 65%+ | 85%+ |
| Control | 40%+ | 55%+ | 90%+ |
| Combo | 30%+ | 50%+ | 85%+ |

These are TARGETS, not guarantees. Disclose actual calculated odds vs targets.

---

## COMMUNICATION RULES

1. **Always show the formula** — don't just give the answer
2. **State assumptions** — "assuming 6 random prizes" or "assuming no disruption"
3. **Distinguish theory vs practice** — theoretical odds vs what actually happens in games with search, draw, disruption
4. **Never manufacture precision** — "~65%" not "64.7%" unless calculation supports it
5. **Acknowledge uncertainty** — "this assumes opponent doesn't disrupt; if they do, odds drop significantly"

---

## QUICK REFERENCE TABLE

Common scenarios and typical probabilities (60-card deck, 7-card opening):

| Scenario | Typical Probability |
|---|---|
| At least 1 Basic Pokémon | 60-70% |
| At least 1 evolution piece | 70-80% |
| At least 1 specific card (4x) | ~37% |
| At least 1 specific card (2x) | ~21% |
| At least 2 energy | 50-60% |
| At least 1 supporter | 70-80% |
| Full evolution line by T3 | 40-60% (no search) |
| Full evolution line by T3 (with search) | 75-90% |

*These are approximations — ALWAYS calculate for the specific deck.*
