# 🐞 Bookstore App — Defect Log (Week 2)
Team: LPP Team  
Project: Bookstore Web Application  
Phase: Week 2 — Test Design & Early Execution  
Date: November 13, 2025  
Prepared by: LPP Team  

---

## 🧩 Overview
This defect log documents bugs and usability issues detected during Week 2 testing of the Bookstore App.  
Testing covered routing, navigation, checkout workflow, and accessibility of major components (App.js, Navbar.js, and CheckoutPage.js).

---
| ID | Date | Component | Summary | Steps to Reproduce | Expected Result | Actual Result | Severity | Priority | Status | Assignee | Evidence |
|----|------|-----------|----------|--------------------|-----------------|----------------|-----------|-----------|---------|-----------|----------|
| BUG001 | 2025-11-12 | CheckoutPage | 'Pay Now' button allows multiple clicks | 1. Proceed to checkout<br>2. Click 'Pay Now' repeatedly | Only one payment request should trigger | Multiple payment attempts processed when clicked quickly | Critical | High | Open | Peter Adebisi | <img width="1920" height="1080" alt="Bug001" src="https://github.com/user-attachments/assets/9269d6ff-43de-4049-b00b-6e240c34e1af" /> |
| BUG002 | 2025-11-12 | CheckoutPage | Missing input validation for postal code format | 1. Enter letters in postal code<br>2. Click 'Next' | Should display validation error | Form proceeds without validating postal code | Major | High | Open | Peter Adebisi | <img width="1920" height="1080" alt="BUG002" src="https://github.com/user-attachments/assets/e1c376a9-0568-4c3f-b678-3bbe1adf5df5" /> |
| BUG003 | 2025-11-12 | CheckoutPage | Invalid email accepted | 1. Enter "abc@" as email<br>2. Click 'Next' | Should show "Enter valid email" error | Form accepts invalid email | Major | High | Open | Peter Adebisi | <img width="1920" height="1080" alt="BUG003" src="https://github.com/user-attachments/assets/344fac87-48c1-46f0-a5b5-60be1b34df27" />|
| BUG004 | 2025-11-13 | CheckoutPage | Payment fails silently on network loss | 1. Disconnect network<br>2. Click 'Pay Now' | User notified of connection issue | Displays "Payment failed to start" without clear cause | Minor | Medium | Open | Lena | [Screenshot] |
| BUG005 | 2025-11-13 | CheckoutPage | Screen reader missing ARIA roles for steps | 1. Open checkout<br>2. Inspect with screen reader | Each step should have proper ARIA labels | Screen reader reads plain text only | Minor | Medium | Open | Prifton Mliwa | [Screenshot] |
| BUG006 | 2025-11-13 | CheckoutPage | Order confirmation flashes before redirect | 1. Complete payment<br>2. Observe redirect | Smooth redirect to /orders/:id | Confirmation flashes briefly | Cosmetic | Low | Open | Lena | [Recording] |
| BUG007 | 2025-11-13 | Navbar | Search not submitting queries correctly | 1. Enter a book title<br>2. Press Enter | Should search and filter catalog results | Pressing Enter only redirects to /catalog without using search input | Major | High | Open | Peter Adebisi | [Screenshot] |
| BUG008 | 2025-11-13 | Navbar | Search bar clears unexpectedly after route change | 1. Search a book<br>2. Navigate to another page<br>3. Go back | Search term should persist | Search field resets automatically | Minor | Medium | Open | Peter Adebisi | [Recording] |
| BUG009 | 2025-11-13 | Navbar | No debounce for keypress in search | 1. Type quickly in search field | Should handle input efficiently | Input lags and re-renders cause delay | Minor | Medium | Open | Lena | [Recording] |
| BUG010 | 2025-11-13 | Navbar | ESC key not consistently resetting focus | 1. Click in search<br>2. Press ESC repeatedly | Should clear and refocus search field | Focus sometimes lost and requires manual click | Minor | Medium | Open | Prifton Mliwa | [Recording] |
| BUG011 | 2025-11-13 | Navbar | Cart count badge overlaps icon on mobile | 1. Open app on narrow screen<br>2. Observe cart icon | Badge should be aligned above icon | Badge overlaps with cart emoji | Cosmetic | Low | Open | Lena | [Screenshot] |
| BUG012 | 2025-11-13 | Navbar | Missing ARIA labels on icons | 1. Inspect cart link with screen reader | Should have descriptive ARIA label | Only reads "link" without context | Minor | Medium | Open | Peter Adebisi | [Screenshot] |
| BUG013 | 2025-11-13 | App.js | 404 redirect loops on invalid URL | 1. Visit /random-page | Should redirect once to /catalog | Rapid redirects flash multiple times | Minor | Medium | Open | Peter Adebisi | [Recording] |

## 📊 Summary

### Severity Breakdown
| Severity | Count |
|-----------|--------|
| Critical | 1 |
| Major | 3 |
| Minor | 7 |
| Cosmetic | 2 |
| **Total** | **13** |
---

## 🧠 Notes
- Payment and validation flows require stricter input handling (postal code, email).  
- Accessibility: Add missing ARIA roles and screen reader labels in Navbar and Checkout steps.  
- Performance: Implement debounce for Navbar search input.  
- UI: Fix mobile alignment for cart icon and badge.  
- Routing: Prevent direct navigation to Checkout when cart is empty.

---

Prepared by:  
 LPP TEAM
📅 November 13, 2025  

📁 File: tests/defect-log.md


