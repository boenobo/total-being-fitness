# Total Being Fitness — Static Site

Static rebuild of [totalbeing.fitness](https://totalbeing.fitness) for Cloudflare Pages.

## File structure

```
total-being-fitness/
├── index.html              ← Homepage (main entry point)
├── thank-you.html          ← Contact form success page
├── _redirects              ← Cloudflare Pages redirect rules
├── _headers                ← Security & cache headers
├── assets/
│   ├── logo.png            ← Brand logo (PNG, transparent bg)
│   ├── favicon.png         ← Favicon (PNG)
│   ├── hero-bg.jpg         ← Hero section background
│   ├── about-bg.jpg        ← About Me section image
│   ├── packages-bg.jpg     ← Packages section background
│   └── connect-bg.jpg      ← Connect section background
├── css/
│   └── styles.css
└── js/
    └── site.js
```

## Cloudflare Pages deployment

### Option A — GitHub → Cloudflare Pages (recommended)

1. Create a new GitHub repo (e.g. `total-being-fitness`)
2. Upload the **contents** of this folder to the repo root
   - `index.html` must be at repo root, not inside a subfolder
3. In [Cloudflare Dashboard](https://dash.cloudflare.com) → Workers & Pages
4. Create application → Pages → Connect to Git → select repo
5. Use these build settings:
   - **Framework preset:** None
   - **Build command:** _(leave blank)_
   - **Build output directory:** `/`
   - **Root directory:** _(leave blank)_
6. Click Save and Deploy

### Option B — Direct Upload (Cloudflare Pages)

1. In [Cloudflare Dashboard](https://dash.cloudflare.com) → Workers & Pages
2. Create application → Pages → Upload Assets
3. Drag the **entire extracted folder** into the upload area
4. Deploy

## Stripe Payment Links

| Tier | Link |
|------|------|
| Tier 1 — Aligned Strength ($69/mo) | https://buy.stripe.com/6oU8wO1XOdl282NbNL4Ni02 |
| Tier 2 — The Strong-HER Experience ($175/mo) | https://buy.stripe.com/7sY9ASdGw6WEdn7cRP4Ni03 |
| Tier 3 — Total Being Method Mentorship ($420/mo) | https://buy.stripe.com/3cI7sKdGw1CkbeZ0534Ni04 |

## Form handling

Contact form uses [Static Forms](https://www.staticforms.xyz/) (`sf_c7f08e6ef12e8ab737661a34`).
Submissions redirect to `/thank-you.html`.

## Pre-launch checklist

- [ ] Verify Static Forms delivers to intended recipient email
- [ ] Test all three Stripe Payment Links on mobile + desktop
- [ ] Confirm custom domain is pointed to Cloudflare Pages project
- [ ] Review copy fidelity with Jaime before going live
