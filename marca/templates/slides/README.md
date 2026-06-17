# Spelbound — Pitch Deck Template

Six brand-aligned pitch slides at **1280×720**, built on the shared design tokens.

## Run it
Open `index.html` for a navigable deck (← / → / space, or the on-screen controls; position persists in `localStorage`). Each slide is also a standalone file you can open, screenshot, or print on its own.

## Slides
| File | Type |
|------|------|
| `slide-01-title.html` | Title / cover (logo lockup) |
| `slide-02-statement.html` | Big editorial statement with script accent |
| `slide-03-services.html` | Light card grid (services) |
| `slide-04-results.html` | Big-number stat band |
| `slide-05-quote.html` | Calligraphic testimonial (light) |
| `slide-06-closing.html` | Closing CTA + contact |

`slide.css` holds the shared slide scaffolding (stage size, eyebrow/heading/body presets, footer lockup).

## Notes
- Alternate dark (maroon) and light (cream) slides for rhythm — the template already does this.
- The deck `index.html` embeds each slide in an iframe; to add a slide, create a new `slide-NN-*.html` and add it to the `slides` array in `index.html`.
- For an editable PowerPoint export, the standalone slides can be captured per-file.
