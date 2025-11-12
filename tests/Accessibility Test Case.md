Accessibility...### TC-A11Y-001: Keyboard Navigation
**Priority:** P1 - High
**Test Type:** Manual
**Pre-conditions:** User is on homepage
**Steps:**
1. Use Tab key to navigate through page
2. Verify focus indicators are visible on all interactive elements
3. Check that all buttons/links are reachable via keyboard
4. Use Enter/Space to activate elements
**Expected Result:** Full keyboard accessibility with visible focus indicators
**Evidence:** `testsevidencekeyboard-nav.png`

### TC-A11Y-002: Screen Reader Compatibility
**Priority:** P2 - Medium
**Test Type:** Manual
**Pre-conditions:** Screen reader enabled (or browser accessibility tools)
**Steps:**
1. Navigate through product grid
2. Verify images have descriptive alt text
3. Check form fields have proper labels
4. Verify interactive elements have meaningful names
**Expected Result:** Screen reader can properly interpret and announce all content
**Evidence:** `tests/evidence/screen-reader.png`

### TC-A11Y-003: Checkout Modal Accessibility Bug
**Priority:** P2 - Medium
**Test Type:** Manual
**Pre-conditions:** User is in checkout process
**Steps:**
1. Proceed to checkout process
2. Open accessibility audit tool (axe DevTools)
3. Scan checkout modal/dialog
**Expected Result:** Modal should have aria-modal="true" and proper focus management
**Actual Result:** Missing aria-modal attribute, focus not trapped in modal
**Evidence:** `tests/evidence/modal-a11y-issues.png`

### TC-A11Y-004: Image Alt Text Missing Bug
**Priority:** P2 - Medium
**Test Type:** Manual
**Pre-conditions:** User is on product catalog page
**Steps:**
1. Navigate to any product listing page
2. Right-click on product image and "Inspect Element"
3. Check alt attribute on img elements
**Expected Result:** All product images should have descriptive alt text
**Actual Result:** Alt attribute is empty or contains generic text like "product image"
**Evidence:** `tests/evidence/missing-alt-text.png`