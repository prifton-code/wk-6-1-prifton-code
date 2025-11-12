Order management ....### TC-ORD-001: Order Confirmation and Details
**Priority:** P1 - High
**Test Type:** Manual
**Pre-conditions:** User has completed a purchase
**Steps:**
1. Complete checkout process successfully
2. Verify order confirmation page loads
3. Check order number is displayed
4. Verify order details match cart items
**Expected Result:** Order confirmation displays correct details
**Evidence:** `tests/evidence/order-confirmation.png`

### TC-ORD-002: Order History Access
**Priority:** P2 - Medium
**Test Type:** Manual
**Pre-conditions:** User has completed previous orders
**Steps:**
1. Navigate to "My Orders" or order history page
2. Verify previous orders are listed
3. Click on a specific order to view details
4. Verify order details match original purchase
**Expected Result:** Order history displays all previous orders with correct details
**Evidence:** `tests/evidence/order-history.png`