# GoPhish Setup and Configuration

## 1. Overview

**GoPhish** is an open-source phishing simulation platform used for security awareness training and authorized phishing assessments.

For this project, GoPhish will be used to create and manage a controlled phishing-awareness campaign, track non-sensitive user interactions, and generate campaign results.

The platform should only be used with proper authorization and within the approved testing scope.

## 2. GoPhish Architecture

A basic GoPhish deployment consists of two important interfaces:

### Admin Server

The Admin Server is used by authorized administrators to:

* Create campaigns
* Configure email templates
* Manage target groups
* Configure landing pages
* Review campaign results
* Manage campaign settings

Access to the Admin interface should be restricted to authorized administrators.

### Phishing Server

The Phishing Server handles the simulated campaign traffic, such as sending approved simulation emails and serving the awareness landing page.

The phishing infrastructure should be isolated and protected from unauthorized access.

## 3. Basic Workflow

The typical GoPhish workflow is:

```text
Target Group
     ↓
Email Template
     ↓
Landing Page
     ↓
Sending Profile
     ↓
Campaign
     ↓
User Interaction
     ↓
Campaign Results
     ↓
Security Awareness Report
```

## 4. Target Groups

A target group contains the approved recipients for a campaign.

For example:

```text
Group: IT-Training
-------------------
user001@example.com
user002@example.com
user003@example.com
```

Only authorized users should be included.

For repository testing, use dummy addresses rather than real employee email addresses.

## 5. Email Templates

Email templates represent the simulated phishing message used for the awareness exercise.

A safe training template should contain realistic phishing indicators without attempting to collect actual credentials.

For example, the simulation could represent a generic account notification and direct the user to an educational page explaining the phishing indicators.

The template should be reviewed and approved before the campaign is launched.

## 6. Landing Pages

A landing page can be used to provide immediate awareness training after a user interacts with the simulation.

Instead of collecting real passwords, the page should explain why the simulated message was suspicious.

Training content can include:

* Suspicious sender information
* Unusual URLs
* Urgency or threatening language
* Unexpected requests
* Safe reporting procedures

## 7. Sending Profile

The sending profile defines how the simulation email is sent.

The organization should use an approved email account or mail infrastructure specifically authorized for the simulation.

Email authentication and organizational policies should be considered to ensure the campaign does not unintentionally affect normal email operations.

## 8. Campaign Configuration

A campaign combines the required components:

```text
Campaign
├── Target Group
├── Email Template
├── Landing Page
└── Sending Profile
```

Before launching, verify:

* The target list is correct.
* The campaign has been approved.
* The email content is safe.
* No real credentials will be collected.
* The landing page provides awareness training.
* Campaign tracking is limited to approved metrics.

## 9. Monitoring Campaign Results

After launching the authorized simulation, GoPhish can provide campaign interaction information.

Important awareness metrics include:

* Emails sent
* Emails delivered
* Emails opened
* Links interacted with
* Training page visits
* Phishing reports

These metrics can be aggregated for the final security awareness report.

## 10. Security Considerations

The GoPhish administration interface should be protected carefully.

Recommended practices include:

* Use strong administrative credentials.
* Restrict administrative access.
* Use HTTPS/TLS where applicable.
* Keep GoPhish and the underlying operating system updated.
* Do not expose the administration interface unnecessarily.
* Do not store real passwords collected from employees.
* Use dummy data in development and documentation.
* Remove temporary campaign infrastructure after testing.
* Follow the organization's data-retention policy.

## 11. Data Handling

Employee information is sensitive organizational data.

Therefore:

* Use only approved recipient information.
* Do not commit real employee email lists to Git.
* Do not commit campaign credentials or secrets.
* Do not store real authentication passwords.
* Restrict access to campaign reports.
* Use anonymized or aggregated data for reporting whenever possible.

Example `.gitignore` entries:

```text
# Sensitive campaign data
*.csv
*.env
secrets/
credentials/
employee-data/
campaign-data/
```

## 12. Testing and Validation

Before conducting the real awareness exercise, the configuration should be tested using an internal test account.

The test should verify:

* Email delivery
* Template rendering
* Landing-page functionality
* Tracking behavior
* Reporting
* Administrative access controls

Only after successful validation and approval should the authorized campaign proceed.

## Conclusion

GoPhish provides a structured way to conduct controlled phishing-awareness exercises. For this project, it will be used to manage approved recipients, simulation content, awareness landing pages, campaign delivery, and non-sensitive interaction metrics.

The primary goal is employee education and security improvement, not credential collection or unauthorized access.
