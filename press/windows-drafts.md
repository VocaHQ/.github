# Windows tip drafts (VocaWin v0.1.0-beta.1)

VocaPress owns these. Draft only. Do not send unless Jatin says send. From vocahq@gmail.com as Jatin. Introduce as Jatin, creator and maintainer. Do not add a name or email closer; the VocaHQ Gmail signature already has the mark and hello@vocahq.com.

Facts used (vocawin.com, GitHub Release, README, PRODUCT.md, VocaWin agent 24 Aug 2026): VocaWin is Beta. Unsigned tester build. Not a Store listing. Not a stable public release. Latest named tag v0.1.0-beta.1 (prerelease, published 2026-08-24). App version files stay 0.1.0; the tag is the public version. Release: https://github.com/VocaHQ/vocawin/releases/tag/v0.1.0-beta.1 with VocaWin_0.1.0_x64-setup.exe (NSIS, current-user) and VocaWin_0.1.0_x64_en-US.msi. Both unsigned. Ready shot on that Release. vocawin.com hero points at /releases, not a pinned tag URL; pitch the named tag yourself. Nightly exists; do not pitch it. SmartScreen / unknown publisher is expected. No purchased CA. No auto-update. AGPL-3.0-or-later. Windows 10 version 1809+ or Windows 11. Tray app (idle / recording / processing; close goes to tray). Default hotkey hold Right Alt; optional double-tap toggle; Settings can change it and the site says that default can still move. Settings also: models, languages, silence detection, sounds, start on login. Insertion path is SendInput. Elevated admin windows may refuse it. README still mentions clipboard restore after injection; do not tell press the clipboard is never used. Do not cite an open clipboard PR. Installer does not bundle a model. Download one in Models. Network needed once, then dictation can work offline. Do not say voice never leaves the PC before the model is downloaded. Site first-run default: tiny.en, language automatic. Languages follow the selected Whisper model; do not invent a language count. Site engine story is Whisper after download. README also documents ONNX (Parakeet, Moonshine, SenseVoice, GigaAM, Canary) with DirectML/CPU and whisper.cpp with Vulkan/CPU; Parakeet CTC and Vosk are not in the catalog. Do not turn those into a performance promise. Capture is WASAPI. No Voca account. No hosted speech API. No telemetry (README). VocaWin does not expose VocaGateway mode today. No feature parity with Linux or Mac. No WER/speed/RAM/GPU numbers. Setup: https://github.com/VocaHQ/vocawin/blob/main/docs/setup.md

Jatin uses the family every day. Linux is available now. VocaMac is beta. VocaPhone is a phone beta. VocaGateway is early and optional (not a VocaWin path).

---

## How these differ

Each note is a letter for that desk. Status is Beta and unsigned in every one. The ask changes.

---

### BetaNews

To: info@betanews.com
Also: contact form on https://betanews.com/contact/ (subject: Submitting news)

Subject: VocaWin v0.1.0-beta.1, on-device dictation for Windows

Hi,

I'm Jatin, creator and maintainer of VocaWin. Product launch, still Beta.

VocaWin is an AGPL-3.0-or-later tray app for Windows 10 (1809+) and Windows 11. Hold Right Alt, talk, and the text is meant to land where the caret already is. The installer does not ship a model. After you download one, speech-to-text runs on that PC. No Voca account. Nothing goes to a vendor cloud that trains on the recording. VocaWin does not have a gateway mode today.

I use this every day on Windows, and I use the Linux, Mac, and phone clients too. Linux is the mature release. This Windows build is the rough one I still run.

Honest limits: the Release is unsigned. SmartScreen will likely say the publisher is unknown. More info, then Run anyway if you trust the file. Not a Store app. No auto-update. Elevated windows may block SendInput.

- Site: https://vocawin.com
- Release: https://github.com/VocaHQ/vocawin/releases/tag/v0.1.0-beta.1
- Family: https://vocahq.com

---

### Neowin

Channel: https://www.neowin.net/contact/ (type: News Tips). Do not use tips@neowin.net.

Subject: News tip: VocaWin v0.1.0-beta.1

Hi,

I'm Jatin, creator and maintainer of VocaWin. Unsigned Windows beta of an on-device dictation app.

Tray icon. Hold Right Alt (or double-tap toggle). Talk. Text is supposed to appear in the focused field: browser, editor, chat, terminal, wherever Windows will take keystrokes. The Whisper model lives in a local folder. After that download, dictation can work without the internet. No Voca account. No hosted speech service.

I use it every day. Same family on Linux (available now), Mac (beta), and phone (beta).

This is not a Store listing and not a signed publisher. GitHub Release v0.1.0-beta.1 has NSIS and MSI. SmartScreen is expected.

- Site: https://vocawin.com
- Release: https://github.com/VocaHQ/vocawin/releases/tag/v0.1.0-beta.1
- Family: https://vocahq.com

---

### Ghacks

To: arno@ghacks.net

Subject: VocaWin, on-device Windows dictation (unsigned beta)

Arno,

I'm Jatin, creator and maintainer of VocaWin. Privacy-shaped Windows app, still Beta.

Most Windows dictation wants an account or a cloud. This one does not. Hold Right Alt, talk, the model runs on that PC after you download it. AGPL-3.0-or-later. No telemetry story to sell you, because there is no Voca cloud to send the audio to. I do not expose a gateway on Windows today.

I use this every day. I also keep Linux, Mac, and phone builds around.

Unsigned NSIS/MSI on GitHub. SmartScreen will complain. Elevated admin windows may refuse the keystrokes. That is all real.

- Site: https://vocawin.com
- Release: https://github.com/VocaHQ/vocawin/releases/tag/v0.1.0-beta.1
- Family: https://vocahq.com

---

### Windows Latest

To: contact@windowslatest.com

Subject: News tip: VocaWin v0.1.0-beta.1

Hi,

I'm Jatin, creator and maintainer of VocaWin. Windows news tip.

v0.1.0-beta.1 is an unsigned tray app: hold Right Alt, talk, text is meant to land at the caret. Whisper model on the PC. No Microsoft Store listing. No Voca account. After the model file is on disk, dictation does not need a vendor speech API.

I use it every day. Linux is further along. This is the Windows cut.

SmartScreen / unknown publisher is expected. Elevated windows may block injection. Language coverage follows the Whisper model you pick. Default first-run is tiny.en.

- Site: https://vocawin.com
- Release: https://github.com/VocaHQ/vocawin/releases/tag/v0.1.0-beta.1
- Family: https://vocahq.com

---

### Thurrott

Channel: https://www.thurrott.com/contact-paul (form). Do not invent a To: if you use the form.

Subject: VocaWin v0.1.0-beta.1, private dictation on Windows

Paul,

I'm Jatin, creator and maintainer of VocaWin. Short note, not a customer-service thing.

I wanted Windows to get the same deal as my Linux and Mac apps: hold a key, talk, text at the caret, model on this PC, no Voca account. v0.1.0-beta.1 is that, and it is still Beta. Unsigned. SmartScreen will warn. I use it every day anyway.

AGPL-3.0-or-later. NSIS or MSI on GitHub. Ready shot is on the Release. No Store. No auto-update. No gateway mode on Windows.

- Site: https://vocawin.com
- Release: https://github.com/VocaHQ/vocawin/releases/tag/v0.1.0-beta.1
- Family: https://vocahq.com

---

### MajorGeeks

To: mgnews@majorgeeks.com

Subject: File submission: VocaWin v0.1.0-beta.1 (AGPL, unsigned beta)

Hi,

I'm Jatin, creator and maintainer of VocaWin. Content / file submission, not a marketing blast.

Free AGPL-3.0-or-later Windows dictation. Tray app. Hold Right Alt, talk, text is meant to appear at the caret. Whisper model stays on the PC after download. No account.

Please test it in a VM if that is still your process. It is unsigned Beta. SmartScreen will likely flag unknown publisher. NSIS current-user setup.exe and MSI are on the Release. Windows 10 1809+ or Windows 11. Elevated windows may refuse SendInput.

I use this every day. vocahq.com is the rest of the family.

- Site: https://vocawin.com
- Release: https://github.com/VocaHQ/vocawin/releases/tag/v0.1.0-beta.1
- Family: https://vocahq.com

---

### The Windows Club

To: thewindowsclub@hotmail.com

Subject: Freeware tip: VocaWin v0.1.0-beta.1

Hi,

I'm Jatin, creator and maintainer of VocaWin. Not asking for a paid review.

VocaWin is a free Windows tray app. Hold Right Alt, talk, the transcript is meant to land in the focused field. Speech-to-text runs on that PC after you download a Whisper model. AGPL-3.0-or-later. No Voca account.

I use it every day. This tag is v0.1.0-beta.1. Unsigned. SmartScreen is expected. Not in the Microsoft Store.

- Site: https://vocawin.com
- Release: https://github.com/VocaHQ/vocawin/releases/tag/v0.1.0-beta.1
- Family: https://vocahq.com

---

### Deskmodder

Channel: https://www.deskmodder.de/public/con_form/index.php (Tipp-Box). Optional: dm_admin@deskmodder.de

Subject: Tipp: VocaWin v0.1.0-beta.1

Hi,

I'm Jatin, creator and maintainer of VocaWin. Software tip.

Windows 10/11 tray app. Hold Right Alt, talk, text should appear at the caret. Whisper model on the PC. No Voca account. AGPL-3.0-or-later. English UI.

Unsigned Beta. SmartScreen will warn. GitHub Release has NSIS and MSI. I use it every day.

- Site: https://vocawin.com
- Release: https://github.com/VocaHQ/vocawin/releases/tag/v0.1.0-beta.1
- Family: https://vocahq.com

---

### BornCity

To: gborn@borncity.de
Also: info@borncity.com for the German newsroom

Subject: VocaWin v0.1.0-beta.1, on-device Windows dictation

Gunter,

I'm Jatin, creator and maintainer of VocaWin.

Unsigned Windows beta: tray, hold Right Alt, local Whisper model, text at the caret. No Voca account. No vendor speech cloud. AGPL-3.0-or-later. I use it every day.

Limits I will not hide: SmartScreen, no signed publisher, no Store, no auto-update, elevated windows may block injection.

- Site: https://vocawin.com
- Release: https://github.com/VocaHQ/vocawin/releases/tag/v0.1.0-beta.1
- Family: https://vocahq.com
