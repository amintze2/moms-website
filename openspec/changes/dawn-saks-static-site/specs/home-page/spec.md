## ADDED Requirements

### Requirement: Hero section
The home page SHALL display a full-width hero section with a green gradient background and a welcome headline.

#### Scenario: Hero renders above the fold
- **WHEN** the home page is loaded
- **THEN** a full-width hero section SHALL be visible with the text "Welcome to a Healthier Lifestyle" and a brief subheading

### Requirement: Practice introduction
The home page SHALL include a short paragraph introducing Dawn Saks and her practice.

#### Scenario: Intro text displayed
- **WHEN** the home page is loaded
- **THEN** the following text (or equivalent) SHALL appear: "Proper nutrition is vital to good health. Dawn Saks is an experienced nutritionist in private practice providing individual nutrition counseling and personalized nutrition programs."

### Requirement: Google Map embed
The home page SHALL include an embedded Google Map showing the practice location.

#### Scenario: Map is visible
- **WHEN** the home page is loaded
- **THEN** an iframe Google Map SHALL render centered on coordinates 40.752850, -73.972180 at zoom level 16

### Requirement: Contact summary
The home page SHALL display the practice address, phone, and email.

#### Scenario: Contact info visible on home page
- **WHEN** the home page is loaded
- **THEN** the address (11 Grand Central East, 16th Floor, NY 10017), phone ((646) 790-5700), and email (dawn@dawnsaks.com) SHALL be visible
