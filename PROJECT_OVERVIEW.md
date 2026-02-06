# A Symbolic Interpretation Engine for Astrology

Dark Folio's Horoscopes are created daily by a modern astrology application I designed around the simple premise that astrology isn't a prediction problem, its an interpretation problem.

Astrology is often misunderstood as an attempt to predict events: who you will meet, what will happen next, whether a given day will be “good” or “bad.” Framed this way, it appears fragile and vulnerable to cherry-picking, and disappointment.
But this framing misses what astrology actually is. 

Astrology is not built on uncertain data. It is grounded in one of the most stable and predictable systems humanity has ever known: the movements of celestial bodies.

Planetary motion is mathematically precise. In antiquity, humans learned to track the Sun, Moon, and planets with enough accuracy to mark days, months, and years. From these observations emerged calendars, hours, minutes, and systems of latitude and longitude.

Geometry, navigation, timekeeping, and astronomy all grew from this same root.

Astrology evolved alongside that precision as a cultural and symbolic system, preserving millennia of human experience in an ever-changing, syncretic form.

Dark Folio Horoscopes seek to combine traditional astrological symbolism with contemporary software design to create a stable, trustworthy interpretive system. One that supports reflection, agency, and self-understanding rather than certainty or fate-based claims.

At its core, this project is an experiment in interpretive system design: how to encode symbolic literacy, restraint, and ethical boundaries into an AI-assisted application.

# Design Philosophy

Most astrology apps treat charts as deterministic outputs and users as passive recipients. Dark Folio takes a different approach.

This system is designed to:

➡️ Mediate symbolic knowledge rather than predict outcomes
➡️ Preserve ambiguity where ambiguity is honest
➡️ Treat contradiction as informative, not as an error
➡️ Favor synthesis over isolated placements
➡️ Maintain a consistent interpretive voice across all features

Interpretations are framed as patterns and tensions, not instructions or guarantees. The user remains the primary interpreter of their own experience.

# Technical Approach

Dark Folio separates computation from interpretation:

Astrological calculations (charts, aspects, transits) are handled programmatically

Interpretation is handled by a carefully constrained language model

A centralized prompt system enforces voice, boundaries, and interpretive hierarchy

Runtime controls (e.g. temperature) are tuned per feature for consistency

The application uses:

TypeScript / Node

OpenAI models for language interpretation

Server-side prompt orchestration (not chat-based UX)

A modular feature architecture (daily, natal, synastry, transits)

Prompts are treated as versioned system components rather than ad hoc instructions.

# Features

Released: Daily horoscopes (symbolic, non-predictive)

Released: Personalized daily readings based on natal charts

In-depth natal chart interpretations

Synastry (relationship dynamics) readings

Monthly transit overviews

Notification copy consistent with the core voice

Each feature is designed to feel like part of the same instrument, not a collection of unrelated outputs.

# Who This Is For

Developers interested in AI beyond chatbots

Designers exploring meaning-centered interfaces

Astrologers and symbolic practitioners curious about digital tooling

Anyone experimenting with ethical, reflective AI systems

This project is as much about how interpretation is handled as what is interpreted.

# Status

Dark Folio is under active development and experimentation.
The codebase reflects an evolving understanding of how symbolic systems, software constraints, and human agency can coexist.


