# Agüita Sustainability LAB — Landing Page

A single-page promotional landing for the **Agüita Sustainability LAB**, a hands-on
sustainable-automation workshop held on the **Agüita House** rooftop in Las Palmas de
Gran Canaria — **Thursday 11 June 2026, from 18:00**.

The lab shows that anyone, with no coding or hardware background, can build small smart
automations (a self-watering plant, a surf-wave tracker web app) that make everyday things
more efficient and more sustainable.

## Content

The page is a single scrolling layout with the following sections:

- **Navbar** — sticky, frosted, with the Agüita House logo, section links and a WhatsApp
  "reserve a spot" CTA.
- **Hero** — full-bleed rooftop-sunset photo, headline, intro and event details
  (date, location, "all levels welcome").
- **Overview** — what the workshop is about, with hardware photos and brand illustration.
- **Timeline** — the 9 steps of the evening (18:00 → 20:40), rendered from a JS data array.
- **Speakers** — Nicola Gasparro (coding support) and Vicente Matus Icaza (hardware support).
- **FAQ** — accordion of six common questions.
- **Final CTA** — "save your seat", reservation via WhatsApp.
- **Footer** — organisers and sponsors (IDeTIC · ULPGC and Digital Consulting Agüita SL).

All three "reserve a spot" buttons open WhatsApp (`wa.me/34603786656`) with a prefilled message.

## Tech stack

- **HTML5** — single static `index.html`, no build step.
- **CSS3** — design tokens in `colors_and_type.css` (colors, type, spacing, radii, shadows)
  plus page styles inline in `index.html`. Layout uses CSS grid/flexbox, `clamp()` fluid
  type, sticky nav and `backdrop-filter`.
- **Vanilla JavaScript** — no framework. Renders the timeline and FAQ from data arrays,
  drives the FAQ accordion, injects inline SVG icons, and animates scroll reveals via
  `IntersectionObserver`.
- **Icons** — inline [Lucide](https://lucide.dev) SVG paths (MIT).
- **Fonts** — self-hosted *Avocado Cake* (display) and *Helvetica Neue* (functional);
  *Caveat* (script) loaded from Google Fonts.

No dependencies, no package manager, no bundler.

## Project structure

```
index.html              # the landing page (markup, styles, scripts)
colors_and_type.css     # Agüita design tokens
fonts/                  # self-hosted Avocado Cake + Helvetica Neue
assets/
  logo/                 # Agüita House logo
  illustrations/        # hand-drawn brand illustrations
img/                    # workshop & speaker photography
```

## Running locally

It's a static page — just open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Credits

Built on the **Agüita** brand design system (a beach/surf hostel in Las Palmas de Gran
Canaria). Organised by Nicola Gasparro & Vicente Matus. Sponsored by IDeTIC · ULPGC and
Digital Consulting Agüita SL.
