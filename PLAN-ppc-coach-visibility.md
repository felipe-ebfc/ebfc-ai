# Plan: ebfc.ai Landing Page Update — PPC Coach Visibility

**Date:** March 23, 2026
**Goal:** Evolve ebfc.ai from a single-product waitlist page into an EBFC AI product family page that gives PPC Coach AI visibility while keeping the companion waitlist active.

---

## Current State

- Single-page "coming soon" for EBFC AI companion
- Waitlist form → Google Sheets
- No mention of PPC Coach, Insurance Genie, or any shipped product
- Badge says "Coming Soon" — but we already have live products

**Problem:** We have shipped products (Insurance Genie, PPC Tracker) and PPC Coach AI launching this week, but ebfc.ai tells visitors nothing is live yet. That's leaving value on the table.

---

## Recommendation: Product Family Landing Page

Transform ebfc.ai from a single waitlist into a product showcase with clear CTAs. One page, three sections — visitors immediately see EBFC has real products, not just promises.

### Page Structure

```
┌─────────────────────────────────────────────┐
│  TOPBAR: EBFC AI logo  |  Products | Blog   │
├─────────────────────────────────────────────┤
│                                             │
│  HERO (updated)                             │
│  "AI Tools That Speak Construction"         │
│  Subtitle: Real tools. Built for the field. │
│                                             │
├─────────────────────────────────────────────┤
│                                             │
│  ★ FEATURED: PPC COACH AI (new section)     │
│  "Your PPC is trying to tell you something" │
│  - AI coaching for Last Planner System      │
│  - Trend analysis + variance tracking       │
│  - Skip two Monsters. Get an AI coach.      │
│  [Try Free for 30 Days] → ppc.ebfc.ai      │
│                                             │
├─────────────────────────────────────────────┤
│                                             │
│  PRODUCT GRID (2-3 cards)                   │
│                                             │
│  ┌──────────┐ ┌──────────┐ ┌──────────┐    │
│  │PPC Coach │ │Insurance │ │ EBFC AI  │    │
│  │  $29/mo  │ │  Genie   │ │Companion │    │
│  │   LIVE   │ │   FREE   │ │  BETA    │    │
│  │ [Start]  │ │  [Use]   │ │[Waitlist]│    │
│  └──────────┘ └──────────┘ └──────────┘    │
│                                             │
├─────────────────────────────────────────────┤
│                                             │
│  SOCIAL PROOF / CREDIBILITY                 │
│  Felipe headshot + credentials              │
│  "From the team behind The EBFC Show"       │
│  IGLC research backing (1,526 papers)       │
│                                             │
├─────────────────────────────────────────────┤
│                                             │
│  COMPANION WAITLIST (existing form)         │
│  "The full AI companion is coming"          │
│  [email signup — keep existing flow]        │
│                                             │
├─────────────────────────────────────────────┤
│  FOOTER                                     │
└─────────────────────────────────────────────┘
```

---

## Product Cards

### 1. PPC Coach AI ★ (featured — golden border)
- **Status:** LIVE (or "Launching This Week")
- **Price:** Starting at $29/mo · 30-day free trial
- **Tagline:** "Know which commitments will break before Monday's pull planning meeting."
- **CTA:** "Try Free for 30 Days" → ppc.ebfc.ai
- **Visual:** PPC trend chart icon or mini screenshot

### 2. EBFC AI Companion (coming soon card — slightly dimmed)
~~Insurance Genie removed — Boldt-internal only, not public facing.~~
- **Status:** EARLY ACCESS
- **Tagline:** "Your personal AI that remembers your projects, drafts your emails, preps your meetings."
- **CTA:** "Join the Waitlist" → scroll to form (or inline)
- **Visual:** Chat/brain icon

---

## Copy Direction

### Hero
- **Before:** "The AI That Speaks Construction"
- **After:** "AI Tools That Speak Construction"
- **Sub:** "Real products. Built by a 30-year PM. Backed by 1,526 IGLC research papers."

### PPC Coach Feature Section
Use the Monster Energy pricing anchor from the PRD:
> "Less than two energy drinks a week. More insight than a month of spreadsheets."

Lean into the pain point:
> "You already track PPC. But does your spreadsheet tell you which commitments will break next week?"

### Badge
- **Before:** "Coming Soon"
- **After:** "Products Live" or remove badge entirely

---

## Technical Approach

**Keep it simple — still a single index.html.** No framework needed for a landing page.

Changes:
1. Update hero text + badge
2. Add featured PPC Coach section (new HTML block with golden accent)
3. Add product grid (3 cards with flexbox/grid)
4. Move waitlist form to bottom section (companion-specific)
5. Update meta tags (og:title, og:description) for SEO
6. Update footer: remove "Coming Soon," add product links

**Estimated effort:** ~200 lines of HTML/CSS additions. One deploy.

---

## Design Principles

- Keep the existing dark theme (var(--bg), var(--blue), var(--gold))
- PPC Coach card gets gold border/accent (it's the revenue product)
- Insurance Genie card is blue accent (free tool, lead gen)
- Companion card is subtle/dimmed (not ready yet)
- Mobile-first — cards stack vertically on phone
- Page should NOT require scrolling for the hero + PPC Coach feature on desktop
- Keep `overflow: hidden` → change to `overflow-y: auto` (page is now scrollable)
- Animation: stagger fadeUp on product cards like existing elements

---

## SEO Updates

```html
<title>EBFC AI — AI Tools for Construction Professionals</title>
<meta name="description" content="AI-powered tools for construction: PPC coaching, COI compliance, and your personal AI companion. Built for superintendents, PMs, and lean coaches." />
```

Add structured data (Organization + Product) for Google rich results.

---

## Timeline

| Step | When | Who |
|------|------|-----|
| Felipe reviews this plan | Mon afternoon | Felipe |
| Build updated page | Mon evening / Tue AM | Osito |
| Deploy to Vercel | Same day | Osito |
| PPC Coach goes live (auth + Stripe) | Wed | Together |

---

## What This Does NOT Change

- Existing waitlist form + Google Sheets integration — untouched
- Existing branding (colors, fonts, Felipe headshot) — preserved
- Insurance Genie deployment — independent, just linked
- ppc.theebfcshow.com — stays live, not mentioned on ebfc.ai (users go to ppc.ebfc.ai)

---

## Alternative Considered: Separate Landing Page for PPC Coach

We could build a standalone landing page at ppc.ebfc.ai instead. But:
- ebfc.ai gets zero traffic benefit from PPC Coach
- Visitors to ebfc.ai still see "coming soon" — bad signal
- We want ebfc.ai to be the front door for the product family

**Recommendation:** Update ebfc.ai AND build a focused landing page at ppc.ebfc.ai later (Sprint 2, alongside the AI coaching launch). The ebfc.ai update is the quick win this week.

---

*Ready for Felipe's review.*
