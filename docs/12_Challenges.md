# Challenges

**Version:** 1.0
**Project:** Legal Services Digital Platform
**Last Updated:** 2026-06-17
**Author:** Mpumelelo Theophilas Nxazonke
**Status:** Complete

## Purpose

This document captures engineering, UX, infrastructure, and deployment-related challenges encountered during the development lifecycle of the Legal Services Digital Platform.

## 1. Overview

Software projects rarely progress in a perfectly linear manner.

Throughout the implementation of the Legal Services Digital Platform, several technical, operational, and project-management challenges were encountered.

This document captures those challenges, the actions taken to address them, and the lessons derived from each situation.

## 2. Challenge 1: Evolving Project Scope

### 2.1. Situation

The project initially began as a relatively straightforward legal services website.

As development progressed, additional opportunities for improvement were identified, including:

* Enhanced user experience
* Additional service presentation structures
* Attorney profile enhancements
* Contact workflow improvements
* SEO optimization
* Production deployment considerations

The platform evolved beyond a simple informational website into a more comprehensive digital presence.

### 2.2. Impact

The evolving scope increased:

* Design effort
* Development effort
* Testing effort
* Documentation requirements

### 2.3. Response

A flexible implementation approach was adopted.

Requirements were reviewed continuously and incorporated through iterative refinement rather than major redesign efforts.

### 2.4. Outcome

The resulting platform better aligned with business objectives while maintaining delivery progress.

## 3. Challenge 2: Content Availability

### 3.1. Situation

Certain content required for final production deployment was not immediately available.

Examples included:

* Professional attorney profile photographs
* Final content confirmations
* Additional stakeholder review feedback

### 3.2. Impact

Some sections could not be finalized exactly as intended during development.

### 3.3. Response

Placeholder content was used during implementation and testing to allow development progress to continue.

The platform architecture was designed to allow easy replacement of temporary assets.

### 3.4. Outcome

Development and testing activities continued without unnecessary delays.

## 4. Challenge 3: Responsive Layout Refinement

### 4.1. Situation

Responsive testing identified layout concerns within the attorney profile section on mobile devices.

Observed behaviour included:

* Text content appearing above profile images
* Visual flow inconsistencies between attorney profiles

### 4.2. Impact

The issue affected content presentation and user experience on smaller devices.

**Severity:** Low to Medium (UI/UX Impact)

### 4.3. Response

The issue was documented during testing and scheduled for refinement prior to production launch.

### 4.4. Outcome

The finding highlighted the value of dedicated mobile testing throughout development.

## 5. Challenge 4: Contact Workflow Reliability

### 5.1. Situation

The contact form represented a critical business workflow because it directly affected lead generation and client communication.

A failed enquiry submission could result in missed business opportunities.

### 5.2. Impact

Additional validation and infrastructure review activities were required.

## 5.3. Response

Implementation included:

* Input validation
* Input sanitization
* Email validation
* Workflow testing

Additional investigations were performed into:

* SMTP
* PHPMailer
* Email routing

## 5.4. Outcome

The enquiry workflow achieved a higher level of deployment readiness and reliability.

## 6. Challenge 5: Email Deliverability Uncertainty

### 6.1. Situation

Although the contact workflow functioned correctly, questions remained regarding long-term email deliverability reliability.

Deliverability concerns are common when relying on standard hosting-based mail infrastructure.

### 6.2. Impact

Potential risk of lost enquiries.

### 6.3. Response

Additional investigations included:

* SMTP review
* Mail routing review
* Deliverability analysis
* Infrastructure assessment

PHPMailer and authenticated SMTP were evaluated as future enhancement options.

### 6.4. Outcome

Potential risks were identified early and documented appropriately.

## 7. Challenge 6: DNS & Email Infrastructure (DMARC Configuration Finding)

### 7.1. Situation

During deployment readiness review, DNS and email infrastructure validation identified a DMARC configuration warning.

### 7.2. Impact

The finding required additional investigation to determine potential production impact.

### 7.3. Response

DNS configuration was reviewed and findings documented.

The issue was classified as a deployment-level infrastructure observation rather than a production-blocking defect.

### 7.4. Outcome

The investigation improved understanding of infrastructure dependencies beyond application development.

## 8. Challenge 7: Balancing Simplicity and Future Scalability

### 8.1. Situation

Several future enhancement opportunities were identified during solution discussions.

Examples included:

* Client portals
* Appointment scheduling
* Case management systems
* Workflow automation
* Centralized enquiry management

### 8.2. Impact

Architectural decisions needed to balance current project scope with future extensibility.

### 8.3. Response

The platform was designed using a modular structure capable of supporting future enhancements without introducing unnecessary complexity into the current release.

### 8.4. Outcome

The solution remains lightweight while preserving future growth opportunities.

## 9. Challenge 8: Deployment Dependencies

### 9.1. Situation

Production deployment depends on activities that extend beyond software development.

Examples include:

* Final stakeholder review
* Content approval
* Asset delivery
* Production deployment scheduling

### 9.2. Impact

A technically complete solution may still be unable to launch immediately.

### 9.3. Response

A staging-first deployment model was used.

This enabled:

* Continued testing
* Stakeholder review
* Documentation completion
* Deployment preparation

without requiring immediate production release.

### 9.4. Outcome

Project progress continued while launch dependencies were addressed.

## 10. Challenge Summary

| Challenge | Category | Status |
| --------- | -------- | ------ |
| Evolving Scope | Project Management | Managed |
| Content Availability | Stakeholder Dependency | Managed |
| Responsive Layout Refinement | UX/UI | Identified |
| Contact Workflow Reliability | Technical | Addressed |
| Email Deliverability | Infrastructure | Investigated |
| DNS Findings | Infrastructure | Documented |
| Scalability Planning | Architecture | Addressed |
| Deployment Dependencies | Operational | Managed |

## 11. Key Lessons

Several important lessons emerged during the project:

* Requirements often evolve during implementation.
* Responsive testing should occur continuously.
* Email delivery workflows require infrastructure consideration.
* DNS configuration directly impacts operational readiness.
* Staging environments reduce deployment risk.
* Technical completion does not always equal deployment readiness.
* Future scalability should be considered without over-engineering the current solution.

## 12. Conclusion

The challenges encountered throughout the project contributed significantly to both the quality of the final solution and the engineering knowledge gained during implementation.

By addressing technical, operational, and stakeholder-related challenges proactively, the project progressed from a simple website initiative into a more comprehensive and deployment-ready digital platform.