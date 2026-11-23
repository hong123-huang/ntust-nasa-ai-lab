# NTUST NASA AI Lab Governance

## Project identity and objective

- **Project ID:** `NTUST_NASA_AI_LAB`
- **Objective:** Build a local NASA C-MAPSS FD001 Engine Health Analysis Website.
- **Required product capabilities:** Engine Unit selector; Cycle selector; Sensor selector; actual source and trend display; health analysis based on verified real data; Evidence Prompt generation.

## Brain responsibilities

- **STUDENT-MAIN BRAIN:** Overall project management; roadmap and Work Order authorization; acceptance criteria; cross-Brain coordination; MAIN Brain direction; final milestone approval.
- **RESEARCH BRAIN:** Dataset research, inventory, profiling, statistical verification, research methodology, and management of Research Workers.
- **DEVELOPMENT BRAIN:** Software architecture, data-processing implementation, backend and frontend, website integration, and management of Development Workers.
- **QA BRAIN:** Testing, data-consistency verification, functional validation, regression testing, and management of QA Workers.

Each Brain independently controls its own Worker; Workers may be Codex or Claude as selected by that Brain. A Work Order is issued to a Brain, not directly to another Brain's Worker. MAIN Brain must not directly control another Brain's Own Worker.

## Work Order authority and scope

- A Worker may execute only the tasks and file changes explicitly authorized in the active Work Order. The Worker must not infer permission, add tasks, or expand the scope.
- Every Work Order must identify its objective, authorized files or deliverables, responsible Brain, measurable acceptance criteria, and STOP conditions before execution.
- Before starting a Work Order, the responsible Brain must read the latest `AGENTS.md` from GitHub `main`; the Worker follows that version. If it cannot be accessed, report `BLOCKED` and do not begin.
- Record work item states distinctly: created, authorized, executed, returned, reviewed, and accepted. Do not mark a later state before it actually occurs.

## File ownership, protection, and modification

### Protected User Data

The following are protected from unauthorized modification, deletion, replacement, or publication:

- Original NASA datasets and other original research data.
- Synthetic CSV datasets and other user-provided datasets.
- User's existing data and documents.
- User's existing code that is outside this project's explicitly authorized scope.
- Credentials, secrets, API keys, tokens, and private personal information.

Do not modify, delete, overwrite, or publish Protected User Data unless the project owner explicitly authorizes the exact action and the active Work Order names the affected files and scope. Credentials and secrets must never be committed or pushed. Do not include private information in public repository content.

### Authorized Project-owned Files

Code and documentation created by a project Worker under an authorized Work Order, and existing project-owned files explicitly listed for modification in that Work Order, may be created or changed within that Work Order's scope. This rule permits authorized Development work on project-owned application code; it does not make original datasets, synthetic datasets, or unrelated user files writable.

Before editing, inspect the target and preserve uncommitted user changes. If ownership or authorization is unclear, stop and ask the responsible Brain; do not overwrite.

## Evidence, review, and milestone acceptance

- No task may be declared complete without actual evidence tied to its acceptance criteria. Do not invent file presence, data reads, execution results, test results, or remote state.
- Worker completion or return does not equal responsible Brain review or acceptance.
- Responsible Brain acceptance does not equal MAIN Brain acceptance or final milestone approval.
- Only STUDENT-MAIN Brain may record the final milestone decision.
- Do not enter or dispatch work for the next milestone until the previous work has been accepted by its responsible Brain, reviewed by MAIN Brain, and explicitly authorized by STUDENT-MAIN Brain.
- Follow M0 → M1 → M2 → M3 → M4 → M5 in `ROADMAP.md`; do not skip gates.

## Git and GitHub governance

- Use the single `main` branch and sequential development. No unauthorized branches, parallel implementation, repository recreation, or history rewriting.
- Preserve existing Git history. Never run `git push --force` (including force-with-lease).
- Stage only files explicitly authorized by the active Work Order and reviewed in the diff. Never use `git add .` or another broad staging command without first inspecting and approving every included path.
- Before committing, inspect `git status`, the full staged path list, and `git diff --cached`; ensure no protected, sensitive, or out-of-scope file is staged.
- Every authorized Work Order must be committed and pushed to GitHub `main` unless a STOP condition prevents it. Report actual commit ID, push result, and any blocker.
- After pushing, the responsible Brain must independently read the remote result and compare it with the intended commit. No remote PASS without this evidence.
- Never publish credentials, secrets, private information, or Protected User Data without explicit project-owner authorization for that exact publication.

## Final authority

The Worker returns evidence and unresolved issues to its responsible Brain. The responsible Brain reviews and reports to MAIN Brain. MAIN Brain coordinates the review and returns the result to STUDENT-MAIN Brain. Only STUDENT-MAIN Brain may approve the next milestone or declare final milestone acceptance.
