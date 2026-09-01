# Voca family catalog

Print-ready family catalogs. Two formats, same truth. Status follows PRODUCT.md (verified 2026-08-24). Do not invent shipping.

## Live files

- [voca-family-catalog-portrait.pdf](voca-family-catalog-portrait.pdf)  -  US Letter portrait (8.5 x 11 in), 10 pages. Handouts and binders.
- [voca-family-catalog-landscape.pdf](voca-family-catalog-landscape.pdf)  -  US Letter landscape (11 x 8.5 in), 6 pages. Desk, wall, print-and-keep.

Page previews: [pages/](pages/) (`portrait-01.png` … `portrait-10.png`, `landscape-01.png` … `landscape-06.png`).

QR codes (print-safe, quiet zone): [qr/](qr/). Each product page points at that product's live URL. The last page is a scan wall.

## Print notes

- Paper: US Letter.
- Color. Solid teal pages are full bleed. Ask the shop for borderless / full-bleed Letter, or print on oversized stock and trim.
- Scale: 100%. Do not shrink to fit. Do not "fit to printable area."
- Print color: exact. The paper is warm (`#F4F1E8`), not white. The teal is `#0F6B57`.
- Binding: portrait can saddle or live in a binder. Landscape is a poster stack; page 6 is the hangable QR wall.


## Reprint from `src/`

HTML in `src/` is the source. Live PDFs and `pages/` are printed from it. A headless print that does not load CSS, marks, or QR produces an unstyled dump — do not commit that.

Before print, resolve HTML-relative assets next to `src/*.html` (do not commit the copies):

- `catalog/qr/` → `src/qr/`
- `brand/vocahq/voca-app-icon.svg` and `brand/vocagateway/vocagateway-1u.svg` → `src/marks/`
- Nimbus Sans Regular/Bold/Italic + DejaVu Sans Mono into `src/fonts/` (see `@font-face` in `src/css/catalog.css`)

Serve `src/` over http (not a CSS-less stdin dump). Chromium print, backgrounds on, `@page` letter, margin 0. Portrait is 10 pages; landscape is 6, landscape Letter.

Rasterize previews at **150 dpi** (Letter → 1275×1650 portrait, 1650×1275 landscape) and keep the dpi tag. Eyeball before replacing live files: cover still editorial “one voice / every machine”; p03 + l01 keep teal; p10 + l06 stay teal QR walls; Linux chip **v0.16.0**; Mac chip **v0.9.0**.

## What is in each book

Portrait: cover (one voice / every machine + ecosystem.map), manifesto, two paths, VocaLinux, VocaMac, VocaPhone, VocaWin (unsigned beta, no invented screenshot), VocaGateway (1U host mark, never on-device), family directory, QR wall.

Landscape: split cover, Linux+Mac spread, Phone+Win spread, Gateway + two paths, manifesto + directory strip, QR wall.

Contact on paper is vocahq.com and github.com/VocaHQ. No email.

## Previous versions

The 2026-08-18 v0.15.0 books (Linux still labeled v0.15.0) live in [studies/2026-08-18-v015/](studies/2026-08-18-v015/). Do not use them as the live files.

The 2026-08-18 v1 spec-sheet (cream field, teal left rail, no QR codes) lives in [studies/2026-08-18-v1/](studies/2026-08-18-v1/). Do not use it as the live file. The old single-file name `voca-family-catalog.pdf` is retired.
