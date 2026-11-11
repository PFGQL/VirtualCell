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


## HQ013 evidence snapshot — 2026-11-11

**Authority:** HQ opened and CRC/SHA-audited uploaded I09/C21/C22/R01-B04/R03-B04/R04-H02 ZIPs; directly re-executed C21's synthetic script in an isolated local directory. This public record does **not** claim access to the full WSL Git objects or original expression matrices.

- **Working Git:** Codex reports WSL HEAD `147c6796c46ae7112a70d5d48736b0180be20073`; local bundle is same-disk verified, not off-device recovery. I09 confirmed original C10 retired from active task boards while preserving history.
- **C21:** 72 rows from 3 seeds × W1/W2/W3 × M0–M3 × 2 targets; HQ independently re-executed 72/72 rows with max difference `4.44e-16` (runtime/RSS not byte-identical). W0 two distributions give equal bulk means (1,1) and co-positive fractions 0.5 vs 0. **Toy M3 is one-dimensional 201-point grid, not scVI/VAE.** W1 M3 MAE 0.0175 vs M1 0.0179; W2 M3 0.1655 vs M0 0.1222; W3 M3 0.1355 but 95% coverage ~0.333. W2/W3 OOD abstain rate 0; model selection and calibrated-interval claims FAIL. C21 methods used unequal/oracle nuisance information (sigma and r), not a fair real-world ranking.
- **C22:** exactly 128 design-only dataset × T0/T1/T2/T5 × M0–M3 rows, 8 assay crosswalks and 5 candidate experiments; no actual expression matrix read. **E2 MATQ** same-study internal sc aggregate/marker measurement pilot is eligible for separate approval; **E5 MERFISH** is potentially independent T2 GT but physical imaging→bulk culture joins remain missing.
- **R01-B04:** 19 new literature records P0048–P0066, hence **66 catalog entries total after validated local staging**, not full systematic search. R01's 21-column CSV must not overwrite canonical 20-column catalog. Bajikar et al. 2014 used multiple small pools from *mammalian epithelial cells* rather than one new bacterial bulk; multi-pool moments give a possible future additional experimental measurement, not current new-input GT. Other tumor/human algorithms are scientific prior art, not bacterial validation.
- **R03-B04:** 23 method records of static review, **not 23 newly installed/running repositories**, including scSemiProfiler, BuDDI, ConDecon, iModulonMiner 2.0 and additional latent models. Existing bulk+sc generation is direct prior art; a specific estimand, identifiability/measurement and independent functional verification remain necessary for originality.
- **R04-H02:** independently reran C21 and documented no direct test-label usage in the inspected path, but unequal simulation information/oracle sigma and RNA weights, inadequate bulk-only baseline hyperparameter selection, OOD/uncertainty failure and synthetic-only status. R04 posthoc RBF bulk-only improvement was exploratory and is **not** part of original preregistered benchmark.
- **W0 interval caveat:** [0,0.5] upper bound for co-detection with mean 1 and threshold >1 assumes nonnegative *integer* counts; it is not a universal bound for normalized continuous assays. Nonidentifiability of joint tails is robust; numeric bounds require correct observation units.

**HQ013 scientific decision:** No algorithm winner. **Prioritize actual real-data internal E2-like MATQ feasibility** and a corrected **fair synthetic C21-v2** in parallel, plus provenance-safe frozen-reference demonstrator; all exploratory results must be clearly labeled. No dependence on user's personal scVI studies. **G1 external sample/reference engineering PROVISIONAL/BLOCKED, G2 INTERNAL, G3 independent T2 GT BLOCKED, G4 prospective D BLOCKED, R2 ABSTAIN.** Original C10 remains RETIRED; scoped new experiments are permitted under HQ013 contracts.


## HQ014 confirmed evidence and decisions — 2026-11-11

**Scope:** nine uploaded ZIPs source integrity audit: I10 16/16, C23 11/11, C24 13/13, each of C25 early/mid/final 16/16 (consecutive revisions of one experiment), R01-B05 7/7, R03-B05 7/7 and R04-H03 13/13 research SHA checks; all ZIP CRC PASS. HQ separately ran delivered C25 11/11 unit tests and tested metadata tampering, and independently re-summarized C23/C24 CSVs. This is **not** a full WSL raw-matrix rerun or independently authenticated Git history. Codex-reported final local HEAD: `50fa369db75f47e9802453762a4d5543788492d7`; full-history off-device restore still unverified.

- **I10:** canonical literature catalog reached 66 paper records after B04; R03 B04's 23 method rows are STATIC NOT RUN. R01-B05 now adds P0067–P0072 (6 candidates) pending safe catalog stage, potentially **72** total; only 2 meet R01 B05's conservative primary verification; other 4 UNKNOWN. R03-B05 17 additional static baseline contracts, no executions.
- **C23:** real MATQ within-study 4-OD leave-one-OD-out, sc-read aggregate target log1pCPM per gene. Mean MAE: identity 1.753193; train-only offset 1.062505; M1 NNLS-then-renormalize 0.957108; simple M3 grid 0.972933. The latter is not a true simplex optimizer, not a cell population model, and not a GT-driven state reconstruction. R04 found train-offset training-OD row shuffle is algebraically invariant/INVALID NEGATIVE CONTROL. Of 12 train-selected `reads>5` technical marker detection events, bulk predictor MAE .458953 **worse** than prior-only .421007 and permuted-bulk .422935. **NO demonstrated marker heterogeneity gain.**
- **C24:** synthetic 216 unique test cultures expanded to 2592 rows by 6 methods × 2 targets. R04 independently replayed all rows. In W3 M3 p MAE .1306 (M0 fixed .1425), but RNA contribution q nominal 95% coverage ~.694; post hoc excluding flagged cultures leaves q coverage **.685** in W3 and **.657** in W2, not calibrated. **336 flagged output rows still contain point values; OOD flag was not a real abstention policy.** Full synthetic train p/q labels are available, unrealistically strong relative to current real bacterial sc/bulk.
- **C25:** one RPO processed log2TPM reference-bound T0 demonstration across three sequential code/report versions; frozen PRECISE-1K 201×4 activity CSV SHA `7a3d072600b0c00ef3a4b18e5e24df8e2b4f33b8752b6aec60b3f74d30efe1a0`, query replicate Pearson .92535569. Two reference profiles' anti-correlation -1 is an algebraic consequence of centering on their mean, not biological confirmation. HQ executed final delivered C25 11/11 unit tests PASS, then demonstrated **forged reference_condition/query_condition, BioSample and culture_id are still accepted as PROVISIONAL by validate_contract**; wrong GSM rejects. Thus METADATA_SOURCE_INTEGRITY_GAP and G1 final BLOCKED. Full original input 4305×586 matrix/model not in handoff, so no independent input-to-output raw recomputation by HQ.
- **R01-B05:** random ~10-cell stochastic mini-pools Bajikar 2014 are mammalian, not bacterial proof; Bacteroides 100-cell size-sorted pools measure *conditional morphology strata*, not random unbiased pool covariance. R03-B05 audit static only. R04-H03 confirms the three executable C23/C24/C25 gaps above and no new culture-linked GT.

**HQ014 authorizations:** I11 project/catalog evidence sync; C26 actual MATQ stronger nulls + optimized simplex QP; C27 realistic sparse-label synthetic selective abstention and genuine withheld predictions; C28 repair immutable scientific provenance and replay actual fixed RPO processed input; C29 conditional small K=2 individual-sc reference distribution + bulk observation pilot (NOT scVI/VAE/production), after C26 source/permission preflight; R02-B11 collaborator-ready independent bulk + dual-marker FISH culture design or only genuinely new physical-source evidence. No algorithm winner; C10 RETIRED; student's scVI work NOT a dependency.

**Gates unchanged:** G1 final real-new-bulk calibration BLOCKED (C25 provisional engineering), G2 SAME_STUDY_INTERNAL, G3 culture-level independent state/marker GT BLOCKED, G4 prospective t0 bulk→future phenotype GT BLOCKED, R2 single unreferenced bulk ABSTAIN. None of C23/24/25 proves single-cell state inference.
