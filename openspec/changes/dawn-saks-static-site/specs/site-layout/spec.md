## ADDED Requirements

### Requirement: Shared navigation bar
The site SHALL include a top navigation bar present on every page with links to: Home, Biography, Practice Information, Services, Contact.

#### Scenario: Navigation renders on all pages
- **WHEN** any page is loaded
- **THEN** the navigation bar SHALL be visible at the top with all 5 links

#### Scenario: Active page is highlighted
- **WHEN** a user is on a specific page
- **THEN** the corresponding nav link SHALL be visually distinguished (e.g., different color or underline)

#### Scenario: Mobile navigation
- **WHEN** the viewport is 768px wide or narrower
- **THEN** the navigation SHALL collapse into a hamburger menu or vertical stack that is fully tappable

### Requirement: Shared footer
The site SHALL include a footer present on every page with copyright text and contact summary.

#### Scenario: Footer renders on all pages
- **WHEN** any page is loaded
- **THEN** the footer SHALL appear at the bottom with dark green background (#006738), white text, and copyright notice

### Requirement: Responsive layout
All pages SHALL be fully responsive and usable on mobile devices without horizontal scrolling.

#### Scenario: Mobile viewport
- **WHEN** the page is viewed at 375px width
- **THEN** all content SHALL be readable, no horizontal scroll SHALL occur, and all tap targets SHALL be at least 44px tall

#### Scenario: Desktop viewport
- **WHEN** the page is viewed at 1200px or wider
- **THEN** content SHALL be centered with a max-width container (no wider than 1100px)

### Requirement: Typography and color system
The site SHALL use a consistent type scale and color palette across all pages.

#### Scenario: Color palette applied
- **WHEN** any page is rendered
- **THEN** accent color SHALL be #7aa957, dark color SHALL be #006738, body text SHALL be #4a4a4a, background SHALL be white

#### Scenario: Base font size
- **WHEN** any page is rendered
- **THEN** body font size SHALL be at least 16px for readability on mobile
