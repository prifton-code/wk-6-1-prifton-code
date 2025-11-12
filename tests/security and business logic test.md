Security & logic...### TC-SEC-001: XSS Vulnerability Check
**Priority:** P1 - High
**Test Type:** Manual
**Pre-conditions:** Access to user content input fields
**Steps:**
1. Access any user-generated content field
2. Attempt to inject: `[Click Me](javascript:alert('xss'))`
3. Submit and view rendered content
**Expected Result:** JavaScript links should be sanitized or blocked
**Actual Result:** javascript: protocol links may execute (based on intentional defect)
**Evidence:** `tests/evidence/xss-vulnerability.png`

### TC-LOGIC-001: Return Window Validation
**Priority:** P2 - Medium
**Test Type:** Manual
**Pre-conditions:** User has completed an order
**Steps:**
1. Complete an order (note order date)
2. Wait 8 days (beyond 7-day return window)
3. Attempt to initiate return on day 8
**Expected Result:** Return should be rejected as outside return window
**Actual Result:** Return process allows initiation on day 8 (off-by-one error)
**Evidence:** `tests/evidence/return-window-bug.png`

### TC-LOGIC-002: Inventory Race Condition
**Priority:** P1 - High
**Test Type:** Manual
**Pre-conditions:** Product with low stock available
**Steps:**
1. Find a product with low stock (1-2 items)
2. Open multiple browser tabs/windows
3. Simultaneously add to cart from multiple sessions
**Expected Result:** Stock should be properly reserved, preventing over-selling
**Actual Result:** Multiple users can add beyond available stock due to race condition
**Evidence:** `tests/evidence/stock-race-condition.png`

### TC-LOGIC-003: Price Rounding Consistency
**Priority:** P1 - High
**Test Type:** Manual
**Pre-conditions:** Multiple items with decimal pricing
**Steps:**
1. Add multiple items with decimal pricing to cart
2. Note line item subtotals in cart
3. Compare with grand total calculation
**Expected Result:** Line item sums should equal grand total exactly
**Actual Result:** 1-2 cent rounding differences between sum of lines and grand total
**Evidence:** `tests/evidence/rounding-variance.png`