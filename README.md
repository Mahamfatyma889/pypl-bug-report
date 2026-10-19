# Pypl Bug Report

A centralized QA repository for documenting, tracking, and managing bugs identified in the **Pypl HR Management System**. This repository helps the QA and development teams reproduce issues, investigate defects, verify fixes, and improve the overall quality and reliability of the application.

## 🔗 Application Portals

| Portal | Description | URL |
|---|---|---|
| **Employee Portal** | Employee access to attendance, leave management, payroll, performance, and other employee services. | [Open Employee Portal](https://pypl.tawha.com/sign-in?redirect=%2Femployee%2Fleave) |
| **Admin Portal** | Administrative access to employee management, organization settings, attendance, leave, payroll, performance, reports, and other HR operations. | [Open Admin Portal](https://pypl.tawha.com/admin/dashboard) |
| **Super Admin Portal** | Platform-level administration for managing tenants, platform settings, subscriptions, support, and system-wide operations. | [Open Super Admin Portal](https://pypl.tawha.com/super-admin) |

> **Note:** Access to the portals and individual features depends on the user's assigned role and permissions. Sign-in may be required.

## 🎯 Repository Objectives

- Maintain a centralized record of identified bugs and defects.
- Provide clear, reproducible steps for each issue.
- Document expected versus actual behavior.
- Track severity, priority, and resolution status.
- Identify UI/UX inconsistencies, functional defects, validation issues, and integration failures.
- Verify fixes through retesting and regression testing.
- Improve communication and collaboration between QA and development teams.
- Track API failures, database-related issues, and data synchronization problems where applicable.

## 🧪 Testing Scope

Testing covers the following areas across the Employee, Admin, and Super Admin portals.

### Employee Portal
- Employee profile and personal information
- Attendance and clock-in/clock-out
- Leave applications and leave balances
- Payroll, payslips, and year-to-date summaries
- Tax documents
- Goals, performance reviews, feedback, and check-ins
- Notifications and employee tasks
- Data synchronization with the Admin Portal

### Admin Portal
- Employee and organization management
- Departments, designations, teams, and organizational structure
- Attendance management
- Leave policies, balances, holidays, and carry-forward rules
- Payroll processing, payslips, and tax documents
- Performance management, goals, reviews, and improvement plans
- Reports and scheduled report delivery
- Notification channels and email configuration
- Localization and language-specific content
- Form validation, permissions, and data integrity

### Super Admin Portal
- Tenant and organization management
- Subscription plans, seat limits, and recurring revenue calculations
- Tenant configuration and regional settings
- Platform support and tenant issue management
- System-level settings and integrations
- Data validation, access control, and platform-wide functionality

### API and Database Testing
- API response codes and error handling
- Failed requests and endpoint availability
- Request and response validation
- Data consistency between API responses and database records
- Database transaction failures and data synchronization
- Performance issues under load, where applicable
- Correlation of API failures with database errors and timestamps

## 🐞 Bug Report Template

Every bug report should provide enough information for another team member to reproduce and investigate the issue.

| Field | Description |
|---|---|
| **Bug Title** | Short, specific summary of the defect |
| **Module / Portal** | Affected module and portal |
| **Environment** | Testing environment, application URL, and browser |
| **Preconditions** | Required user role, permissions, or setup |
| **Steps to Reproduce** | Numbered steps to reproduce the issue |
| **Actual Result** | Behavior observed during testing |
| **Expected Result** | Correct behavior expected |
| **Severity** | Impact of the defect |
| **Priority** | Urgency of fixing the defect |
| **Attachments** | Screenshots, videos, logs, or API responses |
| **API / Database Evidence** | Endpoint, status code, timestamp, and relevant database evidence, if applicable |
| **Status** | Current state of the defect |

### Example Bug Report

**Title:** Employee Leave Balance Not Displayed

**Portal:** Employee Portal

**Module:** Leave Management

**Steps to Reproduce:**
1. Sign in to the Employee Portal.
2. Navigate to Leave Management.
3. Open the leave balance or overview section.
4. Check the displayed leave entitlements.

**Actual Result:** The system displays a message indicating that no leave balances are configured for the employee.

**Expected Result:** The employee should see the applicable leave balances configured by the Admin, according to the employee's eligibility and assigned leave policies.

**Evidence:** Attach a screenshot and include relevant API or database evidence when available.

## 🚦 Severity and Priority

### Severity
- **Critical:** System-wide outage, major security issue, or critical business functionality unavailable.
- **High:** Major functionality is broken or important business operations are blocked.
- **Medium:** A feature behaves incorrectly, but a workaround may exist.
- **Low:** Minor UI, content, or usability issue with limited impact.

### Priority
- **P1 — Urgent:** Requires immediate investigation and resolution.
- **P2 — High:** Should be addressed as soon as possible.
- **P3 — Medium:** Should be resolved in the normal development cycle.
- **P4 — Low:** Can be scheduled for a later release.

Severity describes the impact of a defect; priority describes how urgently it should be fixed.

## 🔄 Bug Lifecycle

A typical defect workflow follows these stages:

1. **Open:** The issue has been identified and documented.
2. **In Progress:** The development team is investigating or fixing the issue.
3. **Fixed:** A fix has been implemented.
4. **Ready for Retest:** QA can verify the fix in the relevant environment.
5. **Reopened:** The issue persists or reappears after the fix.
6. **Closed:** QA has verified that the issue is resolved.

The exact workflow may vary depending on the team's development process.

## ✅ QA Validation Process

1. Identify the defect during functional, UI, integration, API, database, or regression testing.
2. Reproduce the issue and capture supporting evidence.
3. Document the steps, actual result, expected result, and impact.
4. Assign an appropriate severity and priority.
5. Share the report with the development team.
6. Retest the issue after a fix becomes available.
7. Perform regression testing on related functionality.
8. Close the issue when the expected behavior is verified; otherwise, reopen it with updated evidence.

## 📊 API and Performance Defect Evidence

For API, database, and performance-related defects, include additional evidence whenever applicable:

- Test date, start time, end time, and duration
- Endpoint and HTTP method
- Request parameters and sanitized payload
- HTTP status code and response body
- Timestamp of the failure
- Number of virtual users and ramp-up period for load tests
- Request count, throughput, and error rate
- Relevant database queries, transaction details, and sanitized logs
- Correlation between API requests and database errors

**Security note:** Never commit passwords, app passwords, access tokens, API keys, session cookies, or sensitive employee information to this repository. Redact confidential values from screenshots, logs, and request payloads.

## 🛠️ Tools and Testing Methods

Testing may involve the following tools, depending on the scope of the issue:

- **Browser DevTools:** UI inspection, console errors, and network requests
- **Postman:** API validation and integration testing
- **Playwright:** Automated browser and functional testing
- **Apache JMeter:** Load and performance testing
- **DBeaver:** Database inspection and validation
- **GitHub:** Defect documentation, collaboration, and issue tracking

## 📌 Repository Guidelines

- Use descriptive and consistent bug titles.
- Report one primary defect per issue whenever possible.
- Include reproducible steps and relevant evidence.
- Avoid duplicate reports; link related issues when necessary.
- Clearly distinguish observed facts from suspected root causes.
- Never include credentials or confidential production data.
- Update the report when new findings or retest results become available.

## 🎯 Goal

The goal of this repository is to improve Pypl's **functionality, usability, reliability, data accuracy, performance, and consistency** across all three portals through structured QA testing, clear defect documentation, and verified fixes.

---

**Project:** Pypl HR Management System  
**Repository:** [pypl-bug-report](https://github.com/Mahamfatyma889/pypl-bug-report)  
**Maintained by:** Maham-Tester
