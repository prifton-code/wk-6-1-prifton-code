Cart management...### TC-CART-001: Add Item to Cart
**Priority:** P0 - Critical
**Test Type:** Manual
**Pre-conditions:** User is viewing product details page
**Steps:**
1. Click "Add to Cart" button on any book
2. Observe cart icon in header
3. Click on cart icon to view cart
4. Verify item appears in cart with correct details
**Expected Result:** Item is added to cart, cart counter updates, item details are correct
**Evidence:** `test evidence for cart.png`

### TC-CART-002: Update Cart Quantity
**Priority:** P1 - High
**Test Type:** Manual
**Pre-conditions:** User has at least one item in cart
**Steps:**
1. Navigate to cart page
2. Locate quantity input for an item
3. Increase quantity using '+' button
4. Verify total price updates correctly
5. Decrease quantity using '-' button
**Expected Result:** Quantity changes reflect in cart total price calculation
**Evidence:** `tests/evidence/update-quantity.png`

### TC-CART-003: Remove Item from Cart
**Priority:** P1 - High
**Test Type:** Manual
**Pre-conditions:** User has items in cart
**Steps:**
1. Navigate to cart page
2. Click "Remove" button next to an item
3. Confirm removal if prompted
4. Verify item is removed from cart
5. Check cart total updates correctly
**Expected Result:** Item is completely removed from cart, total price recalculated
**Evidence:** `tests/evidence/remove-item.png`

### TC-CART-004: Cart Persistence Across Sessions
**Priority:** P2 - Medium
**Test Type:** Manual
**Pre-conditions:** User has items in cart
**Steps:**
1. Add items to cart
2. Close browser tab
3. Reopen application in new tab
4. Navigate to cart page
**Expected Result:** Cart items persist across browser sessions via localStorage
**Evidence:** `tests/evidence/cart-persistence.png`

### TC-CART-005: Cart Quantity Price Calculation Bug
**Priority:** P1 - High
**Test Type:** Manual
**Pre-conditions:** User has items in cart
**Steps:**
1. Add "React Fundamentals" book to cart (Price: $29.99)
2. Navigate to cart page
3. Click '+' button to increase quantity to 2
4. Observe total price calculation
**Expected Result:** Total price should update to $59.98 (2 × $29.99)
**Actual Result:** Total price remains $29.99 despite quantity showing 2
**Evidence:** `tests/evidence/cart-quantity-bug.png`