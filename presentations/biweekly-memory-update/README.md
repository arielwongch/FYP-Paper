# Biweekly Memory Architecture Update

This folder contains the HTML presentation for the FYP biweekly progress report.

## Open the deck

From the repository root, open `presentations/biweekly-memory-update/index.html` in a browser.

For the most reliable local preview, serve the repository with a small HTTP server:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000/presentations/biweekly-memory-update/index.html
```

## Present

The deck is keyboard-first:

- `Left` / `Right` or `Space`: move between slides
- `S`: open the presenter view with current slide, next slide, notes, and timer
- `T`: cycle through the available themes
- `F`: enter fullscreen
- `O`: open the slide overview
- `R`: reset the presenter timer
- `Esc`: close an overlay

The speaker notes are stored in each slide's `<aside class="notes">` and are hidden from the audience view.

## Render PNG files

The skill's renderer requires Google Chrome at the path used by the script. On macOS, run this from the repository root:

```bash
bash .agents/skills/html-ppt/scripts/render.sh \
  presentations/biweekly-memory-update/index.html \
  all \
  presentations/biweekly-memory-update/rendered
```

This creates one PNG per slide in `presentations/biweekly-memory-update/rendered/`.

To render only the first slide:

```bash
bash .agents/skills/html-ppt/scripts/render.sh \
  presentations/biweekly-memory-update/index.html
```

The bundled script currently hard-codes the macOS Chrome path. In the Linux dev container, use a local Chromium-based screenshot tool or open the HTTP URL above in a browser instead.

## Files

- `index.html`: eight-slide presentation and speaker notes
- `style.css`: presenter-mode template styling
- `README.md`: usage and rendering instructions
