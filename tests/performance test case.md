Performance testing ... ### TC-PERF-001: Page Load Performance
**Priority:** P2 - Medium
**Test Type:** Manual
**Pre-conditions:** Clear browser cache, stable network
**Steps:**
1. Open browser DevTools
2. Navigate to homepage
3. Record page load time
4. Run Lighthouse performance audit
5. Note Core Web Vitals scores
**Expected Result:** Page loads within 3 seconds, Performance score ≥ 80
**Evidence:** `tests/evidence/lighthouse-performance.png`

### TC-PERF-002: Layout Shift (CLS) Measurement
**Priority:** P2 - Medium
**Test Type:** Manual
**Pre-conditions:** Network throttled to "Slow 3G"
**Steps:**
1. Open browser DevTools and go to Performance tab
2. Throttle network to "Slow 3G"
3. Navigate to homepage
4. Scroll down and observe image loading behavior
**Expected Result:** Images should load with reserved space to prevent layout shifts
**Actual Result:** Content jumps significantly as images load (Cumulative Layout Shift > 0.25)
**Evidence:** `tests/evidence/layout-shift-issue.png`