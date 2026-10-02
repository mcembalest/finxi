# analysis (claude, terse, for reconstruction)

## babel / solomonoff / chaitin
- Borges' Babel: fixed-length books, finite → generalize: all finite strings
- index entry = halting program p → string U(p)
- weight m(x) = Σ over p with U(p)=x of 2^−|p| ([solomonoff1964](../references/solomonoff1964-formal-theory-inductive-inference-pt1.pdf))
- coding theorem: −log m(x) = K(x) + O(1) ([chaitin2004](../references/chaitin2004-meta-math-math0404335.pdf))
- prefix-free programs → Kraft: Σ 2^−|p| ≤ 1 → "random entry" well-defined
- Ω = weight of halting entries; uncomputable → index can't be consulted → search, not lookup
- weights depend on machine = primitives ([leike2015](../references/leike2015-bad-universal-priors-1510.04931.pdf)); K invariant up to a constant
- time-bounded search: Levin Kt(x) = min(|p| + log t) (not cited)
- baselines per X:
  - Babel texts: ~|Σ|^|x| draws
  - index sampling: ~2^K(x) draws (= zero-data g₀; [Table 1](../references/cowsik2026-self-play-zero-data-2609.30063.pdf) ">53,000")
  - GEN: Table 1, e.g. Fibonacci round 512

## meng
- sample mean − population mean = ρ × √((1−f)/f) × σ ([meng2018](../references/meng2018-big-data-paradox-aoas1161sf.pdf))
- quality × quantity × difficulty; CCES n≈2.3M ≈ random n≈400
- population = whole index → f≈0 → any ρ≠0 dominates
- natural data = nonrandom selection; D_u ∝ D^μ as effective size (zero-data §4, eqs 7–13)
- generator = selection mechanism; ρ large by design
- estimating: ρ = defect / teaching: ρ = lesson
- exact for: benchmark means; estimates from searching the log
- selection can change the exponent ([sorscher2022](../references/sorscher2022-beyond-neural-scaling-laws-2206.14486.pdf))

## pfn
- train on samples from prior → posterior predictive under prior ([muller2022](../references/muller2022-pfn-transformers-bayesian-inference-2112.10510.pdf))
- PFN + Solomonoff prior = [graumoya2024](../references/graumoya2024-learning-universal-predictors-2401.14953.pdf)
- zero-data learner = PFN; g₀ = Solomonoff prior; self-play = learned prior
- TabPFN: hand-designed prior ([Nature 2025](https://doi.org/10.1038/s41586-024-08328-6)); KumoRFM-2: synthetic + real ([arXiv 2604.12596](https://arxiv.org/abs/2604.12596))
- open: prior changes every round → learner ≈ mixture of priors seen
- craftsman = prior designer
- learner sees outputs, never programs = magician

## powerplay
- accept (task, solver) iff old fails ∧ new succeeds ∧ all old tasks still solved ([schmidhuber2011](../references/schmidhuber2011-powerplay-1112.5309.pdf))
- no reward: predicate + search order (cheapest to invent/verify first)
- split across two minds: invention → craftsman shows (or apprentice first); solver modification → the one shown learns; correctness demo → honest finxi
- sketches:
  - A: powerplay split
  - B: novel to maker ∧ learnable by other ([hughes2024](../references/hughes2024-open-endedness-2406.04268.pdf))
  - C: Pareto frontier ([GEPA](https://arxiv.org/abs/2507.19457))
- not borrowed (TBD): compression progress → S=HEN?
- open: forgetting? powerplay forbids; Eco / Funes

## baselines (laptop)
- Babel texts: computed, no run
- uniform-prior sampling (g₀)
- zero-data GEN (learning-progress reward)
- POWERPLAY
- POET later, at N learners ([wang2019](../references/wang2019-poet-1901.01753.pdf))

## authorship
- creations content-addressed: identical = one row → rediscovery free
- log records acts (who, inputs, output, when, seed), not authors
- authorship / priority / credit = agents' interpretation
- why: Conway (gliders, no author); Turing (judge behavior); Perdix (priority dispute); identity by content
- git: blobs no author, commits authored
- independence: one typed log (event / communication / creation) → "shown before made?" answerable

## kernels before isomorphism
- program sameness undecidable (Rice); depth unprovable (Chaitin)
- → bounded makers need graded similarity = kernel
- prediction: kernel-like tools before isomorphism/category-like ones
- kernels, circuits ≠ primitives (buildable from map, pair, frac, list); lens on the log instead
- kernel → circuit regimes in training: [Kumar et al. 2023](https://arxiv.org/abs/2310.06110), [Merrill et al. 2023](https://arxiv.org/abs/2303.11873)

## representation
- same outputs, different internals; open-ended search → unified ([kumar2025](../references/kumar2025-fractured-entangled-representation-2505.11581.pdf))
