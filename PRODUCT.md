# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

The creator and friends hanging out and playing music together on a desktop or laptop (keyboard + mouse), either for casual continuous background sessions or live back-and-forth mixing.

## Product Purpose

Provide an instant, zero-install dual-deck YouTube / YouTube Music DJ console that runs inside Google Sites, letting friends queue tracks, cue timestamps, crossfade smoothly, and talk over music without needing dedicated DJ hardware or downloaded audio files.

## Positioning

A self-contained single-file YouTube dual-deck mixer built specifically to survive Google Sites sandboxed iframe embedding (`https://`, resilient storage fallback, keyboard focus lock) while combining hands-off `Auto-Next` + `Auto-Load Queue` continuity with live DJ controls (Main Cue, 3 Hot Cues, 4s/8s Loop, Pitch/Nudge, and Talk/Duck).

## Operating Context

- Embedded inside a Google Sites page (`Embed Code` iframe) and opened in desktop browsers such as Brave or Chrome.
- Operated with mouse and single-key keyboard shortcuts (`Q/A`, `P/L`, `1-3/8-0`, `Z/X`, `N/M`, `[/]`, `T`, arrows).
- Tracks are sourced from YouTube and YouTube Music URLs (`watch?v=`, `youtu.be/`, `shorts/`, `live/`, `music.youtube.com`, or 11-character video IDs).

## Capabilities and Constraints

- **Single-file constraint**: Must remain one self-contained HTML/CSS/JS file (`generated-canvas-gemini.html`) with no build step or backend server, ready to paste directly into Google Sites Embed.
- **Core features**: Dual YouTube IFrame API decks (defaulting to `0UmE0QH-AA0` on A and `fxViBvmTM_o` on B), equal-power crossfader, CH A/B + Master faders, Talk/Duck (`25%` ducking), Fader Start (`2s/4s/6s`), `Auto-Next (10s)`, `Auto-Load Queue`, Tap BPM, Main Cue, 3 Hot Cues per deck, 4s/8s Loop, Pitch slider (`0.75x–1.25x`) + hold-to-nudge, and Video Focus Lock.
- **Track Queue**: Auto-fetches track titles via YouTube oEmbed / `noembed.com`, persists to `localStorage` with `try/catch` fallback for sandboxed iframes, and supports JSON Export/Import and saving directly from Deck A/B (including Hot Cues).
- **Browser/iframe constraints**: YouTube IFrame API requires `https://` (works on Google Sites); autoplay with sound on an un-interacted deck may require prior user interaction; keyboard shortcuts require focus inside the embed iframe.

## Evidence on Hand

- Incumbent implementation: `generated-canvas-gemini.html`

## Product Principles

- **Zero-friction hangout**: Casual continuous playback (`Auto-Next` + `Auto-Load Queue` + auto-fetched track titles) must work effortlessly without requiring constant DJ micromanagement.
- **Keyboard-first live control**: Every core deck and mixer action stays reachable via one-key shortcuts, protected by Video Focus Lock so clicking near the player never steals focus.
- **Resilient in hostile iframes**: Storage, URL parsing, and external embeds degrade gracefully inside Google Sites and privacy-strict browsers like Brave.
- **Self-contained portability**: Everything ships in a single pasteable HTML file with zero build tooling.
