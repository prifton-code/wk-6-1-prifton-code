Check out and payment process...### TC-CHK-001: Checkout Process Initiation
**Priority:** P0 - Critical
**Test Type:** Manual
**Pre-conditions:** User has items in cart
**Steps:**
1. Navigate to cart page
2. Click "Proceed to Checkout" button
3. Verify checkout page loads
4. Check that cart items are displayed in checkout
**Expected Result:** Checkout process starts successfully, all cart items visible
**Evidence:** `tests/evidence/checkout-start.png`

### TC-CHK-002: Shipping Information Form Validation
**Priority:** P1 - High
**Test Type:** Manual
**Pre-conditions:** User is on checkout page
**Steps:**
1. Leave required fields empty
2. Click "Continue to Payment"
3. Verify validation messages appear
4. Fill in invalid email format
5. Verify email validation works
**Expected Result:** Form validation prevents proceeding with invalid data
**Evidence:** `tests/evidence/form-validation.png`

### TC-CHK-003: Paystack Test Card Processing
**Priority:** P0 - Critical
**Test Type:** Manual
**Pre-conditions:** User has items in cart, on checkout page
**Steps:**
1. Proceed to payment section
2. Enter test card: 4084084084084081
3. Enter any 3-digit CVV, future expiry date
4. Complete payment process
5. Observe currency displayed in payment gateway
**Expected Result:** Payment processes successfully, order confirmation displayed
**Evidence:** `tests/evidence/paystack-test-success.png`

### TC-CHK-004: Payment Currency Mismatch Bug
**Priority:** P0 - Critical
**Test Type:** Manual
**Pre-conditions:** User is on payment step
**Steps:**
1. Browse products showing prices in $ (dollars)
2. Add items to cart, proceed to checkout
3. Initiate Paystack payment
4. Observe currency in payment gateway
**Expected Result:** Payment gateway should use same currency as UI ($)
**Actual Result:** Payment gateway uses KES (Kenyan Shillings) regardless of UI display
**Evidence:** `tests/evidence/currency-mismatch.png`

### TC-CHK-005: Payment Button State Bug
**Priority:** P1 - High
**Test Type:** Manual
**Pre-conditions:** User is on checkout page with form errors
**Steps:**
1. Fill shipping form with invalid email format
2. Click "Continue to Payment" - form validation should fail
3. Correct email to valid format
4. Attempt to click "Continue to Payment" again
**Expected Result:** Button should become enabled and allow proceeding to payment
**Actual Result:** Button remains permanently disabled, requiring page refresh
**Evidence:** `tests/evidence/payment-button-bug.png`