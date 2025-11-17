# 📘 Bookstore App — Test Execution Log  
Team: LPP Team  
Project: Bookstore Web Application  
Phase: Week 2 — Test Design & Early Execution  
Prepared by: LPP QA Team  
Date: November 12–11-2025

---

## 🧩 Purpose
This document records every test case executed during Week 2: who ran it, when, where (environment), the result, links to evidence, and which Jira/GitHub bug  was filed for failures.

---

## 🖥 Test Environment (common)
- OS: Windows 10
- Browsers: Chrome v120, Firefox 
- Mobile: Chrome mobile emulation (Pixel/Small widths)  
- Network: Normal and Fast 3G throttling used for some perf tests  
- Build: Local dev server (npm start)  

---

## 🧪 Full Execution Records

| Exec ID | Test Case ID | Test Case Title (short) | Tester | Date | Environment | Result | Evidence (path) | Jira / Bug Link |
|--------:|--------------|--------------------------|--------|------|-------------|:------:|------------------|------------------|
| EX001 | FR-CAT-001 | Book search returns results (title/author/desc) | Lena | 2025-11-11 | Chrome / Win10 | Pass | tests/evidence/FR-CAT-001.png | — |
| EX002 | FR-CAT-002 | Catalog page displays all books | Lena | 2025-11-11 | Chrome / Win10 |  Pass | tests/evidence/FR-CAT-002.png | — |
| EX003 | FR-CART-001 | Add item to cart increments counter | Lena | 2025-11-11 | Chrome / Win10 | Pass | tests/evidence/FR-CART-001.png | — |
| EX004 | FR-CART-002 | Update cart quantity and totals | Lena | 2025-11-11 | Chrome / Win10 |  Pass | tests/evidence/FR-CART-002.png | — |
| EX005 | FR-CART-003 | Remove item from cart | Lena | 2025-11-11 | Chrome / Win10 |  Pass | tests/evidence/FR-CART-003.png | — |
| EX006 | FR-CART-004 | Cart persistence across sessions (localStorage) | Peter | 2025-11-11 | Chrome / Win10 | Pass | tests/evidence/FR-CART-004.png | — |
| EX007 | FR-CART-005 | Cart quantity price calculations | Peter | 2025-11-11 | Chrome / Win10 | Pass | tests/evidence/FR-CART-005.png | — |
| EX008 | FR-CHK-001 | Checkout process initiation (cart -> checkout) | Lena | 2025-11-12 | Chrome / Win10 | Pass | tests/evidence/FR-CHK-001.png | — |
| EX009 | FR-CHK-002 | Shipping form validation (required fields & email) | Peter | 2025-11-12 | Chrome / Win10 | Fail | tests/evidence/FR-CHK-002-01.png | SOF-24 / BUG002 |
| EX010 | FR-CHK-003 | Paystack test card processing (happy path) | Prifton | 2025-11-12 | Chrome / Win10 | Pass | tests/evidence/FR-CHK-003.png | — |
| EX011 | FR-CHK-004 | Payment currency mismatch check | Prifton | 2025-11-12 | Chrome / Win10 | Fail | tests/evidence/FR-CHK-004.png | SOF-26 / BUG004 |
| EX012 | FR-ORD-001 | Order confirmation details match cart | Lena | 2025-11-12 | Chrome / Win10 | Pass | tests/evidence/FR-ORD-001.png | — |
| EX013 | FR-ORD-002 | Order history access & details view | Lena | 2025-11-12 | Chrome / Win10 | Pass | tests/evidence/FR-ORD-002.png | — |
| EX014 | FR-A11Y-001 | Keyboard navigation (Tab/Enter/Space) | Lena | 2025-11-13 | Chrome / Win10 | Pass | tests/evidence/FR-A11Y-001.png | — |
| EX015 | FR-A11Y-002 | Screen reader compatibility basic checks | Peter | 2025-11-13 | NVDA/Chrome | Partial Pass | tests/evidence/FR-A11Y-002.png | SOF-31 / BUG013 |
| EX016 | FR-A11Y-003 | Checkout modal accessibility (aria-modal & focus trap) | Peter | 2025-11-13 | Chrome / Win10 | Fail | tests/evidence/FR-A11Y-003.png | SOF-32 / BUG006 |
| EX017 | FR-PERF-001 | Page load performance (Lighthouse quick check) | Prifton | 2025-11-13 | Chrome / Win10 (Lighthouse) | Pass | tests/evidence/FR-PERF-001.png | — |
| EX018 | FR-PERF-002 | Layout Shift (CLS) under throttled network | Prifton | 2025-11-13 | Chrome - Slow 3G | Fail | tests/evidence/FR-PERF-002.png | SOF-40 / BUG010 |
| EX019 | TC-NAV-001 | Navbar search behavior (Enter uses search term) | Peter | 2025-11-13 | Chrome / Win10 | Fail | tests/evidence/TC-NAV-001.png | SOF-36 / BUG008 |
| EX020 | TC-NAV-002 | Search persistence across routes | Lena | 2025-11-13 | Chrome / Win10 | Partial Pass | tests/evidence/TC-NAV-002.png | SOF-37 / BUG009 |
| EX021 | TC-PERF-001 | Navbar search typing latency / debounce check | Peter | 2025-11-13 | Chrome / Win10 | Fail | tests/evidence/TC-PERF-001.png | SOF-39 / BUG010 |
| EX022 | TC-NAV-003 | ESC key behaviour resets & refocus | Peter | 2025-11-13 | Chrome / Win10 | Fail | tests/evidence/TC-NAV-003.png | SOF-41 / BUG011 |
| EX023 | TC-UI-003 | Cart badge alignment on mobile/responsive check | Peter | 2025-11-13 | Chrome Mobile Emulation | Fail | tests/evidence/TC-UI-003.png | SOF-42 / BUG012 |
| EX024 | TC-APP-001 | 404 / unknown routes redirect to /catalog gracefully | Prifton | 2025-11-13 | Firefox / Win10 |  Fail | tests/evidence/TC-APP-001.png | SOF-43 / BUG014 |
| EX025 | FR-CHK-006 | Back button from Payment retains cart & shipping data | Prifton | 2025-11-13 | Chrome / Win10 | Fail | tests/evidence/FR-CHK-006.png | SOF-45 / BUG015 |

---

## 📊 Results (Week 2 run)

| Result Type | Count |
|-------------:|------:|
| ✅ Passed | 9 |
| ⚠ Partial Pass | 2 |
| ❌ Failed | 14 |
| ⏳ Blocked | 0 |
| Total executed | 25 |

---

## 🔎 Observations
- Catalog & Cart features (search, add/remove, persistence, calculations) are stable these tests mostly passed (EX001–EX007). Evidence captured in tests/evidence.
- Checkout: initiation (EX008) and in-flow (EX010) passed, but validation (EX009), currency handling (EX011), back-button state handling (EX025), and modal accessibility (EX016) failed and were logged as defects.
 - CheckoutService.js indicates currency is passed into the payment utils FR-CHK-004 failure shows mismatch between UI currency and gateway, this is logged as BUG004.
- Orders / Order detail (EX012–EX013) displayed expected details when orders existed OrderDetailPage.js handles missing orders gracefully (shows "We couldn't find this order.").
- Accessibility: keyboard navigation largely works (EX014 Pass) but ARIA & screen reader coverage is incomplete (EX015 Partial, EX016 Fail).
- Performance: page load basic metrics passed (EX017), but layout shift (CLS) under throttling failed (EX018).
- Navbar: search behavior, persistence, debounce and ESC behaviour are inconsistent and they produced multiple fails/partials (EX019–EX022).
- Routing: 404 redirect looping observed and logged (EX024).

---

## 🧭 Recommended immediate priority fixes
1. Checkout validation — required fields and email/postal code validation. (SOF-24 / BUG002)  
2. Prevent duplicate payments (disable/lock Pay button during processing) and fix currency argument passed to gateway. (SOF-26 / BUG004 & related)  
3. Modal & focus management in checkout for a11y (SOF-32 / BUG006).  
4. Navbar search: ensure entered search term is actually passed to the Catalog filter, add debounce, and persist state if required (SOF-36 / BUG008, SOF-39 / BUG010).  
5. CLS & perf: reserve image dimensions or use placeholders to reduce layout shift (SOF-40 / BUG010).  
6. Routing guards: redirect user from /checkout when cart is empty (SOF-29 / BUG005) and ensure 404 redirect doesn't loop (SOF-43 / BUG014).

---

*Prepared by:* LPP QA Team  
📅 November 14, 2025  
📁 File: tests/test-execution-log.md