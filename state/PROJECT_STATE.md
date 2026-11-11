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


## HQ011 evidence addendum — 2026-11-11 (supersedes older C16/C17 snapshot)

**Source**: uploaded, CRC- and SHA256-verified handoffs I07 (16/16), C16 (15/15), C17 (27/27), R02-B09 (8/8), R04-G02 (9/9). Those checks authenticate the supplied files, **not** an independent rerun of original expression matrices or an authenticated remote WSL commit history.

- **I07**: locally recovered a complete Git bundle through `789b21d5b98675754640c1032065db2a8ee3e0ea` with `git bundle verify`, test clone and `git fsck` according to the handoff. Local bundle is **not** off-device. Later Codex user report: final WSL HEAD `ed9e342b6376f90502c42971ab07421ba6776693` and newer bundle SHA256 `ccea855cdfc58b5a152600e776fc8b05d71dfd4245056639232caf70c22f2f55`; these latest values are Codex-reported, not independently checked via the public repository. Public `main` has unrelated history.
- **C16**: PETRI SB346 real count parsing stopped on the very first matrix row after 491,157 expanded bytes; SB345 was not opened. No PETRI cell-level numerical QC was delivered. R04-G02 independently demonstrated that the corrected C16 parser accepts a **synthetic negative integer** (`-1\t2`), contrary to the expected nonnegative-count contract. This is a real code bug; **not evidence that PETRI source has negative counts**. Fix parser, numeric overflow, task-status semantics and fixture tests before any new full read.
- **C17**: official Zenodo v1 PRECISE-MG1655 ZIP downloaded, official MD5 and local SHA256 verified; selected seven files extracted under resource budget. `log_tpm.csv`: 4305 b-number genes × **586** columns (150 reused `p1k`, **436** `pxk`), whereas the publication reports **584/434**; six rows labeled SDT122 need inclusion/strain audit. An RPO MG1655/BOP27 project reference pair (`pxk_0132/0133`) and two query replicates (`pxk_0134/0135`) supported a **provisional external reference-relative projection** through frozen PRECISE-1K 201-module M: 4168 common genes, query-module Pearson **0.9253557**, relative residual norms **0.75852/0.70310**. The author normalizations matched the four-column calculated project centering; independent least-squares projection agreed numerically. **This is engineering evidence only**, not proof of calibration accuracy, independent biological cell-state inference or single-bulk reference-free performance. C12 published-A mismatch and incomplete sample alias/strain mapping remain OPEN.
- **R02-B09**: PETRI SB345/SB346 and SB365 share explicitly described source cells, but Table 4 physical-row mapping, culture and aliquot IDs remain UNKNOWN; PETRI GEO lists 18 samples even though a prior extraction enumerated only 17. MG1655 study Table S1/S2/S10 direct rows remain missing from this research packet (C17 has a subset of archive metadata, not proof that each supplemental worksheet was independently read).
- **R04-G02**: source/negative-control audit agrees C16 numeric QC NOT PASS and C17 a provisional engineering result. No culture-independent GT or t0 bulk to future CFU chain established.

**Gates as of HQ011: G1 BLOCKED (with provisional reference-relative external engineering result), G2 INTERNAL ONLY, G3 BLOCKED, G4 BLOCKED, R2 single new bulk without validated reference ABSTAIN. C10 / novel VAE / Bulk Projector / prospective phenotype model still NOT AUTHORIZED.**


## HQ012 active correction — 2026-11-11

**Scientific governance change:** C10 retired/superseded; earlier blanket language forbidding all VAE/Bulk Projector research is **overruled**. Method family M3 (sc-reference latent population generator + bulk-conditioned inference/projector) is **ACTIVE IN RESEARCH**, alongside program-constrained M2, reference-mixture/partial identification M1 and bulk-only M0, without privileging scVI or E+A+D. All AI teams must continue this research independently of the student's personal scVI training. Permitted: source audit, identifiability theory, preregistered synthetic comparisons, bounded internal real-data pilots. Not permitted: unreviewed selection or full model training; claims of GT-backed recovery. Read `governance/ALGORITHM_EXPLORATION_POLICY.md`.

**HQ012 new verified handoff scope:** I08 (13/13 SHA; local bundle restored by Codex); C18 (21/21; reproduced C17 201×4 CSV identical SHA, but published-A mismatch OPEN, G1 BLOCKED); C19 (16/16; synthetic parser negative/overflow fixed, real PETRI fragment `UNEXPLAINED_REAL_SCHEMA`, Phase B NOT RUN); C20 (15/15; four estimand design contracts only, no method-family contest executed); R02-B10 (10/10; original PETRI Table4/MG1655 S1/S2/S10 still not obtained; collaborator GT template only, NOT SENT). Source ZIP CRC all PASS; these are reported-file audits, not independent on-disk WSL reruns.

**Codex-reported latest local HEAD:** `e9835122b1aa6de88081f0bf60730dc03c0fe35b`. Local final bundle SHA256 `78a13ce27582a79f4f2df3ad32a1dd7d9a0babe2788400be21c94bb0219f80be`; tested locally, off-device recovery UNKNOWN. Remote public repo remains a curated independent-historical memory mirror.

**Gates unchanged**: G1 reference-relative real-new-bulk engineering still provisional, G2 INTERNAL, G3 independent-state GT BLOCKED, G4 prospective GT BLOCKED, R2 ABSTAIN. Gate status does not stop hypothesis testing. Next parallel programs: R01/R03 focused methodology/prior-art comparison, Codex bounded synthetic inverse-problem competition and scientific-output/data compatibility, plus small PETRI schema forensics only if warranted.
