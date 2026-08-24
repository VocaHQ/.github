# Linux tip drafts (Vocalinux v0.16.0)

VocaPress owns these. Draft only. Do not send unless Jatin says send. From vocahq@gmail.com as Jatin. Introduce as Jatin, creator and maintainer. Do not add a name or email closer; the VocaHQ Gmail signature already has the mark and hello@vocahq.com.

Facts used (release notes, 23 Aug 2026, plus vocalinux.com / vocahq.com / vocamac.com / vocawin.com on 24 Aug 2026): Vocalinux v0.16.0 is a stable minor on the 0.15 line. AGPL-3.0. On-device speech-to-text for Linux (X11 or Wayland). Text lands in the focused field. No Voca account. No usage telemetry. VocaGateway is optional and is not on-device. New installs default to hold Right Alt push-to-talk; toggle mode exists. Lives in the system tray. Injection uses IBus when available, clipboard fallback on unbridged compositors. Engines: whisper.cpp default (Vulkan, AMD/Intel/NVIDIA), Whisper (CUDA/PyTorch), VOSK (small/old machines), Remote API to a server you configure. Distros on the site: Ubuntu 24.04+, Debian 12+, Fedora 39+, Arch, openSUSE Tumbleweed. Installer needs distro python3-gi and no longer pip-builds PyGObject. IBus and X11 layout restore fixes. AppImage ships GI typelibs for non-Debian hosts. In-app update checker. Searchable language list. Delete unused models. Test Dictation no longer says "no speech" when no model is downloaded. Site dropped the stale 100% offline badge. Press meaning of offline (Jatin, 24 Aug 2026): speech stays on hardware the user controls. Default is this machine. A gateway is still a LAN box or a host they run, not a vendor cloud that trains on or sells the audio.

Everyday use to sell (from the sites, not invented): hold a key, talk, text appears in the app already open (browser, editor, IDE, terminal, office). Stays in the tray. Engine is a setting. Jatin uses the family every day on each device. Family with honest status: Vocalinux available now (this pitch); VocaMac beta, macOS 14+ Apple Silicon; VocaWin unsigned beta v0.1.0-beta.1; VocaPhone Android beta / iOS path; VocaGateway early and optional. Do not claim feature parity or that every secure field accepts insertion.

Product shots live at https://vocalinux.com/screenshots/ (page is labeled v0.15 UI). Do not claim those frames are from 0.16. Do not put a version on the screenshots bullet.

Do not invent versions, benchmarks, or installer success rates.

---

## How these differ

Same spine: what it is, why it is private and open source, what daily use feels like, the family in one breath, v0.16.0, links. The opening, the ask, and the "already covered us" line change per desk.

---

## First-touch

### OMG! Ubuntu

Channel: https://www.omgubuntu.co.uk/tip (prefer the form). Optional: contact@omgubuntu.co.uk

Subject: Linux app tip: Vocalinux v0.16.0

Joey,

I'm Jatin, creator and maintainer of Vocalinux. It is an AGPL-3.0 dictation app for the Linux desktop. You hold Right Alt (or switch to toggle), talk, and the text lands in whatever field is focused: browser, editor, IDE, terminal, office app. It lives in the tray so it stays out of the way.

The reason it exists is privacy. Speech runs on your computer. There is no Voca account, no telemetry, and no vendor cloud that trains on the recording. If you stand up a gateway, that is still a box you run, usually on your own network. Offline in that sense: the audio does not leave hardware you control.

I use this every day, on every machine I sit at. Linux is the mature one. The same gesture exists on Mac (VocaMac, beta), Windows (VocaWin, unsigned beta), and phone (VocaPhone). Optional shared compute is VocaGateway, which you host.

v0.16.0 shipped 23 Aug. New installs default to hold Right Alt. The useful part after the 0.14 beta is reliability: IBus restore, X11 keyboard layout coming back after dictation, and the installer no longer tries to compile PyGObject from pip. Engine is a setting: whisper.cpp by default (Vulkan), Whisper if you already live in CUDA, VOSK on a small box.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0
- Family: https://vocahq.com

---

### The Register (Liam Proven)

To: liam.proven@theregister.com
Fallback: news@theregister.com

Subject: Vocalinux v0.16.0, on-device dictation for Linux

Liam,

I'm Jatin, creator and maintainer of Vocalinux, a small AGPL-3.0 app that does speech-to-text on the Linux desktop and types into the focused field.

The reader hook is ordinary and a bit stubborn. You are already in an editor, a browser, an IDE, or a terminal. You hold Right Alt and talk. The tray shows it is listening. Text lands where the cursor already is. The audio and the model stay on that machine. There is no Voca account and no telemetry. Nothing goes to a company that will train on the recording or sell it. A gateway is optional, and if you use one it is still yours (LAN or a host you run).

I use the family every day: Linux, Mac, Windows, phone. Vocalinux is the one that is actually out. VocaMac and VocaWin are betas. VocaPhone is a phone beta. VocaGateway is early self-hosted compute, not a vendor cloud.

v0.16.0 shipped 23 Aug. After the 0.14 beta, this cut is mostly install and injection: IBus engine restore, X11 layout coming back after dictation, AppImage typelibs on non-Debian hosts, and the installer no longer pip-builds PyGObject. New installs default to hold-Right-Alt push-to-talk. You can pick whisper.cpp, Whisper, or VOSK.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0
- Family: https://vocahq.com

---

### LWN.net

To: lwn@lwn.net

Subject: tip: Vocalinux 0.16.0 (on-device STT for Linux)

Jatin here, creator and maintainer of Vocalinux. 0.16.0 is out (2026-08-23). AGPL-3.0. Tray app; hold-Right-Alt PTT (or toggle); injects into the focused field on X11/Wayland (IBus, clipboard fallback). Engines: whisper.cpp (default, Vulkan), Whisper, VOSK, or a Remote API you host. No Voca account, no telemetry. Default path does not send audio to a vendor. Optional gateway is operator-hosted.

I use this daily. Same family on Mac/Windows/phone (those are betas). Linux is the current release.

0.16 is a stable minor on 0.15. Tester-facing changes: default hold-Right-Alt PTT on new installs; in-app update checker; searchable language list; delete unused models; installer requires distro python3-gi (no pip sdist of PyGObject); IBus restore and X11 layout restore after scoped injection; AppImage GI typelibs for non-Debian hosts.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0
- Diff vs 0.15.0: https://github.com/VocaHQ/vocalinux/compare/v0.15.0...v0.16.0
- Family: https://vocahq.com

---

### 9to5Linux

Channel: https://9to5linux.com/contact-us (form only)

Subject: Vocalinux v0.16.0 released

I'm Jatin, creator and maintainer of Vocalinux. 0.16.0 is a stable Linux dictation app release (23 Aug). AGPL-3.0. On-device speech-to-text, X11 or Wayland. Hold Right Alt, talk, text goes into the focused field in the app you already have open. Tray app. No telemetry. Engine is a setting: whisper.cpp, Whisper, VOSK, or a Remote API you host.

It is open source and local. There is no Voca account. Audio does not go to a vendor that trains on user speech. A gateway is optional and is something you host.

I use Vocalinux every day. The rest of the family is the same idea on other machines: VocaMac (Mac beta), VocaWin (Windows unsigned beta), VocaPhone (phone beta), VocaGateway (early, self-hosted).

New installs default to hold Right Alt. The 0.16 cut also fixes IBus restore, X11 layout after dictation, and AppImage startup on non-Debian hosts. Installer needs distro python3-gi.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0
- Family: https://vocahq.com

Install: curl -fsSL https://raw.githubusercontent.com/VocaHQ/vocalinux/main/install.sh -o /tmp/vl.sh && bash /tmp/vl.sh

AppImage and AUR (yay -S vocalinux) are on the release page.

---

### DebugPoint

To: contact@debugpoint.com

Subject: Open-source app: Vocalinux v0.16.0

Hi,

I'm Jatin, creator and maintainer of Vocalinux. It is an AGPL-3.0 speech-to-text app for Linux. It sits in the tray. You hold Right Alt, talk, and the text lands where the cursor already is: browser, editor, IDE, terminal. Pick an engine (whisper.cpp, Whisper, or VOSK) or point it at a server you run.

Speech stays on your computer, or on a gateway you run. It does not go to a company that trains on user audio or sells it. There is no Voca account and no telemetry.

I use this every day. There is a Voca app for Mac, Windows, and phone too. Linux is the one that is available now; the others are betas. vocahq.com has the map.

v0.16.0 shipped 23 Aug. After the 0.14 beta, the work is install and desktop reliability: IBus, X11 layouts, AppImage on Fedora-class hosts, and the installer using distro python3-gi instead of building PyGObject from pip. New installs default to hold Right Alt.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Code: https://github.com/VocaHQ/vocalinux
- Family: https://vocahq.com

Happy to feature this if it fits.

---

### OSNews

To: osnews-crew@osnews.com

Subject: software news: Vocalinux 0.16.0

Hi,

I'm Jatin, creator and maintainer of Vocalinux. 0.16.0 is out. It is an AGPL-3.0 dictation app for Linux desktops. Hold a key, talk, text is injected into the focused field on X11 or Wayland. Tray app. Works in the app you already have open. Engine is a setting (whisper.cpp, Whisper, VOSK).

Source is open. There is no Voca account and no telemetry. Audio stays on hardware you control. A gateway, if you want one, is still a machine you run, not a vendor cloud.

I use the Voca family every day across Linux, Mac, Windows, and phone. Vocalinux is the current Linux release. The others are betas; VocaGateway is early self-hosted compute.

The 0.16 cut is the first stable release that I would point a reviewer at after the 0.14 beta. Hold-Right-Alt push-to-talk is the new-install default. Injection and installer bugs from that beta window are the main fixes.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0
- Family: https://vocahq.com

---

### Dedoimedo

To: webmaster@dedoimedo.com
Subject: REVIEW REQUEST - FREE - Vocalinux

Hi,

This is a free review request for a hobby / non-profit Linux app. No attachments.

I'm Jatin, creator and maintainer of Vocalinux. It is AGPL-3.0 speech-to-text for the Linux desktop. You hold Right Alt, talk, and text goes into the focused field in whatever app you were already using. Tray app. No telemetry. Pick whisper.cpp, Whisper, or VOSK. The model runs on the machine. There is no vendor cloud in the default path. If you host a gateway, that is still your box.

I use this every day. Same idea on Mac, Windows, and phone (those clients are betas). Linux is the one I would have you review.

v0.16.0 (23 Aug) is the build I would have you try. New installs use hold Right Alt. The 0.14 beta was rough on some Fedora and Ubuntu launches; 0.15 and 0.16 are the install and injection cleanup.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0
- Family: https://vocahq.com

Plain-text install:

curl -fsSL https://raw.githubusercontent.com/VocaHQ/vocalinux/main/install.sh -o /tmp/vl.sh && bash /tmp/vl.sh

Needs distro python3-gi. AppImage is also on the release page.

---

### Linux Matters

To: show@linuxmatters.sh

Subject: Vocalinux v0.16.0, on-device dictation (adjacent to the Voxtype chat)

Hi,

I'm Jatin, creator and maintainer of Vocalinux. You talked about talking to a computer / Voxtype in episode 88. Vocalinux is in that pile: AGPL-3.0, Linux desktop, speech-to-text on the machine, text into the focused field. Hold Right Alt (or toggle), talk into the browser or the terminal you already have open. Tray app. No telemetry. Engine is a setting.

No account. Audio does not go to a corporation. A gateway is optional and stays under your control.

I use this every day, and I use the rest of the family on Mac, Windows, and phone. Linux is the mature release. The others are betas.

v0.16.0 shipped 23 Aug. Hold Right Alt is the new-install default. The last two point releases were mostly IBus, X11 layout, and installer work so it actually starts on more distros.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0
- Family: https://vocahq.com

If it is useful for a show note, I can record a 30-second demo.

---

### Linux Uprising

To: contact@linuxuprising.com

Subject: FOSS app: Vocalinux v0.16.0

Hi,

I'm Jatin, creator and maintainer of Vocalinux. Tray app, push-to-talk, text into the focused field in the app you already have open. AGPL-3.0. On-device by default, no Voca account, no telemetry. Speech stays local. A self-hosted gateway is the only other path, and that is still yours, not a company that trains on the audio.

Daily use is the point. Hold Right Alt, talk, keep working. Pick whisper.cpp, Whisper, or VOSK. I use it every day. Same family on Mac, Windows, and phone; those are betas. Linux is available now.

v0.16.0 (23 Aug): hold Right Alt on new installs, in-app update checker, searchable languages, unused-model cleanup, and a pile of IBus / X11 / AppImage fixes after the 0.14 beta.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0
- Family: https://vocahq.com

---

### LINUX Unplugged

Channel: https://linuxunplugged.com/contact

Subject: on-device Linux dictation: Vocalinux v0.16.0

Hi,

I'm Jatin, creator and maintainer of Vocalinux, a small AGPL-3.0 app for talking into any Linux text field without making a Voca account. Hold Right Alt, talk, text lands in the focused app. Tray. No telemetry. whisper.cpp, Whisper, or VOSK. The speech model stays on the computer. Nothing is handed to a vendor to train on. A self-hosted gateway exists if you want shared compute; that is still a machine you run, not a corporate API.

I use this every day on Linux, and I use the rest of the Voca family on Mac, Windows, and phone. Linux is the current release. The others are betas. VocaGateway is early and self-hosted.

v0.16.0 shipped 23 Aug. After a messy 0.14 beta on some Fedora and Ubuntu boxes, 0.16 is the install-and-injection cleanup I would demo on the show. New installs use hold Right Alt.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0
- Family: https://vocahq.com

---

## Follow-ups (already covered 0.14)

### It's FOSS

To: news@itsfoss.com

Subject: Vocalinux v0.16.0, follow-up to Sourav's 0.14 beta piece

Hi,

I'm Jatin, creator and maintainer of Vocalinux. Sourav Rudra wrote about the 0.14 beta on 16 Jul:

https://itsfoss.com/news/vocalinux-beta-release/

That piece is fair. The app failed to launch on Fedora and was unresponsive on Ubuntu after the troubleshooting steps. v0.16.0 (23 Aug) is the first stable tag I would ask you to retry.

The product promise is local, open source dictation you can use all day. Hold Right Alt, talk into the browser or the editor you already have open. Tray app. No telemetry. Engine is a setting. AGPL-3.0 (the 0.14 piece said GPL-3.0, which was true then). No Voca account. Audio stays on a machine you control. A gateway is optional and is still yours, not a vendor that trains on speech.

I use Vocalinux every day. The same gesture exists on Mac, Windows, and phone (those clients are betas). Linux is the one that is available now.

What changed that is relevant to that review: the installer requires distro python3-gi and no longer pip-builds PyGObject; AppImage ships GI typelibs for non-Debian hosts; IBus restore and X11 layout restore after injection; Test Dictation no longer reports "no speech" when no model is downloaded. New installs default to hold Right Alt.

I am not asking you to pretend the beta was fine. I am asking you to try 0.16.0.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0
- Family: https://vocahq.com

---

### Linuxiac

To: info@linuxiac.com

Subject: Vocalinux v0.16.0, follow-up to your July piece

Hi,

I'm Jatin, creator and maintainer of Vocalinux. Thanks for the July write-up:

https://linuxiac.com/vocalinux-is-an-open-source-voice-dictation-app-built-for-linux/

Vocalinux 0.16.0 shipped 23 Aug. Same product: open source dictation on Linux, AGPL-3.0 (moved from GPL-3.0), text into the focused field in the app you already have open. Tray. Hold Right Alt or toggle. Engine is a setting. Speech runs on the machine. There is no Voca account, no telemetry, and no vendor cloud that trains on the audio. A gateway is optional and is a host you run.

I use this every day. There is now a Voca client for Mac, Windows, and phone as well. Linux is the mature release; the others are betas.

The new tag is the install and desktop-reliability cut after 0.14.x: IBus, X11 layouts, AppImage on non-Debian hosts, hold-Right-Alt push-to-talk on new installs, and an in-app update checker.

UI shots are here if you want to refresh the article. No paid-post ask.

- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0
- Family: https://vocahq.com

---

### Phoronix

To: news@phoronix.com

Subject: Vocalinux 0.16.0 (follow-up to the 0.14 beta item)

Michael,

I'm Jatin, creator and maintainer of Vocalinux. You ran the 0.14 beta in July:

https://www.phoronix.com/news/Vocalinux-0.14-Beta

0.16.0 is out (2026-08-23). Stable minor on 0.15. AGPL-3.0. Tray app, hold-Right-Alt PTT, injects into the focused field. Engines: whisper.cpp (Vulkan default), Whisper, VOSK, or a Remote API you host. No Voca account, no telemetry. Audio stays on the host or a gateway the operator runs, not a vendor API.

I use this daily. Same family on Mac, Windows, and phone (betas). Linux is the current release.

Changes that are news-shaped: default hold-Right-Alt PTT, in-app GitHub update checker, installer no longer builds PyGObject from sdist, IBus/X11 injection restore, AppImage GI typelibs, whisper.cpp CUDA device 0 and skip software Vulkan devices.

- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0
- Diff vs 0.15.0: https://github.com/VocaHQ/vocalinux/compare/v0.15.0...v0.16.0
- Family: https://vocahq.com

---

### Linux Magazine

To: edit@linux-magazine.com
Also: pr@linux-magazine.com for a short news note

Subject: Proposal: Vocalinux, on-device dictation on the Linux desktop

Joe,

I'm Jatin, creator and maintainer of Vocalinux. Proposal for a short tools feature, not a finished article.

Vocalinux is an AGPL-3.0 desktop app that does speech-to-text on the Linux machine and types into the focused field. Hold Right Alt, talk, keep working in the browser, the IDE, or the terminal. Tray app. No telemetry. Engine is a setting. No Voca account. The audio does not go to a company that trains on it. A self-hosted gateway is optional and is still a machine the reader runs; it should not be described as a vendor cloud.

I use this every day. The same family exists on Mac, Windows, and phone (those are betas). Linux is the reviewable release.

v0.16.0 (23 Aug) is a usable review point after the 0.14 beta. I would walk through install (install.sh, AppImage, AUR), hold-Right-Alt push-to-talk, model download, engine choice, and dictation into a browser and a terminal. The interesting failures to mention are IBus scoped injection and X11 layout restore, both of which 0.16 fixes.

I can supply a machine and a 1-2 paragraph outline if this slot is useful.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0
- Family: https://vocahq.com

---

### FOSS Post

To: contact@fosspost.org

Subject: Vocalinux v0.16.0, follow-up

Hi,

I'm Jatin, creator and maintainer of Vocalinux. I sent a tip in July about the AGPL dictation app for Linux. v0.16.0 shipped 23 Aug.

Same story, said plainly: open source, local, private. Hold Right Alt, talk, text lands in the app you already have open. Tray. No account. No telemetry. Audio does not go to a vendor. A gateway is optional and is still yours. I use this every day, and I use the rest of the family on Mac, Windows, and phone (those are betas).

This tag is the one I would have a reader install. Hold Right Alt on new installs; installer and injection fixes after the 0.14 beta.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0
- Family: https://vocahq.com

---

### Late Night Linux

To: show@latenightlinux.com

Subject: Vocalinux v0.16.0, follow-up

Hi,

I'm Jatin, creator and maintainer of Vocalinux. I emailed in July. v0.16.0 is out. AGPL-3.0 Linux dictation, tray app, hold Right Alt, text into the focused field in whatever you already have open. Speech stays on your computer. There is no Voca account, no telemetry, and no vendor that trains on the audio. If you want a gateway, you host it.

I use this every day. Same family on Mac, Windows, and phone; those clients are betas. Linux is the one I would demo.

The 0.14 beta was the public introduction; 0.16 is the install-and-injection cleanup I would actually run on the show. New installs use hold Right Alt. Engine is a setting: whisper.cpp, Whisper, or VOSK.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0
- Family: https://vocahq.com

---

### LinuxLinks

To: sde@linuxlinks.com
Also: https://www.linuxlinks.com/suggest-open-source-program/

Subject: Vocalinux v0.16.0, new entry follow-up

Steve,

I'm Jatin, creator and maintainer of Vocalinux. Follow-up to the July note and the New Entry form. 0.16.0 is the current stable tag. AGPL-3.0 on-device dictation for Linux. Tray app. Hold Right Alt, talk into the focused field. No account, no telemetry. Audio stays on a machine you control (this box, or a gateway you run). Engine choice: whisper.cpp, Whisper, VOSK.

I use this every day. Family directory is vocahq.com (Mac and Windows betas, phone beta, early self-hosted gateway). I would list this Linux version, not 0.14.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0
- Family: https://vocahq.com
