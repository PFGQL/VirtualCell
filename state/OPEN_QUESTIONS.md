# Critical open questions and ordered next research tasks

The tasks below are candidate HQ010 successor jobs; do not mistake a written plan for an executed experiment.

| Priority | Unresolved question | Minimum decisive evidence / STOP |
|---|---|---|
| P0 | Is the curated GitHub public mirror actually readable and maintained? | Read back README, charter, project state and decision log via connector; Codex compares local vs public timestamps and verifies public content contains no private paths/secrets. Refresh **local** bundle to latest local HEAD and test-clone; never push full history to public automatically. |
| P1 — PETRI | Can GSE141018 SB345/SB346 numerical sc QC be completed without violating decompression limits? | Run already fixed C14 parser on **one new authorized cumulative 1.7 GiB stream budget**, preflight tests, checkpoint each nested matrix before reading bulk, save per-cell count/UMI semantics, zero fraction, barcode uniqueness, organism mixture, gene overlap; report actual bytes and failures. No redownload if hashes match. |
| P1 — PETRI lineage | Do SB345/SB346/SB365 share a culture/aliquot or only initial source cells? | Obtain actual official paper Supplementary Table 4 and complete GEO SOFT; join internal SB and accession with real culture IDs; preserve UNKNOWN if ambiguous. Two sc aliases and one bulk do not establish independent external GT. |
| P1 — T0 | Is there a verified MG1655 **external** test/reference pair with no PRECISE-1K training overlap? | Use Zenodo file inventory already captured (data ZIP 262,967,116 B / other version 291,268,179 B); first seek individual metadata. If missing, a separately authorized bounded **one-file official archive** can be inspected with integrity checks, selective extraction and no training. Obtain S1/S2/S10, reference, per-sample accessions, compare against 1035 frozen aliases and replicate/run identities. If not found, retain R1 ABSTAIN. |
| P1 — T0 numerical | Why do frozen re-inferred activities disagree with published PRECISE-1K A? | Inspect identical normalization, centering, gene ordering, sign/scale conventions and projection function. No post-hoc fitting to create agreement. |
| P2 — GT | Which T2 feature has independent culture-level FISH/MERFISH/operon label and an authentic bulk input? | Search original replicate/source sheets and physical joins. If unavailable, limit conclusions to internal, in-study diagnostic and design potential. |
| P3 — D | Is any pre-treatment bulk→same-culture future CFU available? | Require culture_id, time0 expression, intervention/dose, time1 phenotype and independent holdout. Otherwise D prospective training remains STOP. |
| P3 — E | Does real sc add predictive information to the chosen scoreable target over equal-information bulk-only and shuffled-sc controls? | Only after T1/T2 GT and train/test scopes fixed; otherwise NO novel model training. |

## Exact known blockers

- GEO PETRI `GSM4192510`/SB365 described as same-source cells as `GSM4192506`/SB346 and `GSM4192507`/SB345; aliquot/culture keys unverified.
- C14 two gzip members expanded about 683/646 MB; numeric summaries lost when a featureCounts comment was parsed as a header. Fixed code **not rerun** on full sc streams.
- PRECISE-MG1655 434 later-generated samples are **paper-level** new profiles; not yet proven to be distinct from every frozen 201-module model training entry on a sample-by-sample basis.
- RiboD, MATQ and BacDrop count units differ; cross-platform matrices must not be treated as equivalent UMI representations.
- Publication and privacy review is still required before syncing additional local state/code beyond the redacted public allowlist.


## HQ011 next authorized research questions

1. **C18 / T0 frozen-coordinate reconciliation (priority 1).** With local C12/C17 artifacts and no new bulk download, determine the published PRECISE-1K `A` discrepancy under exact gene order, centering, sign/scale, pseudocount and projection APIs; evaluate all 201×4 RPO scores, reference-swap and train-overlap negative controls, gene-specific coverage and residual/OOD flags. Do not change the frozen model or tune to evaluation samples. STOP if published coordinate/normalization remains irreconcilable; engineering gate remains provisional.
2. **C19 / PETRI parser closure (priority 2).** Before any full GSE141018 sc reread, fix synthetic negative count acceptance and accumulator overflow, add nonnumeric/blank/decimal/exponent and row-width tests; distinguish `budget_failed` from `task_status=FAILED_PARSER`. A separate **tiny capped real-format fragment** is needed to establish the actual first-row token grammar without a large stream. Only after a clean preregistered proof and a *new* authorized decompression cap may the full, checkpointed numerical QC be considered.
3. **I08 / public vs local recovery.** Refresh local bundle at the final WSL HEAD and actually test clone; record SHA256 and snapshot scope. Copy to an owner-controlled off-device location only after separate channel/privacy check. Curated public GitHub memory stays deliberately distinct from full Git history; update only redacted reviewed text.
4. **PETRI physical mapping.** Table 4 original XLSX still absent; shared source cells != independent culture heldout. Do not infer missing GSM identities or technical replicates.
5. **MG1655 data release reconciliation.** Verify why v1 has 586 columns/436 `pxk` versus article 584/434, whether 6 SDT122 are excluded, and which two columns/quality rules account for the difference. No automatic statement that 436 columns are all independently eligible test samples.
6. **Independent middle-layer biological target and prospective D.** Still no culture-level marker/operon ground truth or t0 bulk→matched future phenotype. Do not upgrade G3/G4 through T0 engineering.


## HQ012 new priority: independent algorithm competition (not a GT waitlist)

1. **R01/R03 methodology audit now:** enumerate algorithms spanning explicit mixture/partial-identification, bulk/sc latent generator + bulk projector (scVI-like only one of several possible backbones), program constraints and conditional prediction. Verify input/output, trained-data permissions, prior art, biological relevance and reproducible baselines. Do not defer to student's scVI work.
2. **C21 bounded synthetic inverse benchmark now:** construct explicit two-world equal-bulk/different-cell-population counterexample plus controlled RNA weights, assay effects, missing states and unseen conditions. Compare M0 bulk-only, M1 constrained reference mixtures, M2 program-structured projection, simplified M3 amortized/latent population inference (if resource contract allows). Report calibration, abstentions and prior sensitivity without implying real-cell recovery.
3. **C22 real-data alignment audit:** for available MATQ/RiboD/MERFISH/PETRI, map gene IDs, count units, biological cultures and assay panels; propose task-specific internal diagnostic and external validations. An input sample or sc reference trained only in the same study is not independent culture GT.
4. **C19 format blocker remains:** if revisited, use tiny real token/schema forensic tool preserving hashes and row structure before any new full stream; do not guess PETRI grammar or consume repeated decompression automatically.
5. **Demo objective OPEN:** beyond stable T0, choose a supported intermediate-resolution output by value, identifiability, actual reference data, original-method boundaries and uncertainty; a validated research output is not guaranteed from existing public GT.

The student's personal scVI project is not part of this task board and must never become a hidden gate.


## HQ013 immediate evidence-driven tasks

1. **I10:** Stage R01 19 new P IDs and R03 23 static method records without corrupting catalog schema; ingest and hash all six source ZIPs; update experiment registry and local/public memory delta, validate current Git bundle; do not push full WSL history.
2. **C23 REAL INTERNAL MATQ:** using already present verified GSE218631/632 processed read-count sc and bulk files, preregister a 4-OD leave-one-OD-out contest on **sc-assay aggregate expression and tightly labeled detection proxies only**. Compare identity, train-only assay offset, fair train-sc-informed bulk-only/NNLS/low-dimensional latent alternatives, condition permutation and prior ablations. Score heldout OD sc only after predictions frozen. No cell fraction/orthogonal GT claim. Run only after unit, gene-ID and split leakage preflight. No new downloads.
3. **C24 SYNTHETIC FAIRNESS:** rerun C21 with equal train-label information permissions; estimate noise/r from permitted train data or report explicit unmeasured-r ranges; use nested train-only hyperparameter tuning and stronger bulk-only; expose oracle runs in a separate sanity appendix. Pre-register coverage/width, OOD/ABSTAIN, prior sensitivity; test equal-mean adversaries and missing-state/assay shifts.
4. **C25 DEMO real reference:** package a frozen PRECISE-1K 201-module RPO reference-aware, processed-bulk input CLI smoke demonstration using already measured samples; strict in-project reference gating, explicit provenance/OOD residual **diagnostics, not calibrated detection**, no-ref ABSTAIN and optional synthetic demo. Published A mismatch, 586/584 and strain nuances remain warnings, not 'PASS_G1'.
5. **R01-B05 / R03-B05:** target experimental small-pool observability and marker feasibility vs direct executable open-source algorithm baselines; do not start another generic exhaustive search or infer automatic bacterial transfer from mammalian papers.
6. **T2 independent GT:** MERFISH imaging biological-replicate ↔ bulk culture linkage, raw marker-positive numerators/denominators and panel thresholds remain unverified. R02 prior SOURCE_STOP is respected until genuinely new source evidence appears. Prospectively matched t0 bulk→t1 CFU remains unavailable in scope.

**Always report both the physical goal ('new bulk → intermediate population property') and the validation tier.** C23 is internal only; C24 is synthetic only; C25 is engineering only. Retired C10 must not be resurrected.


## HQ014 prioritized execution

1. **I11 source/project restore:** ingest nine handoff ZIP sources; verify actual Git ancestry (C23 prereg vs prediction freeze vs scoring), stage R01-B05 6 P IDs and R03-B05 17 static records with schema validation, local bundle clone+fsck, public redacted-only summary.
2. **C26 MATQ true model control:** confirm true simplex QP and train-sc mean/shrinkage/wrong gene namespace baselines against C23; test whether sc contributes beyond assay mapping. Score entire heldout OD sc only after predictions frozen; no independent culture claims.
3. **C27 selective uncertainty:** withhold actual predictions for OOD, analyze unique test CULTURES, train p/q label missingness/noisy selection regimes and wrong-reference failures; calibrate or ABSTAIN, do not hide insufficient independent calibration sample.
4. **C28 immutable RPO provenance:** forged reference_condition, query_condition, BioSample and culture_id must **not** be published as verified source; bind to official fixed metadata and keep culture UNKNOWN; rerun actual local processed source and frozen model; preserve no-reference ABSTAIN.
5. **C29 conditional individual-sc generative method pilot:** train small K=2 per-cell distribution reference from MATQ train individual read-count cells, predict heldout *technical* marker detection under bulk RNA-weighted operator, benchmark vs prior-only; no scVI dependency and no heavy architecture search. Only after C26 source and permission preflight.
6. **R02-B11 actual physical marker test design:** matched independent culture new bulk and 2-marker imaging, positive/total count, probe negative, blinded culture holdout; public MERFISH join only if actual new evidence available. Otherwise STOP and provide collaboration-ready protocol.

Continue independent M0–M3 research, but distinguish technically correct bulk-sc aggregate, identifiable bound, and true culture-validated heterogeneity. User's personal scVI learning is not a project gate.
