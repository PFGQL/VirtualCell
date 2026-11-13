# Public experiment and handoff summary — source-scoped

**Do not mistake this listing for a full Git repository mirror or independent rerun of local expressions.** Detailed commands, scripts and hashes reside in the owner-controlled local WSL work repository and original handoffs. Git SHAs below were reported by Codex and inspected in supplied handoff manifests, but local object authenticity has not been checked against a remote work Git repository.

| ID | Kind | Finding | Validation status |
|---|---|---|---|
| C04b/C04c | Processed data QC | MATQ 384 sc / 12 bulk / 5023 common gene IDs; sparse BacDrop/M3 real file measurements | Local replay reported, same-culture sample-level mapping unresolved |
| C05a | Preregistered research diagnostic | MATQ F01 train-only assay offset improves same-study aggregate correspondence; F02 abstained | Independent R04 static code inspection, no full matrix rerun |
| C06 | Processed sc file audit | RiboD-PETRI GSE260457 8 downloaded processed files; sample GSM8117639 21797 ×4194 | One-GSM, measured QC only |
| C07 | Tutorial experiment | Standard scVI on one-GSM subset; actual biological scIB metrics NOT_SCORABLE | Tutorial only; no scientific Gate |
| C08 | Data/GT feasibility | MERFISH matched-condition bulk and other official small files | NO_SCOREABLE_L2_TARGET_FOUND |
| C09 | Engineering baseline | PRECISE-1K 201-module projection CLI, synthetic smoke tests | Real external bulk gate BLOCKED |
| C11 | PETRI transfer + bounded audit | Files downloaded, decompression overrun detected | FAILED numeric sc QC |
| C12 | T0 internal real-profile check | In-training PRECISE-1K profiles projected; published A inconsistency | No external test success |
| C13 | Preregistered module-state diagnostic | Depth-dependent sc sparse indicators, matched-random-gene comparison | Single GSM/internal; no stable GT state |
| I06 | State/archive synchronization | Complete local bundle through I06 and privacy scan | Local only; historic scan not full publication approval |
| C14 | PETRI bounded one-pass read | Two sc members streamed 1.329 GB total including ancillary; summary lost after parser error | PARTIAL_QC; **NOT PASS_DATA** |
| C15 | PRECISE-MG1655 file inventory | Official CC BY 4.0 archives 262.97/291.27 MB exceed old 80 MiB cap | R1_ABSTAIN_METADATA; R2_ABSTAIN |
| R02-B08 | External provenance research | Source-cells link PETRI, PRECISE-MG1655 434 later-generated profiles | PARTIAL; culture/aliquot and reference still UNKNOWN |

## Source handoffs reviewed at HQ010

- `HANDOFF_I06_20261111T034656Z.zip`: 18 member SHA entries verified; manifest commit `e5f36d4...`.
- `HANDOFF_C14_20261111T035747Z.zip`: 16 member SHA entries verified; manifest commit `530060c...`.
- `HANDOFF_C15_20261111T040718Z.zip`: 14 member SHA entries verified; manifest commit `178768e...`.
- `R02_batch08_evidence_package(1).zip`: archived source files and SHA256 manifest checked; R02 is separate public-evidence analysis, not an original count matrix rerun.

Reported working HEAD after C15: `6dd0cd1`; the I06 bundle only contains history through `31f7c6c`. When updating this document, also record the latest verified working SHA and the most recent off-device backup verification. **Never upload the local backup bundle or original handoff ZIPs to this public repository without separate publication review.**


## HQ011 source-index supplement (2026-11-11)

| ID | Verified handoff content | Scope of validation |
|---|---|---|
| I07 | 16/16 handoff members; local bundle through `789b21d` test-cloned and fsck passed by Codex | Not off-device, not a remote mirror of WSL Git |
| C16 | 15/15; first SB346 row failed parser; no SB345 numeric read, no QC | R04 independently identified synthetic negative count acceptance in final parser |
| C17 | 27/27; real processed PRECISE-MG1655 v1 reference-relative RPO projection on frozen PRECISE-1K 201 modules; 586 vs 584 mismatch; 4168 model genes shared | Provisional engineering, NOT independent cell-state or biological validation |
| R02-B09 | 8/8; PETRI shared source and MG1655 primary metadata audit | Original PETRI Table4 and MG1655 S1/S2/S10 row-level supplements still unavailable in R02 packet |
| R04-G02 | 9/9; source/negative synthetic audit of C16/C17 | Static/programmatic audit; no source TAR or raw-expression rerun |

Codex-reported final WSL HEAD: `ed9e342b6376f90502c42971ab07421ba6776693`. Codex-reported newer bundle SHA256 `ccea855cdfc58b5a152600e776fc8b05d71dfd4245056639232caf70c22f2f55`; HQ has not read these local Git objects through GitHub. Independent full source-matrix recalculation remains out of scope.


## HQ012 evidence audit (2026-11-11)

These are uploaded-source integrity checks, not an independent rerun of original expression matrices. ZIP CRCs PASS; I08 13/13, C18 21/21, C19 16/16, C20 15/15 and R02-B10 10/10 manifest member SHA checks PASS.

| ID | What was actually done | Outcome / claim limit |
|---|---|---|
| I08 | Read public HQ011 mirror and restored local Git bundle by clone/fsck | Private local reproducibility; off-device restore NOT VERIFIED |
| C18 | Reconstructed C17 frozen PRECISE 201×4 reference-relative module activities | Same SHA, numerical replay PASS; published-A inference semantics and external calibration remain UNKNOWN |
| C19 | Fixed negative/overflow synthetic count parsing | Real PETRI SB346 micro fragment failed unexplained schema; Phase B NOT RUN; no numeric PETRI sc QC |
| C20 | Four candidate output estimands with baselines and experiment designs | DESIGN_ONLY; had **not** competitively implemented M0/M1/M2/M3 algorithm families |
| R02-B10 | Read C17 alias crosswalk 586 rows, attempted PETRI Table4 and MG1655 S1/S2/S10 original supplements | PARTIAL / SOURCE_STOP, no L2 GT or prospective t0 bulk→t1 CFU chain |

**HQ012** retired the original C10 implementation task and authorized independent methodology review and bounded synthetic algorithm competition, including latent-population generation + bulk projection approaches, entirely independent of the student's own scVI work. See `governance/ALGORITHM_EXPLORATION_POLICY.md`. Codex-reported latest local working HEAD `e9835122b1aa6de88081f0bf60730dc03c0fe35b`; original WSL Git history is not on public GitHub.


## HQ013 source/replay supplement (2026-11-11)

| ID | Audited source and real scope | Scientific interpretation |
|---|---|---|
| I09 | user-uploaded handoff 16/16 manifest hashes | Governance: C10 retired, research M3 active, user scVI independent |
| C21 | uploaded handoff 10/10 manifest; **HQ re-executed 72/72** rows max numeric difference `4.44e-16` | SYNTHETIC_ONLY; W0 nonidentifiability proven for witness; oracle/unequal data rights; no ranking/95% calibration |
| C22 | uploaded handoff 11/11 manifest; 128 rows/8 unit crosswalks/5 candidate experiments | AUDIT_ONLY; no matrices read or real models evaluated |
| R01-B04 | 5/5 file SHA; 19 P IDs P0048–P0066 (21 columns vs 20 in catalog) | static primary-source research; 66 entries after safe merge, not systematic exhaustive |
| R03-B04 | 6/6 file SHA; 23 static method records | not 23 new installed code repos; licenses/edge requirements may be unresolved |
| R04-H02 | 12/12 file SHA; R04 re-executed C21 72 rows and posthoc RBF | source audit pass; no real expression GT |

Reported WSL HEAD after I09/C21/C22: `147c6796c46ae7112a70d5d48736b0180be20073`. Local bundle only same-disk tested. Public mirror has distinct history and no raw matrices.


## HQ014 evidence audit — 2026-11-11

| Task | File check | Scientific state |
|---|---|---|
| I10 | 16/16 source SHA | Papers 66; R03 methods static |
| C23 | 11/11 source SHA; reported numerical aggregates independently summarized | Real MATQ same-study sc assay aggregate only. M1 NNLS-postnormalized mean MAE .9571; M3 grid .9729. Marker read-detection .459 worse than prior-only .421; shuffle control invalid. No cell heterogeneity GT |
| C24 | 13/13 source SHA; R04 independently reran 2592 synthetic rows | 336 OOD-flagged output rows still have point estimates; W3 M3 RNA q selective coverage .685; no calibrated intervals or method winner |
| C25 early/mid/final | each 16/16; sequential versions of one result | Fixed RPO 201x4 output same SHA; 11/11 final tests pass; HQ independently found false reference conditions/BioSample/culture accepted by validate_contract. Source provenance NOT final |
| R01-B05 | 7/7 research SHA | Six candidates P0067-P0072 to stage; 2 primary-verified, 4 UNKNOWN |
| R03-B05 | 7/7 research SHA | 17 static baseline records; zero installed/trained here |
| R04-H03 | 13/13 nested research SHA | Adversarial review, no independently replayed raw MATQ/RPO source matrix and no culture GT |

Reported local WSL HEAD: `50fa369db75f47e9802453762a4d5543788492d7`; GitHub public mirror has separate history. Off-device backup restoration NOT VERIFIED. Active next work: I11, C26, C27, C28, conditional C29, and R02-B11. C10 retired, user scVI not a task dependency.

## HQ015 original handoff audit (2026-11-12)

Seven user-provided ZIP archives CRC PASS, **77/77 listed payload SHA256 PASS**. I11 12/12, C26 10/10, C27 11/11, C28 10/10, C29 10/10, R02-B11 11/11, R04-H04 13/13. This is not raw data rerun or local Git object verification.

| Stage | Actually reviewed | Status |
|---|---|---|
| I11 | catalog 66→72 papers (six P candidates, only 2 with conservative primary verification), local bundle | METADATA/LOCAL_GIT_REPORTED, off-device UNKNOWN |
| C26 | 28 primary lines, 12 marker lines recomputed | INTERNAL_REAL_ASSAY; 0.960590 simplex 5023 gene aggregate, marker bulk .458953 > prior .421007 |
| C27 | 7776 synthetic records and decisions parsed | SYNTHETIC; 3240 true withheld, W2 M3 false-safe 50/72 |
| C28 | source-pinned real RPO processed-bulk metadata and 201×4 output, 14 controls from independent R04 replay | PINNED_ENGINEERING_PROVISIONAL, no external biology |
| C29 | individual-sc K2 component and 12 marker outputs; recomputed 9 retained MAEs; R04-derived Jensen gap and q prior counterfactual | INTERNAL_EXPLORATORY, PHYSICAL_FORWARD_VETO, TEST_FEEDBACK_USE, 1/9 bounds coverage |
| R02-B11 | six sample rows all PLANNED, data dictionary and FISH design | DESIGN_ONLY, no physical GT |
| R04-H04 | source functions/derived-output/synthetic-control audit, 34 STOP claims | INDEPENDENT_METHOD_AUDIT, not raw-matrix replay |

Codex-reported local HEAD `860d592277071e64b80b6c1de83d920cfb1fbcab`; full work Git history not synced to public `main`. HQ015 method experiment C30 and data triage C31 are new scoped *future* tasks, not completed results.

## HQ016 original ZIP and method evidence — 2026-11-12

All **seven** supplied ZIP CRC PASS. SHA checks: I12 18/18, C30 13/13, C31 10/10, C32 12/12, R03-B06 7/7, R04-H05 10/10 = **70/70**. R02-B12 two readable files but **no internal member SHA manifest**. Actual large source matrix not contained in uploaded handoffs.

| Work | Provenance | Highest justified evidence |
|---|---|---|
| I12 | Codex reports local Git stage and source audit, 72 papers, 25 registry entries | SOURCE_GIT_REPORTED; off-device restore UNKNOWN |
| C30 | Full synthetic code, 6912 rows, 96 summary; R04 independent numeric replay max 1.78e-15 but not byte-identical; HQ 3 invalid-parameter direct sentinels | MATH/SYNTHETIC PASS; W2 inside-hull 70/72 false-safe, q coverage 0/70; nonfinite source function accepts invalid |
| C31 | 5255×12, official GEO processed .gz SHA, 12 alias joins, real file source QC as Codex report | REAL_SOURCE_QC_REPORTED; 100-cell size-sorted pools; dates/depth confounded, no culture GT, matrix absent from uploaded ZIP |
| C32 | 201×4 RPO derived activity, 10 negatives reported, second TRN source ABSTAIN; HQ direct `inspect_csv` NaN/Inf source test | PINNED_REAL_ENGINEERING_PROVISIONAL; 201 modules not state proportions; no external arbitrary bulk |
| R02-B12 | two proposed collaboration docs | DESIGN_ONLY; 0 FISH cultures collected, no input member SHA manifest |
| R03-B06 | 8×10 method physical operator matrix, 2 syntax-only reference prototypes | STATIC_PRIOR_ART; R04 tiny 2-gene smoke only, external real models NOT_RUN |
| R04-H05 | 10 audited output files, source-grade and synthetic numeric tests | INDEPENDENT_ADVERSARIAL_METHOD_AUDIT; no raw MATQ/PRECISE/GSE289312 rerun, no new GT |

Codex-reported WSL last HEAD `655f7eb` does not equal public GitHub `main`, which is an independent-history curated scientific-memory mirror. HQ016 original handoff ZIPs preserved in dispatch, not pushed publicly. C10 retired, M3 research active independent of student's scVI study.

## HQ017 source audit and new training authorization — 2026-11-12
Seven uploaded archives CRC PASS, file SHA manifest counts 18 I13 +17 C33 +15 C34 +11 C35 +13 C36 +11 R02-B13 +11 R04-H06 = 96/96. HQ separately ran original C34 five tests and full FIT; 720 set rows EXACT frozen SHA; 8640 point rows numeric within 1.22e-15 on 6336 nonblank values, not byte-exact point CSV. All actual GEO/PRECISE matrix bytes and local WSL Git objects were NOT in these uploaded packets.
| I13 | Source/local Git reported; public memory separate | local only, off-device recovery UNKNOWN |
| C33 | finite, dimensional, unit and trust validation tested in WSL; complete isolated test suite depends on C25/C28 not in C33 ZIP | FUNCTION_ENGINEERING |
| C34 | 720 set LP, 8640 point synthetic; W2 unknown state interval [0,1] despite robust coverage | SYNTHETIC/MATH, not learned population recovery |
| C35 | 5255 genes x 12 sorted 100-cell pools; no exact marker or matched mother cultures | REAL_SOURCE_TECHNICAL; no GT |
| C36 | 201x4 fixed RPO bulk projection; 14 end-to-end +5 parser negatives | DEMO-E FIXED BULK ONLY; no trained sc state |
| R02-B13 | pilot planning and PI decision brief, NOT SENT, 0 GT | DESIGN_ONLY |
| R04-H06 | independent source/derived math audit | NO_RAW_GEO_REPLAY/BIO_GT |
| HQ017 sc-reference-v0 code | HQ original implementation, four synthetic tests and CLI smoke PASS; no genuine MATQ model fitted by HQ because raw data local | IMPLEMENTATION_SMOKE; C37 REAL TRAINING AUTHORIZED NOT DONE |
| RiboD study candidate | source web-verified E.coli 3h sc GSE260457 and bulk GSE259433 within GSE260458 | WEB_SAME_STUDY only, physical culture link UNKNOWN; C38 FILE_QC pending |
Codex last reported working WSL HEAD short f5807cf. Current public main has unrelated curated history. New tasks I14/C37/C38/C39, R02-B14, R03-B07, R04-H07 not yet executed.


## HQ018 source and real methods — 2026-11-13

Eight ZIP CRC PASS; member SHA counts I14 15, C37 23, C38 13, C39 12, C40 7, R02-B14 9, R03-B07 51, R04-H07 13 = 143/143. HQ executed four C37 synthetic unit tests, original-code rank/depth counterexamples and a pi/r math sentinel; did not independently retrain missing original MATQ matrices/four fitted NPZ binaries.

C37: Codex-reported REAL sc-trained four finite models, 288 individual cells and 9 train bulk per DEV fold; 12 actual source-locked queries. Marker error from q-weighted technical detection must not be interpreted as calibrated cell detection.
C38: RiboD-PETRI real E.coli processed sc prefix and actual related bulk QC; ΔΔ protocol correction, culture and assay gates unresolved.
C39: REAL_SC_TRAINED_DEV_DEMO q=(.090952,.909048), biology ABSTAIN.
C40: joint model fit 0, PRECONDITION_FAILED; after false genotype blocker removal seven source/measurement issues remain.
R02-B14 official corrected genotype/protocol and physical aliases; R03-B07 NNLS_REF and SC_NMF executed on synthetic only; R04-H07 source/functional audit without raw MATQ replay.
I14: local Git final HEAD short decfee7 reported, off-device bundle recovery not verified. New I15/C41/C42/C43/C44/C45 experiments pending, not completed.
