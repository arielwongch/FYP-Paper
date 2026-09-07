# Biweekly Memory Architecture Update

This folder contains the HTML presentation for the FYP biweekly progress report.

For the easiest download and browser rendering experience, use
`biweekly-memory-update-standalone.html`. It is a single self-contained file
with inline CSS, slide content, navigation, fullscreen mode, and speaker notes.

## Open the deck

### Standalone file

Open `biweekly-memory-update-standalone.html` directly in any modern browser.
No server, build step, or additional asset folder is required.

You can also open a specific slide with a hash, for example:

```text
biweekly-memory-update-standalone.html#/4
```

### Template-based version

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

The standalone file supports the same core controls, including `S` for speaker
notes and `F` for fullscreen. Its notes panel is embedded in the same browser
window rather than opening a separate presenter popup.

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
- `biweekly-memory-update-standalone.html`: one-file browser/download version
- `style.css`: presenter-mode template styling
- `README.md`: usage and rendering instructions
