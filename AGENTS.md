# AGENTS.md - Core Mandates for Safety-Critical Development

## 1. Introduction
This document defines the core mandates and operational protocols for the AI agent. In safety-critical development, adherence to process is as important as the code itself.

## 2. Core Mandates

### 2.1. The Safety Mandate
**THE SAFETY OF THE SYSTEM IS THE HIGHEST PRIORITY.**
- The agent must never propose a design or implementation that bypasses defined safety requirements.
- Any potential safety hazard identified during development must be immediately reported to the user.

### 2.2. Mandate for Traceability
**BIDIRECTIONAL TRACEABILITY IS NON-NEGOTIABLE.**
- Every requirement must have a unique ID.
- Every architectural component must trace to a requirement.
- Every unit of code must trace to a design element and requirement.
- Every test case must trace to a requirement.
- The agent must maintain a `Traceability Matrix` artifact throughout the lifecycle.

### 2.3. Mandate for Artifact Integrity
**IF IT ISN'T DOCUMENTED, IT ISN'T DONE.**
- The agent must generate and update all artifacts defined in the `Safety Plan`.
- Artifacts must be stored in a structured format (Markdown/PDF/JSON) as specified.
- No phase can be closed until its required artifacts are verified and committed.

### 2.4. Mandate for Verification Evidence
**CLAIMS OF COMPLETION REQUIRE OBJECTIVE EVIDENCE.**
- The agent must provide logs, screenshots, or tool outputs for every verification activity.
- For software units, structural coverage (Statement, Branch, and where required, MC/DC) must be reported.

### 2.5. Filesystem & Workflow Integrity
- **Additive-Only:** Operations should be additive. Deletions or overwrites require explicit "APPROVED" status.
- **Strict Workflow:** Follow the phase guides in `agents/` sequentially.
- **No Stubs:** Implementation must be complete and robust. Stubbing out safety-critical logic is a violation of this mandate.

## 3. Operational Protocol

### 3.0. Session Bootstrap: Concept Intake
Every new session starts with the agent eliciting the **Project Concept**.
1. The agent MUST ask: "What is the core function of the system we are building, and what is its intended operational environment?"
2. The agent MUST then ask: "Are there any known safety constraints or regulatory requirements (e.g., ISO 26262, IEC 61508) we must adhere to?"
3. Based on the responses, the agent MUST propose the initial entry point (usually `SAFETY_MANAGEMENT.md`).

### 3.1. Phase Transitions
The agent must request explicit approval to move from one phase to the next (e.g., "Design Phase is complete. Requesting approval to move to Planning Phase").

### 3.2. Change Management
Any change to an approved artifact (Requirement, Design, Code) requires an **Impact Analysis** to identify which other artifacts and tests need to be updated.

## 4. Preferred Stack
- **Language:** Rust (preferred for memory safety) or C/C++ (with MISRA/AUTOSAR checks).
- **Documentation:** Markdown for traceability and easy versioning.
- **Verification:** Unit testing frameworks, property-based testing, and coverage tools.
