# Griffin Immigration Website

Production website for **Griffin Immigration Private Limited** — an immigration consultancy and coaching institute in Sonipat, Haryana. Built with SvelteKit + Tailwind CSS, deployed on Cloudflare Pages.

**Live:** https://griffinimmigration.com | **Preview:** https://griffin-immigration.pages.dev

---

## Business Context

| | |
|---|---|
| **Company** | Griffin Immigration Pvt. Ltd. (CIN: U74999HR2022PTC106123) |
| **Founded** | August 26, 2022 |
| **Founder** | Naveen Malik (Sole Director) |
| **Office** | Mayur Vihar, Gali No 15, Near Shambhu Dayal School, Gohana Road Bypass, Sonipat, Haryana — 131001 |
| **Phone** | +91 7274080000 (also WhatsApp) |
| **Email** | hello@griffinimmigration.com |
| **Hours** | Mon–Sat, 10:00 AM – 6:00 PM |
| **Instagram** | @griffinimmigration |
| **Domain** | griffinimmigration.com (Cloudflare registrar, Zoho Mail for email) |

### Services (5 categories)
1. **Student Visa** — university selection, admission, SOP, visa filing for 6 countries
2. **Work Visa & PR** — Express Entry, skilled migration, job seeker, PR pathways
3. **IELTS Coaching** — in-house, all 4 modules, mock tests
4. **PTE Coaching** — in-house, computer-based practice (formerly TOEFL)
5. **Career Guidance** — removed from site per client request (page deleted)

### Target Countries (6)
Canada, Australia, Czech Republic, UK, Germany, USA

### Language
English only

---

## Tech Stack

| | |
|---|---|
| **Framework** | SvelteKit 2.x (`@sveltejs/kit ^2.63`) |
| **Svelte version** | Svelte 5 (runes mode) |
| **CSS** | Tailwind CSS v4 (`@tailwindcss/vite`) |
| **Language** | TypeScript |
| **Adapter** | `@sveltejs/adapter-cloudflare` (deploys to Cloudflare Pages) |
| **Backend** | Cloudflare Pages Functions (SvelteKit server actions) |
| **Database** | Cloudflare KV (`GRIFFIN_DB` namespace) |
| **Email** | Resend.com API (transactional emails from form) |
| **Font** | Inter (Google Fonts, loaded via Tailwind config) |
| **Package manager** | npm |

---

## Design System

### Colors — Professional Blue + Orange
| Token | Hex | Usage |
|---|---|---|
| `brand-500` | `#2563eb` | Primary blue — buttons, links, accents |
| `brand-50`–`900` | Full scale | Backgrounds, borders |
| `accent-500` | `#e67e22` | Warm orange — CTAs, highlights |
| `accent-50`–`900` | Full scale | Badge backgrounds |
| Body bg | `#ffffff` | Pure white |
| Text | `#334155` | Slate-700 |
| Headings | `#0f172a` | Slate-900 |
| Footer bg | `slate-900` | Dark |

### Typography
- **All Inter** (Playfair Display was tried and removed)
- Headings: `font-extrabold` for h1, `font-bold` for h2/h3
- Body: `text-sm` to `text-base`, `text-slate-600`/`text-slate-500`

### Theme tokens defined in `src/app.css`:
```css
@theme {
  --color-brand-50 through 900
  --color-accent-50 through 900
  --font-body: Inter
}
```

---

## File Structure

```
griffin-immigration/
├── src/
│   ├── app.css              # Tailwind import + @theme tokens + base styles
│   ├── app.html             # HTML shell (Google Fonts link)
│   ├── lib/
│   │   ├── site.ts          # ALL site data: countries, services, testimonials, nav, stats, coaching features
│   │   └── components/
│   │       ├── Header.svelte  # Sticky white header, mobile hamburger, 8 nav links, "Call Us Now" CTA
│   │       ├── Footer.svelte  # 4-column: brand + quick links + services + contact, CIN bar
│   │       └── WhatsAppButton.svelte  # Fixed green circle bottom-right
│   └── routes/
│       ├── +layout.svelte   # Root layout: Header + <main> + Footer + WhatsAppButton
│       ├── +page.svelte     # HOMEPAGE
│       ├── services/
│       │   └── +page.svelte # OUR SERVICES page
│       ├── coaching/
│       │   └── +page.svelte # IELTS & PTE COACHING page
│       ├── study-abroad/
│       │   ├── +page.svelte             # STUDY ABROAD listing
│       │   └── [slug]/+page.svelte      # Per-country detail (6 dynamic routes)
│       ├── work-pr/
│       │   └── +page.svelte # WORK & PR page
│       ├── about/
│       │   └── +page.svelte # ABOUT US page
│       ├── success/
│       │   └── +page.svelte # SUCCESS STORIES (+ scorecard gallery)
│       ├── contact/
│       │   ├── +page.svelte       # CONTACT page (form + map + info)
│       │   └── +page.server.ts    # Server action: save to KV + send emails
│       └── admin/
│           ├── +page.svelte       # Admin dashboard (stats + table + delete)
│           ├── +page.server.ts    # Auth check + load/delete submissions
│           └── login/
│               ├── +page.svelte       # Login form
│               └── +page.server.ts    # Password check + cookie set
├── static/
│   ├── logo.jpeg           # Company logo
│   ├── office.jpg           # Office photo 1
│   ├── office-1.jpg         # Office photo 2
│   ├── classroom.jpg        # Classroom photo (IELTS/PTE page)
│   ├── student-review.mp4   # Student testimonial video
│   └── success-stories/     # 17 scorecard images (10 IELTS + 7 PTE)
├── package.json
├── vite.config.ts           # Adapter config + Tailwind plugin
└── tsconfig.json
```

---

## Pages (8 total)

| Route | Title | Content |
|---|---|---|
| `/` | Home | Gradient hero ("Griffin Immigration" + tagline + office photo), 5 service bullets, office photos, country cards with Unsplash backgrounds + flags, services grid, stats, testimonials |
| `/services` | Our Services | Services grid + 4-step process + why-us reasons + CTA |
| `/coaching` | IELTS & PTE Coaching | Hero + classroom photo section (8 feature bullets) + IELTS modules + PTE modules (matching light cards) + coaching features + batch timings (10AM-12PM, 12PM-2PM, weekend) + CTA |
| `/study-abroad` | Study Abroad | Country grid listing with flags → links to 6 slug pages |
| `/study-abroad/[slug]` | Per country | Photo hero, education highlights, visa programs, 4-step process, country-specific data |
| `/work-pr` | Work & PR | 4 visa programs (Express Entry, Skilled Migration, Skilled Worker, EU Blue Card) + 4-step process |
| `/about` | About Us | Story, mission/vision/values, Founder Naveen Malik, office |
| `/success` | Success Stories | Combined IELTS + PTE scorecard gallery (17 images with badges) + 10 written testimonials + student video |
| `/contact` | Contact | Compact info card + Google Map (280px) + enquiry form → saves to KV + sends email |
| `/admin` | Dashboard | Password-protected (`Griffin@2025`), shows stats + table of submissions, delete button |
| `/admin/login` | Login | Password form with cookie auth |

### Nav order (Header & site.ts navLinks):
Home → Our Services → IELTS/PTE → Study Abroad → Work & PR → About Us → Success Stories → Contact

---

## Backend / Features

### Contact Form (`/contact`)
- **Method:** SvelteKit form action (POST via `use:enhance`)
- **Storage:** Cloudflare KV (`GRIFFIN_DB` namespace, key `submissions`)
- **Email:** Resend API (`re_cgqh5g7t_...`) — sends:
  1. Auto-reply to customer (`hello@griffinimmigration.com` as sender)
  2. Notification to Griffin team (`hello@griffinimmigration.com`)
- **Key hardcoded** in `contact/+page.server.ts` (was tried as Cloudflare secret `RESEND_API_KEY` but platform.env unreliable)
- **Resend domain:** `griffinimmigration.com` is verified (status: sending enabled)

### Admin Dashboard (`/admin`)
- **Auth:** Password `Griffin@2025` (stored as Cloudflare Pages secret `ADMIN_PASSWORD`, with hardcoded fallback)
- **Cookie:** `griffin_admin` (httpOnly, sameSite strict, 24h)
- **Features:** Stats (total, today, by service type), submissions table, individual delete (POST form action)
- **Data source:** Cloudflare KV (`GRIFFIN_DB`)

### WhatsApp Float Button
- Fixed bottom-right, green circle, links to `https://wa.me/917274080000`

---

## Deployment

### Cloudflare Pages
- **Project:** `griffin-immigration`
- **Account:** futec805@gmail.com (`b154ccbabd6d4c6ef93015d10bab7d30`)
- **Build command:** `npm run build`
- **Output dir:** `.svelte-kit/cloudflare`
- **KV Binding:** `GRIFFIN_DB` → namespace `f504f44ba5fe406f8516be25f51682d7`
- **Secrets:** `ADMIN_PASSWORD` = `Griffin@2025`, `RESEND_API_KEY` = `re_cgqh5g7t_...`
- **Custom domain:** `griffinimmigration.com` (DNS via Cloudflare nameservers: hope.ns.cloudflare.com, remy.ns.cloudflare.com)

### GitHub
- **Repo:** `https://github.com/futec805/griffin-immigration`
- **Branch:** `master`
- **Deploy:**
  ```bash
  npm run build
  npx wrangler pages deploy .svelte-kit/cloudflare --project-name=griffin-immigration --commit-dirty=true
  ```

### Local Dev
```bash
npm run dev          # → http://localhost:5173
npm run build        # Production build check
```

---

## Design History (Decisions Made)

1. **Navy + Gold** (original) → rejected as too dark
2. **Playfair Display serif + navy/brass "Griffin's Compass"** → rejected (fonts/style mismatch)
3. **Forest Green + brass** → rejected (too dark)
4. **Deep Teal `#0d3b38`** → rejected (near-black)
5. **Medium teal `#38b2a4`** → rejected (gold text invisible on light bg)
6. **Light mint `#5ec9bc` + dark amber `#9a7514`** → rejected (didn't feel right)
7. **Blue `#2563eb` + Orange `#e67e22` professional** → CURRENT (clean, trustworthy, WCAG-compliant)

### Other major decisions
- **Career Guidance page deleted** per client request
- **TOEFL → PTE** renamed across entire codebase (9 files)
- **Country cards** went through 5+ iterations: emoji → gradients → dark photo overlays → light photo overlays → white gradient with flags
- **Free Assessment → Contact Us → "Call Us Now"** (with tel: link)
- **Header** went through dark → white → off-white → warm sand iterations, settled on white
- **Contact page** restructured 3+ times: info+map+form layout

---

## Known Quirks / Gotchas

1. **Svelte 5 runes mode** — uses `$state()`, `$props()`, `{@render children()}`, NOT Svelte 4 syntax
2. **`{@const}` must be inside `{#if}`/`{#each}` blocks** in Svelte 5
3. **Form actions** (not `+server.ts` API routes) — CSRF blocked API routes on Cloudflare
4. **`platform.env` in Cloudflare adapter** — KV binding works but secrets may need fallback hardcoded values
5. **Emoji flags don't render on Windows** — use `flagcdn.com` PNGs instead
6. **`brightness-0 invert` on JPEG logo** creates white box on dark bg — use text instead
7. **Cloudflare Pages Worker** shows `node:async_hooks` warning (non-blocking, requires `nodejs_compat` flag)
8. **`resend` npm SDK incompatible with Cloudflare Workers** — use raw `fetch()` to Resend REST API
9. **Footer Instagram SVG** was incomplete (only outer shape) — replaced with proper camera icon

---

## To Add / Improve

- [ ] SSL certificate finalization for custom domain (currently "verifying" in Cloudflare Pages)
- [ ] Blog / news section
- [ ] Online payment integration
- [ ] Multi-language support
- [ ] SEO meta tags optimization
- [ ] Sitemap.xml generation
