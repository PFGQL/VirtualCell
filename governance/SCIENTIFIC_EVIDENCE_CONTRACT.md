# Scientific outputs, validation and STOP rules

## Estimands (scientific claims) versus model architecture

- **T0 / A:** frozen regulatory-program projection from compatible new bulk data and correctly normalized reference. Unit: reference-relative module activity; not a cell-state ground truth.
- **T1 / B:** reference-conditioned RNA-expression contributions or partial-identification bounds under explicit generative/measurement assumptions; not cell-number fractions without RNA-content calibration.
- **T2 / C:** tightly specified cell-level measurable functionals, e.g. operon detected-cell fraction, two-marker co-detection frequency, bounded program distribution. Threshold, detection units, denominator, imaging filters and independent biological replicate structure must be fixed before evaluation.
- **T3 / D:** pre-treatment bulk and matched culture + drug/dose/time to a future independent phenotype (CFU or comparable); using post-treatment profiles or unmatched survival curves is **not** prospective prediction.
- **T4 / E:** multi-modal/sc-assisted architecture. It must specify **which T1/T2/T3 output it predicts**. A scVI/VAE/Bulk Projector is an implementation candidate, not a scientific finding.

A and E are not exchangeable categories; A is a possible output/coordinate and E an approach.

## Identifiability and observation

A bulk mean alone cannot generally identify cell-to-cell covariance, joint marker-tail probabilities, cell counts per state, or exact state distributions. A and E do not remove that mathematical limit automatically. Technical capture, RNA per cell, read/UMI/probe semantics, gene IDs, batch and strain must be explicit.

## Evidence levels

- **E0:** sourced metadata and published description.
- **E1:** actual file measured, hash and calculation reproducible. In-research pseudo-bulk and within-study cross-modality diagnostics remain E1.
- **E2:** biologically distinct culture/sample held out with authenticated labels and a valid bulk/sc or orthogonal assay relationship. Check both ancestry and information permissions.
- **E3:** independent condition/laboratory/platform or biological orthogonal readout (FISH, MERFISH, reporter, phenotype) on a traceable physical unit, according to the chosen estimand.
- **E4:** independent prospective future-outcome chain; all pre-exposure predictors must precede the measured phenotype.

These are a public shorthand; the canonical local docs/SCIENTIFIC_CONTRACT.md, EVALUATION_PROTOCOL.md and DATA_AUDIT_PROTOCOL.md remain authoritative for detailed acceptance when accessible.

## Experimental rules

1. Predefine input units, sample/strain, time, culture, reference, output target, uncertainty and metrics.
2. Split by biologically independent culture/project/condition as scientifically appropriate, **not by arbitrary individual cells**.
3. Lock prior-art and same-information baselines: bulk-only T0, simple reference/NNLS, assay-offset calibration, applicable published algorithms and shuffled-sc controls.
4. Require a calibration and dataset-shift/OOD policy. A single novel bulk profile without a valid reference anchor must ABSTAIN.
5. Record data lineage, hashes, reproducible commands, failures, negatives and Git commits. A source verification or static code inspection is not a rerun of raw expressions.
6. **No automatic C10/novel VAE/Bulk Projector training** while the scientific target, labels and gate are unapproved.
7. Avoid overstating training/pseudo-bulk gains as independent biology.

## Current status (HQ010)

G1 (real external bulk with authenticated centering/reference) BLOCKED; G2 internal diagnostic only; G3 (independent state marker/functional validation) BLOCKED; G4 (prospective pre-bulk to future outcome) BLOCKED. Local studies MATQ F01, C13 and C14 do **not** close these gaps.

All gates are revisable when new direct source evidence and real experiments support them.
