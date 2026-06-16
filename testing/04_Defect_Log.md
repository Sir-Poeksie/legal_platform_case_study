# Defect Log

**Version:** 1.0<br>
**Project:** Legal Services Digital Platform<br>
**Last Updated:** 2026-06-11<br>
**Author:** Mpumelelo Theophilas Nxazonke<br>
**Status:** Complete

## 1. Overview

This document records defects, observations, findings, and improvement opportunities identified during testing and deployment-readiness activities.

The purpose of the defect log is to provide traceability, support remediation activities, and document known issues prior to production launch.

## 2. Defect Severity Definitions

| Severity | Description |
| -------- | ----------- |
| Critical | Prevents core business functionality |
| High | Major feature impacted |
| Medium | Functional degradation or operational concern |
| Low | Cosmetic or usability issue |
| Informational | Observation or recommendation |

## 3. Defect Sources

Findings recorded within this log originated from:

* Functional testing
* Responsive testing
* Lighthouse audits
* Deployment readiness reviews
* Infrastructure investigations
* Stakeholder content reviews

## 4. Defect Register

| ID | Title | Severity | Status | Source |
| -- | ----- | -------- | ------ | ------ |
| DEF-001 | Attorney profile mobile layout inconsistency | Low | Open | Responsive Testing |
| DEF-002 | SEO score reduced due to robots directive | Informational | Expected | Lighthouse Audit |
| DEF-003 | DMARC configuration warning | Medium | Under Review | Infrastructure Review |
| DEF-004 | Attorney profile photographs unavailable | Low | Pending | Stakeholder Review |
| DEF-005 | SMTP implementation opportunity | Informational | Future Improvement | Infrastructure Investigation |
| DEF-006 | Hero layout shift on initial load | Medium | Open | Usability Testing |

### DEF-001 - Attorney Profile Mobile Layout Inconsistency

| Field | Value |
| ---- | ---- |
| Category | UI / UX |
| Severity | Low |
| Source | Responsive Testing |

#### Description

Responsive testing identified a content flow issue within the attorney profile section on mobile devices.

Observed behaviour:

* Attorney biography content displays above profile image.
* Subsequent attorney images appear immediately after previous content sections.
* Visual hierarchy becomes less intuitive on smaller screens.

#### Reproduction Steps

1. Open website on mobile device.
2. Navigate to attorney profile section.
3. Scroll through multiple attorney profiles.

#### Expected Result

Each attorney profile should maintain a consistent image-to-content relationship across screen sizes.

#### Actual Result

Content flow becomes inconsistent on smaller devices.

#### Impact

Minor usability and presentation concern.

No functional impact.

#### Recommendation

Review responsive layout structure and stacking order for attorney profile components.

### DEF-002 - SEO Score Reduced Due to Robots Directive

| Field | Value |
| ---- | ---- |
| Category | SEO |
| Severity | Informational |
| Status | Expected Behaviour |
| Source | Lighthouse Audit |

#### Description

Lighthouse SEO audit reported reduced SEO score.

Investigation identified:

```html
<meta name="robots" content="noindex, nofollow">
```

within the temporary Coming Soon page.

#### Expected Result

Production pages intended for indexing should permit search engine discovery.

#### Actual Result

Search engines are intentionally instructed not to index the temporary landing page.

#### Impact

Expected during staging and pre-launch phases.

No implementation defect identified.

#### Recommendation

Remove or update robots directive during production launch.

### DEF-003 - DMARC Configuration Warning

| Field | Value |
| ---- | ---- |
| Category | Infrastructure |
| Severity | Medium |
| Status | Under Review |
| Source | Infrastructure Review |

#### Description

Email deliverability review identified a DMARC-related warning.

Observed finding:

* Invalid DMARC version warning reported within hosting environment.

#### Expected Result

DMARC record correctly configured and validated.

#### Actual Result

Configuration warning reported during investigation.

#### Impact

Potential email authentication and deliverability implications.

No confirmed production failure identified.

#### Recommendation

Perform DNS review and validate DMARC configuration before production launch.

### DEF-004 - Attorney Profile Photography Pending

| Field | Value |
| ---- | ---- |
| Category | Content Dependency |
| Severity | Low |
| Status | Pending Stakeholder Input |
| Source | Stakeholder Review |

#### Description

Final professional attorney profile photographs were unavailable during implementation and testing.

Temporary placeholder imagery was utilised during development.

## Expected Result

Production-ready attorney profile photography supplied prior to launch.

## Actual Result

Placeholder images remain in use.

## Impact

Professional presentation incomplete.

No technical impact.

## Recommendation

Replace placeholder imagery before production deployment.

## DEF-005 - SMTP Implementation Opportunity

| Field | Value |
| ---- | ---- |
| Category | Enhancement |
| Severity | Informational |
| Status | Future Improvement |
| Source | Infrastructure Investigation |

### Description

Current contact workflow utilises PHP mail() functionality.

Infrastructure investigations identified an opportunity to improve delivery reliability through authenticated SMTP.

### Expected Result

Reliable enquiry delivery.

### Actual Result

Current implementation operational but may benefit from enhanced delivery controls.

### Impact

No confirmed issue observed.

Improvement opportunity only.

### Recommendation

Consider:

* PHPMailer
* Authenticated SMTP
* Delivery monitoring

for future enhancement.

## DEF-006 - Hero Layout Shift on Initial Load

| Category | UI / Performance |
| Severity | Medium |
| Status | Open |
| Source | Usability Testing |

### Description

Hero content alignment differs between initial page load and subsequent reloads on desktop devices, indicating a layout shift during initial rendering.

### Expected Result

Hero content should render consistently on first load without visual repositioning.

### Actual Result

Hero content alignment changes after page assets finish loading or after page refresh.

### Impact

* Perceived UI instability
* Reduced first-impression quality

No functional impact identified.

## Root Cause Hypothesis

* Web font loading behaviour
* CSS loading sequence
* Asset-driven layout recalculation

### Recommendation

* Preload critical fonts
* Consider font-display: swap
* Stabilise hero container dimensions during initial render

## 5. Known Risks & External Dependencies

### OPS-001 — Domain Transfer and DNS Ownership Dependency

| Field | Value |
| ----- | ----- |
| Category | External Dependency |
| Status | Awaiting Registrar / Client Action |
| Source | Deployment Readiness Review |

#### Description

Production email and DNS configuration activities depend on third-party registrar and hosting-provider actions outside the project team's control.

Observed findings include:

* Domain ownership transfer activities in progress.
* DNS records managed externally.
* Email services affected by unresolved DNS configuration.
* Client approval and registrar coordination required.

#### Impact

* Potential delay to production deployment.
* Potential interruption of email communication.
* Not caused by application implementation.

#### Recommendation

Complete domain ownership transfer and DNS configuration activities before final launch.

## 6. Defect Metrics

| Metric | Count |
| ------ | ----- |
| Critical | 0 |
| High | 0 |
| Medium | 2 |
| Low | 2 |
| Informational | 2 |
| Total Logged Items | 6 |

## 7. Defect Summary

Testing activities identified no Critical or High severity defects.

Most findings relate to:

* Content readiness
* Responsive refinements
* Infrastructure observations
* Future enhancement opportunities

No engineering defects were identified that prevent deployment preparation activities from continuing.

Remaining findings relate primarily to user interface refinements, infrastructure validation observations, stakeholder-supplied content, and future enhancement opportunities.

## 8. Conclusion

The defect review process identified a small number of manageable findings and enhancement opportunities.

The platform remains functionally complete and deployment-ready, with remaining items focused primarily on refinement, infrastructure validation, and stakeholder-supplied content.
