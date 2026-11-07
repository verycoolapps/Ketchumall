# 🤖 GPT / PLUGIN INTEGRATION GUIDE

> How to use POKÉMON TCG WARFORGE as a plugin or integration.

---

## PLUGIN MANIFEST

The `plugin.json` file defines this skill as a plugin for compatible systems.

### Supported Systems
- **Claude Skills** — native SKILL.md format
- **GPT Plugins** — manifest + skill structure
- **Custom Agents** — modular reference architecture
- **RAG Systems** — reference files as knowledge base

---

## INSTALLATION

### Option 1: Direct Clone
```bash
git clone https://github.com/verycoolapps/Mr.-Ketchum.git
cd Mr.-Ketchum
```

### Option 2: Copy Skill Folder
```bash
# Copy pokemon-tcg-warforge/ to your skills directory
cp -r pokemon-tcg-warforge ~/.claude/skills/
# or
cp -r pokemon-tcg-warforge ~/.config/agents/skills/
```

### Option 3: Plugin Manager (if supported)
```bash
# Using plugin.json manifest
plugin install pokemon-tcg-warforge
```

---

## ACTIVATION

### Automatic Triggers
The skill activates when users mention:
- "pokemon tcg"
- "pokemon deck"
- "deck building"
- "decklist"
- "pokemon strategy"
- "pokemon tournament"
- "pokemon matchup"
- "pokemon meta"
- "trading card game"
- "card game strategy"

### Manual Invocation
```
/warforge build me a Charizard deck
/warforge analyze this decklist
/warforge what's the current meta
/warforge prepare me for a tournament
```

### Mode Selection
```
/warforge beginner "build me a simple deck"
/warforge competitive "build me a tournament deck"
/warforge doctor "analyze this decklist"
/warforge matchup "Dragapult vs Grimmsnarl"
```

---

## INTEGRATION PATTERNS

### Pattern 1: Standalone Skill
```
User: "Build me a competitive Charizard deck"
→ SKILL.md activates
→ Mode detection: competitive
→ Deck building engine runs
→ Output: complete decklist + strategy + matchups
```

### Pattern 2: Reference Loading
```
User: "What's the probability of opening a Basic?"
→ SKILL.md detects probability question
→ Loads references/probability-engine.md
→ Calculates with hypergeometric formula
→ Output: calculation + interpretation
```

### Pattern 3: Multi-Step Workflow
```
User: "Prepare me for a Regional with Dragapult"
→ SKILL.md detects tournament prep
→ Loads references/tournament-preparation.md
→ Loads references/matchup-analysis.md
→ Generates matchup matrix
→ Outputs: prep plan + matchup notes + checklist
```

### Pattern 4: Iterative Refinement
```
User: "This deck feels inconsistent, help me fix it"
→ SKILL.md detects deck doctor mode
→ Loads references/deck-building-framework.md
→ Analyzes consistency issues
→ Suggests targeted changes
→ Outputs: diagnosis + fixes + expected improvement
```

---

## API INTEGRATION (Custom)

### For Custom Agents
```python
# Pseudo-code for integration
import pokemon_tcg_warforge

# Initialize skill
warforge = PokemonTCGWarforge()

# Build a deck
result = warforge.build_deck(
    archetype="Charizard ex",
    format="Standard",
    mode="competitive",
    budget="flexible"
)

# Analyze matchup
matchup = warforge.analyze_matchup(
    deck_a="Dragapult ex",
    deck_b="Grimmsnarl",
    format="Standard"
)

# Calculate probability
prob = warforge.calculate_probability(
    deck_size=60,
    success_cards=12,
    cards_drawn=10,
    scenario="evolution line by turn 3"
)
```

### For RAG Systems
```python
# Load reference files as knowledge base
references = {
    "fundamentals": load("references/pokemon-tcg-fundamentals.md"),
    "deck_building": load("references/deck-building-framework.md"),
    "strategy": load("references/advanced-strategy.md"),
    "probability": load("references/probability-engine.md"),
    "matchups": load("references/matchup-analysis.md"),
    "tournament": load("references/tournament-preparation.md"),
    "meta": load("references/meta-research-methodology.md"),
    "legality": load("references/card-legality-verification.md"),
    "templates": load("references/output-templates.md")
}

# Query system
response = rag_query(
    question="Build me a competitive deck",
    context=references,
    skill="pokemon-tcg-warforge"
)
```

---

## CUSTOMIZATION

### Adding New References
```bash
# Add custom card database
pokemon-tcg-warforge/references/card-database.json

# Add custom meta data
pokemon-tcg-warforge/references/current-meta.json

# Add custom templates
pokemon-tcg-warforge/references/custom-templates.md
```

### Modifying Modes
Edit `SKILL.md` section 2 to add/modify operating modes:
```markdown
| `custom-mode` | Custom description | Custom focus |
```

### Adding Personas
Edit `SKILL.md` section 1 to add specialist personas:
```markdown
| **G — Custom Specialist** | Custom role | Custom expertise |
```

---

## QUALITY ASSURANCE

### Pre-Deployment Checklist
- [ ] All reference files present and valid
- [ ] SKILL.md sections complete
- [ ] Examples demonstrate quality
- [ ] QA test suite passes
- [ ] plugin.json manifest valid
- [ ] README documentation complete

### Testing
```bash
# Run QA test suite
cat pokemon-tcg-warforge/qa/test-suite.md

# Verify examples
cat pokemon-tcg-warforge/examples/*.md

# Check skill structure
ls -la pokemon-tcg-warforge/
```

---

## TROUBLESHOOTING

### Skill Not Activating
- Check activation triggers in plugin.json
- Verify SKILL.md is in correct location
- Check file permissions

### Missing References
- Verify references/ directory exists
- Check file paths in SKILL.md
- Ensure all .md files are present

### Quality Issues
- Run QA test suite
- Check examples for format issues
- Verify templates are complete

---

## VERSIONING

Current version: **1.0.0**

### Version History
- **1.0.0** — Initial release with 8 examples, 9 references, 10-gate QA

### Future Updates
- Card database integration
- Real-time meta data
- Price tracking
- More examples
- Additional formats

---

## SUPPORT

For issues, feature requests, or contributions:
- GitHub: https://github.com/verycoolapps/Mr.-Ketchum
- Issues: Create GitHub issue
- Discussions: GitHub Discussions

---

## LICENSE

MIT License — see LICENSE file for details.

---

**Plugin Status:** ✅ Production Ready
**Compatibility:** Claude Skills, GPT Plugins, Custom Agents, RAG Systems
**Documentation:** Complete
**Examples:** 8 worked interactions
**References:** 9 deep modules
**QA:** 10-gate test suite
