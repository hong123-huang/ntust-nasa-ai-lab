# NTUST NASA AI Lab Governance

## Project identity and objective

- **Project ID:** `NTUST_NASA_AI_LAB`
- **Objective:** Build a local NASA C-MAPSS FD001 Engine Health Analysis Website.

## Final product requirements

The website must provide Engine Unit, Cycle, and Sensor selection; real source traceability; sensor trend visualization; engine health analysis; and Evidence Prompt generation.

## Brain responsibilities

- **STUDENT-MAIN BRAIN:** Overall project management, roadmap management, Work Order authorization, acceptance criteria, cross-Brain coordination, and final milestone approval.
- **RESEARCH BRAIN:** Dataset research, data profiling, statistical verification, research methodology, and management of Research Workers.
- **DEVELOPMENT BRAIN:** Software architecture, data-processing implementation, backend and frontend, website integration, and management of Development Workers.
- **QA BRAIN:** Testing, data-consistency verification, functional validation, regression testing, and management of QA Workers.

## Authority and dispatch

- Each Brain independently controls its own Worker. Workers may include Codex or Claude, chosen by the responsible Brain.
- A Work Order is issued to a Brain, never directly to another Brain's Worker.
- The MAIN Brain must not directly control another Brain's Worker.
- Worker completion is not Brain acceptance. The responsible Brain inspects the actual result, and the MAIN Brain authorizes the next task.
- No task is complete without actual evidence. No PASS may be declared without evidence-based review.

## Protected data

Original datasets, including NASA C-MAPSS data, synthetic CSV datasets, research data, source code, user documents, configurations, credentials, secrets, and environment files are read-only/protected by default. Do not modify or publish them without explicit authorization. Never publish credentials or private information.

## Git governance

- Use the single `main` branch and sequential development. Do not create unauthorized branches or perform unauthorized parallel implementation.
- Every accepted task requires a Git commit. Every authorized task must be pushed to GitHub `main`.
- Never force-push or rewrite existing history. Preserve existing repository history.
- Stage only reviewed, explicitly authorized files; never use `git add .` without first inspecting the full staging scope.
- The responsible Brain must independently inspect the actual GitHub remote result. No PASS without remote evidence and acceptance.
- Do not push sensitive files or private datasets without explicit authorization.

## Mandatory pre-work and acceptance

Before dispatching every new Work Order, the responsible Brain must read the latest `AGENTS.md` from GitHub `main`; the Worker must follow that version. If the latest file cannot be accessed, status is BLOCKED. A subsequent task cannot start until its previous task has been accepted by its responsible Brain and the MAIN Brain has authorized the next task.

## Milestone gate

Follow M0 → M1 → M2 → M3 → M4 → M5 as defined in `ROADMAP.md`. Do not skip a milestone. Each gate requires prior Brain acceptance and MAIN Brain authorization.
