# Release & Safety Case Guide

## 1. Introduction
The Release Phase in safety-critical projects culminates in the creation of the **Safety Case**, which argues that the system is safe for its intended use.

## 2. Goal
1. Finalize all safety artifacts.
2. Compile the Safety Case.
3. Perform a final Safety Audit.
4. Release the software and its documentation.

## 3. Workflow

### 3.1. Artifact Consolidation
- Ensure all reports (HARA, TSC, Test Reports, Traceability Matrix) are up-to-date and consistent.

### 3.2. The Safety Case
- Provide a structured argument (e.g., Goal Structuring Notation - GSN) showing how safety goals have been met.
- Reference the evidence (artifacts) for each claim.
- **Artifact:** `Safety_Case.md`

### 3.3. Safety Manual / Release Notes
- Document instructions for the end-user or integrator to maintain safety.
- Specify any assumptions or constraints (e.g., specific hardware versions).
- **Artifact:** `Safety_Manual.md`

### 3.4. Final Release
- Package the binary, source (if required), and the full artifact set.

## 4. Mandates
- **Completeness:** No release without a complete Safety Case.
- **Auditability:** Every claim in the Safety Case must point to a specific, committed artifact.

## 5. Completion Criteria
- Safety Case approved by the user (acting as safety assessor).
- Final release package committed or deployed.
