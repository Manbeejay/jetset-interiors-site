# JetSet Interiors

Marketing website for JetSet Interiors, an interior design and space-planning business based in Enugu, Nigeria.

**Live site:** _add your Vercel/production URL here once deployed_

## About

JetSet Interiors offers residential and commercial interior decoration, space planning, furniture selection, lighting design, wall finishes, curtains and blinds, 3D visualisation, renovations, and full project management. This site is the business's main online presence: it shows the services, pricing, past work, and a way to reach the business directly on WhatsApp.

## Tech stack

- Single self-contained HTML file (`index.html`), inline CSS, vanilla JavaScript
- No frameworks, no build step, no dependencies except Google Fonts
- Fully static, deployable anywhere that serves plain HTML

## File structure

```
.
├── index.html          # the entire site
└── images/             # all photos and logos referenced by the site
    ├── hero-1.jpg … hero-5.jpg      # hero background slideshow
    ├── master-bedroom.jpg
    ├── feature-wall.jpg
    ├── retail-store.jpg
    ├── 3d-render.jpg
    ├── home-office.jpg              # contact section photo
    └── logo-*.png                   # partner logos
```

`index.html` expects the `images` folder to sit next to it. Keep that structure wherever the site is hosted.

## Sections

1. **Hero** — business name, tagline, rotating background slideshow, primary WhatsApp CTA
2. **What we do** — full service list
3. **About / Why us** — differentiators
4. **Pricing** — four tiers (Consultation, Design Package, Design + Project Management, Commercial Fit-Out), each linking into the quote form
5. **Gallery** — clickable project photos with a lightbox
6. **What clients say** — testimonials (placeholder, swap for real Google Business reviews)
7. **Our partners** — logos of organisations JetSet has worked with
8. **Contact** — phone, email, appointment note, opening hours
9. **Terms of service** — pricing terms, materials supply, shopping trips, payment and cancellation, VAT
10. **Footer** — company registration, social links, Privacy Policy pop-up

The **quote form** and **Privacy Policy** both open as in-page pop-ups (no separate pages). The quote form hands off to WhatsApp with the visitor's details pre-filled, since the site has no backend to receive submissions.

## Updating content

Everything lives in `index.html`, there's no CMS. Common edits:

| To change... | Look for... |
|---|---|
| Phone number | `+2348037079002` (tel: and WhatsApp links) |
| Email | `hello@jetsetinteriors.ng` |
| Pricing tiers | the `<section class="pricing">` block |
| Gallery photos | `<figure onclick="openLightbox(...)">` entries, plus matching files in `images/` |
| Hero slideshow photos | the five `.slide` `<div>`s inside `.hero-bg` |
| Reviews | `<div class="rev">` cards |
| Partner logos | `<div class="partner">` cards, plus matching files in `images/` |
| Privacy Policy text | the `#privacyModal` markup |
| Terms of service | the `<details>` accordion items in `#terms` |

Photos should be resized to roughly 1400–1800px wide and compressed (JPEG quality ~80) before adding them, to keep the page fast to load on mobile.

## Deployment

This site is designed to be hosted as static files:

1. Push `index.html` and `images/` to this repository.
2. Import the repo into [Vercel](https://vercel.com) (or Netlify, GitHub Pages, etc.), framework preset **Other**, no build command.
3. Point a custom domain at the deployment once one is registered.

## License

All rights reserved. Content, photos and branding belong to JetSet Interiors.
