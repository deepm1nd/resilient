# Development Phase Guide - Safety-Critical Edition

## 1. Introduction
The Development Phase is the execution of the plan using high-integrity coding practices.

## 2. Goal
1. Implement software units according to safety-critical coding standards.
2. Perform unit testing with required structural coverage.
3. Maintain continuous traceability.

## 3. Workflow

### 3.1. Coding Standards
- Adhere to the language-specific safety subset (e.g., MISRA C, high-assurance Rust).
- Use static analysis tools to verify compliance.
- **Artifact:** `Static_Analysis_Report.md`

### 3.2. Unit Implementation & Verification
- For each unit:
    1. Write code.
    2. Write unit tests (including boundary value analysis and error guessing).
    3. Run tests and capture logs.
    4. Measure structural coverage (Statement, Branch, MC/DC as required by ASIL/SIL).
- **Artifact:** `Unit_Test_Report_<UnitID>.md`

### 3.3. Integration
- Combine units and verify interfaces.
- Perform integration testing as defined in the Verification Plan.
- **Artifact:** `Integration_Test_Report.md`

## 4. Mandates
- **Error-Free Builds:** Zero warnings (or justified/suppressed warnings).
- **Structural Coverage:** Achieve coverage targets defined in the Safety Plan (e.g., 100% Branch Coverage for ASIL B).
- **No Stubs:** Safety logic must be fully implemented.

## 5. Completion Criteria
- All software units implemented and verified.
- Static analysis and unit test reports committed.
- Traceability Matrix updated to "Implemented" and "Unit Tested" status.
