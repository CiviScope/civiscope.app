# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

CiviScope is building **trustworthy AI for democratic participation**. We're creating AI tools that help people understand and participate in governance—tools that show their work and help people decide, not just algorithms.

**Core mission:** AI should distribute—not concentrate—power.

Key principles:
- **Transparent:** The work is shown, not just results
- **Open:** Open source, open methods
- **Useful:** Built for people making decisions

Starting with decentralized organizations, expanding to any institution making public decisions (councils, legislatures, standards bodies).

## Development Commands

```bash
# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## Tech Stack

- **Framework**: Astro 5.14+ (static site generator)
- **Language**: TypeScript with strict mode enabled (`astro/tsconfigs/strict`)
- **Node**: Uses ES modules (`"type": "module"` in package.json)

## Project Structure

```
src/
├── pages/          # Astro pages (index.astro is main landing page)
├── layouts/        # Layout components (Layout.astro with design tokens)
├── components/     # Reusable components (Mark.astro for logo)
├── data/           # Structured content (references.ts)
└── assets/         # Static assets (if needed)
```

## Design Philosophy

**Target aesthetic:** Anthropic-level seriousness but more minimal, with democratic institution gravitas (UN/civic institution meets Swiss modernism).

**Key characteristics:**
- **Typography as design:** Serif headlines (institutional authority), sans-serif body, monospace for section labels
- **Restrained palette:** Muted civic blue (#2c5282), neutral grays, institutional feel
- **Editorial structure:** Document-like layout with clear sections
- **Visual metaphors:** Concentric circles (transparency/layers), trace line (provenance/connections)
- **Minimal but intentional:** Every element has purpose

**Don't:**
- Add startup-style hero sections or flashy graphics
- Use bright colors or generic blue (#0066cc)
- Create buzzword-heavy copy
- Over-design or add decoration for decoration's sake

## Content Guidelines

**Communication principles:**
1. **Vision over specifics:** Communicate broad direction, not implementation details
2. **Avoid jargon:** No "intermediation", "claims/sources", "first-class citizens"
3. **Avoid buzzwords:** No "transparent, accessible, trustworthy" lists
4. **Be direct:** Short sentences, active voice, concrete language
5. **Show don't tell:** The design itself demonstrates taste and seriousness

**What we don't talk about yet:**
- Specific artifacts like "briefs" (too narrow)
- Implementation details (PROV, IPFS, attestations) except in References
- Laundry lists of contexts (just say "any institution making public decisions")

## Code Organization

**Current patterns:**
- **Data separation:** Content lives in `/src/data/` (e.g., references.ts)
- **Component extraction:** Reusable elements in `/src/components/` (e.g., Mark.astro)
- **CSS organization:** Scoped styles with clear section comments (Layout, Hero, Typography, etc.)
- **Design tokens:** Colors, fonts defined in Layout.astro root CSS variables

**When adding new content:**
1. Structured data should go in `/src/data/` as TypeScript exports
2. Reusable UI should be extracted to components
3. CSS should be organized with section comment headers
4. Build after changes to catch errors early

## Current State

The landing page (`/src/pages/index.astro`) is complete and serves as a demonstration of:
- The team's taste and execution capability
- Clear communication of vision
- Institutional design sensibility
- Clean, maintainable code

The page is intentionally minimal and vision-focused. Core product functionality is not yet implemented.
