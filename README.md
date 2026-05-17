# coworker1.com

Personal website for **Aparoop Chakraborty** — fractional AI transformation partner, builder of **Tickerly**, writer of **The Loop**.

Primary domain: `coworker1.com` (legacy from earlier "Coworker Labs" branding, retained).

## Site structure

| File | Purpose |
|---|---|
| `index.html` | Landing — hero, services, Tickerly highlight, newsletter CTA, ICP, engage form |
| `tickerly.html` | Tickerly product page — architecture, current state, roadmap |
| `about.html` | Personal bio — credentials, working style, links |
| `aparoop.jpg` | Profile photo |

## Identity

- **Partner**: Fractional AI transformation engagements (CAIO, orchestration architecture, operational loop design)
- **Builder**: Tickerly — institutional-grade options trading framework, productizing for retail/prosumer
- **Writer**: The Loop by Aparoop — weekly newsletter on LinkedIn

## Things to update before going live

1. **Contact form** (`index.html`, §06 Engage): replace `https://formspree.io/f/YOUR_FORM_ID` with the actual Formspree form action URL after creating the form at [formspree.io](https://formspree.io)
2. **LinkedIn newsletter link** (`index.html`, §04 Loop): the `Subscribe on LinkedIn` button currently points to `linkedin.com/in/aparoop` — update to the actual LinkedIn newsletter URL once published
3. **Profile photo**: `aparoop.jpg` is the current shot; replace if a better one is available

## Architecture

- **3 static HTML files**, no build tools, no frameworks, no runtime dependencies
- **Mobile-first**: responsive, works on any device
- **No JavaScript** beyond a tiny image-fallback on the profile photo

## Deploy

GitHub Pages from `main` branch, served at `https://www.coworker1.com`. Push to `main` triggers automatic deployment (~30 sec).

## Design system

- **Type**: Fraunces (serif) + JetBrains Mono (mono)
- **Colors**: Paper `#F6F2EC` / Ink `#1A1A1A` / Accent blue `#2F4A6B`
- **Layout**: Single column, 760px max-width, mobile-responsive
- **Feel**: Editorial / FT-style, no marketing fluff

## Maintenance

```bash
# Edit any file
git add index.html tickerly.html about.html
git commit -m "Update content"
git push
# Vercel/Pages auto-deploys in ~30 seconds
```

## Future roadmap (when ready)

- Tickerly product page expansion with screenshots / waitlist signup
- Newsletter archive section on `/loop` or `/writing`
- Case study / engagement results section once 2-3 fractional projects close
