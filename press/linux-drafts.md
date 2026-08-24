# Linux tip drafts (Vocalinux v0.16.0)

VocaPress owns these. Draft only. Do not send unless Jatin says send. From vocahq@gmail.com as Jatin. Introduce as Jatin, creator and maintainer. Do not add a name or email closer; the VocaHQ Gmail signature already has the mark and hello@vocahq.com.

Facts used (release notes, 23 Aug 2026): Vocalinux v0.16.0 is a stable minor on the 0.15 line. AGPL-3.0. On-device speech-to-text for Linux (X11 or Wayland). Text lands in the focused field. No Voca account. VocaGateway is optional and is not on-device. New installs default to hold Right Alt push-to-talk. In-app update checker. Searchable language list. Delete unused models. Installer needs distro python3-gi and no longer pip-builds PyGObject. IBus and X11 layout restore fixes. AppImage ships GI typelibs for non-Debian hosts. Test Dictation no longer says "no speech" when no model is downloaded. Site dropped the stale 100% offline claim. Product shots live at https://vocalinux.com/screenshots/ (page is labeled v0.15 UI: tray, dictation, logs, and every Settings page, light and dark). Do not claim those frames are from 0.16.

Do not invent versions, benchmarks, or installer success rates.

---

## How these differ

Same spine: what it is, v0.16.0, why a Linux user would care, links. The opening, the ask, and the "already covered us" line change per desk.

---

## First-touch

### OMG! Ubuntu

Channel: https://www.omgubuntu.co.uk/tip (prefer the form). Optional: contact@omgubuntu.co.uk

Subject: Linux app tip: Vocalinux v0.16.0

Joey,

I'm Jatin, creator and maintainer of Vocalinux. It is an AGPL-3.0 dictation app for the Linux desktop. You hold a key, talk, and the text lands in whatever field is focused: browser, editor, terminal.

v0.16.0 shipped 23 Aug. New installs default to hold Right Alt for push-to-talk. The useful part after the 0.14 beta is reliability: IBus restore, X11 keyboard layout coming back after dictation, and the installer no longer tries to compile PyGObject from pip.

Speech runs on the machine. A self-hosted gateway is optional and is a different path.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0


---

### The Register (Liam Proven)

To: liam.proven@theregister.com
Fallback: news@theregister.com

Subject: Vocalinux v0.16.0, on-device dictation for Linux

Liam,

I'm Jatin, creator and maintainer of Vocalinux, a small AGPL-3.0 app that does speech-to-text on the Linux desktop and types into the focused field.

v0.16.0 shipped 23 Aug. After the 0.14 beta, this cut is mostly install and injection: IBus engine restore, X11 layout coming back after dictation, AppImage typelibs on non-Debian hosts, and the installer no longer pip-builds PyGObject. New installs default to hold-Right-Alt push-to-talk.

The reader hook is ordinary. You are already in an editor, a browser, or a terminal. You talk. The model and the audio stay on that machine unless you point it at a gateway you run.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0

---

### LWN.net

To: lwn@lwn.net

Subject: tip: Vocalinux 0.16.0 (on-device STT for Linux)

Jatin here, creator and maintainer of Vocalinux. 0.16.0 is out (2026-08-23). AGPL-3.0. Local speech-to-text on X11/Wayland; injects into the focused field. Optional self-hosted gateway is a separate path.

0.16 is a stable minor on 0.15. Changes that matter for testers: default hold-Right-Alt PTT on new installs; in-app update checker; searchable language list; delete unused models; installer requires distro python3-gi (no pip sdist of PyGObject); IBus restore and X11 layout restore after scoped injection; AppImage GI typelibs for non-Debian hosts.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0
- Diff vs 0.15.0: https://github.com/VocaHQ/vocalinux/compare/v0.15.0...v0.16.0

---

### 9to5Linux

Channel: https://9to5linux.com/contact-us (form only)

Subject: Vocalinux v0.16.0 released

I'm Jatin, creator and maintainer of Vocalinux. 0.16.0 is a stable Linux dictation app release (23 Aug). AGPL-3.0. On-device speech-to-text, X11 or Wayland, text goes into the focused field.

New installs default to hold Right Alt push-to-talk. The 0.16 cut also fixes IBus restore, X11 layout after dictation, and AppImage startup on non-Debian hosts. Installer needs distro python3-gi.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0

Install: curl -fsSL https://raw.githubusercontent.com/VocaHQ/vocalinux/main/install.sh -o /tmp/vl.sh && bash /tmp/vl.sh

AppImage and AUR (yay -S vocalinux) are on the release page.

---

### DebugPoint

To: contact@debugpoint.com

Subject: Open-source app: Vocalinux v0.16.0

Hi,

I'm Jatin, creator and maintainer of Vocalinux. It is an AGPL-3.0 speech-to-text app for Linux. It sits in the tray, you talk, and the text lands where the cursor already is.

v0.16.0 shipped 23 Aug. After the 0.14 beta, the work is install and desktop reliability: IBus, X11 layouts, AppImage on Fedora-class hosts, and the installer using distro python3-gi instead of building PyGObject from pip. New installs default to hold Right Alt.

Audio and the speech model stay on the machine unless someone sets up a gateway on purpose.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Code: https://github.com/VocaHQ/vocalinux

Happy to feature this if it fits.

---

### OSNews

To: osnews-crew@osnews.com

Subject: software news: Vocalinux 0.16.0

Hi,

I'm Jatin, creator and maintainer of Vocalinux. 0.16.0 is out. It is an AGPL-3.0 dictation app for Linux desktops. Speech-to-text runs on the computer. Text is injected into the focused field on X11 or Wayland.

The 0.16 cut is the first stable release that I would point a reviewer at after the 0.14 beta. Hold-Right-Alt push-to-talk is the new-install default. Injection and installer bugs from that beta window are the main fixes.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0

---

### Dedoimedo

To: webmaster@dedoimedo.com
Subject: REVIEW REQUEST - FREE - Vocalinux

Hi,

This is a free review request for a hobby / non-profit Linux app. No attachments.

I'm Jatin, creator and maintainer of Vocalinux. It is AGPL-3.0 speech-to-text for the Linux desktop. You hold a key, talk, and text goes into the focused field. The model runs on the machine. A gateway is optional and is not the default path.

v0.16.0 (23 Aug) is the build I would have you try. New installs use hold Right Alt. The 0.14 beta was rough on some Fedora and Ubuntu launches; 0.15 and 0.16 are the install and injection cleanup.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0

Plain-text install:

curl -fsSL https://raw.githubusercontent.com/VocaHQ/vocalinux/main/install.sh -o /tmp/vl.sh && bash /tmp/vl.sh

Needs distro python3-gi. AppImage is also on the release page.

---

### Linux Matters

To: show@linuxmatters.sh

Subject: Vocalinux v0.16.0, on-device dictation (adjacent to the Voxtype chat)

Hi,

I'm Jatin, creator and maintainer of Vocalinux. You talked about talking to a computer / Voxtype in episode 88. Vocalinux is in that pile: AGPL-3.0, Linux desktop, speech-to-text on the machine, text into the focused field.

v0.16.0 shipped 23 Aug. Hold Right Alt is the new-install default. The last two point releases were mostly IBus, X11 layout, and installer work so it actually starts on more distros.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0

If it is useful for a show note, I can record a 30-second demo.

---

### Linux Uprising

To: contact@linuxuprising.com

Subject: FOSS app: Vocalinux v0.16.0

Hi,

I'm Jatin, creator and maintainer of Vocalinux. Tray app, push-to-talk, text into the focused field. On-device by default.

v0.16.0 (23 Aug): hold Right Alt on new installs, in-app update checker, searchable languages, unused-model cleanup, and a pile of IBus / X11 / AppImage fixes after the 0.14 beta.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0

---

### LINUX Unplugged

Channel: https://linuxunplugged.com/contact

Subject: on-device Linux dictation: Vocalinux v0.16.0

Hi,

I'm Jatin, creator and maintainer of Vocalinux, a small AGPL-3.0 app for talking into any Linux text field without making a Voca account. The speech model stays on the computer. A self-hosted gateway exists if you want shared compute; that path is not on-device.

v0.16.0 shipped 23 Aug. After a messy 0.14 beta on some Fedora and Ubuntu boxes, 0.16 is the install-and-injection cleanup I would demo on the show. New installs use hold Right Alt.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0

---

## Follow-ups (already covered 0.14)

### It's FOSS

To: news@itsfoss.com

Subject: Vocalinux v0.16.0, follow-up to Sourav's 0.14 beta piece

Hi,

I'm Jatin, creator and maintainer of Vocalinux. Sourav Rudra wrote about the 0.14 beta on 16 Jul:

https://itsfoss.com/news/vocalinux-beta-release/

That piece is fair. The app failed to launch on Fedora and was unresponsive on Ubuntu after the troubleshooting steps. v0.16.0 (23 Aug) is the first stable tag I would ask you to retry.

What changed that is relevant to that review: the installer requires distro python3-gi and no longer pip-builds PyGObject; AppImage ships GI typelibs for non-Debian hosts; IBus restore and X11 layout restore after injection; Test Dictation no longer reports "no speech" when no model is downloaded. New installs default to hold Right Alt. License is AGPL-3.0 (the 0.14 piece said GPL-3.0, which was true then).

I am not asking you to pretend the beta was fine. I am asking you to try 0.16.0.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0

---

### Linuxiac

To: info@linuxiac.com

Subject: Vocalinux v0.16.0, follow-up to your July piece

Hi,

I'm Jatin, creator and maintainer of Vocalinux. Thanks for the July write-up:

https://linuxiac.com/vocalinux-is-an-open-source-voice-dictation-app-built-for-linux/

Vocalinux 0.16.0 shipped 23 Aug. Same product: on-device dictation on Linux, AGPL-3.0 (moved from GPL-3.0), text into the focused field. The new tag is the install and desktop-reliability cut after 0.14.x: IBus, X11 layouts, AppImage on non-Debian hosts, hold-Right-Alt push-to-talk on new installs, and an in-app update checker.

UI shots (labeled v0.15) are here if you want to refresh the article. No paid-post ask.

- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0

---

### Phoronix

To: news@phoronix.com

Subject: Vocalinux 0.16.0 (follow-up to the 0.14 beta item)

Michael,

I'm Jatin, creator and maintainer of Vocalinux. You ran the 0.14 beta in July:

https://www.phoronix.com/news/Vocalinux-0.14-Beta

0.16.0 is out (2026-08-23). Stable minor on 0.15. AGPL-3.0. Same on-device STT story. Changes that are news-shaped: default hold-Right-Alt PTT, in-app GitHub update checker, installer no longer builds PyGObject from sdist, IBus/X11 injection restore, AppImage GI typelibs, whisper.cpp CUDA device 0 and skip software Vulkan devices.

- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0
- Diff vs 0.15.0: https://github.com/VocaHQ/vocalinux/compare/v0.15.0...v0.16.0

---

### Linux Magazine

To: edit@linux-magazine.com
Also: pr@linux-magazine.com for a short news note

Subject: Proposal: Vocalinux, on-device dictation on the Linux desktop

Joe,

I'm Jatin, creator and maintainer of Vocalinux. Proposal for a short tools feature, not a finished article.

Vocalinux is an AGPL-3.0 desktop app that does speech-to-text on the Linux machine and types into the focused field. No Voca account. A self-hosted gateway is optional and should not be described as on-device.

v0.16.0 (23 Aug) is a usable review point after the 0.14 beta. I would walk through install (install.sh, AppImage, AUR), hold-Right-Alt push-to-talk, model download, and dictation into a browser and a terminal. The interesting failures to mention are IBus scoped injection and X11 layout restore, both of which 0.16 fixes.

I can supply a machine and a 1-2 paragraph outline if this slot is useful.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0

---

### FOSS Post

To: contact@fosspost.org

Subject: Vocalinux v0.16.0, follow-up

Hi,

I'm Jatin, creator and maintainer of Vocalinux. I sent a tip in July about the AGPL dictation app for Linux. v0.16.0 shipped 23 Aug. Same story: on-device speech-to-text, text into the focused field, no account. This tag is the one I would have a reader install. Hold Right Alt on new installs; installer and injection fixes after the 0.14 beta.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0

---

### Late Night Linux

To: show@latenightlinux.com

Subject: Vocalinux v0.16.0, follow-up

Hi,

I'm Jatin, creator and maintainer of Vocalinux. I emailed in July. v0.16.0 is out. On-device Linux dictation, AGPL-3.0, tray app, text into the focused field. The 0.14 beta was the public introduction; 0.16 is the install-and-injection cleanup I would actually demo on the show. New installs use hold Right Alt.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0

---

### LinuxLinks

To: sde@linuxlinks.com
Also: https://www.linuxlinks.com/suggest-open-source-program/

Subject: Vocalinux v0.16.0, new entry follow-up

Steve,

I'm Jatin, creator and maintainer of Vocalinux. Follow-up to the July note and the New Entry form. 0.16.0 is the current stable tag. AGPL-3.0 on-device dictation for Linux. Hold Right Alt on new installs. I would list this version, not 0.14.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0
