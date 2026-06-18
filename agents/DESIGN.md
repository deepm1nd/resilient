# Design Phase Guide - Safety-Critical Edition

## 1. Introduction
The Design Phase in safety-critical development is where the foundation for safety is laid. This phase translates a concept into a Technical Safety Concept (TSC) and Architecture Specification.

## 2. Goal
1. Perform Hazard Analysis and Risk Assessment (HARA) or equivalent.
2. Define the Functional Safety Concept (FSC).
3. Establish the Technical Safety Concept (TSC).
4. Create a traceable Architecture Specification.

## 3. Workflow

### 3.1. Hazard Analysis (HARA) Elaboration Loop
1. **Scenario Identification:** The agent asks the user to describe typical use cases and potential "misuse" scenarios.
2. **Hazard Brainstorming:** Based on user input, the agent proposes a list of hazards (e.g., "Brake failure during cornering").
3. **Risk Scoring:** For each hazard, the agent guides the user through scoring Severity, Exposure, and Controllability.
4. **Drafting:** The agent generates the `HARA_Report.md`.

### 3.2. Safety Goal & FSR Elicitation Loop
1. **Goal Derivation:** The agent proposes Safety Goals for each high-risk hazard (e.g., "The system shall maintain vehicle stability during brake component failure").
2. **FSR Breakdown:** The agent asks the user for functional constraints and then proposes Functional Safety Requirements (FSRs).
3. **Drafting:** The agent creates the `Functional_Safety_Concept.md`.

### 3.3. Technical Safety Concept (TSC) Refinement Loop
1. **Mechanism Proposal:** The agent proposes specific technical mechanisms (e.g., "Redundant sensor processing," "Watchdog timer") to meet FSRs.
2. **HSI Elicitation:** The agent asks the user for hardware-specific details (I/O, memory constraints, communication protocols).
3. **Architecture Drafting:** The agent creates the `Architecture_Specification.md` (incorporating the TSC).
4. **Traceability Initialization:** The agent creates the `Traceability_Matrix.md`, mapping Goals -> FSRs -> TSRs.

### 3.4. Iterative Review
The agent MUST present each document to the user and ask: "Does this accurately reflect the safety constraints and technical architecture of the system?" before proceeding.

## 4. Mandates
- **Safety Goals First:** All architectural decisions must be justified by safety goals.
- **Independence:** (For high ASIL/SIL) Ensure independence between safety-critical and non-safety-critical components (ASIL decomposition/freedom from interference).
- **No Ambiguity:** Requirements must have clear pass/fail criteria.

## 5. Completion Criteria
- Approved HARA, FSC, TSC, and Architecture Specification.
- Traceability Matrix initialized and mapping Safety Goals to TSRs.
