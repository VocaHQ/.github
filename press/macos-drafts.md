# macOS tip drafts (VocaMac v0.9.0)

VocaPress owns these. Draft only. Do not send unless Jatin says send. From vocahq@gmail.com as Jatin. Introduce as Jatin, creator and maintainer. Do not add a name or email closer; the VocaHQ Gmail signature already has the mark and hello@vocahq.com.

Facts used (vocamac.com, product.toml, README, v0.9.0 notes, VocaMac agent 24 Aug 2026): VocaMac is Beta v0.9.0. Not Stable. macOS 14+ Apple Silicon only. No Intel build. AGPL-3.0. Menu bar, no Dock icon. Default hotkey hold Right Option, release to transcribe. Double-tap toggle is in the README. Transcript inserts at the cursor via accessibility. Secure fields and some apps can refuse insertion. Clipboard is saved and restored around injection; do not claim the clipboard is never used. Permissions: Microphone, Accessibility, Input Monitoring. Engines in 0.9.0 (site + product.toml): WhisperKit/Core ML, Parakeet, Apple Speech (macOS 26+), sherpa-onnx (Moonshine, SenseVoice, GigaAM, Canary). First WhisperKit download from Hugging Face. After a model is local, transcription can run without sending audio to a cloud. No Voca account. No Voca-hosted cloud. No iCloud dictation claim. PRODUCT.md VocaMac row still only says WhisperKit / Core ML; for tips cite the site/release catalog, not that short row as the full list. Homebrew cask description "powered by WhisperKit" is stale; do not use it as the engine list. 17 pin-able languages in Settings. Do not say 99+. Custom vocabulary and translate-to-English are WhisperKit-only. Do not say vocabulary works on Parakeet, Apple Speech, or sherpa. 0.9.0 release notes also shipped text snippets and a dictation-tone picker (ten pairs + Off; Voca default for new installs). Those are not on the /features page; cite the release if you mention them. Headless file CLI exists; not the reviewer everyday path; it does not auto-download models. Recording overlay exists. Homebrew from the site: brew tap vocahq/vocamac && brew trust vocahq/vocamac && brew install --cask vocamac (cask is 0.9.0, macos :sonoma). DMG: VocaMac-0.9.0-arm64.dmg (~99 MB), Developer ID signed and notarized, https://github.com/VocaHQ/vocamac/releases/tag/v0.9.0. Gateway is optional self-hosted compute and is not on-device. No feature parity. Screenshots: https://vocamac.com/screenshots. Discord: https://discord.gg/t6muquAJbm. Do not use empty "honest/genuine/real" modifiers (TidBITS).

Every tip must say the code is open source (AGPL-3.0) and that people already file bugs, feature requests, and PRs. Do not invent star counts.

Jatin uses the family every day. Vocalinux is available now. VocaWin is an unsigned Windows beta. VocaPhone is a phone beta. VocaGateway is early and optional.

Bodies rewritten 26 Aug 2026 for voice (less telegram, more letter). Gmail drafts must be refreshed by VocaHQ from these files. Do not send unless Jatin says send.

---

## How these differ

TidBITS follows Adam's Jul 2026 pitch guide. MacStories is a test request. Six Colors apps@ is short. The rest stay personal and short.

### TidBITS
To: ace@tidbits.com

Subject: PITCH: VocaMac - Mac app for on-device dictation

Adam,

I'm Jatin, creator and maintainer of VocaMac. I read your July note on pitching apps. This is a personal email, not a press release.

The problem I had: I type all day and I did not want my speech going to a vendor that trains on it. Apple's built-in dictation is there, and MacWhisper is the obvious indie neighbor. I still built VocaMac because I wanted a menu-bar tool that stays on the Mac, inserts at the cursor in the app I already have open, and lets me pick the local model. No Voca account. No Voca speech server. After the model is downloaded, the audio stays on the machine.

I use it every day on this Mac, plus the Linux, Windows, and phone siblings. Linux is further along. The code is open source under AGPL-3.0, and people already file bugs, request features, and send PRs.

v0.9.0 is Beta. Hold Right Option, or toggle. WhisperKit / Core ML by default, plus Parakeet, Apple Speech on macOS 26+, and a few CPU-only ONNX models. 17 pin-able languages. Custom vocabulary is WhisperKit-only. Text snippets and a tone picker. Needs Microphone, Accessibility, and Input Monitoring.

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

VocaMac is a menu-bar dictation app, Beta v0.9.0, for Apple Silicon on macOS 14+. Hold Right Option, talk, and text lands at the cursor. Models run on the Mac (WhisperKit / Core ML, plus a few others in 0.9.0). No Voca account. After a local model is downloaded, the audio stays on that machine. I use it every day.

Homebrew or a signed, notarized DMG. Open source, AGPL-3.0. People already open issues and PRs. Secure fields can still refuse insertion. Linux is the mature sibling; Windows and phone are betas too.

- Site: https://vocamac.com
- Screenshots: https://vocamac.com/screenshots
- Release: https://github.com/VocaHQ/vocamac/releases/tag/v0.9.0
- Family: https://vocahq.com

---

### Six Colors
Fallback: jsnell@sixcolors.com
To: apps@sixcolors.com

Subject: VocaMac, on-device dictation for Apple Silicon

Hi,

I'm Jatin, creator and maintainer of VocaMac. App pitch for the report.

It sits in the menu bar. Hold Right Option, speak, and the Mac transcribes into the app you already have open. After a local model is downloaded, audio stays on the Mac. No Voca account. Open source under AGPL-3.0. People already file bugs, ask for features, and send PRs.

I use it every day on Apple Silicon Macs (macOS 14+). I also use the Linux release and the Windows and phone betas. Devices it covers today: Apple Silicon Macs only. No Intel.

- Site: https://vocamac.com
- Screenshots: https://vocamac.com/screenshots
- Release: https://github.com/VocaHQ/vocamac/releases/tag/v0.9.0
- Family: https://vocahq.com

---

### 9to5Mac
To: tips@9to5mac.com

Subject: Indie tip: VocaMac v0.9.0, on-device Mac dictation

Hi,

I'm Jatin, creator and maintainer of VocaMac. Indie App Spotlight / news tip, if that is still the right bucket.

I wanted a Mac dictation app that did not need an Apple ID tied to iCloud dictation, and did not send audio to a vendor. VocaMac is that: menu bar, Apple Silicon, macOS 14+, Beta v0.9.0. Hold Right Option, talk, and the words go into whatever already has the cursor. WhisperKit / Core ML is the default engine. After the first model download from Hugging Face, transcription can stay on the Mac. No Voca account.

I use it every day on this machine. The code is open source, AGPL-3.0, and people already file bugs, ask for features, and send PRs. Homebrew cask or a Developer ID signed, notarized DMG. Linux is the mature sibling. Windows and phone are betas.

- Site: https://vocamac.com
- Screenshots: https://vocamac.com/screenshots
- Release: https://github.com/VocaHQ/vocamac/releases/tag/v0.9.0
- Family: https://vocahq.com

---

### Cult of Mac
To: news@cultofmac.com
Also: reviews@cultofmac.com

Subject: Review request: VocaMac, on-device Mac dictation (Beta)

Hi,

I'm Jatin, creator and maintainer of VocaMac. Product review request for a free, open-source Mac app.

If you already have a Mac open to Mail or a browser, that is the test: hold Right Option, talk, and the transcript should appear at the cursor. VocaMac lives in the menu bar. It is Beta v0.9.0, Apple Silicon only, macOS 14+. The model runs on the Mac after download. There is no Voca account and no Voca speech server. AGPL-3.0. Testers already file bugs and send PRs.

I use it every day, including the Linux release and the Windows and phone betas. Secure fields can still refuse insertion. Install from Homebrew or the signed, notarized DMG.

- Site: https://vocamac.com
- Screenshots: https://vocamac.com/screenshots
- Release: https://github.com/VocaHQ/vocamac/releases/tag/v0.9.0
- Family: https://vocahq.com

---

### Macworld
To: tips@macworld.com (verify current tips inbox on macworld.com before send)

Subject: Review request: VocaMac v0.9.0

Hi,

I'm Jatin, creator and maintainer of VocaMac. Review request, not a guest post.

VocaMac is the Mac client in a small family of on-device dictation apps. On Apple Silicon (macOS 14+) it sits in the menu bar. You hold Right Option, talk, and text inserts at the cursor in the app you were already using. Speech-to-text runs on the Mac after you download a model. No Voca account. Beta v0.9.0.

I use it every day. The source is AGPL-3.0, and people already file bugs, request features, and send PRs. Homebrew or a Developer ID signed, notarized DMG. Linux is further along. Windows and phone are betas. Secure fields may refuse insertion.

- Site: https://vocamac.com
- Screenshots: https://vocamac.com/screenshots
- Release: https://github.com/VocaHQ/vocamac/releases/tag/v0.9.0
- Family: https://vocahq.com

---

### OSXDaily
To: contact@osxdaily.com

Subject: VocaMac, Homebrew / DMG Mac dictation (Apple Silicon)

Hi,

I'm Jatin, creator and maintainer of VocaMac. You cover Homebrew and small Mac tools. This is one I actually run.

Install is the usual path: brew tap vocahq/vocamac, then the cask, or grab the signed DMG from GitHub. After that it lives in the menu bar. Hold Right Option, talk, and text lands at the cursor. First WhisperKit download comes from Hugging Face. After that, audio can stay on the Mac. No Voca account. Beta, Apple Silicon, macOS 14+.

Open source, AGPL-3.0. People already file bugs and send PRs. I use it every day. Linux is the mature sibling.

- Site: https://vocamac.com
- Screenshots: https://vocamac.com/screenshots
- Release: https://github.com/VocaHQ/vocamac/releases/tag/v0.9.0
- Family: https://vocahq.com

---

### MacSparky
To: david@macsparky.com (verify before send; site contact may change)

Subject: VocaMac, personal note on Mac dictation that stays local

David,

I'm Jatin, creator and maintainer of VocaMac. Personal note, not a sponsor thing.

I built a menu-bar dictation app because I was tired of sending speech somewhere else. Hold Right Option, talk, and the Mac types at the cursor. Local models. No Voca account. I use it every day. Open source under AGPL-3.0, and people already file bugs, ask for features, and send PRs.

Beta on Apple Silicon, macOS 14+. Homebrew or a notarized DMG. Linux is further along in the family.

- Site: https://vocamac.com
- Screenshots: https://vocamac.com/screenshots
- Release: https://github.com/VocaHQ/vocamac/releases/tag/v0.9.0
- Family: https://vocahq.com

---

### AppleInsider
To: tips@appleinsider.com

Subject: News tip: VocaMac v0.9.0, on-device Mac dictation

Hi,

I'm Jatin, creator and maintainer of VocaMac. News tip on a shipping Beta, not a rumor.

v0.9.0 is out for Apple Silicon on macOS 14+. Menu bar, no Dock icon. Hold Right Option and the Mac transcribes into the focused app. Engines start with WhisperKit / Core ML. No Voca account, and audio is not sent to a vendor cloud. Signed, notarized DMG or Homebrew.

I use it every day. The code is open source, AGPL-3.0. Bugs, feature asks, and PRs already show up on GitHub. Linux is the mature sibling. Windows and phone are betas.

- Site: https://vocamac.com
- Screenshots: https://vocamac.com/screenshots
- Release: https://github.com/VocaHQ/vocamac/releases/tag/v0.9.0
- Family: https://vocahq.com

---

### MacRumors
To: tips@macrumors.com

Subject: Product tip: VocaMac, local Mac dictation (Beta)

Hi,

I'm Jatin, creator and maintainer of VocaMac. Product info for coverage, not an ad.

If you want a one-line: free, open-source, on-device dictation for Apple Silicon Macs. VocaMac v0.9.0 is Beta. Hold Right Option, talk, and text goes to the cursor. Models run locally. No Voca account. Homebrew or a notarized DMG.

I use it every day. AGPL-3.0, and people already file bugs and send PRs. Linux is further along. Windows and phone are betas. Secure fields can refuse insertion. Not on the App Store.

- Site: https://vocamac.com
- Screenshots: https://vocamac.com/screenshots
- Release: https://github.com/VocaHQ/vocamac/releases/tag/v0.9.0
- Family: https://vocahq.com

---

### The Sweet Setup
To: tips@thesweetsetup.com (verify current tips address on thesweetsetup.com before send)

Subject: For your pile: VocaMac, on-device Mac dictation

Hi,

I'm Jatin, creator and maintainer of VocaMac. I know you pick "best of" apps on your own schedule. Putting this on the pile rather than asking for a slot.

I built VocaMac for the same reason I built the Linux one: I wanted to talk into Mail, a browser, or Notes without handing the recording to a company. Menu bar. Hold Right Option. Text at the cursor. Local models. No Voca account. Beta v0.9.0, Apple Silicon, macOS 14+.

I use it every day. Open source, AGPL-3.0. People already file bugs, request features, and send PRs. Homebrew or signed DMG. Linux is the mature sibling.

- Site: https://vocamac.com
- Screenshots: https://vocamac.com/screenshots
- Release: https://github.com/VocaHQ/vocamac/releases/tag/v0.9.0
- Family: https://vocahq.com
