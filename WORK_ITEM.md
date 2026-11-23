# Active Work Item

- **WORK_ITEM_ID:** `WO-M0-001`
- **Title:** M0 Governance Initialization
- **Responsible:** MAIN Own Worker (Codex)
- **Status:** BLOCKED — local governance baseline is committed; public GitHub setup and remote verification could not be completed in this environment.
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

Worker result: BLOCKED. The four governance files were committed locally on `main` in commit `e50d8611c06ad5190cb90d233d70a436efd4aa8a`. No GitHub CLI is installed, no remote is configured, and browser automation was stopped because the current browser URL could not be determined with sufficient confidence. No remote repository creation, push, or remote-content verification is claimed.
Blockers: Authenticated GitHub repository creation and remote verification are unavailable.
Next action: await MAIN Brain review and acceptance. Worker cannot self-approve M0.
