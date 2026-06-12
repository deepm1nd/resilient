# Design Phase Guide - Safety-Critical Edition

## 1. Introduction
The Design Phase in safety-critical development is where the foundation for safety is laid. This phase translates a concept into a Technical Safety Concept (TSC) and Architecture Specification.

## 2. Goal
1. Perform Hazard Analysis and Risk Assessment (HARA) or equivalent.
2. Define the Functional Safety Concept (FSC).
3. Establish the Technical Safety Concept (TSC).
4. Create a traceable Architecture Specification.

## 3. Workflow

### 3.1. Hazard Analysis & Risk Assessment (HARA)
- Identify potential hazards associated with the system.
- Assess risks based on Severity, Exposure, and Controllability (ISO 26262) or SIL levels (IEC 61508).
- Assign ASIL (Automotive Safety Integrity Level) or SIL (Safety Integrity Level) to requirements.
- **Artifact:** `HARA_Report.md`

### 3.2. Functional Safety Concept (FSC)
- Define safety goals to mitigate identified hazards.
- Specify functional safety requirements (FSRs).
- **Artifact:** `Functional_Safety_Concept.md`

### 3.3. Technical Safety Concept (TSC) & Architecture
- Translate FSRs into Technical Safety Requirements (TSRs).
- Define the system architecture, including hardware-software interface (HSI).
- Specify safety mechanisms (e.g., watchdogs, CRC checks, memory protection).
- **Artifact:** `Architecture_Specification.md`

### 3.4. Requirements Elicitation & Traceability
- Ensure every requirement is Atomic, Unambiguous, and Verifiable.
- Initialize the **Traceability Matrix**.
- **Artifact:** `Traceability_Matrix.md`

## 4. Mandates
- **Safety Goals First:** All architectural decisions must be justified by safety goals.
- **Independence:** (For high ASIL/SIL) Ensure independence between safety-critical and non-safety-critical components (ASIL decomposition/freedom from interference).
- **No Ambiguity:** Requirements must have clear pass/fail criteria.

## 5. Completion Criteria
- Approved HARA, FSC, TSC, and Architecture Specification.
- Traceability Matrix initialized and mapping Safety Goals to TSRs.
