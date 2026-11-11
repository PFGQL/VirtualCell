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
