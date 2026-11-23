# NTUST NASA AI Lab Roadmap

**Project ID:** `NTUST_NASA_AI_LAB`
**Project objective:** Build a local NASA C-MAPSS FD001 Engine Health Analysis Website with Engine Unit, Cycle, and Sensor selectors; traceable source values and trends; health analysis based on real data; and Evidence Prompt generation.

All inputs below are requirements or expected sources unless expressly identified as locally verified. No milestone may assume that a file exists or has been read until its responsible Brain records actual inventory and verification evidence.

## M0 — Project Governance and Environment

1. **Objective:** Establish project governance, Brain authority, sequential milestone gates, Git workflow, and the project documentation baseline.
2. **Input:** Student-MAIN authorized Work Order; existing project directory and GitHub `main` state, which must be inspected before changes.
3. **Deliverables:** `AGENTS.md`, `ROADMAP.md`, `WORK_ITEM.md`, and `DECISIONS.md`; verified Git history and remote publication evidence for authorized changes.
4. **Responsible Brain:** STUDENT-MAIN Brain for authorization and final milestone decision; MAIN Brain manages the work item and review.
5. **Collaborating Brains:** None required for the governance baseline; Research, Development, and QA Brains follow the accepted governance in their own work.
6. **Acceptance Criteria:** All four governance files exist and are internally consistent; M0 changes are committed and pushed to the canonical `main`; the responsible Brain independently reads back and verifies the remote files; STUDENT-MAIN records the final M0 decision.
7. **STOP_IF Conditions:** Project root or repository is uncertain; existing user changes would be overwritten; scope includes protected data; credentials or private data might be published; repository ownership, push, or remote verification cannot be confirmed; or any required governance file is incomplete.
8. **Next Role / Next Milestone:** After M0 acceptance and explicit STUDENT-MAIN authorization, dispatch a Work Order to RESEARCH BRAIN for M1. No M1 Worker starts before both gates.

## M1 — Synthetic Dataset Profiles

1. **Objective:** Practice Brain-to-Brain delegation and evidence-based data profiling using six local synthetic CSV datasets.
2. **Input:** Six synthetic CSV files that the Research Brain must locate and inventory. The initial project inventory observed `synthetic_sensor.csv`; this does not establish the presence, identity, or validity of the other five files, nor that any file has been profiled. Verify all inputs before analysis.
3. **Deliverables:** Dataset Inventory; six Dataset Profiles; Missing Value Statistics; Descriptive Statistics; Data Quality Report; Verification Code; Research Acceptance Report.
4. **Responsible Brain:** RESEARCH BRAIN.
5. **Collaborating Brains:** STUDENT-MAIN Brain authorizes and gates the task; QA BRAIN may independently verify calculations after MAIN authorization. DEVELOPMENT BRAIN is not required unless the authorized Work Order identifies a concrete integration need.
6. **Acceptance Criteria:** Exactly six input files are individually identified and verified; profile values are reproducible from those files using submitted verification code; missingness, descriptive statistics, and quality findings are evidence-based; no invented paths, data, or run results; the Research Brain issues an acceptance report for MAIN review.
7. **STOP_IF Conditions:** Six eligible files cannot be confirmed; an input appears to be original/protected data outside scope; files are unreadable or their provenance is unclear; observed values conflict with the report; or verification code cannot reproduce reported statistics.
8. **Next Role / Next Milestone:** After Research Brain acceptance, MAIN Brain review, and explicit STUDENT-MAIN authorization, dispatch M2 to RESEARCH BRAIN.

## M2 — NASA C-MAPSS FD001 Data Understanding

1. **Objective:** Understand and verify the real NASA C-MAPSS FD001 source data and its relationship to engine units, cycles, sensors, and remaining useful life.
2. **Input:** Expected source files are `train_FD001.txt`, `test_FD001.txt`, and `RUL_FD001.txt`. Their local presence, exact paths, provenance, field layout, and readability must be verified; names in this roadmap do not assert that the files exist or were read.
3. **Deliverables:** Dataset Inventory; Data Dictionary; Data Validation Report; Data Loading Specification; Source Mapping linking reported values to actual source files, rows, and fields.
4. **Responsible Brain:** RESEARCH BRAIN.
5. **Collaborating Brains:** DEVELOPMENT BRAIN reviews loading and source-mapping needs; QA BRAIN independently checks data consistency when assigned. STUDENT-MAIN controls milestone gates.
6. **Acceptance Criteria:** Every claimed source file is verified locally; field mapping and row/cycle/unit relationships are supported by inspected records; validation results are reproducible; no inferred schema is presented as verified; the Research Brain accepts the report.
7. **STOP_IF Conditions:** Required local files cannot be found or verified; source provenance is uncertain; protected originals would need modification; field mappings cannot be supported by observed data; or any reported validation result lacks reproducible evidence.
8. **Next Role / Next Milestone:** After Research Brain acceptance, MAIN Brain review, and explicit STUDENT-MAIN authorization, dispatch M3 to DEVELOPMENT BRAIN.

## M3 — Engine Health Analysis Core

1. **Objective:** Implement a reliable analysis core whose queries and health outputs are traceable to the verified FD001 source.
2. **Input:** Accepted M2 inventory, data dictionary, loading specification, source mapping, and authorized source files; project-owned code may be created or changed only within the Work Order scope.
3. **Deliverables:** Data Loader; Engine Unit Query; Cycle Query; Sensor Query; Sensor Trend Processing; Health Analysis Module; Unit Tests; source-row traceability metadata.
4. **Responsible Brain:** DEVELOPMENT BRAIN.
5. **Collaborating Brains:** RESEARCH BRAIN clarifies accepted data semantics; QA BRAIN designs and performs authorized data-consistency and regression checks; STUDENT-MAIN authorizes the milestone.
6. **Acceptance Criteria:** Load and query results match the verified source records; engine, cycle, and sensor selection return correct values; trend calculations are reproducible; health analysis states its inputs and method; unit tests cover defined behavior and pass with recorded evidence; source files remain unchanged.
7. **STOP_IF Conditions:** Accepted M2 mappings are missing or contradictory; implementation requires unapproved source-data changes; query results cannot be traced to source records; required tests fail without a resolved explanation; or implementation scope exceeds the Work Order.
8. **Next Role / Next Milestone:** After Development Brain acceptance, QA Brain review, MAIN Brain review, and explicit STUDENT-MAIN authorization, dispatch M4 to DEVELOPMENT BRAIN.

## M4 — Website Interface and Evidence Prompt

1. **Objective:** Deliver the local interactive website for traceable FD001 engine health exploration.
2. **Input:** Accepted M2 source mappings and M3 analysis core; project-owned frontend/backend files within the authorized Work Order.
3. **Deliverables:** Dashboard; Engine Unit Selector; Cycle Selector; Sensor Selector; actual source and sensor-trend display; Health Analysis Display; Evidence Prompt Generator; local startup instructions for this milestone.
4. **Responsible Brain:** DEVELOPMENT BRAIN.
5. **Collaborating Brains:** RESEARCH BRAIN reviews source and analysis interpretation; QA BRAIN performs authorized functional, traceability, and regression validation; STUDENT-MAIN authorizes the milestone.
6. **Acceptance Criteria:** Selectors operate against verified data; displayed source values and trends identify their source rows/fields; health outputs match the accepted M3 core; Evidence Prompt contains sufficient source and method context to reproduce the displayed result; the application runs locally with recorded verification evidence.
7. **STOP_IF Conditions:** Interface would display unverified or fabricated data; source traceability is lost; health analysis diverges from the accepted core; a critical function cannot be verified; or implementation requires files outside the Work Order scope.
8. **Next Role / Next Milestone:** After Development Brain acceptance, QA Brain validation, MAIN Brain review, and explicit STUDENT-MAIN authorization, dispatch M5 to DEVELOPMENT BRAIN with QA BRAIN assigned integration validation.

## M5 — Integration, Validation, and Delivery

1. **Objective:** Integrate the website and analysis core, verify critical end-to-end behavior, and prepare a reproducible local delivery.
2. **Input:** Accepted M2–M4 deliverables, verified source inputs, and the M5 authorized integration Work Order.
3. **Deliverables:** Integrated local website; Integration Test Report; Data Accuracy Report; Bug Report; README; Reproducible Startup Instructions; final evidence for each acceptance criterion.
4. **Responsible Brain:** DEVELOPMENT BRAIN for integration and delivery; QA BRAIN owns independent system validation.
5. **Collaborating Brains:** RESEARCH BRAIN verifies data-source and statistical claims; STUDENT-MAIN coordinates review and makes the final milestone decision.
6. **Acceptance Criteria:** Local startup is reproducible; Engine Unit, Cycle, and Sensor selection work end to end; displayed source values, trends, and health analysis match verified data; Evidence Prompt is reproducible; all critical test results and known bugs are reported with evidence; Brain reviews are recorded; STUDENT-MAIN makes the final decision.
7. **STOP_IF Conditions:** Critical end-to-end behavior fails; results cannot be traced or reproduced; delivery instructions are incomplete; a known critical defect is concealed; sensitive data or credentials would be published; or any required acceptance evidence is missing.
8. **Next Role / Next Milestone:** STUDENT-MAIN Brain reviews the complete delivery and records the final M5 decision. There is no next milestone in this roadmap; any new scope requires a new authorized Work Order.

## Milestone gate

M0 → M1 → M2 → M3 → M4 → M5. No milestone may be skipped. The responsible Brain must accept its work and the STUDENT-MAIN Brain must explicitly authorize the next milestone before its Work Order is dispatched. Worker completion alone is not acceptance.
