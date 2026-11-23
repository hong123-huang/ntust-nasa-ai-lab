# Active Work Item

- **WORK_ITEM_ID:** `WO-M0-001`
- **Title:** M0 Governance Initialization
- **Responsible:** MAIN Own Worker (Codex)
- **Status:** BLOCKED — local governance baseline is committed and GitHub MCP is connected; the authorized account's target repository is absent and the available MCP tools cannot create a repository.
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

Worker result: BLOCKED. The four governance files are committed locally on `main`; the latest local commit is `15a2646a0dcbc3b12d60fabc07d2268248bdf5ac`. GitHub MCP is connected as `hong123-huang`. The target `hong123-huang/ntust-nasa-ai-lab` returned 404 and was not present in the authenticated user's repository listing. Other owners have repositories with the same name; none is authorized for this project. The available GitHub MCP actions do not include repository creation; no GitHub CLI is installed and no Git remote is configured. No remote creation, push, or remote-content verification is claimed.
Blockers: Create `hong123-huang/ntust-nasa-ai-lab` as a public repository (or provide its verified URL), then push local `main` and verify the four governance files remotely.
Next action: await MAIN Brain review and acceptance. Worker cannot self-approve M0.
