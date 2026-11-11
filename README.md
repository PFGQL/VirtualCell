# VirtualCell — public research memory and decision record

**Status:** Early research prototype. No validated bulk-to-cell-state inference claim.  
**Memory snapshot:** 2026-11-11 (HQ-010).  
**Authority:** This public repository contains a **curated, non-sensitive research-memory mirror**, **not** the entire local WSL code repository or a verified backup of its Git history.

## The immutable research mission

Build and rigorously evaluate a tool that takes a **new bacterial bulk RNA-seq sample** and returns a biologically meaningful, physically defined and independently testable **population-scale representation between bulk means and complete single-cell profiles**. Limited bacterial scRNA-seq should be used only where its information gain can be demonstrated. The exact output and model architecture **remain open research decisions**.

Immediate goal: a scientifically credible, reproducible **undergraduate thesis demo** suitable for a prospective experimental collaborator; not a visually impressive but unvalidated generator. Long-term goal: original, high-impact methodological/biological research, potentially including prospective perturbation response, with appropriate validation and collaboration.

## Mandatory reading order for any new AI conversation or Codex task

1. [Research charter](governance/RESEARCH_CHARTER.md): founding motivation, non-negotiable goals and scientific guardrails.
2. [Scientific/evaluation contract](governance/SCIENTIFIC_EVIDENCE_CONTRACT.md): estimands, identifiability, information permissions and independent ground truth.
3. [Latest verified decision snapshot](state/PROJECT_STATE.md): milestones, results, BLOCKED gates, evidence boundaries.
4. [Decision history](state/DECISION_LOG.md) and [open issues](state/OPEN_QUESTIONS.md).
5. [Experiment and handoff index](state/EXPERIMENT_AND_HANDOFF_INDEX.md).
6. [Workflows and publication policy](governance/WORKFLOW_AND_SYNC.md).

**Do not start experiments or commit to E+A+D just because a model can be trained.** Maintain source provenance and explicitly distinguish file-hash audit, static code review, local execution, cross-study prediction and independent biological validation.

## Evidence status

- Historic local research: 47 literature entries, 27 dataset assets (not 27 independent studies), 25 software repository entries as of I06.
- MATQ/BacDrop/M3/RiboD/PETRI/MERFISH and other public resources investigated; no verified independent culture-level bulk-to-cell-state or pre-treatment-bulk-to-future-CFU ground-truth chain in scope.
- Frozen PRECISE-1K bulk-only program projection is an engineering baseline, **not original cell-state inference**.
- C14 PETRI numerical QC **not completed** after a parse/checkpoint failure; C15 PRECISE-MG1655 external test/reference pair **not obtained**.
- Research gates: new external bulk calibration BLOCKED; independent state GT BLOCKED; prospective D BLOCKED; C10 / new bulk projector / heavy VAE NOT AUTHORIZED.
- Public memory mirror does not automatically update when the local Git repository changes.

## Publication and synchronization

Only curated Markdown and minimal metadata are intended to be public. Never publish raw or processed expression matrices, private credentials, internal Git bundles, unreviewed local history, personal identifiers, or possibly restricted/unlicensed source material. Project records must retain failures and UNKNOWN keys rather than silently upgrade evidence.

**Public mirror snapshot is not a disaster-recovery Git backup.** The local full-history bundle reported in I06 covers only the I06-era commit and is not a verified off-device backup. A local Codex agent must not push the full local history here without a distinct historical/privacy review.

[Scientific and workflow entry point](governance/WORKFLOW_AND_SYNC.md).
