## ADDED Requirements

### Requirement: Biography hero
The biography page SHALL display a hero section with the heading "Biography" or "About Dawn Saks".

#### Scenario: Hero renders
- **WHEN** the biography page is loaded
- **THEN** a full-width hero section SHALL be visible with a relevant heading

### Requirement: Biography content
The biography page SHALL display Dawn Saks' professional background and credentials.

#### Scenario: Placeholder shown before content is provided
- **WHEN** the biography page is loaded and bio text has not yet been provided
- **THEN** a clearly marked placeholder section SHALL appear indicating where the biography text will go

#### Scenario: Bio text displayed
- **WHEN** the biography text has been provided and inserted
- **THEN** it SHALL render as readable paragraphs with appropriate spacing
