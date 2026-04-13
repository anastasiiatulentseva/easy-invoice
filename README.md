# Invoice Builder

A lightweight [Astro](https://astro.build/) invoice builder for EU-based freelancers and contractors who need a clean local workflow for issuing invoices and accepting payment in both `EUR` and `USD`.

The app runs entirely in the browser, gives you a live invoice preview as you type, and exports through the browser print dialog so you can save polished PDFs without introducing a backend or account system.

This project is intentionally simple:

- No backend
- No database
- No account system
- Live invoice preview as you type
- Built for EU-based invoicing with EUR and USD payment support
- Optional saved sender/payment profile stored in the browser only

## Who This Is For

This repo is useful if you want a starting point for:

- your own invoice template
- a lightweight internal billing tool
- a static app you can fork and personalize
- a local-only invoice generator that keeps data on your machine

## Quick Start

### Clone or download

You can either fork/clone the repo:

```bash
git clone <your-repo-url>
cd invoices
npm install
npm run dev
```

Or download the project as a ZIP, extract it locally, then run:

```bash
npm install
npm run dev
```

Open the local URL printed by Astro, usually `http://localhost:4321`.

## Requirements

- Node.js 20 or newer recommended
- npm 10 or newer recommended

## Available Scripts

```bash
npm run dev      # start the local development server
npm run build    # create a production build in dist/
npm run preview  # preview the production build locally
npm run check    # run Astro project checks
```

## How To Use It

1. Fill in the invoice fields in the left panel.
2. Watch the invoice preview update live.
3. Optionally save your sender and payment details with `Save to Browser`.
4. Click `Download PDF` to open the browser print dialog.
5. Save the invoice as a PDF from the print dialog.

## Data and Privacy

- This app does not send invoice data to a server.
- Saved profile information is stored in the current browser via `localStorage`.
- Saved values stay on that browser/device unless you clear site storage.

## Customization

Most of the project lives in a single page:

- `src/pages/index.astro` contains the form UI, print layout, and browser-side logic

Common tweaks:

- change branding, typography, and colors in the inline styles
- adjust invoice wording and notes defaults
- add or remove line items
- adapt payment fields for your region or business structure

## Project Structure

```text
.
├── src/
│   └── pages/
│       └── index.astro
├── astro.config.mjs
├── package.json
└── README.md
```

## Sharing This Repo

For public sharing, this repo already excludes generated files and local-only data such as:

- `node_modules/`
- `dist/`
- `.astro/`

That keeps forks clean and makes the project safe to copy locally without bundling generated artifacts by default.

## License

MIT. See [LICENSE](./LICENSE).
