# 🧪 Bookstore App — Test Cases

Project: Bookstore Web Application  
Team: QA Group (Lena Ngarama, Prifton Mliwa, Peter Adebisi)  
Date:11 November 2025  
Test Type: Functional, Non-functional, and Regression Testing  
Tracking Tool: Jira Software (linked with GitHub repo)  

---

## 🧩 1. Test Case Summary

| ID | Feature / Component | Test Objective | Test Type | Priority | Status |
|----|----------------------|----------------|------------|-----------|---------|
| TC001 | User Registration | Verify user can create a new account with valid details | Functional | High | Executed |
| TC002 | Login | Ensure user can log in with valid credentials | Functional | High | Executed |
| TC003 | Catalog Browsing | Verify user can view and filter books by category/author | Functional | Medium | Executed |
| TC004 | Add to Cart | Check that selected books can be added to the shopping cart | Functional | High | Executed |
| TC005 | Checkout Process | Validate that checkout completes successfully with valid details | Functional | Critical | Executed |
| TC006 | Payment Integration | Confirm secure payment via integrated gateway (e.g., Paystack/Stripe) | Functional | Critical | Executed |
| TC007 | Order Confirmation | Ensure order summary and confirmation message are displayed | Functional | High|Executed |
| TC008 | Accessibility (WCAG 2.1) | Confirm app meets basic accessibility guidelines | Non-Functional | Medium| Executed |
| TC009 | Performance | Measure page load time under normal load conditions | Non-Functional | Medium | Executed |
| TC010 | Cross-Browser | Verify consistent display on Chrome, Edge, and Firefox | Non-Functional | Medium | Executed |
| TC011 | Responsive Design | Ensure UI adjusts properly on mobile, tablet, and desktop | Non-Functional | Medium | Not Executed |
| TC012 | Security | Validate input sanitization and data encryption on login and checkout | Security | High | Not Executed |
| TC013 | Error Handling | Confirm meaningful error messages appear for invalid inputs | Functional | Medium | Not Executed |
| TC014 | Logout | Ensure user can successfully log out and session ends properly | Functional | Medium | Not Executed |

---


### Test Case ID: TC005 — Checkout Process

Objective:
To verify that a user can successfully complete the checkout process after adding items to the cart.

Preconditions:
- User account exists and is logged in  
- At least one book is added to the cart  
- Payment gateway integration is active

Test Steps: 
1. Navigate to 'Cart' page.  
2. Click 'Checkout'.  
3. Enter valid billing and shipping details.  
4. Select a payment method.  
5. Submit the order.  

Expected Result: 
- Order confirmation page is displayed with order ID and total amount.  
- Confirmation email is sent to the registered email address.

Post-condition: 
Order is recorded in the database and visible under *My Orders*.

Severity: Critical  
Priority: High  
Status: Not Executed  
Evidence: To be attached after execution 

---

## 🧩 3. Test Data

| Data Type | Example |
|------------|----------|
| Username | testuser01@example.com |
| Password | Test@123 |
| Book Title | "The Lean Startup" |
| Payment Method | Card Payment (Paystack/Stripe) |
| Shipping Address | 123 Nairobi Lane, Kenya |

---

## 📋 4. Traceability Matrix (Optional)

| Requirement ID | Test Case ID(s) | Status |
|----------------|-----------------|--------|
| FR-001 User Registration | TC001 | Pending |
| FR-002 Login | TC002 | Pending |
| FR-003 Catalog Management | TC003, TC004 | Pending |
| FR-004 Checkout & Payments | TC005, TC006, TC007 | Pending |
| NFR-001 Accessibility | TC008 | Pending |
| NFR-002 Performance | TC009 | Pending |
| NFR-003 Cross-Platform | TC010, TC011 | Pending |
| NFR-004 Security | TC012 | Pending |

---

## 📊 5. Test Execution Log (to be updated)

| Date | Tester | Test Case ID | Result | Comments / Defects Logged |
|------|---------|---------------|--------|---------------------------|
| — | — | — | — | — |

---

## ✅ 6. Definition of Done (DoD)

Each executed test case must include:
- [ ] Reproduction steps  
- [ ] Expected vs Actual Results  
- [ ] Attached evidence (screenshots or logs)  
- [ ] Status updated in Jira  
- [ ] Reviewed and approved by QA Lead  

---

*Prepared by:* Lena Ngarama (QA Lead)  
*Reviewed by:* Team Members  
*Tooling:* Jira Software, GitHub, Chrome DevTools, Lighthouse  

---