# Planning Phase Guide - Safety-Critical Edition

## 1. Introduction
Planning for safety involves defining the exact steps to implement and verify each safety requirement.

## 2. Goal
1. Decompose the architecture into Software Units.
2. Define the Development Plan and Verification Plan.
3. Establish the "Definition of Done" (DoD) for each unit, including safety metrics.

## 3. Workflow

### 3.1. Unit Decomposition & Safety Mapping Loop
1. **Initial Decomposition:** The agent proposes a breakdown of the TSC into software units.
2. **Safety Allocation:** For each unit, the agent asks the user if it should be "safety-related" or "non-safety-related."
3. **Traceability Check:** The agent maps each TSR to at least one unit and updates the `Traceability_Matrix.md`.

### 3.2. Development Plan Elicitation
1. **Critical Path Identification:** The agent identifies the most safety-critical units (highest ASIL/SIL) and proposes they be implemented first.
2. **Drafting:** The agent creates the `Development_Plan.md`.

### 3.3. Verification Planning Loop
1. **Method Selection:** The agent proposes verification methods (e.g., "Requirement-based testing," "Boundary value analysis") based on the target safety level.
2. **Environment Elicitation:** The agent asks the user about the available test infrastructure (HIL, SIL, or target hardware).
3. **Drafting:** The agent creates the `Verification_Plan.md`.

### 3.4. Checklist Creation
- Create a step-by-step checklist for the Development Phase.
- Each item must include the required evidence (e.g., "Unit test report with 100% branch coverage").

## 4. Mandates
- **Traceability:** Every task in the plan must trace back to a requirement in the Architecture Specification.
- **Evidence-Based:** Every task must have a defined artifact that proves its completion.

## 5. Completion Criteria
- Approved Development Plan and Verification Plan.
- Development Checklist committed to the repository.
