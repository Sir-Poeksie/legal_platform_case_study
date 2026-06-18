# Test Cases & Scenarios

**Version:** 1.0<br>
**Project:** Legal Services Digital Platform<br>
**Last Updated:** 2026-06-11<br>
**Author:** Mpumelelo Theophilas Nxazonke<br>
**Status:** Complete

## 1. Overview

This document defines the test scenarios and test cases executed to validate the functionality, usability, responsiveness, and deployment readiness of the Legal Services Digital Platform.

The test cases are aligned to project requirements and provide traceability to business and functional objectives. Test coverage is mapped to the Requirements Traceability Matrix (RTM) to ensure all approved business and functional requirements are validated through planned testing activities.

## 2. Functional Test Cases

### 2.1. Homepage

| TC ID | Test Scenario | Test Steps | Expected Result | Priority |
| ----- | ------------- | ---------- | --------------- | -------- |
| TC-001 | Homepage loads successfully | Navigate to homepage URL | Homepage displays correctly | High |
| TC-002 | Hero section displays correctly | Load homepage | Hero heading, CTA and branding visible | High |
| TC-003 | CTA button navigation | Click primary CTA | User navigates to intended destination | High |

### 2.2. Navigation

| TC ID | Test Scenario | Test Steps | Expected Result | Priority |
| ----- | ------------- | ---------- | --------------- | -------- |
| TC-004 | Main navigation links | Click each navigation item | Correct page loads | High |
| TC-005 | Mobile navigation menu | Open mobile menu | Menu expands correctly | High |
| TC-006 | Mobile navigation links | Select menu item | Correct page loads | High |

### 2.3. About Page

| TC ID | Test Scenario | Test Steps | Expected Result | Priority |
| ----- | ------------- | ---------- | --------------- | -------- |
| TC-007 | About page accessibility | Navigate to About page | Page loads successfully | Medium |
| TC-008 | Attorney profile visibility | Scroll to attorney section | Profile information visible | High |
| TC-009 | Attorney image rendering | Review attorney profiles | Images load correctly | Medium |

### 2.4. Services Page

| TC ID | Test Scenario | Test Steps | Expected Result | Priority |
| ----- | ------------- | ---------- | --------------- | -------- |
| TC-010 | Services page loads | Navigate to Services page | Services displayed correctly | High |
| TC-011 | Service cards visibility | Scroll through services section | All service cards visible | High |
| TC-012 | Layout consistency | Review page layout | Consistent spacing and alignment | Medium |

### 2.5. Contact Page

| TC ID | Test Scenario | Test Steps | Expected Result | Priority |
| ----- | ------------- | ---------- | --------------- | -------- |
| TC-013 | Contact page loads | Navigate to Contact page | Contact page displays correctly | High |
| TC-014 | Contact form visibility | Scroll to form section | Form displays correctly | High |
| TC-015 | Required field validation | Submit empty form | Validation messages displayed | High |
| TC-016 | Invalid email validation | Submit invalid email | Error displayed | High |
| TC-017 | Successful form submission | Submit valid form | Submission accepted | Critical |
| TC-018 | Thank-you redirect | Submit valid form | Redirect to thank-you page | Critical |

### 2.6. WhatsApp Integration

| TC ID | Test Scenario | Test Steps | Expected Result | Priority |
| ----- | ------------- | ---------- | --------------- | -------- |
| TC-019 | WhatsApp CTA | Click WhatsApp button | WhatsApp opens correctly | High |

### 2.7. Google Maps Integration

| TC ID | Test Scenario | Test Steps | Expected Result | Priority |
| ----- | ------------- | ---------- | --------------- | -------- |
| TC-020 | Map visibility | Navigate to contact section | Map displays correctly | Medium |
| TC-021 | Map interaction | Select map link | Maps application/location opens | Medium |

## 3. Responsive Testing Scenarios

### 3.1. Desktop

| TC ID | Test Scenario | Expected Result |
| ------ | ------------ | --------------- |
| TC-022 | Homepage desktop layout | Layout renders correctly |
| TC-023 | Services page desktop layout | No overlap or rendering issues |

### 3.2. Tablet

| TC ID | Test Scenario | Expected Result |
| ----- | ------------- | --------------- |
| TC-024 | Tablet rendering | Content adapts correctly |
| TC-025 | Tablet navigation | Navigation remains usable |

### 3.3. Mobile

| TC ID | Test Scenario | Expected Result |
| ----- | ------------- | --------------- |
| TC-026 | Mobile homepage rendering | Content scales correctly |
| TC-027 | Mobile navigation menu | Menu remains accessible |
| TC-028 | Mobile contact form | Form remains usable |
| TC-029 | Attorney section mobile layout | Content remains readable and maintains logical content grouping |

## 4. Cross-Browser Testing

| TC ID | Browser | Scenario | Expected Result |
| ----- | ------- | -------- | --------------- |
| TC-030 | Chrome | Homepage rendering | Pass |
| TC-031 | Chrome | Contact workflow | Pass |
| TC-032 | Edge | Homepage rendering | Pass |
| TC-033 | Edge | Contact workflow | Pass |
| TC-034 | Mobile Chrome | Responsive validation | Pass |

## 5. Accessibility Test Scenarios

| TC ID | Test Scenario | Expected Result |
| ----- | ------------- | --------------- |
| TC-035 | Heading hierarchy review | Semantic structure maintained |
| TC-036 | Lighthouse accessibility audit | Accessibility score acceptable |
| TC-037 | Content readability review | Content readable across devices |

## 6. SEO Validation Scenarios

| TC ID | Test Scenario | Expected Result |
| ----- | ------------ | --------------- |
| TC-038 | Metadata review | Metadata present |
| TC-039 | Robots configuration review | Configuration matches deployment state |
| TC-040 | Lighthouse SEO audit | SEO score reviewed and documented |

## 7. Deployment Readiness Scenarios

| TC ID | Test Scenario | Expected Result |
| ----- | ------------- | --------------- |
| TC-041 | Hosting environment review | Environment supports deployment |
| TC-042 | DNS review | DNS findings documented |
| TC-043 | SMTP review | SMTP configuration assessed |
| TC-044 | Deliverability review | Findings documented |
| TC-045 | Production readiness checklist | All required items reviewed |

## 8. Test Data

### 8.1. Valid Contact Form Data

| Field | Example Value |
| ----- | ------------- |
| Name | Lorem Ipsum |
| Email | lorem.ipsum@example.com |
| Phone | +27 82 123 4567 |
| Service | Family Law |
| Message | Requesting legal consultation |
| Date | 2026-06-20 |

### 8.2. Invalid Contact Form Data

| Scenario | Example |
| -------- | ------- |
| Empty Required Fields | Blank Submission |
| Invalid Email | lorem@ |
| Invalid Date | Invalid Format |

## 9. Defect Classification

| Severity | Description |
| -------- | ----------- |
| Critical | Prevents core business workflow |
| High | Major functionality impacted |
| Medium | Partial degradation of functionality |
| Low | Cosmetic or minor usability issue |
| Informational | Observation only |

## 10. Test Priority Classification

| Priority | Description |
| -------- | ----------- |
| Critical | Core business workflow must function correctly |
| High | Important user-facing functionality |
| Medium | Functionality affects usability but does not block workflows |
| Low | Minor usability or cosmetic concern |

## 11. Test Coverage Summary

| Area | Coverage |
| ---- | -------- |
| Homepage | Covered |
| Navigation | Covered |
| About Page | Covered |
| Services Page | Covered |
| Contact Workflow | Covered |
| Responsive Behaviour | Covered |
| Cross-Browser Testing | Covered |
| Accessibility | Covered |
| SEO Validation | Covered |
| Deployment Readiness | Covered |

## 12. Requirement Coverage Alignment

The test suite provides coverage across all approved functional requirements documented within the Software Requirements Specification (SRS) and Requirements Traceability Matrix (RTM).

Coverage includes:

* Business requirements validation
* Functional workflow validation
* Responsive behaviour validation
* Accessibility verification
* SEO readiness review
* Deployment-readiness assessment

## 13. Conclusion

The defined test scenarios provide coverage across functional, responsive, usability, accessibility, SEO, and deployment-readiness requirements.

These test cases form the basis for execution reporting, defect tracking, and overall quality assessment of the Legal Services Digital Platform.
