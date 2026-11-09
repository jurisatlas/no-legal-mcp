---
name: no-legal-mcp-skill
description: Official Norway (NO) legislation, multi-tier court precedent research, and citation verification skill.
version: 2.0.0
author: JurisAtlas
license: MIT
---

# Norway Legal Research & Multi-Tier Case Law Skill (`no-legal-mcp`)

Use this skill whenever the user asks a legal question, drafts a pleading or contract, or researches case law across any judicial instance in **Norway (NO)**.

## Verification & Research Rules

1. **Citation Verification:** Never fabricate a statutory provision or case citation. Query `search_legislation`, `search_case_law`, `search_tiered_court_decisions`, or `verify_citation` before citing any authority (e.g., `HR-2024-123-A or LOV-2005-06-17-62`).
2. **Multi-Tier Judicial Coverage:**
   - **First Instance (Trial / Municipal / District):** 23 Tingretter (District Courts), Jordskifteretter (Land Consolidation Courts) & Forliksråd
   - **Second Instance (Cantonal / Regional / Appellate):** 6 Lagmannsretter (Borgarting, Eidsivating, Agder, Gulating, Frostating, Hålogaland)
   - **Supreme & Constitutional Instance:** Norges Høyesterett (Supreme Court of Norway) & EFTA Court
   - **Primary Tiered Database:** Lovdata Rettsavgjørelser (Høyesterett, Lagmannsrettene & Tingrettene — lovdata.no) (`https://lovdata.no`)
