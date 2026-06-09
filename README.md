# Detail Haus

Marketing and booking website for **Detail Haus** — premium mobile auto detailing serving Southern Oregon (Medford, Jacksonville, Central Point).

Built with [Next.js](https://nextjs.org) (App Router), TypeScript, and Tailwind CSS.

## Getting Started

Install dependencies and start the development server:

```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## Environment Variables

Copy `.env.example` to `.env.local` and fill in the values:

```bash
cp .env.example .env.local
```

| Variable | Description |
| --- | --- |
| `UPLOADTHING_TOKEN` | API token from the [UploadThing](https://uploadthing.com) dashboard (used for quote-request photo uploads). |
| `NEXT_PUBLIC_FORMSPARK_FORM_ID` | Form ID from the [Formspark](https://formspark.io) dashboard (used for the contact / quote form). |

## Project Structure

```
app/          Next.js App Router pages, layout, and API routes
components/    UI, layout, and page-section components
data/          Site content (services, pricing, reviews, service areas, etc.)
lib/           Shared utilities
public/        Static assets (images, icons)
```

Site content is data-driven — most copy, pricing, and listings can be edited
in the `data/` directory without touching component code.

## Build & Deploy

```bash
npm run build   # production build
npm run start   # serve the production build
```

The site is a standard Next.js application and can be deployed to any
Next.js-compatible host (e.g. [Vercel](https://vercel.com)).
