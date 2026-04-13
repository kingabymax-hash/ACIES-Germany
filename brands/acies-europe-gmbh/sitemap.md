# Sitemap: Acies Europe GmbH

**Client:** Acies Europe GmbH
**Last updated:** 2026-04-13
**Status:** Working

> Curated working doc for the page tree, navigation, and user flow. Per-page detail lives in `pages/{page-name}.md`.

---

## Structural Decision

This is a **single-page site** with anchored in-page sections and a bilingual (DE/EN) language toggle. No multi-page nav. The Privacy Policy is the one exception — it lives on the same page as a distinct anchored section (user's instruction: "1 pager").

This keeps the regulatory evidence in one place, matches what a supervisory check-link expects (a single URL to verify), and avoids the overhead of a multi-page IA for content that does not need it.

---

## Page Tree

```
/  (single page, bilingual)
│
├── Language toggle (DE ↔ EN) — persistent top-right
│
└── In-page sections (anchored, single scroll):
    ├── #intro          — Who we are (1 short paragraph)
    ├── #services       — What Acies Europe GmbH does
    ├── #phoenix        — Phoenix Europe trading name disclosure
    ├── #impressum      — §5 TMG legal notice (address, HRB, VAT, MDs)
    ├── #regulatory     — §34d GewO status, reg number, supervisory authority
    ├── #remuneration   — Commission / fee disclosure
    ├── #register       — Public register lookup (DIHK / vermittlerregister.info)
    ├── #laws           — Commercial law framework citations
    ├── #dispute        — Dispute settlement bodies + ODR link
    ├── #liability      — Liability notice for external links
    ├── #disclaimer     — General disclaimer
    ├── #copyright      — Copyright notice
    ├── #privacy        — EU / GDPR Privacy Policy
    └── Footer          — Contact email, language toggle echo, last updated date
```

---

## Page List

| File | URL | Status | Notes |
|---|---|---|---|
| `pages/home.md` | `/` | Detailed | The single page, containing all sections above. |

---

## Navigation Structure

**Primary nav:** None in the traditional sense. A compact **in-page anchor menu** (sticky or collapsible) listing the section names, so a supervisor or KYC checker can jump straight to Impressum, Register, or Dispute Resolution without scrolling.

**Secondary nav:** None.

**Always-visible CTAs:** None. This page has no CTA in the marketing sense. The functional equivalent of a CTA is the `mailto:info@aciesmgu.com` contact and the language toggle.

**Nav style notes:**
- Language toggle (DE / EN) top-right, persistent.
- Anchor menu either sticky-top-left or collapsed behind a single "Contents / Inhalt" disclosure.
- Skip-to-content link for accessibility.

---

## Intended User Journey

1. Visitor arrives (often from a register check, a KYC search, or a footer link on the main ACIES site).
2. First fold establishes: legal entity name, what it does, where it's licensed, that it's part of ACIES.
3. Visitor scrolls OR uses the anchor menu to jump to whichever section they came to verify (most commonly Impressum, Regulatory status, or Register lookup).
4. Visitor either (a) confirms what they needed and leaves, or (b) copies the contact email to get in touch.

There is no conversion funnel. Success = the visitor finds the fact they came for, without confusion, in their preferred language.

---

## Notes

- Only one page exists in `pages/` because this is a 1-pager. If the privacy policy is later broken out to its own URL (e.g. `/privacy`), add `pages/privacy.md` and update this sitemap.
- Anchor IDs should be stable (and ideally language-neutral, i.e. `#impressum` in both DE and EN versions) so inbound links from the main ACIES site don't break.
