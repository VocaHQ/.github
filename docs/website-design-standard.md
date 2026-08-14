# Voca web design standard

- **Status:** adopted direction
- **Reference implementation:** [VocaPhone landing page](https://vocaphone-demo.netlify.app/)
- **Applies to:** VocaPhone, VocaMac, VocaLinux, VocaWin, VocaGateway, and
  future Voca products

## Purpose

Voca products should feel like members of the same family before a visitor reads
the logo. They should share a point of view, not a copied template.

This standard captures the design language established by the VocaPhone landing
page and turns it into reusable guidance for every Voca website. It covers visual
direction, product storytelling, content, interaction, accessibility,
performance, implementation, and review.

The goal is a family of sites that feels:

- human rather than corporate;
- tactile rather than glossy;
- technically credible rather than abstract;
- calm rather than empty;
- privacy-first without relying on vague claims; and
- native to each product's platform while remaining recognizably Voca.

This document is the source of truth for the shared direction. The reference
site demonstrates it; it is not a component library and should not be copied
without adapting the product story.

## Non-negotiables

- Use the exact approved product name, logo, and platform behavior.
- Lead with a real product interaction and a verified user benefit.
- Explain where speech-to-text runs and when the gateway is optional or required.
- Use warm neutral surfaces, one product accent, solid fills, and no gradients.
- Keep product UI faithful to the operating system it represents.
- Make the primary story work without animation, decoration, or JavaScript.
- Validate desktop, mobile, keyboard, contrast, reduced motion, and published links.

## The design thesis

Voca turns speech into useful text on hardware the user controls. The websites
should make that relationship visible.

Use oversized editorial typography, warm paper-like surfaces, thin borders,
real product UI fragments, small technical annotations, and a restrained product
accent. The result should feel like a thoughtful working desk: interface windows,
notes, folders, status cards, diagrams, and a few hand-placed details.

Avoid the familiar visual shortcuts of generic software landing pages: glowing
orbs, gradient meshes, glass panels, fake dashboards, stock people, anonymous 3D
objects, and unsupported “AI-powered” claims.

## Core principles

### 1. Show the product doing the work

A visitor should understand the core interaction from the hero or the first
proof section. Use a real or faithful product state: a keyboard inserting text,
a macOS window completing a transcript, a Linux desktop command and result, or a
gateway routing audio to a local model.

Do not use an abstract illustration where a product interaction would explain
the same idea more honestly.

### 2. Make privacy concrete

Privacy is an architecture, not a decorative lock icon.

State where audio is recorded, where speech-to-text runs, whether a network is
required, what is retained, and which modes are optional. When a product offers
more than one path, show both paths and let the user see the boundary.

For example:

- **On-device:** The model and audio stay on this device. After the model
  download, transcription can work offline.
- **Self-hosted gateway:** Audio travels to the gateway the user configured.
  The gateway runs the local speech engine and returns the transcript.
- **Cloud service:** Name the service, the data sent, and the retention
  behavior. Do not describe it as local.

Never collapse “private,” “local,” “self-hosted,” and “on-device” into one claim.

### 3. Keep the visual system flat and tactile

Use solid fills, borders, restrained shadows, small rotations, and layered cards
to create depth. Do not use CSS gradients. Shadows should suggest paper or a
window sitting above the page, not a glowing atmosphere.

### 4. Give every element a job

Decorative elements may establish character, but they must support the product
story. A folder suggests saved words, a waveform suggests live speech, a status
card establishes local readiness, and a route diagram explains architecture.

Remove decoration that could belong to any software product.

### 5. Preserve platform truth

The family resemblance comes from composition, typography, materials, voice,
and behavior—not from pretending every operating system looks the same.

- VocaMac should use credible macOS windows and controls.
- VocaLinux should use credible Linux desktop or terminal states.
- VocaWin should use credible Windows surfaces, not macOS traffic lights.
- VocaPhone should show the real iOS and Android interaction differences.
- VocaGateway should show routes, models, readiness, pairing, and server state.

### 6. Be precise before being clever

Lead with the strongest verified benefit. Use memorable headlines, then explain
the boundary in plain language. Do not let a short slogan create a false product
claim.

## Family resemblance and product identity

Every Voca site shares the following:

- a warm neutral foundation;
- dark, high-contrast ink;
- one primary product accent;
- large, tightly spaced display type;
- small monospaced labels for technical detail;
- flat bordered cards and product windows;
- direct product proof;
- concise, human copy;
- restrained motion with reduced-motion support; and
- the accessibility and validation standards in this guide.

Every product keeps the following:

- its approved name and casing;
- its exact logo and app icon;
- its own primary accent, derived from approved brand assets;
- platform-accurate UI;
- its real installation and release status;
- its actual privacy and processing model; and
- its strongest product-specific story.

Do not recolor a logo, redraw a mark, invent product casing, or reuse another
product's screenshots to create artificial consistency. Shared assets belong in
`brand/<product>/` in this repository once approved.

## Visual foundation

### Baseline palette

The VocaPhone reference uses this warm neutral foundation. It is the preferred
starting point for public product sites:

| Token | Reference value | Use |
| --- | --- | --- |
| `--paper` | `#f4f1e8` | Main page canvas |
| `--paper-deep` | `#ebe5d8` | Recessed or alternate surface |
| `--paper-bright` | `#fffdf7` | Cards and windows |
| `--ink` | `#14231c` | Primary text and strong borders |
| `--muted` | `#68726c` | Supporting copy |
| `--line` | `#c9c8bd` | Quiet borders and dividers |
| `--line-dark` | `#9ea59f` | Stronger component outlines |
| `--sun` | `#e9b949` | Focus, annotation, and small emphasis |
| `--red` | `#de6a57` | Small status or window detail |

The primary product accent is not a universal hard-coded green. Define it per
product from approved brand material:

```css
:root {
  --paper: #f4f1e8;
  --paper-deep: #ebe5d8;
  --paper-bright: #fffdf7;
  --ink: #14231c;
  --muted: #68726c;
  --line: #c9c8bd;
  --line-dark: #9ea59f;

  /* Replace these three with the approved product palette. */
  --brand: #0f6b57;
  --brand-dark: #0b493d;
  --brand-soft: #cfe9dc;

  --sun: #e9b949;
  --red: #de6a57;
  --shadow-soft: 0 18px 45px rgb(35 45 39 / 12%);
  --shadow-window: 0 22px 55px rgb(21 37 29 / 16%);
}
```

Secondary colors are functional annotations, not competing brand colors. Most
of a page should be paper, ink, and the product accent.

### Dark surfaces

Marketing pages may use a dark manifesto or proof section for rhythm. Product
dashboards may be dark-first when that matches the product direction. Use neutral
charcoal surfaces rather than blue-black or saturated dashboard colors. Keep the
same border, spacing, typography, and contrast discipline.

Do not create a light or dark theme merely to check a feature box. A second theme
needs a designed palette and the same visual QA as the primary theme.

### Gradients

Do not use linear, radial, or conic gradients. Create hierarchy with solid
surfaces, borders, spacing, typography, illustration, and restrained shadows.

## Typography

Use system-first font stacks by default. The page should remain distinctive
because of scale, weight, spacing, and composition—not because it downloads a
fashionable web font.

```css
:root {
  --font-display: "Avenir Next", "SF Pro Display", "Helvetica Neue",
    Helvetica, Arial, sans-serif;
  --font-body: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont,
    "Segoe UI", sans-serif;
  --font-mono: "SFMono-Regular", Consolas, "Liberation Mono", monospace;
}
```

### Roles

- **Display:** product name, hero statement, and major section headings.
- **Body:** explanations, instructions, FAQ answers, and calls to action.
- **Mono:** section tags, status, timing, architecture notes, metadata, and small
  technical labels.

### Treatment

- Prefer short headlines with tight tracking and `0.9–1.0` line height.
- A hero product name may use `clamp(5rem, 12vw, 11rem)` when the layout supports
  it.
- Major section headings should normally use `clamp(3rem, 7vw, 6.8rem)`.
- Keep body copy between roughly 15 and 18 pixels with comfortable line height.
- Use uppercase mono labels sparingly and keep them small.
- Lowercase editorial headlines are part of the current marketing direction;
  approved product names retain their official casing.
- Avoid long centered paragraphs. Center the hero; left-align explanations.

## Layout and rhythm

### Canvas

- Use a warm paper canvas with generous negative space.
- A quiet SVG dot texture is acceptable, but content must remain readable if it
  is removed.
- Keep primary content within approximately `1120–1200px`.
- Use desktop section spacing around `120–160px` and mobile spacing around
  `80–110px`.
- Alternate editorial copy with product proof instead of stacking identical
  card grids.

### Header

The preferred product-site header is compact and fixed or sticky:

- product mark and name on the left;
- three to five plain-language anchors;
- one clear acquisition action;
- a subtle status or product detail only when it communicates something useful;
  and
- a real mobile menu with accurate `aria-expanded` state.

Do not fill the header with every repository, social channel, or secondary page.

### Hero

The hero should answer four questions without scrolling:

1. What is this product?
2. What is the primary benefit?
3. Why is it trustworthy or different?
4. What should I do next?

Recommended ingredients:

- exact product mark;
- product name or a concise benefit headline;
- one-sentence value proposition;
- one primary and one secondary action;
- a short proof line, such as supported platforms or processing modes;
- one faithful product interaction; and
- a small number of meaningful floating details on wide screens.

The hero should not require animation to communicate its meaning.

### Recommended page sequence

Use this as a story framework, not a mandatory template:

1. Compact navigation
2. Hero with product interaction
3. Optional vocabulary ribbon or transition
4. Two or three differentiated benefits
5. How it works
6. Architecture or privacy choice, when relevant
7. Platform-specific proof
8. Open-source or project-principles statement
9. FAQ with honest limitations
10. Final acquisition action
11. Resource-rich footer

If a section does not teach, prove, or help the visitor act, remove it.

## Component language

### Window shells

Use bordered “window” shells to frame real product states. A window typically has:

- a solid bright surface;
- a one-pixel medium-dark border;
- a 12–22 pixel radius;
- a restrained shadow;
- a compact top bar; and
- platform-appropriate controls.

Window controls must match the platform being represented. Generic editorial
windows may use the Voca paper style; product screenshots must remain authentic.

### Paper notes and status cards

Small cards can communicate privacy, readiness, language support, saved terms,
or a real message. Use a slight rotation of approximately `-4deg` to `4deg`, a
thin border, solid fill, and at most one quiet shadow.

Do not rotate long-form content or interactive controls.

### Section tags

Section tags are small mono pills that orient the reader before a large heading.
They should describe the section—“gateway is optional,” “how it works,” or
“questions, answered”—rather than act as decorative category labels.

### Buttons and links

- Use one filled primary button and one bordered secondary action in the hero.
- Write actions as verbs: “get the beta,” “build for iPhone,” “view on GitHub.”
- Give buttons strong focus states and at least a 44-pixel touch target.
- Hover movement should be subtle: one or two pixels, not a floating animation.
- External arrows may reinforce destination changes but cannot replace clear
  link text.

### Route diagrams

Route diagrams are preferred for privacy and processing explanations. Label the
origin, processing location, connection boundary, and returned result. Do not
hide a network transfer behind a generic “secure” arrow.

### Product proof

Prefer small composed UI recreations when they can be kept accurate and
accessible. Use screenshots when exact detail matters or when a recreation would
drift from the product. Never show a feature state that the released product
cannot reach.

### FAQ

Use native `details` and `summary` when practical. Open one useful question by
default, keep answers plain, and include limitations that affect adoption.

## Art direction

Use visual objects drawn from the product's world:

- waveform and microphone state;
- text caret and inserted transcript;
- app windows and keyboard surfaces;
- folders for saved vocabulary or history;
- model files, integrity state, or readiness;
- terminal output for Linux and headless tools;
- routes between a device and self-hosted hardware; and
- concise ASCII or monospaced annotations.

Avoid:

- stock photography;
- generic people illustrations;
- ungrounded 3D devices;
- abstract neon blobs;
- fake testimonials or customer logos;
- dense feature-icon grids;
- excessive rounded pills; and
- decorative elements that compete with the product name.

## Content and voice

Voca copy is direct, warm, specific, and lightly playful.

### Write like this

- Lead with the user outcome: “voice typing that stays on your phone.”
- Use plain terms: “speech-to-text model,” “your Mac,” “private gateway.”
- Prefer short verbs: speak, download, pair, insert, choose, keep.
- Explain a technical boundary immediately after the memorable headline.
- Name the platform and current delivery state: stable, beta, build from source,
  or coming soon.
- Preserve exact product names and official casing.

### Avoid this

- “Revolutionary AI-powered productivity.”
- “Military-grade privacy.”
- “Works everywhere” when operating-system restrictions exist.
- “No gateway” when the gateway is optional.
- “Local” when audio is sent to a remote service.
- internal implementation language in user-facing copy.

### Claim pattern

Use the sequence **benefit → mechanism → boundary**:

> Dictate offline. The speech-to-text model runs on this device after it is
> downloaded. A self-hosted gateway remains available when you want different
> models or shared compute.

This keeps the first line memorable and the complete statement accurate.

## Motion

Motion should confirm state or add quiet life to a product proof.

Recommended:

- 160–180 millisecond hover and pressed transitions;
- a one-time reveal when a section enters the viewport;
- a restrained live waveform;
- a blinking insertion caret;
- an optional slow vocabulary ribbon; and
- one changing example phrase when it does not affect comprehension.

Avoid:

- scroll-jacking;
- continuous parallax;
- large bouncing elements;
- autoplay video with sound;
- animated gradients;
- motion required to discover content; and
- several unrelated looping animations in one viewport.

Every site must implement `prefers-reduced-motion: reduce`. With reduced motion,
all content must be visible immediately and all essential interactions must
still work.

## Responsive behavior

Design the mobile composition, not just a smaller desktop page.

Suggested breakpoints from the reference implementation:

| Width | Expected behavior |
| --- | --- |
| Above `1180px` | Full composition and meaningful hero decoration |
| `921–1180px` | Reduce scale and decoration density |
| `641–920px` | Stack story rows and product cards; use mobile navigation |
| `640px` and below | Single-column content; hide nonessential decoration |

Rules:

- Critical claims must exist in text outside decorative elements.
- Hide decorative cards before they collide with the product name.
- Stack route diagrams in reading order.
- Keep primary actions full-width when that improves reach and legibility.
- Preserve a clear heading hierarchy.
- Test at `390×844` and at a desktop width of at least `1440px`.
- The document width must equal the viewport width; horizontal page scrolling is
  a release blocker.

## Accessibility

Accessibility is part of the design, not a later audit.

Every public Voca product site must include:

- one clear `h1` and a logical heading sequence;
- semantic `header`, `nav`, `main`, `section`, and `footer` landmarks;
- a skip link;
- visible keyboard focus with at least a three-pixel high-contrast outline;
- descriptive link text;
- meaningful alt text for informative images and empty alt text for decoration;
- `aria-hidden="true"` only on genuinely redundant decoration;
- accessible mobile-menu state;
- touch targets of at least 44 by 44 pixels;
- color contrast meeting WCAG AA;
- information that does not depend on color alone;
- reduced-motion behavior; and
- keyboard-operable FAQ and navigation controls.

Do not place the only version of an important claim inside an `aria-hidden`
mockup or an image.

## Performance and privacy of the website

The marketing site should reflect the product's values.

- Prefer static HTML and CSS for the landing page.
- Use local SVG and raster assets.
- Use system fonts unless an approved brand font materially changes the design.
- Do not require JavaScript for primary content or navigation destinations.
- Avoid third-party trackers by default.
- Do not load chat widgets, session replay, or advertising pixels without an
  explicit project decision and privacy review.
- Keep the initial page lightweight; a useful starting budget is less than
  `500KB` transferred before optional video or demo media.
- Reserve image dimensions to prevent layout shift.
- Keep the primary headline and action in the initial HTML.

The VocaPhone reference is dependency-free and uses local assets and system
fonts. Other stacks may implement the same outcomes without copying its file
structure.

## Implementation starter

A dependency-free site may begin with:

```text
website/
├── assets/
│   ├── product-logo.svg
│   ├── product-mark.svg
│   └── paper-dots.svg
├── tests/
│   └── site.test.mjs
├── index.html
├── styles.css
├── script.js
├── package.json
└── README.md
```

At minimum, the CSS should establish:

```css
* {
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
  scroll-padding-top: 76px;
}

body {
  margin: 0;
  overflow-x: hidden;
  color: var(--ink);
  background: var(--paper);
  font-family: var(--font-body);
  font-size: 16px;
  line-height: 1.5;
  -webkit-font-smoothing: antialiased;
}

:focus-visible {
  outline: 3px solid var(--sun);
  outline-offset: 3px;
}

@media (prefers-reduced-motion: reduce) {
  html {
    scroll-behavior: auto;
  }

  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}
```

Framework components should expose the same semantic structure and tokens. Do
not make the standard dependent on React, Astro, Next.js, or another framework.

## Product adaptation notes

### VocaPhone

- Lead with private on-device speech-to-text.
- Present VocaGateway as an optional second path, not an absent dependency.
- Show real iOS and Android differences.
- Make international language support visible.
- Use keyboard insertion and phone-to-gateway routes as primary proof.

### VocaMac

- Lead with native macOS voice typing and the selected local model behavior.
- Use authentic macOS windows, menu-bar states, microphone selection, and model
  controls.
- Preserve access to real settings and limitations in product demonstrations.
- Avoid turning the site into a generic black developer-tool page.

### VocaLinux

- Lead with local desktop dictation and distribution support.
- Pair a real desktop interaction with terminal or package-manager proof.
- Use Linux-native window treatment; do not imitate macOS chrome.
- Show setup commands only after explaining the user outcome.

### VocaWin

- Use Windows-native surfaces, type behavior, and installation language.
- Make release availability explicit while the product is not generally
  available.
- Reuse the Voca composition and materials without copying Mac controls.

### VocaGateway

- Lead with “your hardware, shared speech-to-text.”
- Show device pairing, authenticated access, model readiness, and the route from
  recording to transcript.
- Distinguish trusted LAN, private encrypted networking, and public exposure.
- When the dashboard is shown in dark mode, use neutral charcoal rather than
  blue-black.

## Required validation

Before a Voca product site is merged or published, verify all of the following.

### Product truth

- [ ] The primary claim matches current product behavior.
- [ ] Platform availability and release status are current.
- [ ] Privacy language states where processing happens.
- [ ] Optional and required components are distinguished.
- [ ] Limitations that affect setup or use are visible.
- [ ] Product terminology is plain and consistent.

### Structure and accessibility

- [ ] There is exactly one `h1`.
- [ ] In-page links resolve to unique IDs.
- [ ] Keyboard navigation and focus states work.
- [ ] Decorative content is correctly hidden from assistive technology.
- [ ] Informative media has useful alternatives.
- [ ] Reduced-motion mode exposes all content.
- [ ] Contrast meets WCAG AA.

### Visual QA

- [ ] Desktop was inspected at `1440px` or wider.
- [ ] Mobile was inspected at `390×844`.
- [ ] At least one intermediate/tablet width was inspected.
- [ ] There is no horizontal overflow.
- [ ] Important decoration does not collide with content.
- [ ] Product UI is accurate for the represented platform.
- [ ] The page contains no CSS gradients.

### Technical and delivery

- [ ] Local tests and syntax checks pass.
- [ ] Local assets exist and load.
- [ ] External acquisition, documentation, and repository links return the
  expected destination.
- [ ] A production-like deploy was checked, not only the local build.
- [ ] The published HTML and core assets return HTTP 200.
- [ ] Unrelated repository changes were not included.

Useful automated assertions include unique document IDs, matching anchor
targets, local asset existence, the absence of gradient functions, and the
presence of a reduced-motion fallback.

## Pull request expectations

A website-design pull request should include:

- the problem the change solves;
- a short summary of the product story;
- desktop and mobile screenshots;
- commands used for validation;
- the public preview URL when available;
- a note explaining any changed product or privacy claim; and
- only the intended files.

Local checks, preview deployment, production publication, and merge are separate
completion states. Report each one accurately.

## Governance

This standard should evolve through reviewed examples rather than trend chasing.

- Change shared principles in this document through a focused pull request.
- Add approved product assets under `brand/<product>/`.
- Keep app-specific implementation in the app repository.
- Treat the newest approved site as evidence, not automatic precedent.
- When two products need different solutions, preserve the shared principle and
  document the platform-specific reason.
- Revisit claims and external links during release work; both can become stale.

The test for a new Voca site is simple: it should look related to the family,
explain its product more clearly than a generic template could, and tell the
truth about where the user's voice goes.
