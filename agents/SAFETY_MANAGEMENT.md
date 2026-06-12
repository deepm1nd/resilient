# Safety Management Guide

## 1. Introduction
Safety Management ensures that the organizational and project-specific processes are in place to achieve functional safety as per ISO 26262 and IEC 61508.

## 2. Goal
1. Define the project Safety Plan.
2. Establish Safety Integrity Levels (ASIL/SIL).
3. Perform Tool Qualification.
4. Establish the Safety Culture and Competence.

## 3. Workflow

### 3.1. Project Initialization & Context Intake
1. **Context Gathering:** The agent MUST ask the user about the project's target industry (Automotive vs. Industrial), intended function, and operational environment.
2. **Standard Selection:** Based on the context, the agent proposes the applicable standard (ISO 26262 or IEC 61508) and awaits confirmation.

### 3.2. Safety Integrity Level (ASIL/SIL) Elicitation Loop
1. **Impact Analysis:** The agent asks the user about the potential consequences of system failure (e.g., "What happens if this component fails while the vehicle is at high speed?").
2. **Target Proposal:** The agent proposes a target ASIL (A-D) or SIL (1-4) based on the user's responses and the standard's criteria.
3. **Refinement:** The agent and user iterate until the safety level is agreed upon.

### 3.3. Safety Plan Elaboration Loop
1. **Role Assignment:** The agent asks the user who will fulfill the roles of Safety Manager and Independent Verifier (if required by the safety level).
2. **Lifecycle Tailoring:** The agent proposes a tailored version of the safety lifecycle (e.g., which optional artifacts to include) based on the agreed safety level.
3. **Drafting:** The agent creates the first draft of the `Safety_Plan.md` using the template.
4. **Approval:** The agent presents the plan and awaits explicit approval.

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
