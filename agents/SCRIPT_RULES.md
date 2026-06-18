# SCRIPT_RULES.md - Safety-Critical Execution

## 1. Command Verification
- Every command must be checked for success.
- If a command fails, the agent MUST stop and analyze the error before proceeding.
- Output from safety-critical tools (e.g., coverage reports) must be captured and summarized.

## 2. Hermetic Environment
- All builds must be reproducible.
- Use lockfiles (`Cargo.lock`, `package-lock.json`) to ensure dependency stability.

## 3. Evidence Collection
- Scripts that run tests must output results in a machine-readable format (e.g., JUnit XML) to be processed into safety reports.
