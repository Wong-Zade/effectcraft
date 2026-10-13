# WongsEffect app icon

**Design:** a white badge with a bold W on a near-black rounded tile (`#0e0d0d`, white `#ffffff`).

**Tile:** 512 x 512 viewBox, filling it edge to edge, which suits Windows and Linux. macOS icons use Apple's
grid instead: an 824 px body centred on a 1024 canvas with a transparent margin.

**Provenance:** supplied by the project owner as `source.png` (503 px). `effectcraft.svg` is a vector trace
of it (potrace, after upscaling and sharpening the edges); every other file here is rendered from the SVG.
Licence: see [LICENSE.txt](LICENSE.txt) (the owner's brand mark, not open source).

## Files

| File | What |
|---|---|
| `source.png` | the supplied image the rest is made from |
| `effectcraft.svg` | master vector (canonical); `effectcraft-small.svg` and the web favicon are copies |
| `effectcraft-1024.png` | 1024 px render |
| `effectcraft-macos-512.png` | runtime Dock icon on macOS, on Apple's 824/1024 grid |
| `effectcraft.icns` | macOS icon (Apple grid) |
| `effectcraft.ico` | Windows icon, 16-256 px; embedded in `effectcraft.exe` by `apps/effectcraft/build.rs` |
| `hicolor/<n>x<n>/apps/ai.storyteller.effectcraft.png` | Linux icon theme, 16-512 px; the 256 px one is the runtime icon on Windows and Linux |
| `hicolor/scalable/apps/ai.storyteller.effectcraft.svg` | Linux scalable icon |

App ID: `ai.storyteller.effectcraft` (Wayland app ID, `packaging/linux/ai.storyteller.effectcraft.desktop`).

## Regenerate

Put a new vector over `effectcraft.svg` (copy it to `effectcraft-small.svg`, the hicolor scalable icon and
`apps/effectcraft-web/web/favicon.svg` too), then run `packaging/icons.sh` (needs `resvg`; `iconutil` on macOS for
the `.icns`).
