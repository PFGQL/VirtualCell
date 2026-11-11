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
