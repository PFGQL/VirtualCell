# VirtualCell project state — HQ010 public mirror

**Snapshot:** 2026-11-11. **Authority level:** HQ evidence reviewed from four uploaded ZIPs; this public document is a curated mirror, not an independently checked checkout of the user's WSL HEAD.

## Original scientific aim

Given a **new bacterial bulk RNA-seq** sample, output a testable intermediate-resolution population-scale biological quantity using extensive bulk + limited real bacterial scRNA-seq data. Output estimand is **still undecided**. Undergrad: credible reproducible demo; long term: original biologically useful methods and perturbation studies. The proposed E+A+D is *not* locked. Independent scientific verification is mandatory before performance claims.

## Repository / evidence history

- Local project: WSL2 + Conda/PyTorch/CUDA; maintained Git repository with preregistrations, analysis code, provenance catalogs, data/QC reports and handoffs.
- Catalog reported by I06: **47 papers, 27 dataset assets, 25 code repositories**. Assets are not independent studies; D0027 GSE268480 is a bulk companion of the same MERFISH study as D0021.
- I06: local Git bundle SHA256 `4fb066df98789be29d70c1d366f0191182bb6349b58a855ed77ec9e588b49032`, covers history through `31f7c6c` only. Local bundle passed `git bundle verify` but was not test-cloned, copied off-device or remotely backed up.
- User's subsequent Codex report says final local HEAD **`6dd0cd1`** after I06, C14 and C15; this is **user/Codex-reported**, not independently verified from remote Git objects.
- This GitHub repository was empty immediately before HQ010 and is now a curated public *memory* mirror. Its commit history is **not** the working WSL history.

## Current dataset and methods facts

| Work | Evidence established | Scientific limitation |
|---|---|---|
| MATQ C04c | Processed sc 384 cells, bulk 12 samples, 5023 common gene IDs; reads-based assay; matching cultures described by source study | Per-aliquot identity and external GT unresolved |
| BacDrop/M3 | Actual sparse processed matrices QC'd; limited BacDrop paper-reported FISH marker co-detection evidence | Low depth/filtered samples, no whole-population GT |
| RiboD-PETRI C06 | Official GSE260457 processed matrices accessed; GSM8117639 21,797 cells × 4,194 genes, single GSM | No independent batch/culture GT; genotype metadata conflict |
| C05a | Four-fold same-study MATQ cross-platform assay-offset diagnostic improved correlation; F02 state weights ABSTAIN | Does not show state inference or external validity |
| C09/C12 | Frozen PRECISE-1K 201-module projection CLI; internal real-profile R0 tested; model uses 4257 genes | G1 external MG1655 real/test reference absent; published A value discrepancy unresolved |
| C13 | Pre-registered module-state diagnostic; single RiboD GSM heavily depth-influenced; MATQ/PRECISE top-gene ID crosswalk unavailable | No validated continuous/binary cell-state labels |
| PETRI C11/C14 | GSE141018 official 8 sc +10 bulk; SB346/SB345 sc and SB365 bulk described as same source cells. C14 fixed streaming metering. C14: 1,329,367,344 bytes expanded under cap. SB365 featureCounts 5236 genes / 6,361,429 aligned reads | Both sc gzip members streamed but an ancillary bulk parser error discarded numeric summaries. **NOT PASS_DATA**; culture/aliquot UNKNOWN |
| PRECISE-MG1655 C15 | Official Zenodo inventoried: 262,967,116 B and 291,268,179 B dataset ZIP versions; 320,556,221 B pipeline ZIP. Frozen PRECISE-1K 1035 alias IDs inventoried | Archives exceeded C15 80 MiB per-file cap; no verified new-test/reference pair, R1/R2 ABSTAIN |
| R02-B08 | Confirmed SB365 to SB345/SB346 shared source; published MG1655 paper describes 434 later-generated WT MG1655 samples, 150 historical | Culture IDs and Supplementary Table 4 missing; 434 not accession-deduplicated |

## Current scientific gates

- **G1 / T0 real external bulk reference:** BLOCKED. R0 in-training projection only. R1 external matched project reference and R2 one-bulk reference-free input ABSTAIN.
- **G2 scientific state-coordinate diagnostics:** INTERNAL ONLY, not GT.
- **G3 / T1-T2 independent marker/state evidence:** BLOCKED (no authenticated L2-level culture-heldout paired target in scope).
- **G4 / T3 prospective perturbation:** BLOCKED (no verified pre-exposure bulk → matched future CFU chain).
- **C10 novel research model, new VAE/Bulk Projector and prospective CFU trainer:** NOT AUTHORIZED.
- scVI/scIB student study remains outside the project's task pipeline.

## What changed at HQ010

Public research charter and state mirror initialized after explicit user permission to publish curated memory in a public GitHub repo. This is a **governance/storage** milestone, **not** an upgrade to scientific validation.

See `state/OPEN_QUESTIONS.md` and `governance/WORKFLOW_AND_SYNC.md` for next work and synchronization.
