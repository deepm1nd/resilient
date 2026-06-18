# Safety-Marrow: ISO 26262 & IEC 61508 Compliant Agent Instructions

This repository defines a rigorous, safety-critical software development lifecycle (SDLC) for an AI engineering agent. It is based on the [Marrow](https://github.com/deepm1nd/marrow) framework, enhanced to ensure full compliance with **ISO 26262** (Automotive) and **IEC 61508** (Industrial) functional safety standards.

## Overview

Safety-critical development requires more than just high-quality code; it requires a documented, verifiable, and traceable process. This repository provides the "marrow" for such a process, enabling an agent to generate all required safety artifacts alongside the application code.

## Structure of Development Phases

The agent's workflow follows a V-Model inspired lifecycle, with each phase producing specific safety artifacts:

1.  **Safety Management (`SAFETY_MANAGEMENT.md`):** Establishing the Safety Plan, ASIL/SIL targets, and tool qualification.
2.  **Concept & Design Phase (`DESIGN.md`):** Performing HARA (Hazard Analysis and Risk Assessment) and defining the Functional and Technical Safety Concepts.
3.  **Planning Phase (`PLANNING.md`):** Creating a detailed Development Plan with strict traceability between requirements and tests.
4.  **Development Phase (`DEVELOPMENT.md`):** Implementing code following safety-critical standards (e.g., MISRA/AUTOSAR for C/C++, or high-assurance Rust) with rigorous unit testing.
5.  **Verification & Validation (`VERIFICATION.md`):** Executing integration and system tests, including fault injection and structural coverage analysis (MC/DC).
6.  **Release & Safety Case (`RELEASE.md`):** Compiling the final Safety Case and Release Documentation.
7.  **Maintenance (`MAINTENANCE.md`):** Managing changes through a controlled Impact Analysis and regression testing.

## Key Controls & Core Mandates

*   **Safety First:** No feature implementation is complete without its corresponding safety verification.
*   **Bidirectional Traceability:** Every line of code must be traceable to a requirement, and every requirement to a test.
*   **Artifact Completeness:** The agent is forbidden from skipping any required artifact defined in the Safety Plan.
*   **Verification Rigor:** "Passed" is only accepted when accompanied by objective evidence (logs, coverage reports, etc.).
*   **Rust for Safety:** While other languages are supported if required by the target environment, Rust is the preferred language for its memory safety guarantees, which significantly aid in IEC 61508/ISO 26262 compliance.

## Getting Started

1.  Read `AGENTS.md` to understand the core mandates.
2.  The agent must begin by initializing the project's **Safety Plan**.
3.  Follow the phases sequentially as defined in the `agents/` directory.
