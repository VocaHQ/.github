# Voca app design standard

- Status: proposed companion standard
- Parent standard: [Voca web design standard](https://github.com/VocaHQ/.github/blob/main/docs/website-design-standard.md)
- Applies to: VocaPhone, VocaMac, VocaLinux, VocaWin, VocaGateway, and future native Voca products

## Purpose

Voca products should feel like members of the same family before someone reads
the logo. They should share a point of view without pretending that iOS,
Android, macOS, Windows, and Linux use the same controls.

This document adapts the Voca web design language to installed applications. It
covers visual direction, platform behavior, navigation, typography, color,
interaction, recording and transcription states, accessibility, content, and
review. It is a companion to the web standard, not a replacement for the
platform design guidance or a requirement to copy the marketing site into an
app.

The goal is a family of apps that feels:

- human rather than corporate;
- tactile rather than glossy;
- calm rather than empty;
- technically credible rather than abstract;
- privacy-first because the processing boundary is visible;
- native to the current operating system; and
- comfortable enough for daily work.

## Non-negotiables

- Use the exact approved product name, logo, app icon, and product accent.
- Keep controls, navigation, menus, windows, keyboard behavior, and system
  integration faithful to the operating system.
- Lead each screen with the task or state that matters now.
- State where recording and speech-to-text happen. Distinguish on-device,
  self-hosted gateway, and external-service paths.
- Use warm neutral or neutral-charcoal foundations, one product accent, solid
  fills, and no gradients.
- Reserve red, amber, and other semantic colors for states that need them.
- Prefer native controls and behaviors to custom imitations.
- Make essential content and actions work without animation, decoration, or
  color.
- Support the platform's accessibility settings from the beginning.
- Validate real product states on the platforms and devices where they ship.

## The design thesis

Voca turns speech into useful text on hardware the user controls. The app
interface should make that relationship understandable without turning routine
dictation into a technical diagram.

Use clear hierarchy, system typography, warm or neutral surfaces, thin borders,
real recording and transcript states, concise technical annotations, and one
restrained product accent. The result should feel like a well-made native tool:
quiet when idle, unmistakable while recording, honest while processing, and
helpful when recovery is needed.

Avoid generic software styling: gradient meshes, glowing accents, glass panels
for ordinary content, fake dashboards, excessive pills, decorative charts,
anonymous illustrations, and unsupported “AI-powered” claims.

## Core principles

### 1. Put the current job first

The most important action or state should be visible without searching:

- a keyboard makes typing and dictation immediately available;
- a recorder makes listening, elapsed time, and Finish unmistakable;
- a setup screen shows the next incomplete step and its action;
- a model screen shows download, integrity, and readiness;
- a gateway screen shows reachability, authentication, and model state; and
- a transcript screen puts the text and its next action first.

Do not give secondary settings the same visual weight as the primary job.

### 2. Make privacy concrete

Privacy is a product behavior, not a lock icon.

Use plain, specific labels:

- **On this device:** the speech-to-text model and audio stay on the device
  after the model is downloaded.
- **Your gateway:** audio is sent to the gateway the user configured; that
  gateway runs the speech-to-text model and returns text.
- **External service:** name the service, what is sent, and what is retained.

Never collapse “private,” “local,” “self-hosted,” and “on-device” into one
claim. Never name a particular host such as “your Mac” when the configured
gateway may run elsewhere.

### 3. Preserve platform truth

Family resemblance comes from hierarchy, materials, color roles, voice, and
behavior—not identical screenshots.

- iOS and iPadOS use native navigation, sheets, menus, keyboard conventions,
  Dynamic Type, VoiceOver, and system appearance.
- Android uses Material behavior, system back, IME conventions, scalable type,
  TalkBack, and Android permission patterns.
- macOS uses real windows, menus, Settings, keyboard shortcuts, focus rings,
  menu-bar behavior, and pointer interactions.
- Windows uses Windows-native windowing, controls, navigation, shortcuts, and
  accessibility behavior.
- Linux follows the chosen desktop toolkit and environment rather than
  imitating macOS or Windows chrome.

Platform conventions override decorative brand consistency when the two
conflict.

### 4. Keep the visual system flat and tactile

Create depth with solid surfaces, borders, spacing, restrained shadows, and
clear grouping. A shadow should suggest a surface sitting above another
surface, not a glow.

Do not use linear, radial, conic, mesh, or animated gradients. Do not use
translucency simply to make a screen look modern. System-provided materials are
acceptable where the operating system uses them for legibility or hierarchy,
such as a toolbar over scrolling content.

### 5. Use one product accent

The product accent identifies selection, focus, readiness, and primary action.
It is not a substitute for semantic status.

- Recording remains red.
- Processing or a warning remains amber.
- Destructive action remains red.
- Unavailable and locked states remain neutral.
- Success may use the product accent when text or a symbol also communicates
  completion.

Avoid cycling through unrelated colors for routine state changes.

### 6. Be precise before being clever

Use memorable, human headings followed immediately by the mechanism and
boundary. Prefer “speech-to-text model,” “on this iPhone,” “your gateway,” and
“insert text” over internal type names or vague AI language.

## Family resemblance and product identity

Every Voca app shares:

- a calm neutral foundation;
- dark, high-contrast ink;
- one approved product accent;
- system-first typography;
- solid surfaces with restrained borders and shadows;
- direct product proof and real states;
- concise, warm, technically precise copy;
- motion that confirms rather than decorates;
- explicit processing and privacy boundaries; and
- the accessibility and validation requirements in this guide.

Every product keeps:

- its approved name and casing;
- its exact logo and app icon;
- its own approved accent;
- its native platform behavior;
- its real installation and release status;
- its actual recording, network, storage, and processing model; and
- its strongest product-specific interaction.

Do not recolor or redraw a logo to force consistency. Do not place another
product's screenshot or behavior inside the app.

## Semantic visual foundation

### Reference palette

These values carry the same direction as the web standard. They are reference
values, not a command to hard-code web colors into every operating-system
control.

| Semantic role | Light reference | Dark reference | Use |
| --- | --- | --- | --- |
| Canvas | `#F4F1E8` | `#212121` | Main branded background |
| Surface | `#FFFDF7` | `#2A2A2A` | Cards, sheets, and panels |
| Recessed | `#EBE5D8` | `#303030` | Grouped or secondary surface |
| Primary ink | `#14231C` | `#F4F1E8` | Primary text and strong glyphs |
| Muted ink | `#68726C` | `#AEB5B0` | Supporting copy and metadata |
| Border | `#C9C8BD` | `#3A3A3A` | Dividers and quiet outlines |
| Strong border | `#9EA59F` | `#555555` | Focused or elevated outlines |
| Focus | `#E9B949` | `#E9B949` | Focus and small emphasis |
| Recording/error | `#C73D38` | `#FF736D` | Live recording and errors |
| Warning/processing | `#A86108` | `#F0B35A` | Waiting and attention |

The product accent comes from approved brand material. VocaPhone uses:

| Role | Light appearance | Dark appearance |
| --- | --- | --- |
| Brand accent | `#0F6B57` | `#77D0B2` |
| Text on accent | `#FFFFFF` | `#003827` |

Platform implementations should expose semantic names such as `canvas`,
`surface`, `primaryText`, `secondaryText`, `border`, `accent`,
`onAccent`, `recording`, `warning`, `error`, and `disabled`. Screens
should consume those roles rather than duplicate literal values.

### Native surface mapping

- Use native dynamic colors for standard lists, text fields, menus, sheets, and
  keyboard keys when they provide better platform integration.
- Use the branded canvas and surfaces for deliberate product moments such as
  onboarding, recording, readiness, and empty states.
- Keep keyboards close to the system keyboard's luminance, key contrast,
  geometry, and host-app appearance. Do not make a keyboard look like the
  marketing website.
- Dark surfaces use neutral charcoal, never saturated blue-black.
- A second appearance must be designed and reviewed independently.

### Contrast

Evaluate contrast against the color as rendered, including alpha compositing,
disabled opacity, pressed states, and system materials. Text and informative
glyphs meet the platform equivalent of WCAG AA. Large text, borders, focus, and
non-text controls remain distinguishable under Increase Contrast or the
platform equivalent.

Information must not depend on color alone. Pair status color with a word,
symbol, shape, or change in control availability.

## Typography

Use the platform system family by default. Distinction comes from scale,
weight, spacing, and composition rather than downloading a fashionable font.

### Roles

- **Display:** rare branded moments, onboarding, or a major empty state.
- **Title:** screen and major section names.
- **Body:** instructions, transcript content, settings, and explanations.
- **Label:** controls and compact state names.
- **Metadata:** time, model, language, version, or technical status.
- **Monospaced:** timers, identifiers, endpoints, logs, and technical values
  where character alignment matters.

### Treatment

- Keep screen titles short and use the platform's normal title behavior.
- Left-align explanations and long-form content.
- Use sentence case for controls and headings unless the operating system
  specifies otherwise.
- Preserve approved product casing, including lowercase `vocaphone` where
  that is the established product treatment.
- Avoid long centered paragraphs.
- Do not use monospaced type as decoration.
- Support platform text scaling without clipping, overlap, or hidden actions.

## Spacing, shape, and elevation

Use a 4-point foundation with 8-point increments for most composition:

- 4 points: tight icon or metadata spacing;
- 8 points: related control spacing;
- 12–16 points: component padding;
- 20–24 points: card or screen grouping; and
- 32 points or more: major section separation.

Prefer a small radius vocabulary rather than a different capsule for every
element:

- 6–8 points for keys and compact controls;
- 10–14 points for fields and ordinary cards;
- 16–24 points for large recording or hero surfaces; and
- capsules only for compact filters, state tags, or controls whose platform
  convention calls for them.

Use one quiet shadow at most on an elevated component. Borders and surface
contrast should carry most grouping.

## Components

### App shell and navigation

- Use the platform's standard window, navigation stack, tab, sidebar, toolbar,
  and back behavior.
- Keep the current task and primary destination easy to find.
- Use three to five top-level destinations at most on compact mobile layouts.
- Do not put every repository, diagnostic action, or minor preference in
  top-level navigation.
- Preserve Settings access even when an optional menu-bar, tray, or keyboard
  entry point is hidden.

### Cards and grouped content

A card is for a coherent state, decision, or task—not a generic wrapper around
every paragraph.

- Use a solid surface, thin border when needed, and restrained radius.
- Put the state or outcome first, supporting explanation second, and action
  last.
- Avoid card grids when a native list or form is easier to scan.
- Never rotate interactive cards or long-form app content.

### Buttons and links

- One filled primary action per local decision area.
- Use bordered, tonal, plain, or native secondary actions according to platform
  convention.
- Write actions as verbs: “Start dictation,” “Download model,” “Test gateway,”
  “Insert text,” or “Open Settings.”
- Use destructive styling only for destructive behavior.
- Icon-only buttons require accessible names and a familiar system symbol.
- General touch targets are at least 44 by 44 points or the platform
  equivalent.
- Disabled controls must remain legible and explain their prerequisite nearby.

### Forms and settings

- Group settings by user intent, not by internal subsystem.
- Put the current value in the row and detailed explanation in supporting text.
- Use native pickers, toggles, text fields, and validation.
- Validate after the person has enough information to act; do not show errors
  on untouched fields.
- Explain consequences before a destructive or privacy-sensitive choice.
- Keep advanced diagnostics and dangerous actions away from routine settings.

### Status and progress

Every status component answers:

1. What is happening?
2. Where is it happening?
3. Does the user need to act?
4. What happens next?

Use determinate progress for downloads or work with measurable completion.
Use indeterminate progress only when duration is unknown. A live audio waveform
must be visually different from an indeterminate processing animation.

### Recording and transcription

- Recording is always visibly red and includes the word “Recording” or
  “Listening.”
- Show elapsed time with monospaced digits when useful.
- Provide an obvious Finish action and a reachable Cancel action.
- State whether transcription runs on this device or on the configured gateway.
- Preview the transcript before a manual insert.
- Preserve retryable work and make Retry the primary recovery action.
- Do not keep recording indicators visible after recording stops.
- Do not imply that standby microphone readiness is active recording.

### Empty, loading, error, and recovery states

- Empty states explain what will appear and the next useful action.
- Loading states preserve enough layout to prevent disruptive jumps.
- Error text says what failed in plain language and whether work was preserved.
- Permission errors name the permission and give the strongest supported
  recovery path.
- When the operating system prevents a direct settings link or automatic app
  return, explain the exact manual steps instead of promising unsupported
  behavior.

### Keyboard surfaces

A keyboard is a high-frequency input surface, not a branded poster.

- Preserve familiar QWERTY alignment and platform modifier placement.
- Keep letters, symbols, and system icons immediately legible.
- Make the main voice action visually dominant without stealing space from
  typing.
- Fill gutters with effective hit regions so near misses resolve predictably.
- Provide clear pressed, selected shift, caps-lock, disabled, and active-plane
  states.
- Match the editor's return action and relevant punctuation.
- Preserve access to the operating system's keyboard switcher where required.
- Avoid decorative animation, oversized logos, dense toolbars, and unrelated
  feature buttons.
- Test inside real host apps; a standalone preview is not sufficient.

## Content and voice

Voca copy is direct, warm, specific, and lightly playful.

### Write like this

- “Voice typing that stays on this iPhone.”
- “Transcribing on your gateway.”
- “Your recording is preserved. Retry when the gateway is ready.”
- “Download a speech-to-text model to dictate offline.”
- “Swipe back to the app where you were typing.”

### Avoid this

- “Revolutionary AI-powered productivity.”
- “Military-grade privacy.”
- “Works everywhere.”
- “Completely local” when a gateway receives audio.
- “Your Mac” when any configured gateway host can perform the work.
- Internal case names, protocol names, or implementation types in ordinary UI.

Use the sequence benefit → mechanism → boundary:

> Dictate offline. The speech-to-text model runs on this device after it is
> downloaded. A self-hosted gateway remains available when you want a different
> model or shared compute.

## Motion and feedback

Motion confirms input, state change, or spatial relationship.

Recommended:

- 160–220 millisecond state transitions;
- subtle press scaling or fill changes;
- a live waveform driven by actual microphone level;
- a restrained recording pulse;
- progress movement that clearly differs from audio; and
- haptic or sound feedback that follows platform settings.

Avoid:

- bouncing primary actions;
- looping decoration;
- animated gradients;
- motion required to discover a control;
- several unrelated animations at once; and
- animation on every polling or status refresh.

Respect Reduce Motion. Essential state changes remain immediate and complete
without crossfades, pulses, scrolling meters, or transforms.

## Accessibility

Accessibility is part of the component contract.

Every Voca app must provide:

- a logical reading and focus order;
- accessible names for icon-only actions;
- values and hints where a name does not describe the current state;
- scalable type without clipped content or unreachable controls;
- keyboard navigation and visible focus on desktop;
- screen-reader announcements for meaningful asynchronous state changes;
- contrast that meets platform requirements;
- status that does not depend on color;
- reduced-motion behavior;
- sufficiently large touch or pointer targets;
- support for bold text, increased contrast, button-shape, and
  differentiate-without-color preferences where the platform exposes them; and
- localization-safe layouts for longer labels and right-to-left scripts.

Do not repeatedly announce timers, meter samples, polling ticks, or decorative
changes. Announce the transition: recording started, transcription completed,
retry needed, or text inserted.

## Responsive and adaptive behavior

Design each size and input mode rather than shrinking a reference screen.

- Compact phones preserve the primary task and remove secondary decoration.
- Landscape reduces vertical chrome before reducing effective hit coverage.
- Tablets use additional width for readable grouping, not oversized phone
  controls.
- Desktop windows support sensible minimum sizes, resizing, keyboard focus, and
  pointer states.
- System keyboards follow host-app appearance and text-input traits.
- Split view, display scaling, large text, right-to-left layout, and connected
  hardware keyboards must not hide critical actions.

## Platform adaptation notes

### VocaPhone

- Lead with voice typing and direct insertion.
- Keep iOS and Android keyboard behavior truthful to each platform.
- Make on-device and gateway routes equally clear.
- Show language and writing-style choices without crowding the keyboard.
- Treat setup completion as an end-to-end proof, not only granted permissions.

### VocaMac

- Lead with native macOS voice typing and the selected speech-to-text model.
- Use real menu-bar, window, microphone, overlay, and Settings behavior.
- Preserve Settings access when the tray item is hidden.
- Keep recording-device choice local to the app and visible.

### VocaLinux

- Use the chosen Linux toolkit and real desktop integration.
- Pair graphical readiness with truthful service, model, or terminal status.
- Do not imitate macOS traffic lights or Windows navigation.

### VocaWin

- Use Windows-native window, navigation, shortcut, and installation language.
- Keep availability and release state explicit.
- Do not port macOS chrome for family resemblance.

### VocaGateway

- Show routes, authentication, model, readiness, and processing location.
- Use neutral charcoal for a dark-first dashboard.
- Keep operational detail available without making every screen a monitoring
  dashboard.
- Never hide a network transfer behind a generic “secure” label.

## Implementation guidance

- Centralize semantic tokens once per platform.
- Keep semantic recording, warning, error, and success colors separate from
  product-brand assets.
- Use native components before creating shared custom ones.
- Share behavior and semantic roles across products; do not force one
  cross-platform pixel implementation.
- Keep design-preview and debug states out of release behavior.
- Add deterministic previews or fixtures for every meaningful state.
- Regenerate derived icons and assets from their approved source; do not
  hand-edit generated outputs.
- Avoid adding a design-system dependency when platform components and a small
  token layer provide the required result.

## Review and release gate

Before a native visual change is accepted:

### Product truth

- Product name, logo, icon, platform, release state, and processing claims are
  correct.
- On-device, gateway, and external-service boundaries are explicit.
- Screens show states the product can actually reach.

### Visual quality

- Light and dark appearances have been reviewed where supported.
- Hierarchy, spacing, type, borders, and radii use the shared roles.
- No gradient, glow, blue-black drift, excessive pills, or decorative glass has
  entered the interface.
- Long copy and localized copy do not clip or overlap.

### Interaction

- Primary, secondary, disabled, pressed, loading, success, error, and recovery
  states are covered.
- Touch, pointer, keyboard, focus, and back behavior match the platform.
- Reduced-motion behavior preserves all essential meaning.

### Accessibility

- Screen-reader order, labels, values, hints, and announcements are checked.
- Text scaling, contrast, bold text, focus, and non-color status are checked.
- General touch targets meet the platform minimum; keyboard hit regions cover
  the complete typing surface.

### Validation

- Automated build and regression checks pass.
- Representative screenshots are reviewed at compact and large sizes.
- Keyboard and system-integration changes are checked inside real host apps.
- Physical-device behavior is verified when permissions, extensions,
  microphones, background execution, Live Activities, or system keyboards are
  involved.

Local compilation is not visual acceptance. Simulator screenshots are not proof
of keyboard-extension handoff, microphone behavior, signing, background
recording, or physical-device ergonomics.

## Maintaining this standard

This standard describes durable principles and semantic roles. Product plans
may make a more specific choice, but they must record why it fits the platform
and product truth.

When the family direction changes:

1. Update this standard.
2. Update the reference implementation or approved visual examples.
3. Review each platform mapping rather than copying a single implementation.
4. Re-run accessibility and visual acceptance for every affected appearance.

Do not declare a new family direction from one unapproved product draft.
