# Safety Management Guide

## 1. Introduction
Safety Management ensures that the organizational and project-specific processes are in place to achieve functional safety as per ISO 26262 and IEC 61508.

## 2. Goal
1. Define the project Safety Plan.
2. Establish Safety Integrity Levels (ASIL/SIL).
3. Perform Tool Qualification.
4. Establish the Safety Culture and Competence.

## 3. Workflow

### 3.1. Safety Plan Development
- Define the safety lifecycle for the specific project.
- Assign roles and responsibilities (e.g., Safety Manager, Developer, Tester).
- Define the "Safety Case" strategy.
- **Artifact:** `Safety_Plan.md`

### 3.2. Safety Integrity Level (ASIL/SIL) Assignment
- Based on the system's intended use and potential impact, determine the target safety level.
- **ISO 26262:** ASIL A, B, C, or D.
- **IEC 61508:** SIL 1, 2, 3, or 4.
- This level dictates the rigor of the methods and measures required in subsequent phases.

### 3.3. Tool Qualification
- Evaluate all software tools used in the development and verification process (e.g., compilers, static analyzers, test runners).
- Assess the Tool Confidence Level (TCL).
- Perform qualification for tools where failure could lead to an undetected safety hazard.
- **Artifact:** `Tool_Qualification_Report.md`

### 3.4. Process Definition
- Define the configuration management, change management, and documentation management processes.

## 4. Mandates
- **Independence:** (For high ASIL/SIL) The person performing verification must be independent from the person who developed the code.
- **Qualification:** No tool can be used for safety-critical work unless it is qualified or justified.

## 5. Completion Criteria
- Approved Safety Plan.
- Initial Tool Qualification Report.
- Safety Lifecycle defined and tailored for the project.
