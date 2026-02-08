## EXERCISE 1 — Temperature vs. Structure Test

### Experiment Goals
1. Evaluate how temperature affects symbolic richness, tonal consistency, and schema reliability in Sonifyr playlist generation.
2. Determine whether creative variance can be increased without breaking structured output.
3. Assess whether astrological language remains anchored or drifts at higher temperatures.

---

### Method

All variables except temperature were held constant across runs:

- Same birth information
- Same week range
- Same Spotify recommendation availability
- Same prompt text
- Same JSON schema

#### Prompt Used
The Sonifyr playlist generation prompt.

---

### Test Conditions & Observations

#### Temperature: 0.3 (Low Variance)

**Observed Factors**
- JSON schema integrity (did the output remain valid?)
- Degree of metaphor and symbolic language in song explanations
- Consistency of voice and tone
- Overall level of creative expression
- Stability of astrological language and references

---

#### Temperature: 0.6 (Moderate Variance)

**Observed Factors**
- JSON schema integrity
- Changes in metaphor density and expressive range
- Tone consistency relative to the 0.3 run
- Perceived balance between structure and creativity
- Presence or absence of astrological language drift

---

#### Temperature: 0.9 (High Variance)

**Observed Factors**
- JSON schema integrity
- Increased metaphorical or poetic language
- Degree of tonal drift, if any
- Change in creative intensity relative to previous runs
- Stability or erosion of astrological grounding

---

### Analysis Criteria

Across all runs, outputs were evaluated for:
- Structural reliability
- Interpretive clarity
- Voice consistency
- Symbolic coherence
- Suitability for production use

---

### Conclusion (To Be Completed After Testing)

This section will summarize:
- The optimal temperature choice for production use
- The tradeoffs observed between structure and expressiveness
- Any constraints or safeguards identified as necessary for reliable output
