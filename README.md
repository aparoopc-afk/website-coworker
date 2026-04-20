# coworker1.com

Landing page for **Coworker Labs** — AI transformation and operational-loop architecture practice for mid-market organizations.

Features **Flip Picker** as the firm's live demo (in-house algorithmic trading platform used to pressure-test orchestration patterns before selling them to clients).

Primary domain: `coworker1.com` (legacy name, retained).

## Architecture

- **Single file**: `index.html` (no build tools, no frameworks, no runtime dependencies)
- **Size**: ~8 KB
- **Load time**: <100ms on any connection
- **Mobile-first**: responsive, works on any device
- **No JavaScript**: pure HTML/CSS for maximum reliability

## Deployment (Vercel + GoDaddy)

### Step 1 — Push to GitHub (5 min)

```bash
cd coworker1_website
git init
git add .
git commit -m "Initial stealth landing"
gh repo create aparoopc/coworker1-website --public --source=. --push
```

If `gh` (GitHub CLI) isn't installed: use https://github.com → New Repo → upload files.

### Step 2 — Deploy to Vercel (5 min)

1. Go to https://vercel.com
2. Sign in with GitHub
3. Click "New Project"
4. Import `aparoopc/coworker1-website`
5. Framework Preset: **Other** (it's static HTML)
6. Click "Deploy"
7. Live at `https://coworker1-website.vercel.app` in ~30 seconds

### Step 3 — Connect GoDaddy domain (10 min)

**In Vercel**:
1. Project Settings → Domains → Add `coworker1.com`
2. Vercel displays DNS records needed

**In GoDaddy**:
1. My Products → coworker1.com → DNS
2. Delete existing A records for `@`
3. Add:
   - **Type**: A, **Name**: @, **Value**: `76.76.21.21`
   - **Type**: CNAME, **Name**: www, **Value**: `cname.vercel-dns.com.`
4. Save. Wait 5-30 min for DNS propagation.

**Verify**:
```bash
dig coworker1.com +short
# Should return: 76.76.21.21

curl -I https://coworker1.com
# Should return: 200 OK
```

Vercel auto-provisions SSL via Let's Encrypt. Site is live at `https://coworker1.com`.

## Maintenance

Updates are trivial:
```bash
# Edit index.html
git add index.html
git commit -m "Update landing copy"
git push
# Vercel auto-deploys in ~30 seconds
```

## Design principles

- **Dark theme** — Stripe/Linear/Vercel convention for serious tech
- **Okabe-Ito blue** `#0072B2` — consistent with trading dashboard palette
- **Minimal copy** — every word earns its place
- **No marketing fluff** — no signup forms, testimonials, or social proof (stealth)
- **Single CTA** — partnership email only
- **Monospace accents** — technical credibility via type choice

## Future iterations (managed by Website Agent)

Roadmap when ready to expand:
- Blog/Substack integration for research publication (Phase 2)
- Waitlist signup with email capture (pre-launch)
- Product demo video (when public-ready)
- FAQ section for partnership inquiries
- Press kit for media outreach
