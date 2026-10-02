# Exploring Design, Technology, and Innovation

A personal blog and portfolio site exploring the intersection of design and technology — where simplicity meets innovation. Features an animated hero section, blog posts, work highlights, a calendar booking embed, and social links.

## Features

- **Animated hero section** — Framer Motion entrance animations over a geometric, bauhaus-inspired layout
- **Blog posts** — curated article cards and reading sections
- **Work highlights** — portfolio showcase of selected projects
- **Calendar embed** — book-a-meeting widget integration
- **Social links** — quick links to social profiles
- **Responsive design** — mobile-first layout with Tailwind CSS
- **Modern UI kit** — full shadcn/ui component set (dialogs, drawers, carousels, charts, forms, and more)

## Tech Stack

- **Framework:** React 18 + TypeScript + Vite
- **Styling:** Tailwind CSS + shadcn/ui (Radix primitives)
- **Animation:** Framer Motion
- **Routing:** React Router (BrowserRouter)
- **Data fetching:** TanStack Query
- **Forms:** React Hook Form + Zod validation
- **Notifications:** Sonner / custom Toaster

## Quick Start

```bash
npm install
npm run dev        # start dev server at http://localhost:8080
npm run build      # production build -> dist/
npm run preview    # preview the production build
```

Requirements: Node.js 18+.

## Project Structure

```
├── index.html
├── public/                  # static assets (favicon, og-image)
├── src/
│   ├── App.tsx              # router + providers (QueryClient, Tooltip, Toaster)
│   ├── main.tsx             # entry point
│   ├── pages/
│   │   ├── Index.tsx        # landing page composition
│   │   └── NotFound.tsx     # 404 page
│   ├── components/
│   │   ├── HeroSection.tsx  # animated hero
│   │   ├── BlogPosts.tsx    # blog section
│   │   ├── WorkHighlights.tsx
│   │   ├── CalendarEmbed.tsx
│   │   ├── SocialLinks.tsx
│   │   └── ui/              # shadcn/ui components
│   ├── index.css            # Tailwind + theme tokens
├── tailwind.config.ts
├── vite.config.ts
└── tsconfig.json
```

## Deploy

Static site — deploy the `dist/` folder to any static host:

```bash
npm run build
# then deploy dist/ to Cloudflare Pages, Netlify, or GitHub Pages
```

No environment variables required. Because the app uses `BrowserRouter`, static hosts should rewrite all routes to `index.html` (a `_redirects` / `/* /index.html 200` rule) so deep links work.

## License

MIT — free to use and adapt.

---

*Built by [Girish Lade](https://ladestack.in) — explore more open-source tools and products at [ladestack.in](https://ladestack.in).*
