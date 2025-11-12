Admin and route management....### TC-ADMIN-001: Admin Route Access Without Role
**Priority:** P1 - High
**Test Type:** Manual
**Pre-conditions:** User is not logged in as admin
**Steps:**
1. Navigate to /admin route directly
2. Observe application behavior
**Expected Result:** "Unauthorized" message displayed, access denied
**Evidence:** `tests/evidence/admin-unauthorized.png`

### TC-ADMIN-002: Admin Route Access With Admin Role
**Priority:** P1 - High
**Test Type:** Manual
**Pre-conditions:** User sets admin role in localStorage
**Steps:**
1. Open browser console
2. Execute: `localStorage.setItem('app.user', JSON.stringify({ role: 'admin' }))`
3. Navigate to /admin route
4. Refresh page and verify access persists
**Expected Result:** Admin console loads successfully
**Evidence:** `tests/evidence/admin-authorized.png`

### TC-ROUTE-001: Route Redirection Logic
**Priority:** P1 - High
**Test Type:** Manual
**Pre-conditions:** User accesses application root
**Steps:**
1. Navigate to `/`
2. Observe automatic redirection
3. Verify current URL changes to `/catalog`
**Expected Result:** Root path redirects to catalog page
**Evidence:** `tests/evidence/root-redirect.png`