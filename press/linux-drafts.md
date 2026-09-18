# Linux tip drafts (Vocalinux v0.16.1)

VocaPress owns these. Draft only. Do not send unless Jatin says send. From vocahq@gmail.com as Jatin. Introduce as Jatin, creator and maintainer. Do not add a name or email closer; the VocaHQ Gmail signature already has the mark and hello@vocahq.com.

Facts used (release notes, 30 Aug 2026, plus vocalinux.com / vocahq.com / vocamac.com / vocawin.com): Vocalinux v0.16.1 is the current Available release on the 0.16 line. AGPL-3.0. On-device speech-to-text for Linux (X11 or Wayland) is the default after the model download. Text lands in the focused field. No Voca account. No usage telemetry. VocaGateway is optional self-hosted compute you run; that path is never on-device and is not a Voca cloud. New installs default to hold Right Alt push-to-talk; toggle mode exists. Lives in the system tray. Injection uses IBus when available, clipboard fallback on unbridged compositors. Engines: whisper.cpp default (Vulkan, AMD/Intel/NVIDIA), Whisper (CUDA/PyTorch), VOSK (small/old machines), Remote API to a server you configure. Distros on the site: Ubuntu 24.04+, Debian 12+, Fedora 39+, Arch, openSUSE Tumbleweed. Installer needs distro python3-gi and no longer pip-builds PyGObject. IBus and X11 layout restore fixes. AppImage ships GI typelibs for non-Debian hosts. In-app update checker. Searchable language list. Delete unused models. Test Dictation no longer says "no speech" when no model is downloaded. Site dropped the stale 100% offline badge. What "offline" means in press (Jatin, 24 Aug 2026): speech stays on hardware the user controls. Default is this machine. A gateway is still a LAN box or a host they run, not a vendor cloud that trains on or sells the audio.

Daily use, from the sites, not invented: hold a key, talk, text appears in the app already open. Stays in the tray. Engine is a setting. Jatin uses the family every day on each device. Family with honest status: Vocalinux available now (this pitch); VocaMac beta, macOS 14+ Apple Silicon; VocaWin unsigned beta v0.1.0-beta.1; VocaPhone Android beta / iOS path; VocaGateway early and optional. Do not claim feature parity or that every secure field accepts insertion.

Product shots live at https://vocalinux.com/screenshots/ (page is labeled v0.15 UI). Do not claim those frames are from 0.16. Do not put a version on the screenshots bullet.

Every tip must say the code is open source (AGPL-3.0) and that people already file bugs, feature requests, and PRs. Do not invent star counts or contributor numbers. Discord is https://discord.gg/t6muquAJbm if a desk needs a community URL.

Do not invent versions, benchmarks, or installer success rates.

Bodies updated 4 Sep 2026: bump to v0.16.1 and strengthen on-device default + optional self-hosted Gateway (never on-device). Gmail drafts must be refreshed by VocaHQ from these files. Do not send unless Jatin says send or expand.

---

## How these differ

Each note is a separate letter for that desk. The opening, the ask, and any earlier coverage change. The product facts stay the same.

---

## First-touch

### OMG! Ubuntu
Channel: https://www.omgubuntu.co.uk/tip (prefer the form). Optional: contact@omgubuntu.co.uk

Subject: Linux app tip: Vocalinux v0.16.1

Joey,

I'm Jatin, creator and maintainer of Vocalinux. Your tip box asks for a Linux app you might cover, so I am sending the one I actually live in.

I built Vocalinux because I wanted to talk into whatever I already had open (mail, a browser field, a terminal) without making an account or shipping my voice to a company that trains on it. It sits in the tray. Hold Right Alt (toggle is there if you prefer), talk, and the words land in the focused field. After the model is downloaded, speech runs on that computer by default. VocaGateway is optional self-hosted compute if you want shared hardware; that path is never on-device and is not a Voca cloud.

v0.16.1 shipped 30 Aug under AGPL-3.0. It is open source, and people already file bugs, ask for features, and send PRs. After the rough 0.14 beta I spent the time on IBus restore, getting the X11 layout back after dictation, and stopping the installer from compiling PyGObject via pip. Default engine is whisper.cpp on Vulkan. Whisper is there if you already live in CUDA. VOSK if the box is small.

I use this every day. Linux is the one that is actually out. Mac, Windows, and phone are still beta (Windows is unsigned). Optional shared compute is VocaGateway: self-hosted, never on-device, not a Voca cloud.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.1
- Family: https://vocahq.com

---

### The Register (Liam Proven)
Fallback: news@theregister.com
To: liam.proven@theregister.com

Subject: Vocalinux v0.16.1, on-device dictation for Linux

Liam,

I'm Jatin, creator and maintainer of Vocalinux. Small AGPL-3.0 app for speech-to-text on the Linux desktop.

The pitch is ordinary on purpose. You are already in some window with a cursor. Hold Right Alt, talk, and the tray says it is listening. The model and the audio stay on that machine. There is no Voca account to hand you, because there is not one, and I do not ship telemetry. A company does not get the recording to train on. On-device is the default. If you want shared compute, VocaGateway is optional self-hosted hardware you run; that path is never on-device and is not a Voca cloud.

I use this every day on Linux, and I also keep the Mac, Windows, and phone builds around. Only Linux is a current release. VocaWin is unsigned. VocaGateway is early self-hosted compute and is never on-device. The code is open source. People who actually run it already file bugs, ask for features, and send PRs.

v0.16.1 shipped 30 Aug. Most of the work after 0.14 is install and injection: IBus coming back, X11 layout coming back, AppImage typelibs on non-Debian hosts, and the installer using distro python3-gi instead of a pip build of PyGObject. Engines are whisper.cpp, Whisper, or VOSK.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.1
- Family: https://vocahq.com

---

### LWN.net
To: lwn@lwn.net

Subject: tip: Vocalinux 0.16.1 (on-device STT for Linux)

Jatin here, creator and maintainer of Vocalinux. 0.16.1 is out (2026-08-30). AGPL-3.0. Tray app. Hold-Right-Alt PTT (toggle exists). Injects into the focused field on X11/Wayland via IBus, with clipboard fallback otherwise. Engines: whisper.cpp (default, Vulkan), Whisper, VOSK, or a Remote API you host. No account, no telemetry. On-device is the default after the model download, so audio stays on the operator's hardware. A gateway is still optional self-hosted compute the operator runs; that path is never on-device. The code is open source; external bugs, feature requests, and PRs are already coming in.

I run it daily on Linux and on the other Voca clients (those are betas). Linux is the current release.

0.16 is a stable minor on 0.15. Tester-facing: default hold-Right-Alt PTT on new installs; in-app update checker; searchable languages; delete unused models; installer requires distro python3-gi (no pip sdist of PyGObject); IBus restore and X11 layout restore after scoped injection; AppImage GI typelibs for non-Debian hosts.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.1
- Diff vs 0.15.0: https://github.com/VocaHQ/vocalinux/compare/v0.15.0...v0.16.1
- Family: https://vocahq.com

---

### 9to5Linux
Channel: https://9to5linux.com/contact-us (form only)

Subject: Vocalinux v0.16.1 released

I'm Jatin, creator and maintainer of Vocalinux. v0.16.1 shipped 30 Aug as a stable Linux dictation release under AGPL-3.0.

It is a tray app for X11 or Wayland. You hold Right Alt, talk, and text goes into the focused field. No telemetry and no Voca account. On-device is the default, so audio does not go to a vendor. VocaGateway is optional self-hosted compute you host; that path is never on-device. The code is open source, and people already file bugs, ask for features, and send PRs.

I use it every day. There are Mac, Windows, and phone clients too; those are betas. Linux is the current release.

New installs default to hold Right Alt. 0.16 also fixes IBus restore, X11 layout after dictation, and AppImage startup on non-Debian hosts. Installer needs distro python3-gi. Engines: whisper.cpp, Whisper, VOSK, or a Remote API you point at.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.1
- Family: https://vocahq.com

Install: curl -fsSL https://raw.githubusercontent.com/VocaHQ/vocalinux/main/install.sh -o /tmp/vl.sh && bash /tmp/vl.sh

AppImage and AUR (yay -S vocalinux) are on the release page.

---

### DebugPoint
To: contact@debugpoint.com

Subject: Open-source app: Vocalinux v0.16.1

Hi,

I'm Jatin, creator and maintainer of Vocalinux. You said you will look at open-source apps. This is one I would actually ask someone to try.

Vocalinux v0.16.1 is AGPL-3.0 speech-to-text for Linux. It sits in the tray. You hold Right Alt, talk, and the text lands where the cursor already is. Pick whisper.cpp, Whisper, or VOSK, or point it at a server you run. On-device is the default: speech stays on your computer after the model download. Remote API / VocaGateway is optional self-hosted compute you configure; that path is never on-device and is not a Voca cloud. There is no Voca account, no telemetry, and no vendor training on the audio. The code is open source, and people already file bugs, ask for features, and send PRs.

I use it every day. Mac and Windows are betas, as is the phone client. VocaGateway is early optional self-hosted compute and is never on-device. Linux is the one that is out.

Shipped 23 Aug. After 0.14 I fixed install and desktop glue: IBus, X11 layouts, AppImage on Fedora-class hosts, and distro python3-gi instead of pip-building PyGObject.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Code: https://github.com/VocaHQ/vocalinux
- Family: https://vocahq.com

---

### OSNews
To: osnews-crew@osnews.com

Subject: software news: Vocalinux 0.16.1

Hi,

I'm Jatin, creator and maintainer of Vocalinux. 0.16.1 is out: AGPL-3.0 dictation for Linux desktops.

You hold a key, talk, and text is injected on X11 or Wayland. It lives in the tray. Engines are whisper.cpp, Whisper, or VOSK. No account and no telemetry. On-device is the default, so audio stays on hardware you control. VocaGateway is optional self-hosted compute; that path is never on-device. The code is open source, and people file bugs, ask for features, and send PRs.

I use the Linux build every day, and I use the Mac, Windows, and phone builds too. Only Linux is a current release.

0.16 is the first tag I would hand a reviewer after the 0.14 beta. The beta-window bugs were injection and the installer. New installs use hold Right Alt.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.1
- Family: https://vocahq.com

---

### Dedoimedo
To: webmaster@dedoimedo.com
Subject: REVIEW REQUEST - FREE - Vocalinux

Hi,

This is a free review request for a hobby / non-profit Linux app. No attachments.

I'm Jatin, creator and maintainer of Vocalinux. It is AGPL-3.0 speech-to-text for the Linux desktop. You hold Right Alt, talk, and text goes into the focused field. On-device is the default: the model runs on the machine after the download. There is no Voca account and no vendor cloud. If you host VocaGateway, that is your box; that path is never on-device. The code is open source, and testers already file bugs, request features, and open PRs.

I use this every day. Linux is the one I would have you review. The Mac, Windows, and phone clients exist; they are betas.

v0.16.1 (30 Aug) is the build to try. 0.14 was rough on some Fedora and Ubuntu launches. 0.15 through 0.16.1 cleaned up install and injection. New installs use hold Right Alt. Engines: whisper.cpp, Whisper, or VOSK.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.1
- Family: https://vocahq.com

Plain-text install:

curl -fsSL https://raw.githubusercontent.com/VocaHQ/vocalinux/main/install.sh -o /tmp/vl.sh && bash /tmp/vl.sh

Needs distro python3-gi. AppImage is also on the release page.

---

### Linux Matters
To: show@linuxmatters.sh

Subject: Vocalinux v0.16.1, on-device dictation (adjacent to the Voxtype chat)

Hi,

I'm Jatin, creator and maintainer of Vocalinux. Episode 88 wandered into talking to a computer and Voxtype. Vocalinux is in that pile.

It is AGPL-3.0 dictation for the Linux desktop. Speech-to-text runs on the machine and text goes into the focused field. Hold Right Alt (or toggle) and stay in the window you were already in. On-device is the default. No telemetry and no Voca account. Audio does not go to a corporation. VocaGateway, if you want shared compute, is a box you run; that path is never on-device. The code is open source, and I get bug reports, feature requests, and PRs from people using it.

I use it every day, including on Mac, Windows, and phone. Linux is the mature release. The others are still beta.

v0.16.1 shipped 30 Aug. 0.15 through 0.16.1 were mostly IBus, X11 layout, and installer work so it starts on more distros.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.1
- Family: https://vocahq.com

If a show note would help, I can record a 30-second demo.

---

### Linux Uprising
To: contact@linuxuprising.com

Subject: FOSS app: Vocalinux v0.16.1

Hi,

I'm Jatin, creator and maintainer of Vocalinux. Short app tip for a FOSS utility I use every day.

v0.16.1 is AGPL-3.0. It lives in the tray. Hold Right Alt, talk, and text goes into the focused field. On-device is the default: speech stays on the machine after the model download. No account and no telemetry. The only other path is VocaGateway you host, optional self-hosted compute, never on-device, not a company that trains on the audio. The code is open source, and people already file bugs, ask for features, and send PRs.

whisper.cpp, Whisper, or VOSK. Linux is available now. I also keep the Mac, Windows, and phone clients around; those are betas.

23 Aug also brought an update checker, searchable languages, unused-model cleanup, and the IBus / X11 / AppImage fixes from after 0.14.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.1
- Family: https://vocahq.com

---

### LINUX Unplugged
Channel: https://linuxunplugged.com/contact

Subject: on-device Linux dictation: Vocalinux v0.16.1

Hi,

I'm Jatin, creator and maintainer of Vocalinux. Small AGPL-3.0 tray app for talking into a Linux text field without making a Voca account.

Hold Right Alt, talk, and text lands in the focused app. On-device is the default: the model stays on the computer. Nothing is handed to a vendor. If you want shared compute, VocaGateway is optional self-hosted hardware you run; that path is never on-device. The code is open source, and the community around it already files bugs, asks for features, and sends PRs.

I use this every day on Linux. I also use the Mac, Windows, and phone builds (those are betas; Windows is unsigned).

v0.16.1 shipped 30 Aug. 0.14 was messy on some Fedora and Ubuntu boxes. 0.16.1 is the install-and-injection cut I would actually demo. Engines: whisper.cpp, Whisper, or VOSK.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.1
- Family: https://vocahq.com

---

## Follow-ups (already covered 0.14)

### It's FOSS
To: news@itsfoss.com

Subject: Vocalinux v0.16.1, follow-up to Sourav's 0.14 beta piece

Hi,

I'm Jatin, creator and maintainer of Vocalinux. Sourav Rudra wrote about the 0.14 beta on 16 Jul:

https://itsfoss.com/news/vocalinux-beta-release/

That piece is fair. It failed to launch on Fedora and sat unresponsive on Ubuntu after the troubleshooting steps. Those are the bugs I went after.

v0.16.1 shipped 30 Aug. The installer now requires distro python3-gi and no longer pip-builds PyGObject. The AppImage ships GI typelibs for non-Debian hosts. IBus and the X11 layout come back after injection. Test Dictation no longer says "no speech" when no model is downloaded. New installs default to hold Right Alt. License is AGPL-3.0. Sourav had GPL-3.0, which was true for 0.14.

I still use this every day. Hold Right Alt, talk, and text goes into the focused field. On-device is the default. No telemetry and no Voca account. Audio stays on a machine I control. VocaGateway is optional self-hosted compute and still mine; that path is never on-device. The code is open source, and people already report bugs, ask for features, and send PRs.

Linux is the current release. Mac, Windows, and phone are betas. I am not asking you to pretend the beta was fine. I am asking you to try 0.16.1.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.1
- Family: https://vocahq.com

---

### Linuxiac
To: info@linuxiac.com

Subject: Vocalinux v0.16.1, follow-up to your July piece

Hi,

I'm Jatin, creator and maintainer of Vocalinux. Thanks for the July write-up:

https://linuxiac.com/vocalinux-is-an-open-source-voice-dictation-app-built-for-linux/

0.16.1 shipped 30 Aug, so this is an update, not a first hello. Still Linux dictation. License is now AGPL-3.0 (it was GPL-3.0 when you wrote). Tray, hold Right Alt or toggle, pick an engine, text into the focused field. On-device is the default: speech runs on the machine after the model download. No Voca account, no telemetry, and no vendor cloud. VocaGateway is optional self-hosted compute; that path is never on-device.

The code is open source. People already file bugs, request features, and send PRs. That is how the last two cuts got better.

I use this every day. Linux is the mature release. Mac, Windows, and phone clients are betas.

The new tag is install and desktop reliability after 0.14.x: IBus, X11 layouts, AppImage on non-Debian hosts, and an in-app update checker.

Shots are there if you want to refresh the article. I am not asking for a paid post.

- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.1
- Family: https://vocahq.com

---

### Phoronix
To: news@phoronix.com

Subject: Vocalinux 0.16.1 (follow-up to the 0.14 beta item)

Michael,

I'm Jatin, creator and maintainer of Vocalinux. You ran the 0.14 beta in July:

https://www.phoronix.com/news/Vocalinux-0.14-Beta

0.16.1 is out (2026-08-30), a stable minor on the 0.16 line under AGPL-3.0. Tray app, hold Right Alt, injects into the focused field. Engines: whisper.cpp (Vulkan default), Whisper, VOSK, or a Remote API you host. On-device is the default after the model download. No account and no telemetry. Audio stays on the host, or on optional self-hosted VocaGateway the operator runs; Gateway mode is never on-device. The code is open source, and outside bugs, feature requests, and PRs are already landing.

I use this daily. Linux is the current release.

Versus the beta you ran: default hold-Right-Alt PTT on new installs, in-app GitHub update checker, installer no longer builds PyGObject from sdist, IBus and X11 injection restore, AppImage GI typelibs, whisper.cpp CUDA device 0 and skip software Vulkan devices.

- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.1
- Diff vs 0.15.0: https://github.com/VocaHQ/vocalinux/compare/v0.15.0...v0.16.1
- Family: https://vocahq.com

---

### Linux Magazine
To: edit@linux-magazine.com
Also: pr@linux-magazine.com for a short news note

Subject: Proposal: Vocalinux, on-device dictation on the Linux desktop

Joe,

I'm Jatin, creator and maintainer of Vocalinux. Proposal for a short tools feature. Not a finished article.

v0.16.1 (30 Aug) is an AGPL-3.0 desktop app. Hold Right Alt, talk, and text goes into the focused field while you stay in the current window. Tray. On-device is the default. No telemetry and no Voca account. Audio does not go to a company that trains on it. VocaGateway is optional self-hosted compute and is still a machine the reader runs; that path is never on-device. The code is open source, and readers who try it already file bugs, request features, and send PRs.

I use this every day. Linux is the reviewable release. Mac, Windows, and phone exist as betas.

Walk-through I would give a writer: install.sh / AppImage / AUR, download a model, pick an engine, dictate into a browser and a terminal. IBus scoped injection and X11 layout restore are the failures worth mentioning. 0.16 fixes both.

I can send a 1-2 paragraph outline, and a machine, if the slot is real.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.1
- Family: https://vocahq.com

---

### FOSS Post
To: contact@fosspost.org

Subject: Vocalinux v0.16.1, follow-up

Hi,

I'm Jatin, creator and maintainer of Vocalinux. I sent a tip in July. v0.16.1 shipped 30 Aug. Still AGPL-3.0.

Hold Right Alt, talk, and text lands in the focused field. Tray. On-device is the default. No account and no telemetry. Audio does not go to a vendor. VocaGateway is optional self-hosted compute and yours; that path is never on-device. The code is open source, and people already file bugs, ask for features, and send PRs.

I use this every day, including on Mac, Windows, and phone (those clients are betas).

This is the tag I would have a reader install. Installer and injection fixes after 0.14.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.1
- Family: https://vocahq.com

---

### Late Night Linux
To: show@latenightlinux.com

Subject: Vocalinux v0.16.1, follow-up

Hi,

I'm Jatin, creator and maintainer of Vocalinux. I emailed in July. v0.16.1 is out.

AGPL-3.0 tray app. Hold Right Alt and text goes into the focused field. On-device is the default: speech stays on the computer after the model download. No Voca account, no telemetry, and no vendor. If you want VocaGateway, you host it; that path is never on-device. The code is open source, and the community is already filing bugs, asking for features, and sending PRs.

I use this every day. Linux is the one I would demo. I also carry the Mac, Windows, and phone builds; those are betas.

0.14 was the public introduction. 0.16 is the cleanup I would actually run on the show. Engines: whisper.cpp, Whisper, or VOSK.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.1
- Family: https://vocahq.com

---

### LinuxLinks
To: sde@linuxlinks.com
Also: https://www.linuxlinks.com/suggest-open-source-program/

Subject: Vocalinux v0.16.1, new entry follow-up

Steve,

I'm Jatin, creator and maintainer of Vocalinux. Follow-up to the July note and the New Entry form. Please list 0.16.1, not 0.14.

AGPL-3.0 on-device dictation for Linux. Tray. Hold Right Alt and talk into the focused field. On-device is the default. No account and no telemetry. Audio stays on a machine you control. VocaGateway is optional self-hosted compute if you want shared hardware; that path is never on-device. Engines: whisper.cpp, Whisper, or VOSK. The code is open source, and people already file bugs, request features, and send PRs.

I use this every day. The rest of the family is there if you catalog siblings. Linux is the current release.

- Site: https://vocalinux.com
- Screenshots: https://vocalinux.com/screenshots/
- Release: https://github.com/VocaHQ/vocalinux/releases/tag/v0.16.1
- Family: https://vocahq.com
