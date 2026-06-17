# Deployment Checklist

**Version:** 1.0
**Project:** Legal Services Digital Platform
**Date:** 2026-06-11
**Author:** Mpumelelo Theophilas Nxazonke
**Status:** Pre-Deployment Checklist

## 1. Overview

This checklist defines the final verification steps required before deploying the Legal Services Digital Platform to production.

It ensures that all functional, technical, SEO, and infrastructure requirements are validated prior to public release.

## 2. Source Code & Production Build

* [ ] All latest changes committed to repository
* [ ] Production branch confirmed (main / production)
* [ ] No untracked or uncommitted files remaining
* [ ] All debug code removed
* [ ] Console logs removed or disabled
* [ ] Environment-specific configs verified

## 3. File Deployment Verification

* [ ] All HTML files uploaded
* [ ] All CSS files uploaded
* [ ] All JavaScript files uploaded
* [ ] All PHP backend files uploaded
* [ ] All image assets uploaded
* [ ] All media files verified
* [ ] Folder structure preserved on hosting environment
* [ ] No missing asset references in console/network tab

## 4. SEO & Meta Tag Validation

### 4.1 Page-Level Meta Tags

Verify each production page includes:

```html
<title>Correct Page Title</title>

<meta name="description" content="Accurate page description aligned with services">
<meta name="robots" content="index, follow">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### 4.2 Open Graph Tags (Social Sharing)

* [ ] og:title present
* [ ] og:description present
* [ ] og:image present
* [ ] og:url correctly set

### 4.3 SEO Configuration Checks

* [ ] `noindex` removed from all production pages
* [ ] `nofollow` removed from production pages
* [ ] `robots.txt` verified and accessible
* [ ] `sitemap.xml` generated and accessible
* [ ] Canonical URLs correctly set

## 5. Performance Validation

* [ ] Lighthouse performance acceptable (target ≥ 80)
* [ ] Images compressed and optimized (WebP where possible)
* [ ] Lazy loading implemented for non-critical images
* [ ] No render-blocking scripts where avoidable
* [ ] No long-running JavaScript tasks detected

## 6. Accessibility Validation

* [ ] Lighthouse accessibility score verified (target 100)
* [ ] All images have alt attributes
* [ ] All form fields have labels
* [ ] Keyboard navigation tested
* [ ] Heading hierarchy validated (H1 → H2 → H3)

## 7. Functional Testing

* [ ] Homepage loads correctly
* [ ] Navigation works across all pages
* [ ] Services page displays correctly
* [ ] Attorney profiles display correctly
* [ ] Contact form submits successfully
* [ ] Thank-you page redirect works
* [ ] WhatsApp integration tested
* [ ] Google Maps integration tested

## 8. Contact Form & Email System

* [ ] Contact form validation tested
* [ ] Form submission successful
* [ ] Email routing verified
* [ ] SMTP (if enabled) tested
* [ ] Inbox delivery confirmed
* [ ] Spam folder check completed

## 9. DNS & Domain Configuration

* [ ] Domain points to correct hosting provider
* [ ] A record verified
* [ ] CNAME records verified (if applicable)
* [ ] MX records configured
* [ ] SPF record configured
* [ ] DMARC record validated
* [ ] DNS propagation completed

## 10. SSL & Security

* [ ] SSL certificate installed
* [ ] HTTPS enforced across all pages
* [ ] HTTP redirects to HTTPS
* [ ] No mixed content warnings
* [ ] Security headers verified (if configured)

## 11. Browser & Device Testing

* [ ] Chrome (Desktop)
* [ ] Edge (Desktop)
* [ ] Mobile Chrome
* [ ] Tablet layout verified
* [ ] Responsive breakpoints tested

## 12. Final Production Validation

* [ ] No console errors in production
* [ ] No broken links detected
* [ ] All forms functional
* [ ] All images loading correctly
* [ ] All external integrations working

## 13. Go-Live Readiness

* [ ] Stakeholder approval received
* [ ] Content finalized (no placeholders remaining)
* [ ] Legal/branding review completed
* [ ] Backup of previous version taken
* [ ] Rollback plan confirmed

## 14. Deployment Decision

**Status:**

- [ ] Approved for Production Deployment
- [ ] Not Ready for Deployment

## 15. Notes

This checklist should be completed immediately prior to production release to ensure system stability, SEO readiness, and full functional integrity of the Legal Services Digital Platform.
