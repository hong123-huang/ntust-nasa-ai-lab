# NTUST NASA AI Lab Roadmap

Project: `NTUST_NASA_AI_LAB`
Objective: Build a local NASA C-MAPSS FD001 Engine Health Analysis Website.

## M0 — Project Governance

**Goal:** Establish governance, Git workflow, Brain authority, and project documentation.

**Deliverables:** `AGENTS.md`, `ROADMAP.md`, `WORK_ITEM.md`, `DECISIONS.md`.

**Acceptance:** All four files exist, are complete, and are remotely verifiable.

## M1 — Synthetic Dataset Profile

**Goal:** Use six local synthetic CSV files to practice Brain-to-Brain delegation and evidence-based acceptance.

**Input:** Local synthetic CSV directory; known filename: `synthetic_sensor.csv`.

**Deliverables:** Dataset Inventory; six Dataset Profiles; Missing Value Statistics; Descriptive Statistics; Data Quality Report; Verification Code; Research Acceptance Report.

**Acceptance:** All six files are actually verified. Do not invent data or execution results.

## M2 — NASA FD001 Data Understanding

**Goal:** Understand and verify the real NASA C-MAPSS FD001 dataset.

**Expected inputs:** `train_FD001.txt`, `test_FD001.txt`, `RUL_FD001.txt`.

**Deliverables:** Dataset Inventory; Data Dictionary; Data Validation Report; Data Loading Specification; Source Mapping.

**Acceptance:** Actual local files and field mappings are verified.

## M3 — Engine Health Analysis Core

**Goal:** Build the data query and analysis engine.

**Deliverables:** Data Loader; Engine Unit Query; Cycle Query; Sensor Query; Sensor Trend Processing; Health Analysis Module; Unit Tests.

**Acceptance:** All queried values match the original dataset.

## M4 — Website and Evidence Prompt

**Goal:** Build the interactive local health analysis website.

**Deliverables:** Dashboard; Engine Unit Selector; Cycle Selector; Sensor Selector; Trend Charts; Source Viewer; Health Analysis Display; Evidence Prompt Generator.

**Acceptance:** All displayed information is traceable.

## M5 — Integration and Final Delivery

**Goal:** Complete integration and system validation.

**Deliverables:** Final Website; Test Report; Data Accuracy Report; Bug Report; README; Reproducible Startup Instructions.

**Acceptance:** Website works locally and all critical functions pass.

## Gate rule

M0 → M1 → M2 → M3 → M4 → M5. No milestone may be skipped. A new milestone requires both previous Brain acceptance and explicit MAIN Brain authorization.
