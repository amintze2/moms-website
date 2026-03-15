## ADDED Requirements

### Requirement: GitHub Pages configuration
The repository SHALL be configured to serve the static site from the root of the `main` branch via GitHub Pages.

#### Scenario: Site accessible via GitHub Pages URL
- **WHEN** GitHub Pages is enabled on the repository
- **THEN** the site SHALL be accessible at https://amintze2.github.io/moms-website/

### Requirement: Root-level HTML files
All HTML pages SHALL live at the repository root so GitHub Pages serves them at clean URLs.

#### Scenario: Home page at root
- **WHEN** a user visits the GitHub Pages URL
- **THEN** `index.html` SHALL be served as the home page

#### Scenario: Inner pages accessible
- **WHEN** a user navigates to `/biography.html`, `/practice-information.html`, `/services.html`, or `/contact.html`
- **THEN** the respective page SHALL load correctly

### Requirement: Custom domain readiness
The repository SHALL include a placeholder `CNAME` file (empty or commented) so the domain can be pointed to GitHub Pages later without a code change.

#### Scenario: CNAME file present
- **WHEN** the repository is inspected
- **THEN** a `CNAME` file SHALL exist at the root, ready to be populated with `dawnsaks.com` when the domain transfers
