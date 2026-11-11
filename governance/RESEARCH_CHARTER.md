# Founding research charter / 最初科研目标约束

**Status: enduring mission, not a frozen method choice.** Written as a public, identity-minimized reconstruction of the original project brief, not a literal transcript.

## The biological problem

Bacterial scRNA-seq is still sparse, platform-dependent and limited in experimental scale. Large public bacterial bulk RNA-seq collections span many conditions, but a bulk average loses population heterogeneity. VirtualCell seeks a scientifically defensible way to use **many bacterial bulk profiles plus limited authentic bacterial single-cell measurements**.

**Target user input:** a new bacterial bulk RNA-seq experiment, with measured units, species/strain, metadata and a documented reference/calibration where required.

**Intended output:** one or more measurable, biologically meaningful **intermediate-resolution population quantities** (between a bulk expression vector and a full single-cell joint distribution). The output is *not specified in advance*; it must be selected by biological value, identifiability, data availability, reproducibility, novel prior art boundaries and capacity for independent validation. It may be continuous programs, identifiable state-weighted signal, targeted marker/operon functionals, response-relevant representation, or an uncertainty/abstention set.

**Undergraduate deliverable:** a convincing, honest and reproducible research/demo tool that can be shown to experimental collaborators. Its engineering baseline may be an established method; any claimed scientific contribution requires its own evidence.

**PhD horizon:** develop substantive original methods/biology, potentially including response to perturbations, out-of-condition and cross-strain generalization, mechanistic experiments and prospective validation. High-impact publication is an ambition, **never a substitute for scientific rigor**.

## How this project must be managed

- Research leadership coordinates distinct literature (R01), data/ground truth (R02), algorithm/prior art (R03), adversarial critique (R04), local Git/Codex and a scientific HQ decision process.
- **No pretend exhaustive search.** Record search coverage, access failures, unknowns, competing studies and selection bias.
- Data portfolio and scientific estimands must update each other: do not select MATQ/PETRI/RiboD only because files are convenient, or select a VAE because it is interesting to build.
- Compare **identical information permissions**, preserve independent cultures and metadata joins, and report test-data leakage risks.
- Real negative findings and ABSTAIN are valid research outcomes.
- Research supervisor may revise any candidate hypothesis in light of stronger evidence. The student's interest in scVI/scIB is personal study and does **not** gate research progress.
- Decisions persist through Git-authored evidence and explicit state snapshots, **not presumed assistant memory**.

## Candidate methods are hypotheses, not mandates

A: regulatory module activity and potentially continuous program coordinates.  
B: limited reference-conditioned RNA-expression contribution / identification interval, not automatic cell fractions.  
C: targeted distribution functionals, e.g., FISH marker detection/co-detection or defined operon heterogeneity; not automatically identifiable from bulk means.  
D: prospective, matched pre-perturbation bulk + intervention to future phenotype; not post-treatment description.  
E: hybrid bulk/sc representation or generative strategy; must demonstrate improvement over equal-information bulk-only controls.

**E+A+D is an explicitly uncommitted hypothesis.** A can provide coordinates, a prior or an evaluation proxy; using A for both training and truth is circular. E alone is not innovative. D requires a real temporal phenotype chain.

## Hard boundary

A model should never output a confident full single-cell distribution, cell fraction or future survival label when the measured information and validated assumptions do not identify it. STOP/ABSTAIN should be a first-class software result.


## HQ012 clarification — algorithm exploration is independent of student scVI work

The research director must continue independent, evidence-driven method development and discovery **including** latent-population generators with bulk projectors, as well as explicit mixture, program constraints, Bayesian and partial-identification alternatives. The student’s personal scVI/scIB learning or intended scVI modifications **never constitute a prerequisite**, steering vote, or experimental Gate. **E+A+D remains one unprivileged hypothesis.** No new model is chosen in advance. See [open competition policy](ALGORITHM_EXPLORATION_POLICY.md).
