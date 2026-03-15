## Context

The existing dawnsaks.com is a WordPress site managed by a third-party developer (White Wave Graphics). It's a 5-page informational site for a solo nutritionist practice that changes infrequently. All content is static — no user accounts, no CMS, no dynamic data. The site uses a green brand palette (#7aa957, #006738) and has a professional medical practice aesthetic.

The goal is to replicate the site as a zero-dependency static site, lightly modernize the design, and deploy it for free on GitHub Pages.

## Goals / Non-Goals

**Goals:**
- Match the content and structure of the existing site exactly
- Lightly refresh the design: cleaner typography, more whitespace, same green palette
- Mobile responsive — works well on phones without zooming
- Contact form that delivers emails via Formspree (no backend)
- Google Map embed on Home and Contact pages
- Deploy from `main` branch root on GitHub Pages (amintze2/moms-website)
- Zero ongoing cost

**Non-Goals:**
- CMS or admin interface
- Blog or dynamic content
- Animations or heavy interactivity
- Replicating the hero image slider (static hero with gradient overlay instead — simpler, faster)
- Setting up the custom domain (done later when domain transfers)

## Decisions

### Decision: Pure static HTML/CSS, no build step
**Chosen**: Hand-authored HTML files + a single shared CSS file
**Alternatives considered**: Jekyll, Eleventy, Next.js static export
**Rationale**: The site is 5 pages. A build tool adds complexity and a dependency to maintain. The person maintaining this after handoff may not be a developer — plain HTML files are the most durable and editable format. GitHub Pages serves them directly with no config.

### Decision: Shared navigation via JS include vs. copy-paste
**Chosen**: Copy-paste nav/footer HTML into each page (no JS includes)
**Alternatives considered**: Fetch-based HTML includes, web components, server-side includes
**Rationale**: 5 pages is small enough that duplication is acceptable. JS-based includes flicker on load and break when opened as local files. Keeping it simple wins.

### Decision: Formspree for contact form
**Chosen**: Formspree free tier (HTML form POST, no JS required)
**Alternatives considered**: Netlify Forms (requires Netlify hosting), EmailJS (requires JS config), self-hosted backend
**Rationale**: Formspree works with a plain HTML `<form>` POST — no JavaScript, no backend, no API keys in the repo. Free tier covers 50 submissions/month which is sufficient. Setup is just adding `action="https://formspree.io/f/<id>"` to the form.

### Decision: Hero section as CSS gradient overlay, not image slider
**Chosen**: Full-width section with a green gradient + brief headline
**Alternatives considered**: Replicating the original slider (requires JS), using a static hero photo
**Rationale**: A CSS gradient hero is fast, looks clean, requires no images to source, and is trivially maintainable. A slider would require a JS library and sourcing licensed images.

### Decision: Single shared CSS file
**Chosen**: One `styles.css` file for all pages
**Rationale**: Simple, cacheable, easy to find and edit.

### Decision: Deploy from `main` branch root
**Chosen**: Files live at repo root, GitHub Pages serves from `main`
**Alternatives considered**: `/docs` subfolder, `gh-pages` branch
**Rationale**: Root of main is the simplest setup — no branch gymnastics, no subfolder config. GitHub Pages supports it natively.

## Risks / Trade-offs

- **Nav/footer duplication** → Any nav change requires editing 5 files. Acceptable for a 5-page site that rarely changes.
- **Formspree free tier limit** → 50 submissions/month. If practice grows, upgrade is $8/month. Risk is very low for a solo practice.
- **No biography content yet** → Bio page will ship with a placeholder. User will paste real content before launch.
- **Domain not yet transferred** → Site will be accessible at `amintze2.github.io/moms-website` until domain transfers. Can add a `CNAME` file at transfer time.
- **Google Maps embed** → Uses a free iframe embed. No API key required at this traffic level.

## Open Questions

- What photo (if any) should appear on the Biography page? For now, assume text-only.
- Formspree account: the form owner (user) will need to sign up at formspree.io and get their form ID before the contact form is live.
