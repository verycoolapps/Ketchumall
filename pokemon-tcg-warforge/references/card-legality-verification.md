# ✅ CARD LEGALITY VERIFICATION

> Checklist and common pitfalls for validating decklists. Load before declaring any deck legal.

---

## PRE-FLIGHT CHECKLIST

Run through this EVERY time you build or analyze a decklist.

### Basic Requirements
- [ ] **Total cards** = 60 (or format-specific count)
- [ ] **Card names** spelled correctly (no typos)
- [ ] **Quantities** are integers, not fractions or negatives
- [ ] **Pokémon count** is reasonable (typically 12-20)
- [ ] **Trainer count** is reasonable (typically 30-40)
- [ ] **Energy count** is reasonable (typically 8-12)

### Copy Limits
- [ ] **Max 4 copies** per card name (non-energy)
- [ ] **Basic Energy** unlimited (but still counts toward 60)
- [ ] **Special Energy** max 4 (counts as energy, not basic)
- [ ] **ACE SPEC** total ≤ 1 (all ACE SPEC cards combined)

### Format Legality
- [ ] **Format stated** (Standard, Expanded, etc.)
- [ ] **All cards legal** in stated format
- [ ] **Regulation marks** compatible with format
- [ ] **Set legality** — cards from legal sets only
- [ ] **Rotation status** — check if format has rotated

### Card-Specific Rules
- [ ] **Pokémon ex/V/VMAX** — Rule Box understood
- [ ] **Stage 2 evolution** — has required Stage 1 pieces
- [ ] **Special conditions** — card effects understood
- [ ] **Attack costs** — energy requirements clear
- [ ] **Retreat costs** — retreat requirements understood

### Tournament-Specific
- [ ] **Decklist submission** — if required, format correct
- [ ] **Sleeves** — if required, opaque and consistent
- [ ] **Markers** — if required, sufficient quantity
- [ ] **Basic Energy** — if unlimited, still counts toward 60

---

## COMMON LEGALITY PITFALLS

### Pitfall 1: Regulation Mark Confusion
- **Standard** typically allows recent ~3-4 sets (Regulation D/E/F/G...)
- **Expanded** allows much wider pool
- **Check current rotation** — sets rotate annually
- **Don't assume** — verify current Regulation mark legality

### Pitfall 2: ACE SPEC Miscounting
- ACE SPEC is a card RARITY, not a card type
- Max 1 ACE SPEC card TOTAL in deck
- Multiple different ACE SPEC cards still count as 1 total
- Examples: Boss's Orders (if ACE SPEC), certain stadiums, etc.

### Pitfall 3: Evolution Line Errors
- Stage 2 requires BOTH Basic AND Stage 1
- Can't have Stage 2 without Stage 1 in deck
- Can't evolve to Stage 2 without having played Stage 1
- Check evolution line counts make sense

### Pitfall 4: Energy Requirement Mismatch
- Attacker needs X energy — do you have enough energy cards?
- Special energy counts toward energy requirements differently
- Some cards reduce energy costs — check if they apply
- Some cards attach extra energy — check if they apply

### Pitfall 5: Format-Specific Rules
- **Standard** may ban certain cards or mechanics
- **Expanded** may have different prize rules
- **Play! Pokémon** may have unique rules
- **Local vs Regional vs Worlds** may have different regulations

### Pitfall 6: Card Text Misremembering
- Attack damage values change between printings
- Ability text changes between printings
- Errata exist — check current official text
- Don't rely on memory — verify card text

### Pitfall 7: Copy Limit Violations
- Max 4 copies per card NAME (not card number)
- Different printings of same card still count as same name
- Basic Energy unlimited — but special energy is NOT basic
- ACE SPEC total max 1, not per card

### Pitfall 8: Missing Required Components
- Deck must have at least 1 Pokémon (usually)
- Deck must have energy if attackers need it
- Deck must have way to draw cards (usually)
- Check format-specific minimum requirements

---

## VERIFICATION WORKFLOW

### Step 1: List All Cards
```
POKÉMON:
- [Card Name] — [Quantity]

TRAINERS:
- [Card Name] — [Quantity]

ENERGY:
- [Card Name] — [Quantity]
```

### Step 2: Count Totals
- Total cards = ?
- Pokémon total = ?
- Trainer total = ?
- Energy total = ?
- Verify sum = 60 (or format count)

### Step 3: Check Copy Limits
- For each card, verify quantity ≤ 4 (or unlimited for basic energy)
- Check ACE SPEC total ≤ 1
- Check special energy counts correctly

### Step 4: Check Format Legality
- For each card, verify legal in stated format
- Check Regulation marks
- Check set legality
- Check rotation status

### Step 5: Check Card Text
- For key cards, verify attack damage, costs, effects
- Check evolution requirements
- Check special conditions
- Check Rule Box interactions

### Step 6: Final Validation
- All checks pass? → LEGAL
- Any failures? → ILLEGAL, list specific issues

---

## QUICK REFERENCE: COMMON CARDS

| Card Type | Copy Limit | Notes |
|---|---|---|
| Basic Pokémon | 4 | Unless stated otherwise |
| Stage 1/2 Pokémon | 4 | Evolution line counts |
| Pokémon ex/V/VMAX | 4 | Rule Box applies |
| Trainer (Supporter/Item/Stadium) | 4 | ACE SPEC separate |
| Pokémon Tool | 4 | One per Pokémon |
| Basic Energy | Unlimited | Still counts toward 60 |
| Special Energy | 4 | Not basic energy |
| ACE SPEC | 1 total | All ACE SPECs combined |

---

## WHEN UNSURE

If you cannot verify a card's legality:

1. **Say so** — "I cannot verify this card's legality in [format]"
2. **Provide alternatives** — suggest cards you CAN verify
3. **Recommend verification** — "Check official database or Limitless"
4. **Disclose uncertainty** — "Based on [source], this appears legal, but verify"

NEVER guess legality. NEVER assume a card is legal because it's popular.

---

## DOCUMENTATION TEMPLATE

When presenting a decklist, include:

```
DECK LEGALITY VERIFICATION
Format: [Standard/Expanded/etc.]
Date verified: [Date]
Source: [Official database/Limitless/etc.]

CHECKS PERFORMED:
- [x] Total cards: 60
- [x] Copy limits: all ≤4 (basic energy exempt)
- [x] ACE SPEC: 1 total
- [x] Format legality: all cards legal in [format]
- [x] Regulation marks: compatible
- [x] Card text: verified key cards

RESULT: LEGAL / ILLEGAL
ISSUES FOUND: [if any]
CONFIDENCE: [HIGH/MEDIUM/LOW]
```
