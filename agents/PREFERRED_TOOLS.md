# PREFERRED_TOOLS.md - Safety-Critical Tooling

## 1. Static Analysis
- **Rust:** `clippy` (configured for strictness), `cargo-deny`, `cargo-audit`.
- **C/C++:** `Cppcheck` (with MISRA addon), `Clang-Tidy`.

## 2. Testing and Coverage
- **Unit Testing:** `cargo test` (Rust), `Google Test` (C++).
- **Coverage:** `llvm-cov`, `grcov`.
- **Property-Based Testing:** `proptest` (Rust).
- **Fault Injection:** Custom scripts or `fail-rs` (Rust).

## 3. Traceability
- **Tool:** Markdown-based traceability matrix or dedicated tools like `Doorstop`.

## 4. Documentation
- **Format:** Markdown for all safety artifacts.
- **Diagrams:** Mermaid.js (inlined in Markdown).
