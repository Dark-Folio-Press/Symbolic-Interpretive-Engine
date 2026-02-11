# Sonifyr - Open Source Module

This repository contains the open-source implementation of Sonifyr, a structured generative system that produces astrology-informed weekly playlists within a strict JSON schema.

It is a production-safe experimental module extracted from a larger system currently under development: The Symbolic Interpretation Engine.

### AI-Powered Astrological Playlist Engine

Sonifyr is a structured generative system that translates natal chart data and planetary transits into personalized weekly music playlists.

It combines deterministic astrology calculations with controlled large language model output, enforcing a strict JSON schema to ensure structural reliability while preserving symbolic richness.

### What It Does

Calculates Sun, Moon, and Rising using accurate astronomical data

Injects natal and transit data into a structured prompt

Generates a 7-song weekly playlist

Enforces a strict JSON contract

Optionally enriches songs with Spotify metadata

Prevents song reuse within a rolling window

# Architecture Philosophy

<b>The system separates</b>

- Deterministic computation (ephemerides, natal data, transit math)
- Interpretive generation (LLM-based symbolic narration)
- Structural enforcement (strict JSON contract)
- This separation allows controlled experimentation with temperature and creativity while preserving schema integrity.

<b>What This Is Not</b>

- Not predictive
- Not deterministic
- Not a forecasting engine
- Not storing persistent user identity data

It is a research-grade generative interface for structured symbolic systems.

### Core Design Principle

Creativity is allowed.
Identity is not negotiable.

### The system separates:

- Computation (astrology engine)
- Narration (LLM interpretation)
- Structure (JSON schema)
- Enrichment (Spotify API layer)

Temperature tuning is used as a diagnostic tool to test identity stability under entropy variation.

### Prompt Engineering Focus

This project demonstrates:

- Entropy sensitivity testing
- Schema enforcement under stochastic conditions
- Identity binding across model temperature variation
- Controlled generative architecture
- Output validation for production environments

### Current Status

Temperature sweep completed (0.8 → 0.3).
Astrological identity drift identified.
Data injection reinforcement in progress.
Next step: re-run sweep after identity binding hardening.

### Why This Matters

LLM systems are expressive.
Production systems require discipline.
Sonifyr explores how to balance both.

### Related Links

[Symbolic Interpretation Engine Overview:](https://github.com/Dark-Folio-Press/Symbolic-Interpretive-Engine/blob/main/PROJECT_OVERVIEW.md)

[Live Sonifyr Demo:](https://sonifyr.darkfoliopress.com/) 

[Lab Notes & Experiments:](sonifyr/experiments/lab-note.temperature.md) 

[Dark Folio Press:](https://www.darkfoliopress.com/)




                ┌────────────────────┐
                │   User Birth Data  │
                └──────────┬─────────┘
                           │
                           ▼
                ┌────────────────────┐
                │ Astrology Engine   │
                │ (Sun/Moon/Rising)  │
                └──────────┬─────────┘
                           │
                           ▼
                ┌────────────────────┐
                │ Transit Generator  │
                └──────────┬─────────┘
                           │
                           ▼
                ┌────────────────────┐
                │ Data Injection     │
                │ (Hard Binding)     │
                └──────────┬─────────┘
                           │
                           ▼
                ┌────────────────────┐
                │ Prompt Construction│
                └──────────┬─────────┘
                           │
                           ▼
                ┌────────────────────┐
                │ OpenAI Model       │
                │ (Temperature Tuning)│
                └──────────┬─────────┘
                           │
                           ▼
                ┌────────────────────┐
                │ JSON Schema        │
                │ Validation Layer   │
                └──────────┬─────────┘
                           │
                           ▼
                ┌────────────────────┐
                │ Spotify Enrichment │
                └──────────┬─────────┘
                           │
                           ▼
                ┌────────────────────┐
                │ UI Rendering Layer │
                └────────────────────┘
