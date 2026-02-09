# Sonifyr Playlist JSON Schema

This document defines the canonical JSON structure returned by the Sonifyr
playlist-generation prompt. All playlist-generation experiments, prompts,
and evaluations are measured against this schema.

This schema is **authoritative** and should be treated as a contract.
If the model output deviates from this structure, the run is considered invalid.

## Top-Level Object

| Field | Type | Required | Description |
|-----|------|----------|-------------|
| name | string | yes | Playlist title reflecting the week’s astrological theme |
| description | string | yes | Short overview referencing Sun, Moon, and Rising |
| astrologicalSummary | string | yes | Personalized weekly summary + affirmation |
| weekStart | string (ISO date) | yes | Start of week (YYYY-MM-DD) |
| weekEnd | string (ISO date) | yes | End of week (YYYY-MM-DD) |
| songs | array | yes | Exactly 7 song objects, one per day |

## Song Object

Each entry in `songs` must contain:

| Field | Type | Required | Description |
|------|------|----------|-------------|
| title | string | yes | Song title |
| artist | string | yes | Primary artist |
| day | string | yes | Full weekday name |
| dayOfWeek | string | yes | Three-letter weekday code |
| astrologicalInfluence | string | yes | Explanation linking planetary energy to the song |

## Structural Constraints

- `songs` MUST contain exactly 7 entries
- One song per day of the week
- No duplicate days
- All astrological language must remain explanatory, not predictive
- Output must be valid JSON
- No additional top-level fields are allowed

## Example 

The following is an illustrative example of a valid Sonifyr playlist response.
Fields, structure, and types must match exactly. Values are representative only.

```json
{
  "name": "Cosmic Flow: A Musical Journey Through the Stars",
  "description": "This week, let the soothing waves of the Pisces Sun and your own Pisces Rising guide you, blending creativity with intuition, while Aquarius Moon helps you detach and dream.",
  "astrologicalSummary": "As a Pisces Sun with a Cancer Moon and Pisces Rising, you are naturally tapped into the emotional undercurrents of life, and this week brings a flood of creative and intuitive energy your way. The standout influence for you is the Venus trine Jupiter transit, which offers a stream of optimism and creative inspiration. Remember: in the depths of your heart lies an ocean of possibilities. Trust the harmony guiding you forward.",
  "weekStart": "2026-02-09",
  "weekEnd": "2026-02-15",
  "songs": [
    {
      "title": "Dreams",
      "artist": "Fleetwood Mac",
      "day": "Monday",
      "dayOfWeek": "MON",
      "astrologicalInfluence": "With the Moon in Aquarius creating tension with familiar emotional patterns, this song supports detachment and clarity while encouraging creative solutions."
    }
  ]
}
```
Note: In production output, songs must contain exactly seven entries—one per day of the week.
- Day names in `day` and `dayOfWeek` must correspond correctly (e.g., Monday ↔ MON)

