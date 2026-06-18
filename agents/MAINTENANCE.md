# Maintenance & Change Management Guide

## 1. Introduction
Changes to safety-critical systems must be handled with extreme care to avoid introducing new hazards or regressions.

## 2. Goal
1. Perform Impact Analysis for every change request.
2. Update all affected artifacts.
3. Re-verify the system.

## 3. Workflow

### 3.1. Impact Analysis
- Identify which requirements, design elements, code units, and tests are affected by the proposed change.
- Evaluate if the change impacts the HARA or Safety Goals.
- **Artifact:** `Impact_Analysis_Report.md`

### 3.2. Controlled Implementation
- Follow the Design -> Planning -> Development flow for the scope of the change.

### 3.3. Regression Testing
- Execute all relevant tests (even those not directly touched) to ensure no side effects.
- **Artifact:** `Regression_Test_Report.md`

## 4. Mandates
- **No "Quick Fixes":** Every change, no matter how small, requires an Impact Analysis.
- **Traceability Maintenance:** The Traceability Matrix must be updated to reflect the new state of the system.

## 5. Completion Criteria
- Updated Safety Case reflecting the changes.
- Successful regression testing.
