# South Coast Sundecks & Exteriors website

A one-page website for South Coast Sundecks & Exteriors Ltd., built with [Astro](https://astro.build). Astro turns the files in `src/` into plain HTML, CSS and images in a `dist/` folder, which any static host (Vercel, Netlify, etc.) can serve.

## Where things are

| What you want to change | File |
| --- | --- |
| Text, services, products, areas, phone | `src/pages/index.astro` (lists at the top, HTML below) |
| Colours, fonts, spacing, animations | `src/styles/global.css` (colours are variables at the top) |
| Page title, Google/social sharing info | `src/layouts/Layout.astro` |
| Photos | `src/assets/` (converted to WebP automatically) |
| Favicon and social sharing image | `public/` |
| Live domain name | `astro.config.mjs` |

## Run it on your computer

You need [Node.js](https://nodejs.org) version 22.23.4 or newer (24 recommended).

```bash
npm install      # first time only
npm run dev      # opens a live preview at http://localhost:4321
npm run build    # makes the final site in dist/
```

## Deploy on Vercel

1. In Vercel, click **Add New → Project** and pick this GitHub repo.
2. Vercel detects Astro on its own. Keep the default settings and click **Deploy**.

## Connect the quote form (must be done before launch)

> **Right now the quote form does not send anything.** The business has no email address yet, so there is nowhere to send requests. Until the form is connected, pressing **Send request** shows the message *"Our online form isn't connected yet. Please call us at 604 921 9185."*

To have quote requests arrive by email:

1. Get an email address from the client for quote requests.
2. Make a free form at [formspree.io](https://formspree.io), sent to that address.
3. Copy the form URL (looks like `https://formspree.io/f/abcdwxyz`).
4. In `src/pages/index.astro`, paste it into `const FORM_ENDPOINT = '';`.
5. Send a test request from the live site and check it arrives.

Once connected, visitors see "Thanks. We'll be in touch about your project." If sending fails, they're asked to try again or call.

## Still to confirm with the client

- **Email address:** none was found on the current site (needed for the form above).
- **Higher-resolution photos:** the current ones are about 1000px wide and watermarked.
- **Vector logo:** get one if available. The current one is a photo banner, so the site uses a simple CSS sun mark and the favicon is drawn to match it.
- **Pages to link:** the existing Warranties, Testimonials, Multi-unit and Seasonal incentives content.

## Undoing a change

Every change is a separate git commit. To undo the most recent one safely (this keeps history):

```bash
git revert HEAD
```
