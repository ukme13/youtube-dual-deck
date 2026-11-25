---
name: YouTube Dual-Deck DJ Console
description: Tactile dark-mode pro DJ hardware console for YouTube mixing
colors:
  bg: "#000000"
  panel: "#121212"
  surface: "#181818"
  surface-elevated: "#242424"
  surface-hover: "#2a2a2a"
  text-primary: "#ffffff"
  text-muted: "#b3b3b3"
  text-subtle: "#9a9a9a"
  deck-a: "#3b82f6"
  deck-b: "#f43f5e"
  cue-amber: "#f59e0b"
  loop-purple: "#7c3aed"
  warn-red: "#f15e6c"
typography:
  display:
    fontFamily: "DM Sans, system-ui, sans-serif"
    fontSize: "0.85rem"
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: "0.12em"
  body:
    fontFamily: "DM Sans, system-ui, sans-serif"
    fontSize: "0.8rem"
    fontWeight: 500
    lineHeight: 1.4
  label:
    fontFamily: "DM Sans, system-ui, sans-serif"
    fontSize: "0.76rem"
    fontWeight: 600
    lineHeight: 1
  mono:
    fontFamily: "JetBrains Mono, monospace"
    fontSize: "0.6875rem"
    fontWeight: 700
    lineHeight: 1
  icons:
    fontFamily: "Material Symbols Rounded"
rounded:
  sm: "6px"
  md: "8px"
  lg: "10px"
  pill: "999px"
  circle: "50%"
spacing:
  xs: "4px"
  sm: "8px"
  md: "10px"
  lg: "14px"
components:
  deck-chassis:
    backgroundColor: "{colors.panel}"
    rounded: "{rounded.lg}"
    padding: "14px"
  button-play:
    backgroundColor: "{colors.text-primary}"
    textColor: "{colors.bg}"
    rounded: "{rounded.circle}"
    size: "36px"
  button-standard:
    backgroundColor: "{colors.surface-elevated}"
    textColor: "{colors.text-primary}"
    rounded: "{rounded.pill}"
    padding: "7px 12px"
  badge-bpm:
    backgroundColor: "rgba(255, 255, 255, 0.06)"
    textColor: "{colors.text-muted}"
    rounded: "{rounded.sm}"
    padding: "2px 7px"
---

# Design System: YouTube Dual-Deck DJ Console

## Overview

**Creative North Star: "The Midnight Hardware Deck"**

The console translates the weight, responsiveness, and tactical precision of physical club hardware (such as Pioneer DJ or Traktor controllers) into a single-file, zero-dependency browser interface. It rejects generic SaaS aesthetics—no playful cartoon illustrations, no washed-out pastel backgrounds, and no generic purple-to-blue gradient hero blocks. Instead, it commits to a deep black chassis (`#000000` / `#121212`) punctuated by high-contrast functional color codings.

Visual density is tuned for rapid glanceability under live DJ conditions: Deck A is anchored in Electric Blue (`#3b82f6`), Deck B in High-Energy Rose (`#f43f5e`), and mixer operations in neutral monochromes with luminous amber cue highlights. Frosted LED deck lamps pulse subtly to audio energy, and tactile side-peeking vinyl records animate to convey playback velocity and scrubbing feedback.

### Key Characteristics:
- **Hardware Density**: Compact, high-signal UI that fits complex two-deck mixing into a single view without scrolling.
- **High-Contrast Signal Routing**: Immediate color distinction between Deck A (Blue), Deck B (Rose), and System/Mixer controls.
- **Monospace Precision**: Monospaced tabular numerals for BPM, elapsed time, pitch percentages, and loop counts.
- **Tactile Depth**: Layered matte panels with crisp borders rather than floaty, diffuse shadows.

## Colors

The palette is strictly functional: black absorbs light, while sharp saturated accents indicate live audio states.

### Primary
- **Deck A Electric Blue** (`#3b82f6`): Identifies Deck A audio state, fader bias, active cues, and channel VU meter peaks.
- **Deck B Crimson Rose** (`#f43f5e`): Identifies Deck B audio state, fader bias, active cues, and channel VU meter peaks.

### Secondary & Functional
- **Cue Amber** (`#f59e0b`): Reserved for active Main Cues, Hot Cue triggers, and timestamp indicators.
- **Loop Purple** (`#8b5cf6`): Used specifically for active loop steps and beat-fraction divisions.
- **Warning Coral** (`#f15e6c`): Indicates track-ending alerts (<10s remaining) and audio ducking states.

### Neutral
- **Deep Black** (`#000000`): Canvas background and video container backdrops.
- **Chassis Panel** (`#121212`): Base deck and mixer surface container.
- **Surface Elevated** (`#242424`): Elevated hardware controls, fader tracks, and inputs.
- **Border Subtle** (`rgba(255, 255, 255, 0.06)`): Edge separation without visual clutter.
- **Text High-Contrast** (`#ffffff`): Primary typography and tactile active switches.
- **Text Muted** (`#b3b3b3`): Descriptive labels, inactive shortcuts, and subtitles.

### Named Rules
**The Functional Accent Rule.** Colors are never applied for decorative flair. If an element is colored Blue, Rose, or Amber, it communicates channel assignment or an active audio state.

## Typography

**Display / Header Font:** DM Sans (Google Fonts)  
**Body Font:** DM Sans  
**Label & Numerics Font:** JetBrains Mono  

**Character:** Clean European grotesque geometry for control labels paired with tabular monospaced engineering digits for times, BPM, and keyboard shortcuts.

### Hierarchy
- **Display / Title** (700, 0.85rem, uppercase, 0.12em tracking): Deck headers and console title.
- **Body** (500, 0.8rem, 1.4 line-height): Track titles, notifications, and queue labels.
- **Label** (600, 0.76rem, uppercase): Buttons, toggle switches, and mode controls.
- **Mono / Digits** (700, 0.6875rem, tabular numbers): BPM badges, Hot Cue millisecond timestamps, keyboard shortcuts.

## Layout

- **Console Grid**: A 3-column symmetrical desktop layout (`minmax(280px, 1fr) 252px minmax(280px, 1fr)`):
  - Left column: Deck A (Video stage, Hot Cues, Pitch fader, Loops).
  - Center column: Mixer (Master volume, Crossfader, Channel faders, Auto-Next, Talk/Duck).
  - Right column: Deck B (Video stage, Hot Cues, Pitch fader, Loops).
- **Breakpoint**: Below `960px`, the console collapses gracefully into a stacked single-column layout for narrower windows.
- **Spacing Rhythm**: 10px and 14px grid padding ensure compact, high-density hardware feel.

## Elevation & Depth

Surfaces rely on tonal layering and inner LED backlights rather than heavy drop shadows.

### Shadow Vocabulary
- **Deck Chassis**: Flat matte with subtle border line (`border: 1px solid rgba(255, 255, 255, 0.06)`).
- **Deck Lamp Glow**: Dynamic internal bloom (`box-shadow: inset 0 0 24px rgba(59, 130, 246, var(--glow))`) tied to channel audio levels.
- **Vinyl Disc**: `box-shadow: 0 12px 32px rgba(0, 0, 0, 0.75)` to lift the interactive turntable disc above the base.

## Shapes

- **Hardware Cards**: `10px` border-radius for decks and mixer pods.
- **Interactive Badges**: `6px` border-radius for BPM tags and hot cue buttons.
- **Action Buttons**: Pill-shaped (`999px`) or circular (`50%`) to mimic physical drum pads and rotary knobs.

## Components

### Play / Pause Button
- **Shape**: Circular (`36px × 36px`, `50%` radius).
- **Style**: High-contrast white background with pure black icon.
- **Hover**: Subtle enlargement (`transform: scale(1.04)`), active bounce (`scale(0.97)`).

### Cue & Hot Cue Buttons
- **Shape**: Pill or rounded rectangle (`6px` radius).
- **Style**: Surface elevated base with Amber or Deck accent text. Flash animation when triggered.

### Faders (Crossfader & Volume)
- **Track**: Recessed dark channel with center notch.
- **Handle**: Tactile metallic block with grip grooves.

### Vinyl Scratch Disc
- **Shape**: Pure circle (`50%` radius), vinyl groove radial and conic textures.
- **Behavior**: Spins in real time while playing (`spinVinyl 2.8s linear infinite`), interactive scratch-scrub on drag.

## Do's and Don'ts

### Do:
- **Do** maintain the 3-column symmetrical layout to keep muscle memory for Deck A and Deck B.
- **Do** show single-key keyboard shortcuts (`kbd-hint`) directly on or next to every actionable button.
- **Do** ensure text against dark backgrounds satisfies WCAG AA contrast (≥ 4.5:1).

### Don't:
- **Don't** use pastel tones or generic SaaS gradients (e.g. purple-to-pink).
- **Don't** use slow, floaty animations—DJ feedback must feel instant (<150ms).
- **Don't** hide critical playback state behind multi-click dropdowns.
