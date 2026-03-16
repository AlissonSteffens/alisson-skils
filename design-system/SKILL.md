---
name: design-system
description: >
  Visual design system based on the "Editorial Ink" aesthetic: warm cream/parchment backgrounds,
  refined serif typography, terracotta accents, and a literary/artisanal personality.
  Use this skill whenever the user wants to create interfaces, components, or design systems
  inspired by Editorial Ink, warm editorial design, paper-tone UIs, literary portfolios,
  or asks for something that feels "sophisticated", "warm", "analog", or "anti-dark-mode tech".
  Also trigger when building portfolio pages, personal sites, or any UI that should feel
  intentionally crafted rather than generic.
---

# Editorial Ink — Visual Style Guide

A design language that trades the ubiquitous dark-mode tech aesthetic for a warm, literary
personality. Feels like a well-designed book or a Parisian editorial — rare in developer
portfolios precisely because it breaks the mold.

---

## Core Philosophy

> Intentional craft over technical sterility. Every element should feel considered, warm,
> and slightly analog — as if the page was typeset rather than coded.

- **Light, not dark.** Parchment and cream as base, not white or gray.
- **Serif for display.** Headlines use an elegant serif; mono for metadata only.
- **Restrained accent.** One warm terracotta color does all the work.
- **Low contrast borders.** Subtle, warm-toned dividers — never harsh.

---

## Color Tokens

| Token     | Hex       | Usage                                      |
|-----------|-----------|--------------------------------------------|
| `base`    | `#F5F0E8` | Page/app background — warm parchment       |
| `surface` | `#EDE7DA` | Cards, panels, elevated surfaces           |
| `border`  | `#D4C9B5` | Dividers, outlines, input borders          |
| `muted`   | `#6B5E52` | Secondary text, placeholders               |
| `ink`     | `#1E1810` | Primary text, headings, nav logos          |
| `accent`  | `#C05B2E` | CTAs, highlights, italic display text, dots|

**Never use:** pure `#000000` black, cool grays (`#888`, `#999`), any blue or purple accent.

---

## Typography System

### Display — Fraunces
- Font: `'Fraunces', serif`
- Weight: `300` (light) for the roman; `italic` for the accent portion
- Size: `clamp(2.2rem, 5vw, 3.5rem)`
- Letter-spacing: `-0.03em`
- Color: `#1E1810` (roman) + `#C05B2E` (italic)

```css
.display-heading {
  font-family: 'Fraunces', serif;
  font-weight: 300;
  font-size: clamp(2.2rem, 5vw, 3.5rem);
  letter-spacing: -0.03em;
  line-height: 1.05;
  color: #1E1810;
}
.display-heading em {
  font-style: italic;
  color: #C05B2E;
}
```

### Labels / UI Metadata — DM Mono
- Font: `'DM Mono', monospace`
- Weight: `400`
- Size: `0.65rem – 0.75rem`
- Letter-spacing: `0.08em – 0.12em`
- Text-transform: `uppercase`
- Color: `#8A7E73` (secondary) or `#C05B2E` (tag/accent)

```css
.label {
  font-family: 'DM Mono', monospace;
  font-size: 0.7rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: #8A7E73;
}
```

### Body Copy — Figtree
- Font: `'Figtree', sans-serif`
- Weight: `300`
- Size: `0.88rem – 0.95rem`
- Line-height: `1.6`
- Color: `#6B5E52`

---

## Component Patterns

### Navigation Bar
```css
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1.5rem 2.5rem;
  border-bottom: 1px solid #D4C9B5;
  background: #F5F0E8;
}
```
- Logo: DM Mono, `0.75rem`, `#3D3530`, uppercase with `·` separator (e.g. `AS · dev`)
- Nav links: DM Mono, `0.7rem`, `#8A7E73`, no underline on hover

### Buttons
```css
/* Primary */
.btn-primary {
  background: #1E1810;
  color: #F5F0E8;
  padding: 0.6rem 1.3rem;
  font-family: 'DM Mono', monospace;
  font-size: 0.72rem;
  letter-spacing: 0.05em;
  border: none;
  border-radius: 3px;
}

/* Secondary / Ghost */
.btn-secondary {
  background: transparent;
  color: #3D3530;
  padding: 0.6rem 1.3rem;
  font-family: 'DM Mono', monospace;
  font-size: 0.72rem;
  letter-spacing: 0.05em;
  border: 1px solid #C0B4A4;
  border-radius: 3px;
}
```

### Cards / Panels
```css
.card {
  background: #EDE7DA;
  border: 1px solid #D4C9B5;
  border-radius: 8px;
  padding: 1.2rem 1.4rem;
}
.card-label {
  font-family: 'DM Mono', monospace;
  font-size: 0.6rem;
  color: #8A7E73;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  margin-bottom: 0.5rem;
}
.card-item::before {
  content: '◆';
  color: #C05B2E;
  margin-right: 0.3rem;
}
```

### Tags / Badges
```css
.tag {
  font-family: 'DM Mono', monospace;
  font-size: 0.65rem;
  color: #C05B2E;
  letter-spacing: 0.1em;
  text-transform: uppercase;
}
/* Prefix arrow convention: */
/* "↳ MSc Applied Computing" */
```

### Footer Strip (dark inversion)
```css
.footer-strip {
  background: #1E1810;
  padding: 0.75rem 2.5rem;
  font-family: 'DM Mono', monospace;
  font-size: 0.65rem;
  color: #6B5E52;
  display: flex;
  justify-content: space-between;
}
```

---

## Layout Principles

- **Max width:** `1200px`, centered with `margin: 0 auto`
- **Padding:** generous — `2.5rem` horizontal, `3rem` vertical for hero sections
- **Grid:** two-column hero (`1fr auto`) with main content left, info card right
- **Spacing rhythm:** multiples of `0.25rem`; prefer `1.5rem`, `2rem`, `2.5rem` gaps

---

## Accent Usage Rules

The terracotta `#C05B2E` is the **only** accent color. Use it for:
- Italic portions of the display headline
- Tag/label text (e.g. `↳ MSc Applied Computing`)
- Bullet/list decorators (`◆`, `→`)
- CTA hover states
- Borders on focus states

**Do not** use it for large filled backgrounds — it overpowers. Reserve fills for the ink `#1E1810`.

---

## Google Fonts Import

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,wght@0,300;0,400;1,300&family=DM+Mono:wght@300;400&family=Figtree:wght@300;400;500&display=swap" rel="stylesheet">
```

---

## Personality Checklist

Before shipping any component, verify:

- [ ] Background is parchment-warm, not white or cool-gray
- [ ] Display text uses Fraunces serif (not sans-serif)
- [ ] The only pop of color is terracotta `#C05B2E`
- [ ] Metadata/labels use DM Mono with letter-spacing
- [ ] No shadows heavier than `0 1px 3px rgba(0,0,0,0.08)`
- [ ] Borders use `#D4C9B5`, never a gray or blue-tinted tone
- [ ] Body copy uses Figtree at weight 300, color `#6B5E52`
- [ ] Buttons are small and typographically restrained (mono font, small size)

---

## Anti-patterns to Avoid

| ❌ Avoid                          | ✅ Instead                              |
|-----------------------------------|-----------------------------------------|
| Dark background (`#0f0f0f`)       | Parchment base `#F5F0E8`               |
| Sans-serif display heading        | Fraunces serif with italic accent       |
| Blue/purple accent                | Terracotta `#C05B2E` exclusively        |
| Large radius buttons (`16px+`)    | Tight radius `3px–5px`                 |
| Bold heavy body text              | Figtree 300, muted `#6B5E52`           |
| Glowing/neon effects              | Flat, matte surfaces with warm borders |
| Emoji or colorful icons           | Typographic symbols (`◆`, `↳`, `→`) or Lucide icons    |