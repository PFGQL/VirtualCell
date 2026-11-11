# AI coordination and GitHub memory runbook

## Mandatory first step in each new HQ, R01–R04 or Codex conversation

Read, in this order, the GitHub **main** files:

1. README.md
2. governance/RESEARCH_CHARTER.md
3. governance/SCIENTIFIC_EVIDENCE_CONTRACT.md
4. state/PROJECT_STATE.md
5. state/DECISION_LOG.md
6. state/OPEN_QUESTIONS.md
7. state/EXPERIMENT_AND_HANDOFF_INDEX.md

Then, for local execution, read the **local WSL Git repository** files `AGENTS.md`, `docs/SCIENTIFIC_CONTRACT.md`, `docs/EVALUATION_PROTOCOL.md`, `docs/DATA_AUDIT_PROTOCOL.md`, `state/PROJECT_STATE.md`, experimental preregistrations and task-specific instructions. Compare snapshot timestamps and commit IDs; **prefer newer direct local evidence over an older public mirror**, without rewriting historical decisions.

GitHub does NOT push model-memory changes or automatically inject these files into a new conversation. The AI must actively use the connected GitHub app or retrieve the public URLs. New chats without those tools must be given the URLs or a local project bundle.

## Two repositories: different trust boundaries

- The working WSL repo contains current Git history, code, tests, reports and local file manifests; data/raw and data/processed stay out of public Git. Local branches may be `master`.
- Public `PFGQL/VirtualCell` `main` is a **curated memory mirror**. It was initialized independently from an empty GitHub repository and has an unrelated Git history. **Never force-push the WSL `master` into public `main` or automatically merge unrelated histories.**
- The I06 local full-history Git bundle ends at I06 and excludes C14/C15 and raw files. Refresh it locally after subsequent commits; copy off-device to an owner-controlled secure location after inspection. This public mirror is not a full disaster-recovery backup.

## Public publication allowlist

Allowed after review: original research charter without identifying details; immutable methodological contracts, high-level decisions and Gate status; source URLs/accessions; reproducible code that contains no sensitive material; redacted summaries and references to Git commits.

Do NOT publish: credentials, WSL user/home path, personal names and affiliations, email patterns, detailed collaborator contacts, raw/processed expression matrices, private datasets, reports that reproduce copyrighted material at length, Git bundles, unreviewed Git object history or ZIP handoff dumps. Check *all historical commits* before ever pushing local Git history, since .gitignore affects only current tracked paths.

## Update protocol after each HQ

1. Codex writes and tests local outputs and commits to the WSL working repository.
2. HQ checks task artefacts, sources, failures, checksum audit, scientific scope and newly justified Gate.
3. Generate a PUBLIC-REVIEWED delta for `state/PROJECT_STATE.md`, `state/DECISION_LOG.md`, `state/OPEN_QUESTIONS.md` and experiment index. Include local reported HEAD and provenance, mark unverified external claims.
4. Modify public mirror files by explicit commit, not by uploading the local tree. Read back each changed path from GitHub and verify the content and current commit.
5. If local and public status disagree, record a `SYNC_CONFLICT` in the next HQ report and resolve with evidence; do not silently prefer whichever is newer.
6. Keep research paths and tasks unapproved unless documented by a new Gate decision.

## Independence of assistants

R01 sources original literature; R02 validates public data and physical sample lineage; R03 audits methods/prior art; R04 argues against optimistic HQ claims; Codex operates the real local WSL; HQ chooses estimands and approves work only after evidence review.

Human-supervised scientific and biosecurity review takes precedence. This mirror must not imply perpetual monitoring or autonomous background work.
