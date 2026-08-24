# macOS tip drafts (VocaMac v0.9.0)

VocaPress owns these. Draft only. Do not send unless Jatin says send. From vocahq@gmail.com as Jatin. Introduce as Jatin, creator and maintainer. Do not add a name or email closer; the VocaHQ Gmail signature already has the mark and hello@vocahq.com.

Facts used (vocamac.com, product.toml, README, v0.9.0 notes, VocaMac agent 24 Aug 2026): VocaMac is Beta v0.9.0. Not Stable. macOS 14+ Apple Silicon only. No Intel build. AGPL-3.0. Menu bar, no Dock icon. Default hotkey hold Right Option, release to transcribe. Double-tap toggle is in the README. Transcript inserts at the cursor via accessibility. Secure fields and some apps can refuse insertion. Clipboard is saved and restored around injection; do not claim the clipboard is never used. Permissions: Microphone, Accessibility, Input Monitoring. Engines in 0.9.0 (site + product.toml): WhisperKit/Core ML, Parakeet, Apple Speech (macOS 26+), sherpa-onnx (Moonshine, SenseVoice, GigaAM, Canary). First WhisperKit download from Hugging Face. After a model is local, transcription can run without sending audio to a cloud. No Voca account. No Voca-hosted cloud. No iCloud dictation claim. PRODUCT.md VocaMac row still only says WhisperKit / Core ML; for tips cite the site/release catalog, not that short row as the full list. Homebrew cask description "powered by WhisperKit" is stale; do not use it as the engine list. 17 pin-able languages in Settings. Do not say 99+. Custom vocabulary and translate-to-English are WhisperKit-only. Do not say vocabulary works on Parakeet, Apple Speech, or sherpa. 0.9.0 release notes also shipped text snippets and a dictation-tone picker (ten pairs + Off; Voca default for new installs). Those are not on the /features page; cite the release if you mention them. Headless file CLI exists; not the reviewer everyday path; it does not auto-download models. Recording overlay exists. Homebrew from the site: brew tap vocahq/vocamac && brew trust vocahq/vocamac && brew install --cask vocamac (cask is 0.9.0, macos :sonoma). DMG: VocaMac-0.9.0-arm64.dmg (~99 MB), Developer ID signed and notarized, https://github.com/VocaHQ/vocamac/releases/tag/v0.9.0. Gateway is optional self-hosted compute and is not on-device. No feature parity. Screenshots: https://vocamac.com/screenshots. Discord: https://discord.gg/t6muquAJbm. Do not use empty "honest/genuine/real" modifiers (TidBITS).

Every tip must say the code is open source (AGPL-3.0) and that people already file bugs, feature requests, and PRs. Do not invent star counts.

Jatin uses the family every day. Vocalinux is available now. VocaWin is an unsigned Windows beta. VocaPhone is a phone beta. VocaGateway is early and optional.

---

## How these differ

TidBITS follows Adam's Jul 2026 pitch guide (PITCH subject, problem, competition, scannable facts). MacStories is a test request, no paid review. Six Colors apps@ is short: what it does, which devices. The rest stay personal and short.

---

### TidBITS

To: ace@tidbits.com

Subject: PITCH: VocaMac - Mac app for on-device dictation

Adam,

I'm Jatin, creator and maintainer of VocaMac. I read your July note on pitching apps. This is a personal email, not a press release.

The problem I had: I type all day and I did not want my speech going to a vendor that trains on it. Apple's built-in dictation is there, and MacWhisper is the obvious indie neighbor. I still built VocaMac because I wanted a menu-bar tool that stays on the Mac, inserts at the cursor in the app I already have open, and lets me pick the local model. No Voca account. No Voca speech server. After the model is downloaded, the audio stays on the machine.

I use it every day on this Mac, and I use the Linux, Windows, and phone siblings too. Linux is further along. VocaMac is Beta. The code is open source. People already file bugs, request features, and send PRs.

v0.9.0 (Apple Silicon, macOS 14+): hold Right Option, or toggle. WhisperKit / Core ML by default. 0.9.0 also ships Parakeet, Apple Speech on macOS 26+, and a few CPU-only ONNX models. Settings has 17 pin-able languages. Custom vocabulary is WhisperKit-only. The 0.9.0 notes also added text snippets and a tone picker. Homebrew cask or a signed, notarized DMG. AGPL-3.0. Free, no subscription. Needs Microphone, Accessibility, and Input Monitoring.

What it is not: Intel. App Store. A ChatGPT wrapper. A guarantee that every secure field will accept insertion.

App: VocaMac 0.9.0
Developer: Jatin Malik / VocaHQ
Requires: macOS 14+ Apple Silicon
Price: free (AGPL-3.0)
Status: Beta, shipping
Site: https://vocamac.com
Install: brew tap vocahq/vocamac && brew install --cask vocamac, or https://github.com/VocaHQ/vocamac/releases/tag/v0.9.0
Reviewer license: not needed, the app is free
Screenshots: https://vocamac.com/screenshots
Source: https://github.com/VocaHQ/vocamac

---

### MacStories

To: viticci@macstories.net, voorhees@macstories.net

Subject: VocaMac v0.9.0, on-device dictation (no paid-review ask)

Hi,

I'm Jatin, creator and maintainer of VocaMac. You only write about apps you have used. I am not offering money.

VocaMac is a menu-bar dictation app for Apple Silicon. Hold Right Option, talk, text lands at the cursor. Models run on the Mac (WhisperKit / Core ML, plus a few others in 0.9.0). No Voca account. I use it every day.

Beta. macOS 14+. Homebrew or a signed, notarized DMG. Open source, AGPL-3.0. People already open issues and PRs. Secure fields can still refuse insertion.

If you want to try it, the DMG and the Homebrew tap are on vocamac.com. Shots: https://vocamac.com/screenshots

- Site: https://vocamac.com
- Screenshots: https://vocamac.com/screenshots
- Release: https://github.com/VocaHQ/vocamac/releases/tag/v0.9.0
- Family: https://vocahq.com

---

### Six Colors

To: apps@sixcolors.com
Fallback: jsnell@sixcolors.com

Subject: VocaMac, on-device dictation for Apple Silicon

Hi,

I'm Jatin, creator and maintainer of VocaMac. App pitch for the report.

What it does: menu-bar voice typing. Hold Right Option, speak, the Mac transcribes, the words go to the cursor. After a local model is downloaded, audio stays on the Mac. No Voca account.

Devices: Apple Silicon Macs, macOS 14+. Beta v0.9.0. Not Intel. Homebrew or signed DMG.

I use it every day. Open source, AGPL-3.0. People already file bugs and send PRs. https://vocamac.com

- Site: https://vocamac.com
- Screenshots: https://vocamac.com/screenshots
- Family: https://vocahq.com

---

### 9to5Mac

To: tips@9to5mac.com
Also: https://9to5mac.com/contact/

Subject: Indie app: VocaMac v0.9.0

Hi,

I'm Jatin, creator and maintainer of VocaMac. Indie App Spotlight / news tip.

VocaMac v0.9.0 is a menu-bar dictation app for Apple Silicon. Hold Right Option, talk, text at the cursor. On-device models (WhisperKit / Core ML). No Voca account. AGPL-3.0. Open source. I use it every day. The community already files bugs, asks for features, and sends PRs.

Beta. macOS 14+. Homebrew or notarized DMG. You already cover MacWhisper; this is the same neighborhood with a Voca family on Linux, Windows, and phone.

- Site: https://vocamac.com
- Screenshots: https://vocamac.com/screenshots
- Family: https://vocahq.com

---

### Cult of Mac

To: reviews@cultofmac.com
Also: news@cultofmac.com if you would rather file it as a tip

Subject: Review request: VocaMac v0.9.0

Hi,

I'm Jatin, creator and maintainer of VocaMac. Product review request.

Menu-bar dictation on Apple Silicon. Hold Right Option, talk, words at the cursor. The model runs on the Mac. No Voca account. Free, AGPL-3.0. Beta v0.9.0. Signed DMG or Homebrew. Open source. People already file bugs and send PRs.

I use it every day. I can send the DMG. Screenshots are already public.

- Site: https://vocamac.com
- Screenshots: https://vocamac.com/screenshots
- Family: https://vocahq.com

---

### Macworld

To: rloyola@macworld.com

Subject: Product for review: VocaMac v0.9.0

Roman,

I'm Jatin, creator and maintainer of VocaMac. Review request, not a guest post.

VocaMac is a free AGPL-3.0 menu-bar app for Apple Silicon (macOS 14+). Hold Right Option, talk, text inserts at the cursor. Speech-to-text runs on the Mac after you download a model. No Voca account. Beta v0.9.0. Homebrew or a Developer ID signed, notarized DMG.

I use it every day. Open source. Testers already open issues and PRs. I can send a build. Secure fields may refuse insertion; that is a platform limit, not a hidden one.

- Site: https://vocamac.com
- Screenshots: https://vocamac.com/screenshots
- Family: https://vocahq.com

---

### OSXDaily

To: contact@osxdaily.com

Subject: Open-source Mac utility: VocaMac v0.9.0

Hi,

I'm Jatin, creator and maintainer of VocaMac. You cover Homebrew and small Mac tools. This is one.

brew tap vocahq/vocamac && brew trust vocahq/vocamac && brew install --cask vocamac

Menu bar. Hold Right Option. Text at the cursor. Models stay on the Mac. No Voca account. AGPL-3.0. Apple Silicon, macOS 14+. Beta v0.9.0. I use it every day. The source is open. People already file bugs and send PRs.

- Site: https://vocamac.com
- Screenshots: https://vocamac.com/screenshots
- Family: https://vocahq.com

---

### MacSparky

To: desk@macsparky.com

Subject: VocaMac, menu-bar dictation I actually use

David,

I'm Jatin, creator and maintainer of VocaMac. Personal note, not a sponsor thing.

I built a menu-bar dictation app because I was tired of sending speech somewhere else. Hold Right Option, talk, the Mac types at the cursor. Local models. No Voca account. I use it every day.

Beta, Apple Silicon, macOS 14+, open source AGPL-3.0. People already send bug reports, feature requests, and PRs. Homebrew or a signed DMG. vocamac.com

- Site: https://vocamac.com
- Screenshots: https://vocamac.com/screenshots
- Family: https://vocahq.com

---

### AppleInsider

To: news@appleinsider.com
Also: https://appleinsider.com/contact

Subject: Tip: VocaMac v0.9.0, on-device Mac dictation

Hi,

I'm Jatin, creator and maintainer of VocaMac. News tip.

v0.9.0 is a Beta menu-bar app for Apple Silicon. On-device speech-to-text. Hold Right Option, text at the cursor. No Voca account. Free AGPL-3.0. Signed, notarized DMG or Homebrew. I use it every day. Open source. Bugs, feature asks, and PRs already show up on GitHub.

- Site: https://vocamac.com
- Screenshots: https://vocamac.com/screenshots
- Family: https://vocahq.com

---

### MacRumors

To: tips@macrumors.com
Also: https://www.macrumors.com/share.php

Subject: Product info: VocaMac v0.9.0

Hi,

I'm Jatin, creator and maintainer of VocaMac. Product info for coverage, not an ad.

VocaMac v0.9.0: menu-bar dictation, Apple Silicon, macOS 14+, on-device models, no Voca account. Hold Right Option, talk, text at the cursor. AGPL-3.0. Beta. Homebrew or notarized DMG. I use it every day. The code is open source. People already file bugs and send PRs.

- Site: https://vocamac.com
- Screenshots: https://vocamac.com/screenshots
- Family: https://vocahq.com

---

### The Sweet Setup

To: desk@blancmedia.org

Subject: VocaMac, on-device Mac dictation

Hi,

I'm Jatin, creator and maintainer of VocaMac. I know you pick "best of" apps on your own schedule. Putting this on the pile.

Menu-bar dictation for Apple Silicon. Local models. Text at the cursor. No account. Free, open source, AGPL-3.0. I use it every day. People already file bugs, request features, and send PRs. vocamac.com

- Site: https://vocamac.com
- Screenshots: https://vocamac.com/screenshots
- Family: https://vocahq.com
