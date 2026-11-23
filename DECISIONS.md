# Decision Log

Dates use ISO 8601 (`YYYY-MM-DD`). These decisions were recorded for M0 on 2026-11-23.

| ID | Decision | Reason | Date | Status |
|---|---|---|---|---|
| D001 | The project uses a multi-Brain architecture. | Separate research, development, QA, and project authority. | 2026-11-23 | Active |
| D002 | STUDENT-MAIN Brain is the overall project manager. | Keep roadmap, authorization, and milestone authority centralized. | 2026-11-23 | Active |
| D003 | Each Brain independently manages its own Worker. | Preserve each Brain's control over its execution. | 2026-11-23 | Active |
| D004 | MAIN Brain cannot directly control other Brain Workers. | Work is dispatched through the responsible Brain. | 2026-11-23 | Active |
| D005 | The project follows sequential M0–M5 milestones. | Establish ordered gates from governance through delivery. | 2026-11-23 | Active |
| D006 | M1 uses six local synthetic CSV files for delegation and verification practice. | Practice evidence-based research workflow before real-data work. | 2026-11-23 | Active |
| D007 | The final product uses real NASA C-MAPSS FD001 data. | Ground the engine health analysis in the specified source dataset. | 2026-11-23 | Active |
| D008 | Original datasets are read-only by default. | Protect source data integrity. | 2026-11-23 | Active |
| D009 | GitHub `main` is the canonical governance baseline. | Provide one remotely reviewable source of truth. | 2026-11-23 | Active |
| D010 | Every task requires evidence-based acceptance. | Ensure completion claims can be independently checked. | 2026-11-23 | Active |
| D011 | No subsequent Worker starts without previous Brain acceptance and MAIN authorization. | Enforce milestone gates and project authority. | 2026-11-23 | Active |
| D012 | Failure to access GitHub or verify remote results must be reported as BLOCKED. | Avoid claiming a remote result that cannot be confirmed. | 2026-11-23 | Active |
| D013 | File modification authority is scoped to the active Work Order: explicitly authorized project-owned code and documentation may be changed within scope, while Protected User Data remains protected unless the owner explicitly authorizes the exact change. | Enable authorized Development work without weakening safeguards for original datasets, user files, credentials, or out-of-scope code. | 2026-11-23 | Active |
