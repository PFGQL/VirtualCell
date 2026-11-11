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
