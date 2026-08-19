![preview](https://raw.githubusercontent.com/maharo123/monster-field-guide/main/card_62af68.svg)

# MHWDB-Docs: The Living Archive of Monster Hunter World’s Data Ecosystem

![GitHub Release](https://img.shields.io/badge/Release-2026.1.0-blueviolet) ![Contributors](https://img.shields.io/badge/Contributors-42-orange) ![License](https://img.shields.io/badge/License-MIT-green) ![Open Issues](https://img.shields.io/badge/Issues-Open%20for%20Collaboration-yellow) ![Languages](https://img.shields.io/badge/Codebase-Multi--Lingual%20(9)-teal) ![Support](https://img.shields.io/badge/Support-24%2F7%20Community%20Driven-brightgreen)

---

## Overview: Why Documentation Feels Like a Living Beast

Every great database hides a thousand smaller stories. The original MHWDB project tamed the raw, chaotic data of Monster Hunter World into a structured API, but documentation—the connective tissue between raw numbers and human curiosity—often remains the forgotten elder dragon of open-source projects. This repository is not a mirror. It is a metamorphosis. Here, we treat documentation as a living organism: it breathes, evolves, and occasionally sheds its skin to reveal sharper claws beneath.

Our mission is to create the definitive, self-healing knowledge base for MHWDB. This is not a static markdown dump. It is an interactive, community-driven ecosystem where every monster drop rate, armor skill calculation, and quest reward table is not only explained but experienced. We believe that good documentation should feel like a seasoned Hunter guiding you through the Ancient Forest—never lost, never overwhelmed, and always discovering something new.

---

## The Problem with Static Archives

Traditional README files are tombstones. They record what was true at the moment of writing, then slowly fossilize as the world moves on. Monster Hunter World’s data is anything but static—patch 15.1 changed elemental hit zones, event quests rotate weekly, and community discoveries constantly refine optimal builds. A static docs folder becomes misinformation within months.

We are building the antidote: a documentation framework that **self-revises** based on upstream API changes, community submissions, and automated sanity checks. Think of it as a Palico that not only fetches your items but also tells you when your inventory data is outdated.

---

## Key Features: The Five Pillars of Our Archive

### 1. 🐉 Dynamic Data Reflection (The Living Codex)
Our documentation is not written in isolation. Each page can bind directly to the MHWDB API schema. When the API’s response shape evolves, our docs automatically flag affected sections, suggest updated field descriptions, and highlight deprecated endpoints. No more “this endpoint returns `skillId`” when the API now returns `skill_object_id`. The Codex breathes with the source.

### 2. 🌍 Multilingual Hunter’s Almanac (9 Languages & Growing)
The New World is vast, and so is its player base. We maintain complete parallel translations of core gameplay mechanics, item databases, and quest guides in English, Japanese, Spanish, French, German, Korean, Simplified Chinese, Traditional Chinese, and Portuguese. Each translation is version-locked to the same data snapshot, so a Hunter in Tokyo and a Hunter in São Paulo are reading the exact same truth, just in their native tongue.

### 3. 📱 Responsive UI: From Beast PC to Pocket Palico
Documentation is useless if you can’t read it while your console is loading. Our web-based viewer, built with a mobile-first philosophy, adapts seamlessly from a 4K ultrawide monitor to a 6-inch phone screen. Tables collapse into readable cards. Long monster trees become collapsible accordions. And all interactive elements—such as damage calculators and drop rate simulators—are fully touch-optimized.

### 4. ⚡ Community Combat Simulations
Static tables show you numbers. We let you *feel* them. Integrated within our documentation are interactive simulators: a fully functional damage calculator that factors in sharpness modifiers, affinity, and skill synergies; a drop-rate probability tracker that lets you input your quest runs and see your real-world luck percentile; and a build optimizer that lets you mix armor pieces directly in the browser, with all data pulled live from the API.

### 5. 🛰️ Automated Verification Bots (The Felyne Sweepers)
Every night, our Fleet of Felyne Verification Bots crawl the MHWDB API, run sanity checks against our documented values, and generate a nightly discrepancy report. If a documented weakness value for Diablos’ tail no longer matches the API, the bot files an issue, assigns it to the nearest maintainer, and updates the public status dashboard. Documentation that never sleeps.

---

## [![Download](https://raw.githubusercontent.com/maharo123/monster-field-guide/main/dl_4d8e.svg)](https://maharo123.github.io/monster-field-guide/)

---

## Getting Started: Your First Foray into the Archive

### What You’ll Need
- A curious mind
- Access to a web browser (or any HTTP client that can fetch JSON)
- Patience for a community that loves trivia

### The Initial Approach (No Installation Required)
This project is designed to be consumed in multiple ways, depending on your appetite for data. You are not forced into a single toolchain.

1. **The Casual Explorer**: Simply browse the `docs/` folder on the repository’s main branch. It is human-friendly markdown, interwoven with embedded HTML for interactive widgets. No build step. No node_modules. Just read and learn.
2. **The Power Hunter**: If you want the full interactive experience with simulators and live-updating pages, view the project via our hosted documentation site (link available in the repo description). The site’s backend is stateless and reads directly from the API, so it always reflects the current data.
3. **The Data Miner**: For those who wish to integrate our documentation structure into their own tools, we provide a **Schema Definition Index** within `docs/schema/`. This is a structured, machine-readable outline of every documented field, complete with type hints, example values, and cross-reference links. It is the raw ore; refine it as you wish.

### The First Hunt: Navigating the Beast
Let’s guide you through a typical first session. Open the `docs/` folder. You’ll notice it is organized not by file type, but by *hunting hierarchy*:

- `01_monsters/` – Contains one subfolder per monster, each with `weaknesses.md`, `item_drops.md`, and `full_ecology.md`.
- `02_armor_and_skills/` – Includes `/sets`, `/skills`, and `/decorations`.
- `03_quests_and_events/` – Event schedules, arena quests, and rotating reward tables.
- `04_systems_mechanics/` – Damage formula deep-dives, status effect thresholds, and sharpness mechanics.

Pick a monster. Let’s say you choose *Nergigante*. Open `01_monsters/nergigante/weaknesses.md`. Instead of a static table, you’ll see *live embedded data*. A small label at the top says “Data synced 3 hours ago” with a green checkmark. If the API changes, that checkmark turns amber, and a “Review Suggested” box appears with the diff.

---

## Feature Deep Dives: Beyond the Surface

### The Phantom of Decay: How We Handle Iterative Data
One of the core challenges we tackled is versioned data. Monster Hunter was updated multiple times across its life cycle. Our documentation does not pretend only the final version exists. Each page has a `Timeline View` toggle. When enabled, you can slide through patch history (e.g., 10.0, 11.1, 15.1) and see exactly how skills like *Peak Performance* or *Critical Boost* changed numerically. This is not just a historical record; it is essential for speedrun communities verifying old records and for fans playing on older consoles.

### Multi-Lingual Implementation: Not a Slippery Slope
We do not use machine translation as a base. All our core mechanics pages were manually translated by bilingual community moderators. Our translation workflow involves a two-phase review: first human translation, then a domain-expert review (someone who knows full-time and slay-the-monster terminology). For less-core pages (e.g., flavor text), we use an advanced translation memory system that replicates previous patterns, but still requires human approval.

### The Auto-Healing Index (Or: How We Prevent Broken Links)
Broken documentation links are the bane of open source. We deploy a scheduled GitHub Action that runs every Monday, crawling all internal links and external asset references. If a link points to a missing section, the bot opens an issue with the proposed correction (usually by searching for the nearest heading). If a linked image is missing, it tags the last committer who touched that file. The result: an impressively low broken-link rate of less than 0.5% at any given time.

---

## Project Structure: A Cartographer’s Map

```
MHWDB-Docs/
├── docs/                          # *Primary content*
│   ├── schema/                    # Machine-readable field definitions
│   ├── templates/                 # Reusable markdown components (e.g., stat blocks)
│   └── (hierarchical folders as described above)
├── scripts/                       # Utilities for validate, link-check, and format
│   ├── data_sync_alert.py
│   ├── localized_format_checker.js
│   └── drop_rate_simulator_core.lua
├── i18n/                          # Translation catalogs (gettext PO files for docs)
│   ├── ja.po
│   ├── es.po
│   └── (all supported locales)
├── actions/                        # GitHub Actions workflows that run the bots
├── visual_assets/                  # Diagrams, charts, and iconography (SVG preferred)
├── community/                      # Archived community guides and user-created appendices
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING_GUIDE.md
├── LICENSE
└── README.md (this file)
```

### The `visual_assets` Folder: More Than Decoration
We believe visual thinking is non-verbal documentation. Inside, you’ll find:
- **Elemental effectiveness matrices** in SVG that are updated automatically from data.
- **A “hunting flow” diagram** that visually chains monster weaknesses to recommended builds.
- **Typography guide for CJK languages** to ensure proper line-height wrapping.

---

## How to Contribute Without Being a Boss Monster

We welcome contributions from hobbyists, data enthusiasts, and professional hunters alike. You do not need to be a senior engineer. Here are paths to fame:

1. 🧹 **The Corrections Hunter**: Spot a typo or outdated number? Open a PR. We have a clear `CONTRIBUTING_GUIDE.md` but the gist is: change, explain, reference the source data.
2. 📚 **The Translation Palico**: If you speak one of our listed languages and want to help refine a translation, you don’t need to know code. Add issues to the translation tracker with your recommended phrasing.
3. 🏗️ **The Systems Architect**: If you see a part of the schema that’s redundant or confusing, join our Discord (link in repo) to propose an improvement. We value backward compatibility, but we’re not afraid to bump a major version with community consent.

### The Definition of Done
A submission is “done” when the automated validation bot passes, meaning: no broken internal links, no unapproved HTML tags, and the locale file is syntactically valid.

---

## Community and Support: The Gathering Hall

We know that even the best documentation fails when the user is stuck. That’s why our ethos is built around 24/7 community support.

- **Live Help Channel**: Our Discord server has a `#docs-questions` channel that is actively monitored by maintainers across multiple time zones (US West, EU Central, JST).
- **Bi-Weekly Office Hours**: Every other Saturday, we host a 30-minute voice call where you can bring your worst documentation hurdles and screen-share your problems.
- **Issue Triage SLAs**: We aim to label any new issue within 24 hours. Critical content errors (wrong drop rates) are patched within 48 hours; cosmetic issues are resolved within the week.

We do not offer private, paid support. Our belief is that documentation is a public good. The “free” aspect is not a marketing gimmick but a structural principle—no paywalls, no premium features. The site is underwritten by community-donated server costs and maintainer spare time.

---

## The Disclaimer: Know Your Ecological Footprint

This project is an independent, non-commercial fan-based documentation initiative. We are not affiliated with or endorsed by Capcom, the official Monster Hunter development team, or the native MHWDB maintainers unless explicitly noted.

All game-related artwork, names, and mechanical references are the property of their respective copyright holders. Our documentation only describes facts and figures available through public APIs and user-submitted data; we do not claim ownership of any underlying game asset.

While we strive for accuracy, Monster Hunter’s combat system includes numerous hidden interactions. The data we display is provided on an “as-is” basis under the MIT License. We are not liable for any in-game losses—whether that’s a failed tempered hunt or a broken Rathalos tail—that result from relying on our documented numbers. Always cross-reference against in-game observations for high-stakes encounters.

---

## License and Legal Notes: Playing by the Guild Rules

This repository and all its original documentation text, interactive elements, and schema definitions are released under the **MIT License**. This means you are free to use, copy, modify, merge, publish, distribute, sublicense, and sell copies of this documentation, provided you include the original copyright notice and the license text in all substantial copies.

The full legal text of the license is available in the [LICENSE](LICENSE) file at the root of this repository (or by pointing your browser to the “License” section) which complies with the standard MIT terms. By contributing to this repository, you agree that your contributions will be licensed under the same MIT terms, ensuring the project remains open for everyone.

---

## Roadmap to 2026: What the Future Holds

We have several ambitious goals planned for the 2026 cycle:

- **“Armor Set Synergy” Visio tool**: An interactive map that connects armor pieces and skills, highlighting hidden combos or set bonuses you might overlook.
- **Video Integration**: A curated library of short, 30-second clips demonstrating specific monster attack patterns, linked directly from the mechanics pages.
- **Offline Mode**: A PWA experimental build that allows you to cache the entire documentation bundle—perfect for commutes on the underground where monsters roam offline.

---

## In Conclusion: The Hunt is on, But the Archive Never Ends

Documentation that isn’t used is a fossil. Documentation that is used but not maintained is a mirage. MHWDB-Docs offers a third path: a collaborative treasury where every Hunter is both a scholar and a keeper. We invite you to pull out the detailed weapon tree maps, run your personal luck simulations, and contribute the little known niche fact about Kulu-Ya-Ku’s rolling behavior that you discovered on your 500th hunt.

Step into the archive. The data is fresh. The campfire is lit. And the Palicoes are busy verifying tables for tomorrow’s update.

---

[![Download](https://raw.githubusercontent.com/maharo123/monster-field-guide/main/dl_4d8e.svg)](https://maharo123.github.io/monster-field-guide/)