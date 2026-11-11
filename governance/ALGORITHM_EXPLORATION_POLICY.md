# HQ012 — Open algorithm competition (2026-11-11)

**Status: ACTIVE. This policy corrects an earlier HQ overrestriction.** Authoritative founding goal: using many bacterial bulk profiles and limited real bacterial scRNA-seq, produce a biologically useful, testable intermediate-scale output for a **new bulk**. Final output and architecture are OPEN.

## User independence / scientific independence

The user's interest in building a scVI-like bacterial single-cell reference state generator is one possible algorithmic idea, **not a chosen HQ method and not a prerequisite**. Their independent scVI/scIB learning, modifications, outcomes, timing or lack thereof must NOT affect scientific priority or gate decisions. HQ/R01/R03/R04/Codex should actively research and test the full algorithm space even if the user's personal implementation is never supplied.

## Retire C10

The earlier `C10` instruction prescribing or awaiting a chosen novel VAE/Bulk Projector implementation is **RETIRED / SUPERSEDED (HQ012)**. Do not execute, re-approve or treat it as a pending gate. Keep historical copies in Git history for audit, but remove it from active task boards/prompts in the working tree where safe. This is not a prohibition on studying or experimentally testing bulk projection and latent generative approaches; **those approaches are actively in scope**.

## Two orthogonal selection axes

**Estimand:** T0 bulk regulatory activity (comparator), T1 RNA-weighted bounded contributions, T2 specified detectable single-cell/marker/program functionals, T3 correctly prospective future response, or other empirically justified intermediate-resolution variables. Their exact physical meaning, calibration, and limitations matter more than arbitrary 'cell state' wording.

**Algorithm families** (all legitimate candidates; none chosen):
- M0: Frozen and learned bulk-only module/program/feature baselines, condition-aware models.
- M1: Explicit reference-mixture / NNLS / Bayesian / convex partial-identification methods with uncertainty and missing-state sensitivity.
- M2: Program-constrained joint bulk/sc representations, cross-assay measurement models, regularized factorization, reference adaptation and continuous state coordinates.
- M3: Latent-population distribution generator + bulk observation/projection/inference, potentially variational/flow/transport/diffusion, **not mandated to use scVI**; must distinguish bulk-identified from sc-prior-determined features and enforce RNA weighting and assay-specific counts.
- M4: Time- and perturbation-conditioned model families for eventual T3, separately requiring time0 bulk and prospective labels.

Mathematical caveat: one bulk mean does not uniquely identify within-population covariance, joint tails or a complete latent distribution. A probabilistic generator may yield a prior-conditioned posterior/ensemble, not a verified unique recovery of actual cells.

## Research permissions — importantly distinct from claim permissions

**NOW AUTHORIZED with scoped preregistration:** mathematical counterexamples; source/literature and repository method audit; compact simulations with known population truth; synthetic mixtures and reference perturbations; small CPU pilot comparisons of M0/M1/M2 and simplified M3 on synthetic benchmarks; carefully labeled internal diagnostics using already authorized processed public data with valid gene/assay units, with resource limits and failure reporting. Results may support feasibility, failure-mode identification and choosing the next experiment, **not** L2 biological validity.

**NOT AUTHORIZED automatically:** selection of scVI as model backbone; unreviewed full-scale VAE/Bulk Projector implementation/training; test-label access disguised as training; full-genome exact single-cell reconstruction claims; prospective CFU modeling without pre-exposure labels; new downloads beyond explicit bounds; upgrading external G1, cell GT G3 or prospective G4 based on simulations or in-study pseudo-bulk. Major model training needs a separate explicit scoped technical approval grounded in interim experiments, but **absence of independent GT is not a blanket ban on exploratory algorithm experiments**.

## Competitive evaluation requirements

Use a common simulation truth with at least one pair of different cell populations with identical bulk mean and different joint distributions. Vary sparsity, counts semantics, RNA-per-cell, batch shift, reference composition, missing programs, number of training sc conditions, train/test biological cultures and OOD conditions. Report estimand-level calibration/coverage and sensitivity, not only reconstruction correlation. Compare identical training information permissions; include bulk-only, NNLS/explicit reference, program constraints, condition-only, shuffled-sc/incorrect-reference and, as feasible, scSemiProfiler, BuDDI, ConDecon and iModulonMiner 2.0 based on actual prior-art applicability.

Label results **SYNTHETIC**, **IN_STUDY_INTERNAL**, **EXTERNAL_ASSAY**, **CULTURE_HELDOUT**, or **PROSPECTIVE**; never conflate.

## Next gates

R01/R03 method/novelty review and a Codex bounded synthetic *methods contest* can proceed immediately, in parallel with C18/C19 source fixes. No algorithm must wait for the user's personal scVI project. New HQ decisions should evaluate value, identifiability, GT availability, prior-art novelty, data suitability and the user's undergraduate demo time and computational constraints, rather than simply maximizing held-out Pearson.

Any local/remote conflict must be recorded and not silently overwritten.
