# 03 — Attacks

**The question:** how do you fool a malware detector when the input is a binary feature vector and only some features may change?

This is the longest search in the repository. It starts with a shared attack library and the first-generation attacks, works through PGD in depth, tries a genetic algorithm, and ends with the CW-sine lineage — the line of experiments that, refined, became the σ-binary attack of the thesis and the paper. If you read one section closely, read the last notebook here.

## Reading order

1. [`attack_library.ipynb`](attack_library.ipynb) — the shared attack functions everything else imports or copies.
2. [`first_generation_attacks.ipynb`](first_generation_attacks.ipynb) — the first attack experiments against the early detectors.
3. [`attack_bench.ipynb`](attack_bench.ipynb) — a bench for running attacks side by side, including the Drebin bench.
4. [`pgd_and_adversarial_training_first_codebase.ipynb`](pgd_and_adversarial_training_first_codebase.ipynb) — PGD (and a first adversarial training) in the first codebase: the PGD2 build, the draft, and the Max/StepwiseMax variants.
5. [`pgd_analysis.ipynb`](pgd_analysis.ipynb) — PGD taken apart: what the iterations, norms and step sizes actually do.
6. [`genetic_algorithm_attack.ipynb`](genetic_algorithm_attack.ipynb) — a gradient-free alternative, in its three versions.
7. [`cw_sine_lineage.ipynb`](cw_sine_lineage.ipynb) — the CW attack with the sine reparameterisation, through its versions to the complete build. This is the direct ancestor of σ-binary.

The image-domain attack experiments (FGSM on MNIST and friends) live with the coursework in [`07-coursework-and-side-studies/`](../07-coursework-and-side-studies/), where they belong.

**Before:** the detectors under attack are in [`02-detectors/`](../02-detectors/), and the manipulation maps that constrain these attacks are in [`01-data-and-features/`](../01-data-and-features/). **Next:** defending against them, in [`04-defenses/`](../04-defenses/).
