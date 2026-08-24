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

### 1.4 How other repos consume this book

Product agents own their product repos. They do not fork identity into a local
copy of this book.

**Rules for product repos:**

1. Cite `brand/README.md §N` in visual and copy PRs (example: “per brand book
   §5.3 — gateway is never on-device”).
2. Shared assets live in **this** org repo under `brand/<product>/` (and
   `brand/vocahq/` for family marks). Do not invent accents or redraw marks in
   a product CSS file.
3. **Do not copy** this brand book into product repos. Link to it.
4. Prefer stable raw links for the book and for SVG/PNG assets, for example:

   - Book:
     `https://raw.githubusercontent.com/VocaHQ/.github/main/brand/README.md`
   - Family logo:
     `https://raw.githubusercontent.com/VocaHQ/.github/main/brand/vocahq/voca-logo.svg`
   - VocaPhone mark:
     `https://raw.githubusercontent.com/VocaHQ/.github/main/brand/vocaphone/vocaphone-mark.svg`

   Until this PR merges, substitute the working branch name for `main` when you
   need the proposed text. After merge, use `main`.

5. Implementation detail (layout, components, platform chrome) stays in the
   web/app standards or the product repo. Brand identity stays here.

---

## 2. Who Voca is

Voca is offline / on-device-first speech-to-text across machines you already
own. You speak; useful text lands where you are already typing when the
platform allows it. There is no required Voca account. The software is free and
open source, with the actual license named per project. Voca is a **family of
products**, not a cloud suite and not one universal app.

The family home is VocaHQ ([vocahq.com](https://vocahq.com)). Individual
products ship (or will ship) on their own platforms with honest status and
explicit network boundaries. **VocaGateway** is optional self-hosted
infrastructure, not a client and not on-device.

---

## 3. Naming

### 3.1 Canonical public names

`PRODUCT.md` wins for canonical display names:

| Name | Role |
| --- | --- |
| **Voca** | Family |
| **VocaHQ** | Org + family site |
| **VocaLinux** | Linux product |
| **VocaMac** | macOS product |
| **VocaWin** | Windows product |
| **VocaPhone** | Phone product |
| **VocaGateway** | Optional self-hosted compute (infrastructure, not a client) |

These are not interchangeable: **Voca ≠ VocaHQ ≠ VocaPhone ≠ VocaGateway**.

Never in public copy: “the Voca app” as if there is one app; **VOCA** as a
wordmark; **Voca-HQ**; **VocaServer**; **Local Flow** (except uninstall notes
that must match existing package strings); treating **vocaphone-server** as a
product name.

### 3.2 Known conflicts and exceptions (do not “fix” in this PR)

| Fact | How this book treats it |
| --- | --- |
| Canonical public name is **VocaLinux** (`PRODUCT.md`) | Official name for new family copy and org surfaces |
| vocalinux.com H1, Linux README, and vocalinux `web/PRODUCT.md` currently say **Vocalinux** | **Known site exception** to reconcile later. Flagged only — **do not rename vocalinux.com in this PR.** |
| Repo slug `vocalinux` | Fine in paths and package names. Not public casing. |
| Lowercase **vocaphone** | Established editorial / logo treatment (site H1, `aria-label`). Preserve it. Not a rename. |
| Lowercase **vocawin** in a hero | Editorial treatment only. Not a rename of **VocaWin**. |
| Other repo / path slugs (`vocamac`, …) | Fine in paths and package names. Not public casing. |

### 3.3 Domains

| Domain | Use |
| --- | --- |
| [vocahq.com](https://vocahq.com) | Family headquarters |
| [vocalinux.com](https://vocalinux.com) | VocaLinux product site (**Vocalinux** spelling is a known site exception — §3.2) |
| [vocamac.com](https://vocamac.com) | VocaMac |
| [vocawin.com](https://vocawin.com) | VocaWin |
| [vocaphone.vocahq.com](https://vocaphone.vocahq.com) | VocaPhone |

### 3.4 Family vs product identity

- Family surfaces (VocaHQ, org profile, shared docs) speak for **Voca** and
  route to products.
- Product surfaces keep their approved name, mark, and (when approved) accent.
- **VocaGateway** is infrastructure (optional self-hosted compute), not a
  client app and not on-device.
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
| on-device *(path where audio and the model stay on the device after download)* | collapsing **on-device / local / private / self-hosted** into one soft word |
| self-hosted / optional VocaGateway | calling gateway mode “on-device” or “local” without naming the boundary |
| stays on your device *(on-device transcription after the model is present)* | “100% offline,” “never touches the network,” or “stays on your device” during download / update check / gateway mode |
| insert / land text where you are typing | vague “AI magic” outcomes |
| AGPL-3.0 or **AGPL-3.0-or-later** *(exact string per project)* | flattening every project to “AGPL-3.0” when a repo differs |
| exact status labels from `PRODUCT.md` | inventing “stable”, “GA”, or shipping claims |

### 4.3 Copy non-negotiables

These are hard stops for visitor-facing copy:

1. **No “AI-powered” fluff** — do not use “AI-powered” as decoration or
   positioning.
2. **No 100% offline overclaim** — model download and update check are real
   network actions. “Stays on your device” applies only to **on-device
   transcription after the model is present**, not to setup, download, or
   update flows.
3. **Gateway is optional self-hosted compute** — never call VocaGateway
   on-device.
4. **No Voca account** — do not imply sign-in is required.
5. **Name the actual license per project** — do not invent a single family
   license line. Today that usually means **AGPL-3.0**, except **VocaWin**,
   which is **AGPL-3.0-or-later** in the repository. Do not flatten VocaWin to
   AGPL-3.0.

### 4.4 Also banned

- “Military-grade privacy,” “works everywhere,” or other absolutisms the
  platforms cannot support.
- “No gateway” when the gateway is optional.
- “Local” or “private” as a soft synonym that hides network travel.
- “Free forever.”
- **VocaServer**, **Local Flow** (except uninstall notes), and
  **vocaphone-server** as a public product name.
- Fabricated screenshots, release assets, customer proof, benchmarks, usage
  numbers, feature parity, or hard-coded star counts.

---

## 5. Product truth in copy

### 5.1 Source of truth

`VocaHQ/vocahq` → [`PRODUCT.md`](https://github.com/VocaHQ/vocahq/blob/main/PRODUCT.md)
owns public status, version numbers, and shipping calls. This book may **quote**
status language. It must never invent or update it. If a product site and
`PRODUCT.md` disagree, cite `PRODUCT.md`.

Verified public matrix (labels for current copy; do not paraphrase status; do
not invent shipping). Always defer to `PRODUCT.md` if it moves:

| Product | Status (public copy today) | Notes |
| --- | --- | --- |
| VocaLinux | Available now | Current release **v0.15.0**; Linux X11/Wayland; AGPL-3.0 |
| VocaMac | Beta | **macOS 14+** Apple Silicon; AGPL-3.0 |
| VocaWin | Beta | Unsigned NSIS/MSI on GitHub Releases; latest tag **v0.1.0-alpha.3**. SmartScreen expected. **AGPL-3.0-or-later** in repo |
| VocaPhone | Android beta / iOS source build | **Android 13+** public beta; **iOS 17+** build from source; gateway optional; AGPL-3.0 |
| VocaGateway | Early | Optional self-hosted compute; **never on-device**; infrastructure, not a client; AGPL-3.0 |

> **Footnote — VocaMac:** Public status is **Beta** per `PRODUCT.md`. If
> vocamac.com (or similar) says “stable” or shows a version such as v0.7.2, still
> **defer to `PRODUCT.md` (Beta)**. Do not invent shipping or status language
> beyond what `PRODUCT.md` says.

### 5.2 Non-negotiable product principles

From `PRODUCT.md`:

1. On-device speech-to-text first.
2. Free and open source, with the actual license named per project.
3. Text lands where the user is already typing when the platform allows it.
4. No required Voca account.
5. Honest platform status and explicit network boundaries.
6. Built in public.

### 5.3 Two processing paths — never collapse these

**On-device.** After a model is downloaded, on-device transcription keeps the
speech-to-text model and audio on the phone or computer. A gateway is not
required for this path. Model download and update check still use the network —
do not call the product “100% offline.”

**Optional VocaGateway.** When someone deliberately configures it, audio leaves
the client and travels to the self-hosted machine they selected. The gateway
runs a local speech engine and returns the transcript. Recommend a trusted LAN,
Tailscale / encrypted private network, or HTTPS. **Do not describe this path as
on-device.** VocaGateway is optional self-hosted compute and is never on-device.

### 5.4 Shipping honesty

- Never imply VocaWin is signed or a Store app. Tester builds are unsigned. SmartScreen is expected. Do not invent a `v0.1.0-beta.1` tag.
- Do not fabricate screenshots or release assets for unshipped surfaces.
- Name licenses per project; **VocaWin is AGPL-3.0-or-later**, not flattened to
  AGPL-3.0.
- No required Voca account in any product story.

---

## 6. Visual thesis

Voca turns speech into useful text on hardware the user controls.

**Feel:** human not corporate; tactile not glossy; calm not empty; technically
credible not abstract; privacy-first because the boundary is visible.

**Materials:** warm paper, dark ink, one product accent, solid fills, thin
borders, restrained shadows. (The VocaLinux *site* is a known visual site
exception — iron-white / `#1a7f4e`, never warm cream/beige as the default —
§7.5. Not a new family default.)

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

### 7.1 Family foundation (canonical page tokens)

Encode the adopted website-design-standard table. Do not invent a second
official palette.

| Token | Hex | Role |
| --- | --- | --- |
| paper / canvas | `#F4F1E8` / `#f4f1e8` | Main canvas |
| paper-deep | `#EBE5D8` / `#ebe5d8` | Recessed / alternate surface |
| paper-bright / surface | `#FFFDF7` / `#fffdf7` | Cards, windows, raised surfaces |
| ink | `#14231C` / `#14231c` | Primary text and strong borders |
| muted | `#68726C` / `#68726c` | Supporting copy (**family token**) |
| line | `#C9C8BD` / `#c9c8bd` | Quiet borders (**family token**) |
| line-dark | `#9EA59F` / `#9ea59f` | Stronger outlines |
| sun / focus | `#E9B949` / `#e9b949` | Focus, annotation, small emphasis |
| decorative window red | `#DE6A57` / `#de6a57` | Small physical web detail only |

### 7.2 Live-site drift (not a second official palette)

Some live sites currently diverge. Document as **drift to reconcile later** —
do not treat these as approved family tokens, and do not silently “fix” the
sites in this PR:

| Drift | Seen today | Family token |
| --- | --- | --- |
| muted | vocahq / vocamac `#58625C` | `#68726C` |
| line | vocahq `#d5d0c4` | `#C9C8BD` |
| faint | vocahq `#7c847d` | (vocahq-local only; not a family page token) |

### 7.3 Logo-only fills (not CSS page tokens)

| Fill | Hex | Use |
| --- | --- | --- |
| mark on teal | `#F2F6F2` | Mic mark on the teal circle / icon |
| mark on paper / dark-ink | `#0B1A15` | Standalone mark on paper; dark-ink sections |

Do not promote these into ordinary page CSS tokens.

### 7.4 Approved product accent (only)

| Role | Hex | Notes |
| --- | --- | --- |
| Brand teal | `#0F6B57` / `#0f6b57` | **Only** approved product accent today (VocaPhone / family) |
| Brand-dark | `#0B493D` / `#0b493d` | Pressed / deep accent in the approved set |
| Brand-soft / mint | `#CFE9DC` / `#cfe9dc` | Soft accent surface in the approved set |
| Mint-soft | `#E5F2EB` / `#e5f2eb` | Quieter mint surface |
| App dark accent (VocaPhone) | `#77D0B2` | Dark-appearance accent; text on accent `#003827` |

**Current reuse (not approved unique accents):** VocaMac, VocaWin, and VocaHQ
surfaces currently reuse family teal `#0F6B57`. Document that as current
practice. Do not call those unique product accents.

### 7.5 VocaLinux visual site exception (document only — do not migrate)

vocalinux.com is a **known visual site exception**. It is **not** family
paper/cream. Do not add a Linux accent to the approved family palette. Do not
migrate vocalinux.com in this PR.

- Foundation: **iron-white / near-black** (explicitly not warm paper).
- Accent: `#1a7f4e` (deep `#14663e`, dark `#50c878`).
- Their rule (paraphrased / quoted in spirit): **never warm cream/beige as the
  default.**
- Linux mark assets live in the **vocalinux** repo under `web/public/`, not
  under `brand/vocalinux/` in this org repo. Status: **documented exception +
  MISSING from this repo’s `brand/` folder.**

Family surfaces that speak about Linux still use family tokens. The Linux *site*
keeps its existing exception in place until a deliberate reconciliation lands.

### 7.6 VocaGateway

Approved host marks live in [`brand/vocagateway/`](vocagateway/). The
microphone is the family geometry from `brand/vocahq/` (capsule, cradle,
stem, base, two side brackets). The chassis is a 1U, a three-unit stack,
a standing tower, or a two-bay box so the icon reads as a host you run
yourself, not another client.

- `vocagateway-1u.svg` is the default app / favicon mark.
- `vocagateway-rack.svg` is the three-unit hardware lockup. Do not use it under 64px.
- `vocagateway-tower.svg` is a standing case.
- `vocagateway-twobay.svg` is a two-bay chassis.

Plate `#0F6B57`. No unique Gateway accent. Dark-first dashboard surfaces
still use **neutral charcoal**.

### 7.7 Semantic app colors

From the app design standard — encode, do not invent:

| Role | Light | Dark |
| --- | --- | --- |
| Recording / error | `#C73D38` | `#FF736D` |
| Warning / processing | `#A86108` | `#F0B35A` |

**Recording stays red.** Do not recolor live recording to brand teal.

### 7.8 One-accent rule

- Most of a surface is paper, ink, and **one** accent.
- The only approved product accent in this repo today is VocaPhone / family
  teal `#0F6B57`.
- Until a product has an approved accent under `brand/<product>/`, use family
  teal (except the documented VocaLinux *site* exception in §7.5, which this
  PR does not change).
- Do not invent per-product palettes in a one-off CSS file.

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

### 9.2 Current shared geometry

The **same microphone geometry** is used today for **Voca**, **VocaHQ**,
**VocaPhone**, **VocaMac**, and **VocaWin**. Labels differ
(`aria-label="Voca"` vs `aria-label="vocaphone"`). Document that shared mark;
**do not draw new product marks** in this PR.

| Set | Status | Location / notes |
| --- | --- | --- |
| Family / VocaHQ | Present in this repo | [`brand/vocahq/`](vocahq/) (copied from `VocaHQ/vocahq` `web/assets/brand/`) |
| VocaPhone | Approved in this repo | [`brand/vocaphone/`](vocaphone/) — keep as-is |
| VocaMac / VocaWin | Same shared mic geometry; Win installer bitmaps in this repo | [`brand/vocawin/installer/`](vocawin/installer/). No unique Win accent. |
| VocaLinux | **Separate** microphone assets in vocalinux `web/public/`; **MISSING** from `brand/` here | Documented exception; do not replace in this PR |
| VocaGateway | Approved host marks (family mic on 1U, stack, tower, or two-bay) | [`brand/vocagateway/`](vocagateway/) |

### 9.3 Approved treatments (shared mic)

| Treatment | Spec | Use |
| --- | --- | --- |
| Logo lockup / app icon | Mic on teal circle or square `#0F6B57` with mark fill `#F2F6F2` | Default identity on light marketing and store icons |
| Standalone mark on paper | Mark in `#0B1A15` | Headers and ink-on-paper placements |
| Dark / inverse variants | Approved dark SVGs/PNGs only | Dark sections; do not freestyle recolors |

### 9.4 Clear space and size

- Keep clear space around the mark at least equal to the thickness of the mic
  stand stroke in the artwork (visually: a quiet margin on all sides — do not
  crowd with badges, pills, or competing icons).
- Minimum practical size: keep the full mic readable. As a working floor, do
  not render the circular lockup smaller than **24 CSS pixels** on the web or
  the platform’s smallest recommended app-icon slot without testing legibility.
- Do not crop the brackets or stand.

### 9.5 Do not

- Redraw or “improve” the mic.
- Recolor the mark outside approved fills.
- Add unapproved wordmarks, taglines baked into the SVG, or drop shadows on the
  mark.
- Use the teal circle as a generic bullet, avatar, or decoration unrelated to
  the brand mark.
- Stretch, rotate for decoration, or place the mark on busy photography that
  destroys contrast.
- Invent distinct Mac / Win marks without landing approved files under
  `brand/<product>/`. Gateway already has an approved pack in `brand/vocagateway/`.

---

## 10. App icons

- Default construction: mic mark on teal (`#0F6B57`) square or circle as already
  established in the approved SVGs.
- VocaGateway is the one exception: same family mic, punched through a host
  chassis in `brand/vocagateway/` (1U, three-unit stack, tower, or two-bay).
  Use the 1U at small sizes.
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
| Asset library | How studies and approved files are filed | [`brand/LIBRARY.md`](LIBRARY.md) |
| Promo shelf | Social cards, post drafts, family catalog PDF | [`brand/promo/`](promo/) |
| Family / VocaHQ marks | Present (copied); shared mic geometry | `brand/vocahq/` · upstream `VocaHQ/vocahq/web/assets/brand/` |
| VocaPhone marks + 512 PNGs | Approved; shared mic geometry; `aria-label="vocaphone"` | `brand/vocaphone/` (keep as-is) |
| VocaPhone / family accent | **Only** approved product accent | Teal `#0F6B57` (+ app dark `#77D0B2`) — §7.4 |
| VocaMac / VocaWin marks | Same shared mic geometry in product surfaces; Win installer bitmaps approved | Reuse family mark; unique accents **not** approved. Win installer: [`brand/vocawin/installer/`](vocawin/installer/) |
| VocaMac / VocaWin / VocaHQ accent | Currently reuse family teal | Current practice, **not** approved unique accents |
| VocaLinux marks | **MISSING** from this repo’s `brand/` folder; live in vocalinux `web/public/` | Documented exception — do not migrate here |
| VocaLinux site palette | Visual **site exception**: iron-white / `#1a7f4e` …; never warm cream/beige default | §7.5; not a family accent |
| VocaGateway host marks | Approved; family mic on 1U, stack, tower, or two-bay; family teal plate | `brand/vocagateway/` · no unique accent; dark-first = charcoal |
| Web design standard | Adopted | `docs/website-design-standard.md` |
| App design standard | Proposed companion | `docs/app-design-standard.md` |

Checklist when a product gets its own identity:

1. Land approved SVG/PNG under `brand/<product>/`.
2. Record the accent hexes in that folder and in §7 / §13 of this book.
3. Update product sites and apps to reference the approved files — do not leave
   one-off CSS accents as the source of truth.
4. Do not invent resolutions for the Vocalinux naming site exception or the
   Linux visual site exception here — those wait on deliberate follow-up.

---

## 14. Do / don’t

| Do | Don’t |
| --- | --- |
| Cite `PRODUCT.md` for status | Invent shipping or paraphrase status labels |
| Link this book / assets via raw.githubusercontent.com (§1.4) | Copy the brand book into product repos |
| Use canonical names; treat **Vocalinux** on vocalinux.com as a known site exception (§3.2) | Rename vocalinux.com here; write “Voca Phone”, “the Voca app”, or “VocaServer” |
| Say “speech-to-text model” | Lead with unexplained engine names |
| Say “free and open source”; name the **exact** license (VocaWin = AGPL-3.0-or-later) | Say “free forever” or “AI-powered”; flatten licenses |
| Scope “stays on your device” to on-device transcription after the model is present | Claim “100% offline”; collapse on-device / local / private / self-hosted |
| Keep on-device and gateway paths distinct | Call gateway traffic “on-device”; treat Gateway as a client |
| Use family paper tokens + approved teal | Bless Linux iron-white accents as family; invent Mac/Win accents |
| Use the shared approved mic mark files; Gateway uses `brand/vocagateway/` | Redraw the mic; invent a second Gateway chassis |
| Show real UI | Fake VocaWin or stock-people proof |
| Motion that confirms | Motion that merely sparkles |
| Point PRs at `brand/README.md §N` | Treat the design standards as the brand parent |

---

## 15. Review checklist

Use this on design and copy PRs (in addition to the web/app validation lists):

- [ ] Cites this brand book section when changing identity, voice, color, or mark (§1.3 / §1.4).
- [ ] Does not copy the brand book into the product repo; links instead (§1.4).
- [ ] Canonical names used; **Vocalinux** on vocalinux.com is a known **site exception** (§3.2); preserve vocaphone / vocawin editorial; no VocaServer / vocaphone-server-as-product.
- [ ] Status labels match `PRODUCT.md` / §5.1 only; VocaMac public copy is **Beta**; defer to PRODUCT.md if a site says otherwise.
- [ ] On-device vs VocaGateway language is not collapsed; Gateway is infrastructure, never on-device (§5.3).
- [ ] “Stays on your device” is scoped to on-device transcription after the model is present; no “100% offline” overclaim (§4.3).
- [ ] Says “speech-to-text model” and “free and open source”; names the actual license (VocaWin = AGPL-3.0-or-later) (§4.3).
- [ ] No “AI-powered”, “free forever”, required Voca account, fabricated proof, or hard-coded stars (§4.3 / §4.4).
- [ ] Does not bless Linux site accents as family or invent Mac/Win/Gateway accents; Linux iron-white / `#1a7f4e` remains a visual site exception (§7.5).
- [ ] Colors use family tokens; only approved accent is family/VocaPhone teal unless `brand/<product>/` exists (§7.1 / §7.4); Linux visual site exception left alone (§7.5).
- [ ] Recording remains red; warning/processing use semantic roles (§7.7).
- [ ] No gradients; solid fills; restrained shadows (§6).
- [ ] Logo/mark from approved shared mic files; Gateway uses `brand/vocagateway/`; clear space and no recolor (§9).
- [ ] App icon stays mask-safe and ungilded (§10).
- [ ] Imagery is platform-true; no fake unshipped UI (§11).
- [ ] Motion confirms and respects reduced motion (§12).
- [ ] New product accents or marks, if any, land under `brand/<product>/` (§13).

---

## Governance

VocaDesign keeps this book sharp and citeable. Jatin approves material changes.
Product agents own their repos, cite `brand/README.md §N`, and link shared
assets from this repo — they do not copy the book or silently fork identity in
a CSS file.

When in doubt: tell the truth about where the user’s voice goes, use the
approved mic, and keep the desk quiet enough that the product can speak.
