# SMTP Review

**Version:** 1.0<br>
**Project:** Legal Services Digital Platform<br>
**Date:** 2026-06-11<br>
**Author:** Mpumelelo Theophilas Nxazonke<br>
**Status:** In Review

## 1. Overview

This document captures SMTP configuration considerations identified during deployment-readiness and email infrastructure validation activities for the Legal Services Digital Platform.

The purpose is to assess email delivery configuration options, authentication requirements, and potential improvements to ensure reliable communication between the platform and business email systems.

## 2. Current Email Implementation

The platform currently uses a server-side email delivery mechanism integrated into the contact workflow:

* PHP-based mail handling (`mail()` function)
* Hosting-provider email routing
* Basic form submission delivery workflow

### 2.1. Current Flow

```text
Visitor
 ↓
Contact Form
 ↓
Validation
 ↓
contact.php
 ↓
Server Mail Handler
 ↓
Business Email Inbox
```

## 3. SMTP Configuration Assessment

### 3.1 Current State

SMTP is not currently enforced as the primary mail transport method.

Email delivery is dependent on hosting-level mail configuration and default server routing behavior.

### 3.2 Observations

The following considerations were identified during review:

* Default `mail()` function may have inconsistent deliverability across providers
* Lack of authenticated SMTP may increase spam classification risk
* Limited visibility into email delivery success/failure tracking
* No centralized email delivery logging implemented

## 4. Authentication Considerations

SMTP authentication was reviewed as part of deployment readiness.

Key authentication components typically required:

* SMTP host configuration
* Port selection (25 / 465 / 587 depending on provider)
* Username/password authentication
* TLS/SSL encryption support

## 5. Risk Assessment

| Risk Area | Impact |
| --------- | ------ |
| Unauthenticated mail delivery | Medium |
| Email deliverability inconsistency | Medium |
| Lack of delivery tracking | Low |
| Spam classification risk | Medium |

## 6. Recommended Improvements

To improve reliability and production-grade email delivery, the following enhancements are recommended:

### 6.1 SMTP Integration

* Implement authenticated SMTP for all outbound mail
* Replace or supplement `mail()` function where necessary

### 6.2 Suggested Libraries

* PHPMailer (recommended)
* Symfony Mailer (alternative)

### 6.3 Delivery Enhancements

* Enable TLS encryption for email transport
* Configure retry logic for failed deliveries
* Implement logging for email success/failure states

## 7. Deployment Impact

SMTP configuration does not block initial platform deployment.

However, it impacts:

* Email reliability
* Contact form deliverability consistency
* Long-term operational robustness

## 8. Assessment

The current email system is functional but not optimized for production-grade deliverability assurance.

From an engineering perspective:

* Core functionality is operational
* Improvements are classified as enhancement-level changes
* No critical deployment blockers identified

## 9. Status

**Open – Enhancement Recommended**

SMTP upgrade is advised for improved reliability but is not required for initial production deployment.
