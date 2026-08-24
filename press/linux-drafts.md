# Linux tip drafts (Vocalinux v0.16.0)

VocaPress owns these. Draft only. Do not send unless Jatin says send. From vocahq@gmail.com as Jatin. Introduce as Jatin, creator and maintainer. Do not add a name or email closer; the VocaHQ Gmail signature already has the mark and hello@vocahq.com.

Facts used (release notes, 23 Aug 2026, plus vocalinux.com / vocahq.com / vocamac.com / vocawin.com on 24 Aug 2026): Vocalinux v0.16.0 is a stable minor on the 0.15 line. AGPL-3.0. On-device speech-to-text for Linux (X11 or Wayland). Text lands in the focused field. No Voca account. No usage telemetry. VocaGateway is optional and is not on-device. New installs default to hold Right Alt push-to-talk; toggle mode exists. Lives in the system tray. Injection uses IBus when available, clipboard fallback on unbridged compositors. Engines: whisper.cpp default (Vulkan, AMD/Intel/NVIDIA), Whisper (CUDA/PyTorch), VOSK (small/old machines), Remote API to a server you configure. Distros on the site: Ubuntu 24.04+, Debian 12+, Fedora 39+, Arch, openSUSE Tumbleweed. Installer needs distro python3-gi and no longer pip-builds PyGObject. IBus and X11 layout restore fixes. AppImage ships GI typelibs for non-Debian hosts. In-app update checker. Searchable language list. Delete unused models. Test Dictation no longer says "no speech" when no model is downloaded. Site dropped the stale 100% offline badge. What "offline" means in press (Jatin, 24 Aug 2026): speech stays on hardware the user controls. Default is this machine. A gateway is still a LAN box or a host they run, not a vendor cloud that trains on or sells the audio.

Daily use, from the sites, not invented: hold a key, talk, text appears in the app already open. Stays in the tray. Engine is a setting. Jatin uses the family every day on each device. Family with honest status: Vocalinux available now (this pitch); VocaMac beta, macOS 14+ Apple Silicon; VocaWin unsigned beta v0.1.0-beta.1; VocaPhone Android beta / iOS path; VocaGateway early and optional. Do not claim feature parity or that every secure field accepts insertion.

Product shots live at https://vocalinux.com/screenshots/ (page is labeled v0.15 UI). Do not claim those frames are from 0.16. Do not put a version on the screenshots bullet.

Every tip must say the code is open source (AGPL-3.0) and that people already file bugs, feature requests, and PRs. Do not invent star counts or contributor numbers. Discord is https://discord.gg/t6muquAJbm if a desk needs a community URL.

Do not invent versions, benchmarks, or installer success rates.

---

## How these differ

Each note is a separate letter for that desk. The opening, the ask, and any earlier coverage change. The product facts stay the same.

---

## First-touch

### OMG! Ubuntu

Channel: https://www.omgubuntu.co.uk/tip (prefer the form). Optional: contact@omgubuntu.co.uk

Subject: Linux app tip: Vocalinux v0.16.0

Joey,

I'm Jatin, creator and maintainer of Vocalinux. You asked for a Linux app you might cover, so here is mine.

Vocalinux v0.16.0 is AGPL-3.0. It sits in the tray. Hold Right Alt (toggle is there if you prefer it), talk, and the words show up in whatever field has focus. I do this all day: mail, a browser box, a terminal. Speech runs on that computer. No Voca account, no telemetry, and nothing goes to a company that trains on the recording. If someone wants a gateway, they host it. Usually on their own network.

The code is open source. People already file bugs, ask for features, and send PRs. I am not sitting on this alone.

I also run the Mac, Windows, and phone clients every day. Linux is the one that is actually out. The others are still beta (Windows is unsigned). Optional shared compute is VocaGateway, which you host.

0.16 shipped 23 Aug. New installs use hold Right Alt. After the 0.14 beta I spent the time on IBus restore, getting the X11 layout back after dictation, and stopping the installer from compiling PyGObject via pip. Default engine is whisper.cpp on Vulkan. Whisper is there if you already live in CUDA. VOSK if the box is small.

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

I'm Jatin, creator and maintainer of Vocalinux. Small AGPL-3.0 app. Speech-to-text on the Linux desktop, into the field that already has the cursor.

You are already in some window. Hold Right Alt. Talk. The tray says it is listening. The model and the audio stay on that machine. I do not have a Voca account to give you, because there is not one. I also do not ship telemetry. A company does not get the recording to train on. A gateway is optional, and if you use one it is yours: a LAN box or a host you run.

Source is public, AGPL-3.0. The repo takes issues and PRs from people who actually run it.

I use this every day on Linux, and on the Mac, Windows, and phone builds as well. Only Linux is a current release. The rest are betas. VocaWin is unsigned. VocaGateway is early and self-hosted.

v0.16.0 shipped 23 Aug. Most of the work after 0.14 is install and injection: IBus coming back, X11 layout coming back, AppImage typelibs on non-Debian hosts, and the installer using distro python3-gi instead of a pip build of PyGObject. New installs default to hold Right Alt. whisper.cpp, Whisper, or VOSK.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0
- Family: https://vocahq.com

---

### LWN.net

To: lwn@lwn.net

Subject: tip: Vocalinux 0.16.0 (on-device STT for Linux)

Jatin here, creator and maintainer of Vocalinux. 0.16.0 is out (2026-08-23). AGPL-3.0. Tray app. Hold-Right-Alt PTT (toggle exists). Injects into the focused field on X11/Wayland via IBus, clipboard fallback otherwise. Engines: whisper.cpp (default, Vulkan), Whisper, VOSK, or a Remote API you host. No account, no telemetry. Audio stays on the operator's hardware; a gateway is still operator-hosted. Open source (AGPL-3.0). External bugs, feature requests, and PRs are already coming in.

I run it daily on Linux and on the other Voca clients (those are betas). Linux is the current release.

0.16 is a stable minor on 0.15. Tester-facing: default hold-Right-Alt PTT on new installs; in-app update checker; searchable languages; delete unused models; installer requires distro python3-gi (no pip sdist of PyGObject); IBus restore and X11 layout restore after scoped injection; AppImage GI typelibs for non-Debian hosts.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0
- Diff vs 0.15.0: https://github.com/VocaHQ/vocalinux/compare/v0.15.0...v0.16.0
- Family: https://vocahq.com

---

### 9to5Linux

Channel: https://9to5linux.com/contact-us (form only)

Subject: Vocalinux v0.16.0 released

I'm Jatin, creator and maintainer of Vocalinux. v0.16.0 is out (23 Aug). Stable Linux dictation release. AGPL-3.0. X11 or Wayland. Hold Right Alt, talk, text goes into the focused field. Tray app. No telemetry, no Voca account. Audio does not go to a vendor. A gateway is optional and you host it. Open source. People already open issues and PRs.

Engines: whisper.cpp, Whisper, VOSK, or a Remote API you point at.

I use it every day. There are Mac, Windows, and phone clients too; those are betas. Linux is the current release.

New installs default to hold Right Alt. 0.16 also fixes IBus restore, X11 layout after dictation, and AppImage startup on non-Debian hosts. Installer needs distro python3-gi.

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

I'm Jatin, creator and maintainer of Vocalinux. You said you will look at open-source apps. This is one.

Vocalinux v0.16.0 is AGPL-3.0 speech-to-text for Linux. Tray icon. Hold Right Alt, talk, the text lands on the cursor. whisper.cpp, Whisper, or VOSK, or a server you run. The speech stays on your computer (or on that server). No Voca account. No telemetry. No vendor training on the audio.

I use it every day. vocahq.com is the rest of the family if you care: Mac and Windows betas, a phone beta, an early self-hosted gateway. Linux is the one that is out.

The code is open source. People already file bugs and send PRs.

Shipped 23 Aug. After 0.14 I fixed install and desktop glue: IBus, X11 layouts, AppImage on Fedora-class hosts, distro python3-gi instead of pip-building PyGObject. New installs use hold Right Alt.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Code: https://github.com/VocaHQ/vocalinux
- Family: https://vocahq.com

---

### OSNews

To: osnews-crew@osnews.com

Subject: software news: Vocalinux 0.16.0

Hi,

I'm Jatin, creator and maintainer of Vocalinux. 0.16.0 is out. AGPL-3.0 dictation for Linux desktops. Hold a key, talk, text is injected on X11 or Wayland. Tray app. whisper.cpp, Whisper, or VOSK.

No account. No telemetry. Audio stays on hardware you control. A gateway is still a machine you run. The source is open. People file bugs and send PRs.

I use the Linux build every day, and I use the Mac, Windows, and phone builds too. Only Linux is a current release.

0.16 is the first tag I would hand a reviewer after the 0.14 beta. New installs use hold Right Alt. The beta-window bugs were injection and the installer.

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

I'm Jatin, creator and maintainer of Vocalinux. AGPL-3.0 speech-to-text on the Linux desktop. Hold Right Alt, talk, text goes into the focused field. Tray. No telemetry. Pick whisper.cpp, Whisper, or VOSK. The model runs on the machine. There is no Voca account and no vendor cloud. If you host a gateway, that is your box.

I use this every day. Linux is the one I would have you review. The code is open source (AGPL). Testers already file bugs, request features, and open PRs. The Mac, Windows, and phone clients exist; they are betas.

v0.16.0 (23 Aug) is the build to try. New installs use hold Right Alt. 0.14 was rough on some Fedora and Ubuntu launches. 0.15 and 0.16 cleaned up install and injection.

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

I'm Jatin, creator and maintainer of Vocalinux. Episode 88 wandered into talking to a computer and Voxtype. Vocalinux is in that pile.

AGPL-3.0. Linux desktop. Speech-to-text on the machine. Text into the focused field. Hold Right Alt (or toggle) and stay in the window you were already in. Tray. No telemetry. No Voca account. Audio does not go to a corporation. A gateway, if you want one, is a box you run.

The source is open. I get bug reports, feature requests, and PRs from people using it.

I use it every day, including on Mac, Windows, and phone. Linux is the mature release. The others are still beta.

v0.16.0 shipped 23 Aug. Hold Right Alt is the new-install default. 0.15 and 0.16 were mostly IBus, X11 layout, and installer work so it starts on more distros.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0
- Family: https://vocahq.com

If a show note would help, I can record a 30-second demo.

---

### Linux Uprising

To: contact@linuxuprising.com

Subject: FOSS app: Vocalinux v0.16.0

Hi,

I'm Jatin, creator and maintainer of Vocalinux. Short app tip.

v0.16.0, AGPL-3.0. Tray. Hold Right Alt, talk, text goes into the focused field. Speech stays on the machine. No account, no telemetry. The only other path is a gateway you host, not a company that trains on the audio.

Open source. People already help: issues, feature requests, PRs.

I use it every day. whisper.cpp, Whisper, or VOSK. Linux is available now. I also keep the Mac, Windows, and phone clients around; those are betas.

23 Aug. New installs use hold Right Alt. Also an update checker, searchable languages, unused-model cleanup, and the IBus / X11 / AppImage fixes from after 0.14.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0
- Family: https://vocahq.com

---

### LINUX Unplugged

Channel: https://linuxunplugged.com/contact

Subject: on-device Linux dictation: Vocalinux v0.16.0

Hi,

I'm Jatin, creator and maintainer of Vocalinux. Small AGPL-3.0 tray app. You talk into a Linux text field. No Voca account. Hold Right Alt, talk, text lands in the focused app. whisper.cpp, Whisper, or VOSK. The model stays on the computer. Nothing is handed to a vendor. If you want shared compute, you run a gateway.

The code is public. The community around it already files bugs and sends PRs.

I use this every day on Linux. I also use the Mac, Windows, and phone builds (those are betas; Windows is unsigned). Linux is the current release.

v0.16.0 shipped 23 Aug. 0.14 was messy on some Fedora and Ubuntu boxes. 0.16 is the install-and-injection cut I would actually demo. New installs use hold Right Alt.

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

That piece is fair. The app failed to launch on Fedora and sat there unresponsive on Ubuntu after the troubleshooting steps. Those are the bugs I went after.

v0.16.0 shipped 23 Aug. The installer now requires distro python3-gi and no longer pip-builds PyGObject. The AppImage ships GI typelibs for non-Debian hosts. IBus and the X11 layout come back after injection. Test Dictation no longer says "no speech" when no model is downloaded. New installs default to hold Right Alt. License is AGPL-3.0. Sourav had GPL-3.0, which was true for 0.14.

I still use this every day. Hold Right Alt, talk, text goes into the focused field. Tray. No telemetry. No Voca account. Audio stays on a machine I control. A gateway is optional and is still mine.

Source is open. People already report bugs, ask for features, and send PRs.

Linux is the current release. I also run the Mac, Windows, and phone clients (betas). I am not asking you to pretend the beta was fine. I am asking you to try 0.16.0.

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

0.16.0 shipped 23 Aug, so this is an update, not a first hello. Still Linux dictation. License is now AGPL-3.0 (it was GPL-3.0 when you wrote). Text still goes into the focused field. Tray, hold Right Alt or toggle, pick an engine. Speech runs on the machine. No Voca account, no telemetry, no vendor cloud. A gateway is a host you run.

Still open source. The issue tracker and incoming PRs are how the last two cuts got better.

I use this every day. Linux is the mature release. There are Mac, Windows, and phone clients now; those are betas.

The new tag is install and desktop reliability after 0.14.x: IBus, X11 layouts, AppImage on non-Debian hosts, hold Right Alt on new installs, in-app update checker.

Shots are there if you want to refresh the article. I am not asking for a paid post.

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

0.16.0 is out (2026-08-23). Stable minor on 0.15. AGPL-3.0. Tray app, hold Right Alt, injects into the focused field. Engines: whisper.cpp (Vulkan default), Whisper, VOSK, or a Remote API you host. No account, no telemetry. Audio stays on the host or a gateway the operator runs. AGPL-3.0 source is public. Outside bugs and PRs are already landing.

I use this daily. Linux is the current release.

Versus the beta you ran: default hold-Right-Alt PTT on new installs, in-app GitHub update checker, installer no longer builds PyGObject from sdist, IBus and X11 injection restore, AppImage GI typelibs, whisper.cpp CUDA device 0 and skip software Vulkan devices.

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

I'm Jatin, creator and maintainer of Vocalinux. Proposal for a short tools feature. Not a finished article.

Vocalinux v0.16.0 (23 Aug) is an AGPL-3.0 desktop app. Speech-to-text on the Linux machine. Text into the focused field. Hold Right Alt, talk, stay in the current window. Tray. No telemetry. No Voca account. Audio does not go to a company that trains on it. A self-hosted gateway is optional and is still a machine the reader runs.

The code is open source (AGPL-3.0). Readers who try it already file bugs, request features, and send PRs.

I use this every day. Linux is the reviewable release. Mac, Windows, and phone exist as betas.

Walk-through I would give a writer: install.sh / AppImage / AUR, hold Right Alt, download a model, pick an engine, dictate into a browser and a terminal. IBus scoped injection and X11 layout restore are the failures worth mentioning. 0.16 fixes both.

I can send a 1-2 paragraph outline, and a machine, if the slot is real.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0
- Family: https://vocahq.com

---

### FOSS Post

To: contact@fosspost.org

Subject: Vocalinux v0.16.0, follow-up

Hi,

I'm Jatin, creator and maintainer of Vocalinux. I sent a tip in July. v0.16.0 shipped 23 Aug. Still AGPL-3.0.

Hold Right Alt, talk, text lands in the focused field. Tray. No account. No telemetry. Audio does not go to a vendor. A gateway is optional and yours. The code is open source. People already open issues and PRs. I use this every day, including on Mac, Windows, and phone (those clients are betas).

This is the tag I would have a reader install. New installs use hold Right Alt. Installer and injection fixes after 0.14.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0
- Family: https://vocahq.com

---

### Late Night Linux

To: show@latenightlinux.com

Subject: Vocalinux v0.16.0, follow-up

Hi,

I'm Jatin, creator and maintainer of Vocalinux. I emailed in July. v0.16.0 is out.

AGPL-3.0 tray app. Hold Right Alt. Text into the focused field. Speech stays on the computer. No Voca account. No telemetry. No vendor. If you want a gateway, you host it.

Open source. The community is already filing bugs and sending PRs.

I use this every day. Linux is the one I would demo. I also carry the Mac, Windows, and phone builds; those are betas.

0.14 was the public introduction. 0.16 is the cleanup I would actually run on the show. New installs use hold Right Alt. whisper.cpp, Whisper, or VOSK.

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

I'm Jatin, creator and maintainer of Vocalinux. Follow-up to the July note and the New Entry form. Please list 0.16.0, not 0.14.

AGPL-3.0 on-device dictation for Linux. Tray. Hold Right Alt, talk into the focused field. No account, no telemetry. Audio stays on a machine you control. whisper.cpp, Whisper, or VOSK.

AGPL and public. People already file bugs, request features, and send PRs.

I use this every day. vocahq.com has the rest of the family if you catalog siblings. Linux is the current release.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.0
- Family: https://vocahq.com
