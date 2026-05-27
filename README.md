# Finance Executive Portal (Prototype)

A Marcel-style, exec-first finance portal prototype that turns an **Excel-tab mental model** into a lightweight web UI: **About**, **Financials**, **Performance**, **KPIs**, **People**, and **Access & Governance**.

This repo is designed to be safe to publish: it uses **mock datasets only** (no internal systems, no Power BI tokens, no private endpoints).

## What’s included

- Exec landing page with a 15‑second “thumb test” and editable narrative.
- KPI semantic layer with finance-owned thresholds (traffic lights).
- Performance drivers table + charts.
- Controlled ingestion stubs (P&L / Balance Sheet upload placeholders).
- Governance page to adjust KPI thresholds (prototype role switch).

## Tech stack

- React + Vite (dev server / build tooling)
- shadcn/ui components (local `@/components/ui/*`)
- Tailwind CSS (styling)
- framer-motion (animations), recharts (charts), lucide-react (icons)

## Quick start

### 1) Prerequisites

- Node.js: use a modern Node version supported by Vite.

### 2) Install

```bash
npm install
```

### 3) Initialise shadcn/ui (required for `@/components/ui/*` imports)

This project imports UI primitives like:

- `@/components/ui/card`, `button`, `badge`, `input`, `label`, `select`, `separator`, `switch`, `textarea`, `tooltip`, `alert`, `progress`, `tabs`

Run:

```bash
npx shadcn@latest init -t vite
```

Then add the components you use. Example (run as needed):

```bash
npx shadcn@latest add card
npx shadcn@latest add button
npx shadcn@latest add badge
npx shadcn@latest add input
npx shadcn@latest add label
npx shadcn@latest add select
npx shadcn@latest add separator
npx shadcn@latest add switch
npx shadcn@latest add textarea
npx shadcn@latest add tooltip
npx shadcn@latest add alert
npx shadcn@latest add progress
npx shadcn@latest add tabs
```

> Note: Ensure your project has the `@` import alias pointing to `src` so imports like `@/components/ui/card` resolve.

### 4) Run the app

```bash
npm run dev
```

### 5) Build

```bash
npm run build
npm run preview
```

## Where to put the portal code

- Put your main portal component in `src/App.jsx` (or import it from `src/components/Portal.jsx` and render from `src/App.jsx`).

## Notes on data / security

- All data in this repo is mock data defined in code.
- No private URLs, tokens, SSO config, or internal API calls.

## Licence

Choose a licence appropriate for your use (MIT is common for open-source prototypes). Add a `LICENSE` file if you’re publishing publicly.
