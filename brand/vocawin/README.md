# VocaWin marks

VocaWin reuses the family microphone from `brand/vocahq/`. There is no unique Win accent. Plate `#0F6B57`, mark on teal `#F2F6F2`.

## Live files

- `installer/` — MSI/NSIS bitmaps. Do not redraw the mic or invent a maroon WiX theme.
- `vocawin-sidebar.svg` — 31×31 tile for the app sidebar. Official paths, tighter crop so the glyph reads at sidebar size. Drop this in at 31×31. Do not scale the 1024 family icon down.
- `vocawin-dictate-idle.svg` — 78×78 circle, cream mic on teal. Ready / idle.
- `vocawin-dictate-listening.svg` — 78×78 circle, teal mic on cream. Listening. Recording stays red in the app; these files do not cover that state.

Previews at true size: `previews/`.

Cite `brand/README.md` §7, §9, and §10. Public status is Beta per PRODUCT.md. Builds stay unsigned. Latest Release is v0.1.0-beta.1 (prerelease): https://github.com/VocaHQ/vocawin/releases/tag/v0.1.0-beta.1
