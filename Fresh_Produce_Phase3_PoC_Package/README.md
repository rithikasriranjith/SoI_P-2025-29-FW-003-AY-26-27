# Direct Local Fresh Produce Exchange and Community Delivery Platform

## Project details
- Team: THE TITANS
- Team ID: P-2025-29-FW-003
- Primary vertical: FW — Full Stack Web
- Submission component: Phase 3 Proof of Concept (PoC)
- Test data: fictional/synthetic data only

## What is included
- `prototype/index.html`: a local browser-based mock prototype with fictional orders, role selection, status actions, a timer, and an in-browser test runner.
- `templates/status_test_cases.csv`: seven predefined order-status scenarios.
- `templates/permission_test_cases.csv`: unauthorized role-action checks.
- `templates/timing_results.csv`: blank timing data collection template.
- `evidence/logs/`: places to save actual test logs and calculations.
- `evidence/screenshots/`: place actual screenshots here.
- `evidence/demo/`: place the actual MP4 demo (maximum two minutes) here.
- `SoI_P3_Presentation.pptx`: current Phase 3 presentation supplied with this package.

## How to run the prototype
1. Extract the ZIP file.
2. Open `prototype/index.html` in a modern browser (Chrome, Edge, or Firefox). No installation or server is required for this mock prototype.
3. Choose a role from the role selector.
4. Select an order and use only actions allowed for that role.
5. Use **Run 7 status checks** to run the scripted demonstration checks.
6. Use the timer controls to record elapsed time for a task. Record a separate manual/shared-sheet comparison using the same task and start/end definitions.
7. Save screenshots and enter actual observations in the CSV templates.

## Important implementation limitation
This is a self-contained front-end demonstration. It stores order changes only in the current browser page and does not provide a server, database, authentication, or server-side authorization. Browser-side role restrictions are for demonstration only and are not production security. Reloading the page resets the mock orders. Do not use real customer data, live orders, payments, or location data.

## Original P2 criteria
1. All 7 planned test orders should be coordinated correctly (7/7).
2. At least 5 out of 5 assessed orders should be accurate (5/5).
3. Reduce coordination time compared with the manual/shared-sheet workflow.

## Phase 3 test targets
- Seven predefined status cases produce the expected result (7/7).
- Zero unauthorized edits accepted in the defined role-permission tests.
- Median prototype update time is 60 seconds or less.

Keep original P2 thresholds distinct from Phase 3 targets. Document any change, reason, approval/review status, and date before testing. Do not copy Phase 3 criteria over the original P2 criteria.

## Test protocol
For every case, record the date, prototype version, test ID, role, initial status, action, expected result, observed result, pass/fail/inconclusive, and evidence filename. Use the same comparable tasks and start/end definitions for prototype and manual/shared-sheet timing. Keep raw results, failures, and retests; do not erase initial failures.

### Status tests
- T1: Farmer confirms a retail order → Confirmed.
- T2: Farmer marks an order ready for pickup → Ready for Pickup.
- T3: Farmer confirms a wholesale order → Confirmed.
- T4: Delivery participant starts delivery → Out for Delivery.
- T5: Delivery participant completes delivery → Delivered.
- T6: Customer attempts to confirm → status unchanged.
- T7: Customer attempts to mark delivered → status unchanged.

### Permission tests
Use `templates/permission_test_cases.csv`. An unauthorized edit is accepted only if the restricted status change actually takes effect. Target: zero accepted unauthorized edits across the tested attempts.

### Timing test
Start the timer when the defined update task begins and stop it when the correct updated status is visibly confirmed. Record seconds for each comparable task. Compare the prototype median with the manual/shared-sheet median. The 60-second threshold is a Phase 3 target; the original P2 effort criterion is comparative reduction versus manual workflow.

## Stop rule
Stop testing if personal/sensitive data is exposed, a restricted role action succeeds, or a real order/payment/live location is accidentally used. Preserve the evidence, record the incident, and fix the issue before continuing.

## Evidence and demo
- Put actual screenshots in `evidence/screenshots/`.
- Put actual logs and calculations in `evidence/logs/`.
- Record a real demonstration video no longer than two minutes and put it in `evidence/demo/`.
- Suggested demo sequence: open prototype, show mock orders, perform an allowed update, attempt a restricted action, and show the observed result.

No test outcomes are pre-filled as passed. The test runner in the prototype is a scripted demonstration aid; independently execute and document the checks and preserve actual screenshots/logs before reporting final results.

## Current status checklist
- Prototype file: included (front-end mock only).
- Seven status checks: run and record actual evidence.
- Permission tests: run and record actual evidence.
- Timing comparison: collect actual measurements.
- Screenshots/logs: collect after testing.
- MP4 demo: record and add; not included unless you add your actual recording.
- Production readiness: not established by this PoC.
