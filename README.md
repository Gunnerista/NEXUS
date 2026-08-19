<div align="center">

# NEXUS

**Agent-First Transfer Intelligence Platform**
*Built and operated by L&K Agency*

[**▶ Live Showcase**](https://gunnerista.github.io/NEXUS/) · [About L&K](#about) · [How it works](#how-it-works)

![Status](https://img.shields.io/badge/status-live-brightgreen) ![Markets](https://img.shields.io/badge/markets_scanned-15-blue) ![Locked](https://img.shields.io/badge/predictions_locked-12-blue) ![Resolved](https://img.shields.io/badge/resolved_%26_scored-2-orange)

<img src="assets/overview.png" width="850" alt="NEXUS Platform overview">

</div>

---

## What is NEXUS?

Most football scouting tools tell you **how good a player is**. NEXUS answers a different question — the one an agent actually gets paid for:

> **"Which club, right now, genuinely needs this player and will actually move this window?"**

NEXUS reads live squad gaps, registration rules, and window deadlines across **15 markets in 8 languages**, ranks realistic destinations with evidence attached, and then does something most platforms never dare to do: **it predicts transfer outcomes in advance, locks the prediction, and publicly scores itself when the player signs.**

---

## Modules

### 🗺 League Boards
Pick a league, see only that market: window deadline, registration and foreigner rules, and which clubs have a **verified open need** right now — graded HOT / WARM / DEAD, every claim dated and sourced.

<img src="assets/league-board.png" width="850" alt="League board — MLS view">

### 🔄 Reverse Match
The selling-side engine. Player profile in → ranked destination clubs out, each with a match index, the reasons behind the rank, and an explicit `Verify` flag on anything that could not be confirmed live. Club identities are anonymized while a deal is active.

<img src="assets/reverse-match.png" width="850" alt="Reverse Match — Case #001">

### 🎯 FA Prediction Tracker
For a pool of real, currently unattached free agents, NEXUS predicts the destination league and top-3 clubs — then **locks the prediction with a date**. No retro-editing, ever.

### 📊 Accuracy Scoreboard
When a tracked player signs, the system grades itself:

| Result | Points |
|---|---|
| Exact club in predicted top 3 | **3** |
| Right league, different club | **2** |
| Adjacent / same-tier market | **1** |
| Miss | **0** |

**Sample size, stated first: 2 resolved cases out of 12 locked predictions.**

That is a calibration sample, not a track record, and pretending otherwise would defeat the purpose of building a self-scoring system. The two graded cases so far: one **exact club hit** (P1 predicted, player signed there days later) and one **adjacent-market resolution** (1 pt) — 4 of a possible 6 points.

Read that as evidence the loop runs end to end, not as an accuracy claim. The number becomes a credibility claim at n=20+, not before. Every subsequent case is added whether it scores 3 or 0.

---

## How it works

```mermaid
flowchart LR
    A[Player profile / query] --> B{{NEXUS Engine}}
    C[Local press · 8 languages] --> B
    D[Registration & quota rules] --> B
    E[Proprietary demand signals] --> B
    B --> F[Ranked destinations + evidence]
    B --> G[Locked predictions]
    G --> H[Weekly auto-scan] --> I[Public accuracy score]
```

Three ranking axes, in strict priority order: **league level & guaranteed minutes** → **budget & wage fit** → **position & squad gap verified against this week's news**. A club must clear all three.

Two design principles that make the output trustworthy:

1. **Dated snapshots, not vague claims.** Every board carries an "as of" date; every finding carries a source. What can't be verified gets a flag, not an assertion.
2. **Demand signals over headlines.** A loud injury story doesn't make a club a buyer. NEXUS weighs quiet preparation moves and relationship-level signals above public emergencies — a hierarchy learned and validated on live deals.

> 🔒 **Proprietary core.** Scoring weights, data pipeline, and source integrations are L&K Agency IP and are not published. This repository hosts the public showcase only.

---

## Stack

Single self-contained HTML showcase (zero dependencies, GitHub Pages) on top of an **agentic AI research loop** that performs multilingual press scanning, rule verification, and structured ranking. Private modules (internal console with full deal data, contact-log demand layer, interactive query app) run separately and are not public.

**Roadmap:** interactive private web app — profile in, full analysis out, on demand.

---

## Work with NEXUS

**A club with an open brief** — send the position, the budget band, and your registration constraints. You get back a dated shortlist of clubs and market conditions relevant to that brief, sources attached, unverified items flagged. No retainer to start the conversation.

**An agency or intermediary with a player to place** — send the profile and the fee structure. Reverse Match returns ranked destinations with the reasoning attached, counterparties anonymized while the deal is live.

**An investor or club owner** — L&K's club M&A and sponsorship desks run on the same evidence-first method shown here.

📧 **ikjunj19@gmail.com** — subject line `NEXUS`, plus one line on the brief, is enough to start.

---

## License

© 2026 L&K Agency. All rights reserved — see [LICENSE](LICENSE).

This repository is a **published showcase, not open source.** The presentation layer may be read and referenced; it may not be copied, redistributed, or reused in a derivative product. Scoring weights, source integrations, and the filter pipeline are neither published nor licensed.

---

## About

<a name="about"></a>**L&K Agency** is a sports investment and deal-making agency operating across football club M&A, player placement, sponsorship, and esports — Europe, MENA, Asia, and the Americas.

Designed & operated by **Ikjun Jang** · [GitHub](https://github.com/Gunnerista) · ikjunj19@gmail.com

<sub>© 2026 L&K Agency. Showcase data is compiled from public sources. Club identities in live deal cases are anonymized. Players listed in the FA tracker are publicly unattached free agents; entries describe market conditions and reported interest only — NEXUS does not publish medical, disciplinary, or character assessments of named individuals. Engine internals are proprietary.</sub>
