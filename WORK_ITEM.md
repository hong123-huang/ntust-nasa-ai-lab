# Active Work Item

- **WORK_ITEM_ID:** `WO-M0-001`
- **Title:** M0 Governance Initialization
- **Responsible:** MAIN Own Worker (Codex)
- **Status:** PUBLISHED — governance files are pushed to GitHub `main`; awaiting MAIN Brain review and acceptance.
- **Project:** `NTUST_NASA_AI_LAB`

## Scope

- Inspect the project root, existing files, protected data, and Git state.
- Create the four governance files in the project root.
- Initialize Git if no repository exists, preserving any existing history.
- Create or verify the public GitHub repository `ntust-nasa-ai-lab` under the authenticated account.
- Commit and push only the four authorized governance files to `main`.
- Verify the remote files and compare them with the committed local versions.

## Out of scope

- Modifying or deleting datasets, source code, user documents, credentials, or unrelated configurations.
- Publishing protected or sensitive files.
- Force-pushing, rewriting history, or creating an unauthorized branch.

## Evidence required for completion

- Actual root and initial repository status.
- Names of files created/modified and protected inputs observed.
- Git branch, commit message, commit object ID, configured remote, and push result.
- GitHub repository URL and evidence that all four remote files match the committed local files.
- Sensitive-file/staging-scope review and actual process exit codes.

## Stop conditions

Stop and report `BLOCKED` if the root is unclear, an existing governance file would be overwritten, history is unclear, authentication or ownership cannot be verified, the name conflicts with an unrelated repository, publication could expose sensitive content, push fails, or remote verification is unavailable. Preserve files and history; do not claim PASS.

## Worker return

Worker result: PUBLISHED; M0 acceptance remains pending and cannot be self-approved by the Worker. GitHub MCP is connected as `hong123-huang`. The owner created `https://github.com/hong123-huang/ntust-nasa-ai-lab`, verified public with default branch `main` and push/admin permission. The repository was empty before publication. The local `main` history was pushed normally to `origin/main`; the pushed history contains only `AGENTS.md`, `ROADMAP.md`, `WORK_ITEM.md`, and `DECISIONS.md`. Push result: exit code 0. Initial published HEAD: `5c4c01ed891d8bf61eb964fd6948f4ba29e0fd6e`.

Remote review: GitHub MCP fetched all four files from `main`; their contents matched the corresponding local committed versions at the time of review. No unrelated datasets or user files were staged or pushed. Existing untracked local data remains outside Git.
Blockers: NONE for repository publication. Await MAIN Brain remote inspection and acceptance; the next milestone still requires explicit MAIN authorization.
Next action: await MAIN Brain review and acceptance. Worker cannot self-approve M0.
