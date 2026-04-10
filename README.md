# Cloudcore Astro Frontend

An Astro starter for Cloudcore CMS.

## Quick Start

```bash
# Install dependencies
npm install

# Configure CMS URL
# Create .env file with:
PUBLIC_CMS_URL=http://localhost:8787/api/v1

# Start development
npm run dev
```

## Structure

```
src/
├── components/
│   └── BlockRenderer.astro  # Renders CMS content blocks
├── layouts/
│   └── Base.astro           # Base layout with header/footer
├── lib/
│   └── api.ts               # CMS API client
├── pages/
│   ├── index.astro          # Homepage
│   ├── blog/
│   │   ├── index.astro      # Blog listing
│   │   └── [slug].astro     # Single post
│   └── [...slug].astro      # Dynamic pages
└── styles/
    └── globals.css
```

## Environment Variables

| Variable | Description |
|----------|-------------|
| `PUBLIC_CMS_URL` | Cloudcore CMS API URL (default: `http://localhost:8787/api/v1`) |

## Customization

### Adding Block Types

Edit `src/components/BlockRenderer.astro` to add new block type handling.

### Styling

Uses Tailwind CSS. Edit `tailwind.config.mjs` to customize theme.

## Build & Deploy

```bash
# Build static site
npm run build

# Preview build
npm run preview
```

Deploy the `dist/` folder to any static hosting (Cloudflare Pages, Vercel, Netlify, etc.).
