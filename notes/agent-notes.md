# agent notes (terse, for reconstruction; see AGENTS.md)

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

## eurekabench ([geng2026](../references/geng2026-eurekabench-2610.00492.pdf))
- 26 tasks, 6 domains, 306 insight questions
- scores: predictive accuracy (PA) vs scientific insight (SI)
- best agents ≈ human PA (47.4 vs 48.8), far below human SI (42.4 vs 69.7)
- role: eval data only, not method inspiration
- scale mismatch: H100, 1,000 iterations, 4h, frontier LLM agents, simulator CLIs, LLM judges
- tiny laptop GEN can't run it directly
- possible transfer test: give an agent the workshop log/creations as a library → does SI change?
- contamination: web blocked, pretraining exposure not ruled out

## schaeffer: tokenizer myths ([thread](https://x.com/RylanSchaeffer/status/2106082985032454155))
- BPB = tokens/byte × bits/token → not tokenizer-agnostic (random init prefers V≈24K)
- lower BPB ≠ better model: random-init BPB varies with V, accuracy flat at chance
- trilemma: only truth scores best / same predictions same score / untrained models tie → pick two
- "BPB tells us about coding length, nothing else"
- "intelligence is … discriminating correct from plausible-but-incorrect continuations" (his tin-foil-hat claim)
- zero-data paper: scaling laws + transfer reported in BPB ([cowsik2026](../references/cowsik2026-self-play-zero-data-2609.30063.pdf) Figs 1, 2, 7)
  - fixed byte vocab (256) → myth #1 mostly avoided within their comparisons
  - myth #2 applies: BPB transfer ≠ downstream ability
- role: inspiration for S≠HEN
- → "have they created X yet" over BPB
- discrimination ↔ GAN discriminator ↔ honest finxi check?

## datasets in the 20 references (skimmed via text + links; ✓ = link found in paper, ? = from memory, verify)
- useful now
  - grau-moya 2024: UTM / Solomonoff data generators, Chomsky-hierarchy tasks ✓ [neural_networks_solomonoff_induction](https://github.com/google-deepmind/neural_networks_solomonoff_induction), [chomsky](https://github.com/google-deepmind/neural_networks_chomsky_hierarchy)
  - cowsik 2026: zero-shot eval set ✓ (no code link found)
    - math: Metamath set.mm ✓ [metamath](https://github.com/metamath/) ← closest to "universal mathematical structure"
    - code: AITDCC C source ✓ [aitdcc](https://github.com/AITDCC/aitdcc.github.io), GitHub Python
    - text DCLM; images CIFAR-10; audio Speech Commands, ESC-50, PCM; MIDI Mutopia; DNA
    - Table 1 sequence families (arithmetic, Fibonacci, geometric, quadratic, cubic) → template for X
  - finzi 2026: epiplexity estimation code ✓ [epiplexity](https://github.com/shikaiqiu/epiplexity) → measure structure in the log; datasets used: OpenWebText, SlimPajama, Lichess positions, CIFAR-5M ✓
  - müller 2022: PFN priors as data generators ? [TransformersCanDoBayesianInference](https://github.com/automl/TransformersCanDoBayesianInference); demo ✓ HF space
- useful later
  - eurekabench 2026: 26 tasks, 306 insight questions, simulators ✓ Zenodo [10.5281/zenodo.22110253](https://doi.org/10.5281/zenodo.22110253) (verify it is the benchmark release); GitHub + website linked
  - kumar 2025: Picbreeder genomes (human open-ended creations) ✓ [fer](https://github.com/akarshkumar0101/fer)
  - voyager 2023: skill library = example log of creations ? [MineDojo/Voyager](https://github.com/MineDojo/Voyager)
  - poet 2019: environment generator ? [uber-research/poet](https://github.com/uber-research/poet)
- not useful for finxi
  - goodfellow 2014: MNIST, TFD, CIFAR-10
  - sukhbaatar 2017: Mazebase, RLLab envs
  - sorscher 2022: CIFAR-10, SVHN, ImageNet (pruning metrics; release ?)
  - meng 2018: CCES 2016 survey (stats demo only)
- no data: hutter, leike, solomonoff, chaitin, schmidhuber 2008, powerplay, hughes, schaeffer (thread)
- not in refs but obvious for X: OEIS (integer sequences)

## OEIS rediscovery (small, for fun)
- question: which OEIS sequences show up in the log, when, in what order
- data ✓: [stripped.gz](https://oeis.org/stripped.gz) (A-number + first terms, ~34 MB), [names.gz](https://oeis.org/names.gz); license CC BY-SA 4.0 ?
- milestone subset ✓: keyword:core = 183 sequences ([search](https://oeis.org/search?q=keyword:core)) e.g. A000040 primes
- match: creation output (integer list) vs OEIS prefixes
  - require ≥ ~10 terms; short prefixes match too many
  - byte substrate → values mod 256 (zero-data Table 1 matches "family (mod 256)"); int primitive avoids this
- exclude X derivable trivially from primitives (constant, naturals) → per notes: only X absent at start
- per sequence: first round seen, who made it (craftsman / apprentice), shown before made?
- baseline: expected first round under index sampling (~2^K(x)) vs GEN
- replays → order + variance of first appearance
- keep small: core subset, exact prefix match, no fuzzy search
