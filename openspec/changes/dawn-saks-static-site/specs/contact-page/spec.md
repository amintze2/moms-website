## ADDED Requirements

### Requirement: Contact page hero
The contact page SHALL display a hero section with the heading "Contact Us".

#### Scenario: Hero renders
- **WHEN** the contact page is loaded
- **THEN** a full-width hero section SHALL appear with the heading "Contact Us"

### Requirement: Contact form
The contact page SHALL include a form that submits to Formspree and sends an email to dawn@dawnsaks.com.

#### Scenario: Form fields present
- **WHEN** the contact page is loaded
- **THEN** the form SHALL contain fields for: Name (required), Email (required), Message (required textarea), and a Submit button

#### Scenario: Form submission
- **WHEN** a user fills out all required fields and submits the form
- **THEN** the form SHALL POST to the Formspree endpoint and the user SHALL be shown a confirmation message

#### Scenario: Form validation
- **WHEN** a user submits the form with a required field empty
- **THEN** the browser SHALL prevent submission and indicate the missing field

### Requirement: Contact information display
The contact page SHALL display the full practice contact details.

#### Scenario: Contact details visible
- **WHEN** the contact page is loaded
- **THEN** the following SHALL be visible: address (11 Grand Central East, Formerly 733 Third Avenue, 16th Floor, New York, NY 10017), phone ((646) 790-5700), fax ((646) 478-9186), email (dawn@dawnsaks.com)

### Requirement: Google Map embed on contact page
The contact page SHALL include an embedded Google Map showing the practice location.

#### Scenario: Map renders
- **WHEN** the contact page is loaded
- **THEN** an iframe Google Map SHALL render centered on coordinates 40.752850, -73.972180
