# Phishing Simulation Methodology

## 1. Introduction

The phishing awareness simulation will be conducted as a controlled security training exercise. The purpose is to evaluate employee awareness of phishing techniques and provide targeted security education.

All activities must be performed only within the scope approved by Internee.pk management.

## 2. Define the Scope

Before starting the simulation, the testing scope should be clearly defined.

The scope should include:

* Target department or employee group
* Approved email addresses
* Simulation duration
* Approved phishing scenario
* Testing infrastructure
* Metrics that will be collected
* Responsible team members
* Data-retention requirements

No users or systems outside the approved scope should be included.

## 3. Obtain Authorization

Written authorization should be obtained before conducting the simulation.

The authorization should define:

* Purpose of the exercise
* Target users
* Testing dates
* Approved infrastructure
* Data that may be collected
* Responsible personnel
* Emergency contact information

This ensures that the activity remains an authorized security-awareness exercise.

## 4. Prepare Test Data

The approved internal email list may be used only within the authorized environment.

For repository documentation and development/testing, dummy data should be used.

Example:

```csv
employee_id,email,department
EMP001,user001@example.com,HR
EMP002,user002@example.com,IT
EMP003,user003@example.com,Finance
```

Real employee information should not be committed to a public Git repository.

## 5. Prepare the Simulation Environment

GoPhish can be used to manage the authorized phishing-awareness campaign.

The environment should be isolated and properly secured. Administrative access should be restricted to authorized personnel.

The simulation should use a harmless training scenario and should not deploy malware or collect real passwords.

## 6. Create the Awareness Scenario

The simulated email should represent a realistic but controlled phishing scenario.

Possible awareness themes include:

* Suspicious account notification
* Fake password-expiration notice
* Unusual login notification
* General security-awareness message

The purpose of the email is to test whether employees recognize phishing indicators.

The simulation should avoid requesting or storing actual authentication credentials.

## 7. Conduct the Simulation

The campaign should be launched only during the approved testing period.

During the campaign, the team should monitor high-level interaction metrics such as:

* Emails delivered
* Emails opened
* Links interacted with
* Training page visits
* Phishing reports

The campaign should remain within the approved scope.

## 8. Analyze Results

After the campaign, the collected metrics should be analyzed to identify general awareness trends.

For example:

```text
Total Recipients:       100
Emails Delivered:       96
Emails Opened:          75
Link Interactions:      18
Reported as Phishing:   42
```

These numbers are illustrative only. Actual results should be taken from the authorized campaign.

The goal is to identify areas where additional security awareness training may be useful.

## 9. Provide Awareness Training

After the simulation, employees should receive educational material explaining:

* How to identify suspicious emails
* How to verify a sender
* How to inspect links safely
* Why unexpected attachments can be dangerous
* How to report suspected phishing
* Why passwords and authentication codes should never be shared

The purpose of the exercise should be clearly communicated as employee education.

## 10. Generate the Security Awareness Report

The final report should contain:

* Executive summary
* Scope and authorization
* Methodology
* Campaign metrics
* Key observations
* Awareness gaps
* Recommendations
* Future training plan

Individual employee information should be minimized in the report and handled according to organizational privacy requirements.

## 11. Cleanup

After the simulation:

* Disable unnecessary campaign infrastructure.
* Remove temporary test data.
* Securely handle campaign logs.
* Review access permissions.
* Document lessons learned.
* Preserve only information required by the organization's retention policy.

## 12. Continuous Improvement

Phishing awareness should be treated as an ongoing security program rather than a one-time exercise.

Future simulations can be used to measure whether awareness improves over time.

The organization can compare aggregated results from different training periods and use those results to improve security-awareness training.

## Overall Workflow

```text
Authorization
      ↓
Define Scope
      ↓
Prepare Test Data
      ↓
Configure Simulation Environment
      ↓
Create Awareness Scenario
      ↓
Conduct Authorized Simulation
      ↓
Collect Non-Sensitive Metrics
      ↓
Analyze Results
      ↓
Employee Awareness Training
      ↓
Security Awareness Report
      ↓
Continuous Improvement
```

## Conclusion

The methodology focuses on conducting a controlled, authorized, and educational phishing simulation. The main objective is not to compromise users or systems, but to identify awareness gaps and help employees recognize and report phishing attempts more effectively.
