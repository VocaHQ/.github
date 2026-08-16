# Voca family brand book

- **Status:** proposed — awaiting Jatin approval
- **Owner:** VocaDesign proposes; Jatin approves; product agents implement in
  their repos
- **Public product truth:** [VocaHQ/vocahq `PRODUCT.md`](https://github.com/VocaHQ/vocahq/blob/main/PRODUCT.md)
- **Web implementation:** [`docs/website-design-standard.md`](../docs/website-design-standard.md)
- **App implementation:** [`docs/app-design-standard.md`](../docs/app-design-standard.md)

This is the parent brand book for the Voca family. Cite it in visual and copy
PRs (`brand/README.md §N`). The two design standards explain how to build sites
and apps; this book explains who Voca is, how we name and sound, how the mark
works, and what is allowed to change.

---

## 1. How to use this book

### 1.1 Hierarchy

| Layer | Document | Owns |
| --- | --- | --- |
| Brand | This file (`brand/README.md`) | Identity, naming, voice, mark rules, family vs product, asset ownership |
| Product truth | `VocaHQ/vocahq` → `PRODUCT.md` | Public status labels, version numbers, shipping calls, processing paths |
| Web | `docs/website-design-standard.md` | Site layout, components, validation |
| App | `docs/app-design-standard.md` | Native app surfaces, states, platform behavior |

If this book and a design standard disagree on identity, naming, voice, color
roles, or logo use, this book wins. If this book and `PRODUCT.md` disagree on
status, shipping, or where audio goes, **`PRODUCT.md` wins**. Do not “fix”
product truth in the brand book.

### 1.2 Ownership and change

1. Propose brand changes here (or in a focused PR that updates this file).
2. Jatin approves.
3. Product agents apply the approved language and assets in their repos.
4. Implementation detail stays in the web/app standards or the product repo —
   do not turn this book into a component library.

### 1.3 Citing

Prefer section numbers: “per brand book §4.2”, “per brand book §7.3”. A later
PR should be able to resolve that reference without guessing.

---

## 2. Who Voca is

Voca is offline / on-device-first speech-to-text across machines you already
own. You speak; useful text lands where you are already typing when the
platform allows it. There is no required Voca account. The software is free and
open source, with the actual license named per project. Voca is a **family of
products**, not a cloud suite and not one universal app.

The family home is VocaHQ ([vocahq.com](https://vocahq.com)). Individual
products ship (or will ship) on their own platforms with honest status and
explicit network boundaries.

---

## 3. Naming

### 3.1 Public casing (exact)

| Name | Role | Never write |
| --- | --- | --- |
| **Voca** | Family name | VOCA as a wordmark; “the Voca app” as if there is one app |
| **VocaHQ** | Org + family site | Voca-HQ, Voca HQ (as the product name) |
| **VocaLinux** | Linux product | Voca Linux; Vocalinux as a public display name |
| **VocaMac** | macOS product | Voca Mac |
| **VocaWin** | Windows product | Voca Win |
| **VocaPhone** | Phone product | Voca Phone |
| **VocaGateway** | Optional self-hosted compute | Voca Gateway as if it were on-device |

`vocalinux` / `vocamac` / lowercase repo and file slugs are fine in paths and
package names. That is not public casing.

### 3.2 Domains

| Domain | Use |
| --- | --- |
| [vocahq.com](https://vocahq.com) | Family headquarters |
| [vocalinux.com](https://vocalinux.com) | VocaLinux |
| [vocamac.com](https://vocamac.com) | VocaMac |
| [vocawin.com](https://vocawin.com) | VocaWin status / future product |
| [vocaphone.vocahq.com](https://vocaphone.vocahq.com) | VocaPhone |

### 3.3 Family vs product identity

- Family surfaces (VocaHQ, org profile, shared docs) speak for **Voca** and
  route to products.
- Product surfaces keep their approved name, mark, and (when approved) accent.
- Do not invent a second family wordmark. Do not rebrand a product as “Voca”
  alone on its own store listing or installer when an approved product name
  exists.

---

## 4. Voice

### 4.1 Character

Warm, precise, human, short. Technically credible without jargon cosplay.
Privacy is **architecture**, not a lock icon. Lead with a memorable heading,
then state the mechanism and the boundary.

Claim pattern: **benefit → mechanism → boundary**.

> Dictate offline. The speech-to-text model runs on this device after it is
> downloaded. A self-hosted gateway remains available when you want different
> models or shared compute.

### 4.2 Preferred phrases

| Prefer | Avoid / ban |
| --- | --- |
| speech-to-text model | unexplained engine jargon in visitor copy |
| free and open source | “free forever” |
| on-device (for the path where audio and the model stay on the device) | calling gateway mode “on-device” |
| self-hosted / optional VocaGateway | collapsing gateway into “local” or “private” without naming the boundary |
| stays on your device *(on-device mode only)* | “stays on your device” when audio leaves for a gateway |
| insert / land text where you are typing | vague “AI magic” outcomes |
| exact status labels from `PRODUCT.md` | inventing “stable”, “GA”, or shipping claims |

### 4.3 Banned patterns

- “AI-powered” as decoration or positioning.
- “Military-grade privacy,” “works everywhere,” or other absolutisms the
  platforms cannot support.
- “No gateway” when the gateway is optional.
- “Local” or “private” as a soft synonym that hides network travel.
- Fabricated screenshots, release assets, customer proof, benchmarks, usage
  numbers, feature parity, or hard-coded star counts.

---

## 5. Product truth in copy

### 5.1 Source of truth

`VocaHQ/vocahq` → [`PRODUCT.md`](https://github.com/VocaHQ/vocahq/blob/main/PRODUCT.md)
owns public status, version numbers, and shipping calls. This book may **quote**
status language. It must never invent or update it. If a product site and
`PRODUCT.md` disagree, cite `PRODUCT.md`.

Verified matrix (labels copied exactly; do not paraphrase status):

| Product | Status | Notes |
| --- | --- | --- |
| VocaLinux | Available now | Linux X11/Wayland; current release v0.15.0; AGPL-3.0 |
| VocaMac | Beta | macOS 14+ Apple Silicon; WhisperKit/Core ML; AGPL-3.0 |
| VocaWin | Coming soon | No public installer or release; AGPL-3.0-or-later in repo |
| VocaPhone | Android beta / iOS source build | Android 13+ public beta; iOS 17+ build from source; gateway optional; AGPL-3.0 |
| VocaGateway | Early | Optional self-hosted compute; never on-device; AGPL-3.0 |

> **Footnote — VocaMac status tension:** some public surfaces (for example
> vocamac.com copy) may read like a “stable” release. Per `PRODUCT.md`
> (verified 2026-08-14), public status remains **Beta**. Defer to `PRODUCT.md`
> until that file changes.

### 5.2 Non-negotiable product principles

From `PRODUCT.md`:

1. On-device speech-to-text first.
2. Free and open source, with the actual license named per project.
3. Text lands where the user is already typing when the platform allows it.
4. No required Voca account.
5. Honest platform status and explicit network boundaries.
6. Built in public.

### 5.3 Two processing paths — never collapse these

**On-device.** After a model is downloaded, the speech-to-text model and audio
stay on the phone or computer. A gateway is not required.

**Optional VocaGateway.** When someone deliberately configures it, audio leaves
the client and travels to the self-hosted machine they selected. The gateway
runs a local speech engine and returns the transcript. Recommend a trusted LAN,
Tailscale / encrypted private network, or HTTPS. **Do not describe this path as
on-device.** VocaGateway is never on-device.

### 5.4 Shipping honesty

- Never imply VocaWin ships.
- Do not fabricate screenshots or release assets for unshipped surfaces.
- Name licenses per project; do not invent a single family license line that
  erases differences.

---

## 6. Visual thesis

Voca turns speech into useful text on hardware the user controls.

**Feel:** human not corporate; tactile not glossy; calm not empty; technically
credible not abstract; privacy-first because the boundary is visible.

**Materials:** warm paper, dark ink, one product accent, solid fills, thin
borders, restrained shadows.

**Principles (tight):**

1. Show the product doing the work — real UI, not abstract decoration.
2. Make privacy concrete — architecture, paths, and boundaries in plain words.
3. Flat and tactile — no CSS gradients (linear / radial / conic / mesh).
4. No glass for ordinary content; no glowing orbs; no fake dashboards.
5. No stock people, anonymous 3D, or unsupported “AI-powered” claims.
6. Apps stay native to the OS. Family resemblance is hierarchy, materials,
   color roles, voice, and behavior — not identical chrome.
7. Every element has a job.

---

## 7. Color

### 7.1 Family foundation (canonical)

Prefer these family tokens. Encode them; do not reinvent.

| Token | Hex | Role |
| --- | --- | --- |
| paper / canvas | `#F4F1E8` | Main canvas |
| paper-deep | `#EBE5D8` | Recessed / alternate surface |
| paper-bright / surface | `#FFFDF7` | Cards, windows, raised surfaces |
| ink | `#14231C` | Primary text and strong borders |
| muted | `#68726C` | Supporting copy (**family token**) |
| faint | `#7C847D` | Quieter secondary (vocahq site today) |
| line | `#C9C8BD` | Quiet borders (**family token**) |
| line-dark | `#9EA59F` | Stronger outlines |
| sun / focus | `#E9B949` | Focus, annotation, small emphasis |
| decorative window red | `#DE6A57` | Small physical web detail only |

**Local variants to reconcile later (do not silently “fix” sites):**

| Token | Family token | vocahq `DESIGN.md` today |
| --- | --- | --- |
| muted | `#68726C` | `#58625C` |
| line | `#C9C8BD` | `#d5d0c4` |

Document both. Prefer the website-design-standard values as the family tokens.
Treat the vocahq site values as a local variant until a deliberate reconciliation
PR lands.

### 7.2 Brand accent (approved today)

| Token | Hex | Role |
| --- | --- | --- |
| brand teal | `#0F6B57` | Family / VocaHQ / VocaPhone accent |
| brand-dark | `#0B493D` | Pressed / deep accent |
| brand-soft / mint | `#CFE9DC` | Soft accent surface |
| mint-soft | `#E5F2EB` | Quieter mint surface |
| dark-ink | `#0B1A15` | Dark sections; mark on paper |
| mark-on-teal fill | `#F2F6F2` | Mic mark on teal circle / icon |

VocaPhone dark-appearance accent reference (apps): accent `#77D0B2`, text on
accent `#003827`. See the app design standard for semantic mapping.

### 7.3 Semantic app colors

From the app design standard — encode, do not invent:

| Role | Light | Dark |
| --- | --- | --- |
| Recording / error | `#C73D38` | `#FF736D` |
| Warning / processing | `#A86108` | `#F0B35A` |

**Recording stays red.** Do not recolor live recording to brand teal.

### 7.4 One-accent rule

- Most of a surface is paper, ink, and **one** accent.
- Until a product has an approved accent under `brand/<product>/`, use family
  teal `#0F6B57`.
- Today the only approved accent in this repo is the VocaPhone / family teal
  set above. Other products do **not** yet have approved distinct accents —
  do not invent them in a one-off CSS file.
- Per-product accents are allowed later and must be derived from approved brand
  material checked into `brand/<product>/`.

---

## 8. Typography

### 8.1 Sites

No remote webfont downloads. Distinction comes from scale, weight, spacing, and
composition.

| Role | Stack |
| --- | --- |
| Display | `"Avenir Next", "Helvetica Neue", ui-sans-serif, system-ui, sans-serif` |
| Body | system UI stack (`ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif`) |
| Mono | system monospace for technical labels |

Approved product names keep their official casing even when nearby editorial
headlines are lowercase.

### 8.2 Apps

System-first typography (SF, Segoe, platform UI fonts). No remote font
dependency. Prefer platform title and body behaviors over marketing display
scale inside installed apps.

---

## 9. Logo and mark

### 9.1 What the mark is

The family mark is a **stylized microphone**: capsule, stand, and side brackets.
It is **not** a letterform V.

### 9.2 Approved treatments

| Treatment | Spec | Use |
| --- | --- | --- |
| Logo lockup / app icon | Mic on teal circle or square `#0F6B57` with mark fill `#F2F6F2` | Default identity on light marketing and store icons |
| Standalone mark on paper | Mark in `#0B1A15` | Headers and ink-on-paper placements |
| Dark / inverse variants | Approved dark SVGs/PNGs only | Dark sections; do not freestyle recolors |

### 9.3 Clear space and size

- Keep clear space around the mark at least equal to the thickness of the mic
  stand stroke in the artwork (visually: a quiet margin on all sides — do not
  crowd with badges, pills, or competing icons).
- Minimum practical size: keep the full mic readable. As a working floor, do
  not render the circular lockup smaller than **24 CSS pixels** on the web or
  the platform’s smallest recommended app-icon slot without testing legibility.
- Do not crop the brackets or stand.

### 9.4 Do not

- Redraw or “improve” the mic.
- Recolor the mark outside approved fills.
- Add unapproved wordmarks, taglines baked into the SVG, or drop shadows on the
  mark.
- Use the teal circle as a generic bullet, avatar, or decoration unrelated to
  the brand mark.
- Stretch, rotate for decoration, or place the mark on busy photography that
  destroys contrast.

### 9.5 Where the files live

| Set | Location | Notes |
| --- | --- | --- |
| Family / VocaHQ | [`brand/vocahq/`](vocahq/) in this repo (copied from `VocaHQ/vocahq` `web/assets/brand/`) | `voca-logo.svg`, `voca-mark.svg`, `voca-app-icon.svg`, PNGs, dark variants |
| Upstream source | `VocaHQ/vocahq` → `web/assets/brand/` | Remains a shipping source for the family site; keep copies in sync when marks change |
| VocaPhone | [`brand/vocaphone/`](vocaphone/) | Approved logo, mark, app icon, 512 PNGs; same mic-on-teal geometry; `aria-label="vocaphone"` |

---

## 10. App icons

- Default construction: mic mark on teal (`#0F6B57`) square or circle as already
  established in the approved SVGs.
- No gradients, fake gloss, or skeuomorphic shine.
- Keep platform mask-safe: important geometry stays inside the safe area; do not
  rely on squircle corners that iOS/Android will clip away.
- Do not place marketing screenshots or unapproved product chrome inside the
  icon.

---

## 11. Imagery

- Prefer **real product UI**, platform-true.
- Marketing window chrome may use the paper language; the product surface inside
  must stay authentic to the OS.
- No stock people. No anonymous 3D devices as the main story.
- No fake VocaWin screenshots. No fabricated proof for unshipped states.
- Code-native diagrams may explain a flow; do not present them as screenshots.

---

## 12. Motion

- Motion **confirms** state or adds quiet life to product proof. It does not
  decorate empty space.
- Keep transitions short; prefer opacity and gentle translation over bounce.
- Honor `prefers-reduced-motion` (and the page/app being backgrounded): stop or
  replace non-essential motion.
- Essential content and actions must work with motion off.

---

## 13. Asset inventory

| Asset | Status | Location |
| --- | --- | --- |
| Family brand book | This document (proposed) | `brand/README.md` |
| Family / VocaHQ marks | Present (copied) | `brand/vocahq/` · upstream `VocaHQ/vocahq/web/assets/brand/` |
| VocaPhone marks + 512 PNGs | Approved | `brand/vocaphone/` |
| VocaPhone / family accent | Approved | Teal set in §7.2 |
| VocaLinux mark + accent | **MISSING / TBD** | — |
| VocaMac mark + accent | **MISSING / TBD** | — |
| VocaWin mark + accent | **MISSING / TBD** | — |
| VocaGateway mark + accent | **MISSING / TBD** | — |
| Web design standard | Adopted | `docs/website-design-standard.md` |
| App design standard | Proposed companion | `docs/app-design-standard.md` |

Checklist when a product gets its own identity:

1. Land approved SVG/PNG under `brand/<product>/`.
2. Record the accent hexes in that folder and in §7 / §13 of this book.
3. Update product sites and apps to reference the approved files — do not leave
   one-off CSS accents as the source of truth.

---

## 14. Do / don’t

| Do | Don’t |
| --- | --- |
| Cite `PRODUCT.md` for status | Invent shipping or paraphrase status labels |
| Use exact public casing | Write “Voca Phone”, “Vocalinux”, “the Voca app” |
| Say “speech-to-text model” | Lead with unexplained engine names |
| Say “free and open source” | Say “free forever” |
| Keep on-device and gateway paths distinct | Call gateway traffic “on-device” |
| Use paper / ink / one accent | Introduce gradients, glass chrome, glow orbs |
| Use approved mic mark files | Redraw, recolor, or bulletize the teal circle |
| Use family teal until a product accent is approved | Invent per-product palettes in CSS |
| Show real UI | Fake VocaWin or stock-people proof |
| Motion that confirms | Motion that merely sparkles |
| Point PRs at `brand/README.md §N` | Treat the design standards as the brand parent |

---

## 15. Review checklist

Use this on design and copy PRs (in addition to the web/app validation lists):

- [ ] Cites this brand book section when changing identity, voice, color, or mark.
- [ ] Product names use exact public casing (§3).
- [ ] Status labels match `PRODUCT.md` exactly (§5.1); no invented shipping.
- [ ] On-device vs VocaGateway language is not collapsed (§5.3).
- [ ] “Stays on your device” is scoped to on-device mode only.
- [ ] Says “speech-to-text model” and “free and open source” where relevant.
- [ ] No “AI-powered”, “free forever”, fabricated proof, or hard-coded stars.
- [ ] Colors use family tokens; accent is approved or defaults to family teal (§7).
- [ ] Recording remains red; warning/processing use semantic roles (§7.3).
- [ ] No gradients; solid fills; restrained shadows (§6).
- [ ] Logo/mark from approved files; clear space and no recolor (§9).
- [ ] App icon stays mask-safe and ungilded (§10).
- [ ] Imagery is platform-true; no fake unshipped UI (§11).
- [ ] Motion confirms and respects reduced motion (§12).
- [ ] New product accents or marks, if any, land under `brand/<product>/` (§13).

---

## Governance

VocaDesign keeps this book sharp and citeable. Jatin approves material changes.
Product agents implement; they do not silently fork identity in a CSS file.

When in doubt: tell the truth about where the user’s voice goes, use the
approved mic, and keep the desk quiet enough that the product can speak.
