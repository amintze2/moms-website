## Why

Dawn Saks currently pays a monthly fee to a web developer for a WordPress site that rarely changes. Rebuilding it as a free static site hosted on GitHub Pages eliminates that recurring cost while giving her full ownership of the content.

## What Changes

- Build a new 5-page static HTML/CSS website replicating the content and design of dawnsaks.com
- Lightly refresh the visual design while keeping the existing green brand palette
- Replace the WordPress contact form with a Formspree-powered form (free, no backend)
- Deploy to GitHub Pages at amintze2/moms-website (free hosting)
- Replace the paid web developer dependency with a self-maintained static site

## Capabilities

### New Capabilities
- `site-layout`: Shared navigation, header, footer, and responsive grid used across all pages
- `home-page`: Landing page with hero section, practice intro, and embedded Google Map
- `biography-page`: Dawn's professional background and credentials
- `practice-information-page`: Areas of practice listed with brief descriptions
- `services-page`: Initial consultation and continuing counseling service descriptions
- `contact-page`: Contact form (Formspree), address, phone, email, and embedded Google Map
- `github-pages-deployment`: GitHub Pages configuration for deploying from main branch root

### Modified Capabilities
- None (greenfield project)

## Impact

- **Dependencies**: No runtime dependencies. Formspree free tier for contact form email delivery.
- **Hosting**: GitHub Pages (free), served from `amintze2/moms-website` main branch root
- **Domain**: Currently controlled by existing web developer — can be pointed to GitHub Pages later
- **Content**: Biography text will be provided by user before launch; all other content sourced from existing site
