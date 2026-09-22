---
name: Dot Field
description: Aura-inspired glass control panel for a canvas-first SVG studio
colors:
  canvas-night: "#07080d"
  glass-panel: "rgba(16,18,27,.76)"
  raised-glass: "rgba(255,255,255,.07)"
  field-well: "rgba(7,8,13,.66)"
  hairline: "rgba(255,255,255,.09)"
  hairline-strong: "rgba(255,255,255,.17)"
  text-primary: "#f7f7fb"
  text-muted: "#c2c4ce"
  text-quiet: "#6f7382"
  violet: "#7448e8"
  indigo: "#4f46d8"
  violet-soft: "#a78bfa"
  danger: "#fb7185"
  ready: "#8bffbb"
typography:
  title:
    fontFamily: "Bricolage Grotesque, -apple-system, BlinkMacSystemFont, Segoe UI, sans-serif"
    fontSize: "18px"
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: "-0.035em"
  body:
    fontFamily: "Bricolage Grotesque, -apple-system, BlinkMacSystemFont, Segoe UI, sans-serif"
    fontSize: "14px"
    fontWeight: 400
    lineHeight: 1.4
  label:
    fontFamily: "Bricolage Grotesque, -apple-system, BlinkMacSystemFont, Segoe UI, sans-serif"
    fontSize: "11px"
    fontWeight: 600
    lineHeight: 1.3
    letterSpacing: "0.12em"
  value:
    fontFamily: "Bricolage Grotesque, -apple-system, BlinkMacSystemFont, Segoe UI, sans-serif"
    fontSize: "12px"
    fontWeight: 400
    lineHeight: 1.3
rounded:
  value: "7px"
  micro: "8px"
  brand: "11px"
  control: "12px"
  panel: "20px"
spacing:
  xs: "8px"
  sm: "10px"
  md: "12px"
  lg: "16px"
  section: "18px"
  panel: "20px"
components:
  glass-panel:
    backgroundColor: "{colors.glass-panel}"
    textColor: "{colors.text-primary}"
    rounded: "{rounded.panel}"
    width: "356px"
  button-primary:
    backgroundColor: "{colors.violet}"
    textColor: "{colors.text-primary}"
    rounded: "{rounded.control}"
    padding: "9px 12px"
    height: "40px"
  button-secondary:
    backgroundColor: "{colors.raised-glass}"
    textColor: "{colors.text-primary}"
    rounded: "{rounded.control}"
    padding: "9px 12px"
    height: "40px"
  input:
    backgroundColor: "{colors.field-well}"
    textColor: "{colors.text-primary}"
    rounded: "{rounded.control}"
    padding: "8px 10px"
    height: "38px"
  value-badge:
    backgroundColor: "rgba(255,255,255,.035)"
    textColor: "{colors.text-muted}"
    rounded: "{rounded.value}"
    padding: "3px 7px"
---

# Design System: Dot Field

## Overview

**Creative North Star: "The Floating Aura Instrument"**

Dot Field is a canvas-first creative tool with one floating, continuous glass panel. The dark canvas stays dominant; the controls feel like a precise translucent instrument suspended above it. White information, restrained violet-to-indigo accents and fine white-alpha rules carry the hierarchy.

The approved visual authority is [Aura component 8442B](https://www.aura.build/component/8442B), preserved locally in `/Users/sergeymaximov/.codex/attachments/03183e65-c732-46be-b325-4f80bdfdb9f4/Pasted text.txt`. Its glass material and violet gradients are intentional exceptions to generic warnings against glassmorphism or purple gradients.

**Key Characteristics:**
- One floating glass shell over an uninterrupted dark canvas.
- Bricolage Grotesque throughout, with compact labels and tabular values.
- Violet/indigo reserved for interactive emphasis; white and cool gray carry content.
- Flat internal sections separated by hairlines, never nested cards.
- Persistent export actions and a mobile bottom sheet sized for real touch use.

## Colors

The palette is a near-black canvas, translucent neutral glass, white-to-gray text and a focused violet/indigo accent.

### Primary
- **Aura Violet:** primary actions, active ranges and selected controls.
- **Deep Indigo:** the lower end of the approved primary gradient.
- **Soft Violet:** focus outlines and subtle interactive borders.

### Neutral
- **Canvas Night:** uninterrupted artwork ground.
- **Glass Panel:** the single floating control shell.
- **Raised Glass:** secondary actions and hover states.
- **Field Well:** select, number and file-input wells.
- **Primary White:** titles, actions and high-emphasis labels.
- **Muted Silver / Quiet Slate:** supporting copy, values and low-emphasis status.
- **White-alpha Hairlines:** panel edge, section dividers and control borders.

### Named Rules

**The Aura Exception Rule.** The approved Aura reference intentionally permits restrained glass and violet-to-indigo gradients; do not “correct” them into flat graphite or another accent color.

**The Accent Is State Rule.** Violet marks interaction and primary completion, not ambient glow or decorative chrome.

## Typography

**Display Font:** Bricolage Grotesque with system sans-serif fallbacks
**Body Font:** Bricolage Grotesque with system sans-serif fallbacks

**Character:** Contemporary and expressive without becoming editorial. Tight title tracking and compact uppercase labels give the panel a crafted tool-like voice.

### Hierarchy
- **Title:** 600 weight with tight tracking; product identity only.
- **Body:** 400–600 weight; controls, buttons and status copy.
- **Label:** 600 weight, uppercase and widely tracked; section and source labels.
- **Value:** compact, right-aligned and tabular; numeric readouts and status.

### Named Rules

**The Single Voice Rule.** Use Bricolage Grotesque throughout; do not introduce a display serif, faux-terminal mono or system-only substitute when the webfont is available.

## Layout

Desktop uses a 356px panel inset 12px from the left, top and bottom edges. Header and export footer are fixed flex children; only the settings body scrolls. Sections use 20px horizontal insets, 18px vertical rhythm and full-width internal dividers.

At 759px and below, the panel becomes an 8px-inset bottom sheet at `min(72dvh, 640px)`. At 390×844, preserve a 204px visible settings-scroll target between the grip/header and export footer. The 48px grip collapses the sheet; all mobile fields and buttons have at least 44px touch targets.

## Elevation & Depth

Depth comes from translucent surfaces, 28px backdrop blur with restrained saturation, white-alpha borders and neutral black shadows. The outer panel uses one soft shadow plus a faint inset highlight; controls use only subtle inset highlights. No chromatic glow.

### Shadow Vocabulary
- **Floating panel:** `0 18px 42px rgba(0,0,0,.42)` on desktop; `0 -18px 50px rgba(0,0,0,.44)` on mobile.
- **Primary action:** `0 8px 20px rgba(0,0,0,.18)` with a white inset highlight.
- **Brand tile:** `0 8px 18px rgba(0,0,0,.18)` with a white inset highlight.

### Named Rules

**The Neutral Elevation Rule.** Shadows may separate layers, but their hue stays neutral; violet never becomes a glow.

## Shapes

The outer glass panel uses a generous 20px radius. Inputs and buttons use 12px, the brand tile 11px, and compact value or micro surfaces 7–8px. Dividers and flattened sections remain square; circles are reserved for status or the mark.

## Components

### Glass Panel
- **Material:** translucent near-black surface, 1px white-alpha border, 28px blur and neutral elevation.
- **Structure:** fixed header, flexible scrolling body and fixed export footer inside one continuous shell.

### Buttons
- **Primary:** violet-to-indigo gradient, white text, 12px radius and neutral shadow.
- **Secondary:** low-alpha white surface and border; hover increases only neutral opacity.
- **States:** 160ms hover/focus feedback, 1px active translation and a 2px soft-violet focus outline. Mobile minimum height is 44px.

### Inputs / Fields
- **Style:** dark translucent well, thin white-alpha border, 12px radius and compact padding.
- **States:** hover may pick up a faint violet border; focus uses a visible 2px outline with no glow. Errors use the danger token.

### Values and Sections
- **Values:** 7px compact badge, muted text and tabular numerals; 8px is available for micro-surfaces and scrollbar geometry.
- **Sections:** transparent, borderless groups separated by one hairline. Do not wrap section content in nested cards.

### Export Footer
- **Behavior:** a fixed flex child with its own top divider; it never scrolls away with settings. SVG is secondary and video export is primary.

### Mobile Bottom Sheet
- **Behavior:** 72dvh maximum working height, 48px collapse grip and a 204px scroll-area target at 390×844. Motion is removed under reduced-motion preferences.

## Do's and Don'ts

### Do:
- **Do** keep the artwork dominant and the 356px desktop panel visually self-contained.
- **Do** preserve 28px blur, white-alpha borders and neutral elevation as one material system.
- **Do** keep export actions visible while settings scroll.
- **Do** preserve keyboard focus, reduced motion, live status announcements and 44px mobile targets.
- **Do** treat the Aura URL and pasted source above as the intentional visual authority.

### Don't:
- **Don't** split the interface into nested cards; flatten sections with dividers.
- **Don't** replace Bricolage Grotesque with generic system typography.
- **Don't** add chromatic shadows, neon bloom or decorative purple haze.
- **Don't** overuse violet outside active, focused or primary states.
- **Don't** shrink the mobile scroll target below 204px at 390×844 or let the export footer scroll away.
