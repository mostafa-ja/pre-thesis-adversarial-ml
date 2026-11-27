# 06 — Thesis evaluation

**The question:** measured one fair way, how robust is each defence — against each attack?

The culminating section, and the organised form of the thesis experiments behind the paper. One protocol throughout: the same data, the same manipulation mask, the same scoring; eight models (DNN, AT-rFGSM, AT-MaxMA, KDE, DLA, DNN+, ICNN, PAD); results saved as tensor archives so the comparisons read from the runs themselves. The defences come from `04-defenses/`, the attacks from `03-attacks/`, and the final published method lives in the separate sigma-binary repository.

## Reading order

1. [`clean_evaluation.ipynb`](clean_evaluation.ipynb) — the baseline: every model on clean data, thresholds set. Every later number is measured against this.
2. [`pgd_effectiveness.ipynb`](pgd_effectiveness.ipynb) — PGD in L0, L2 and L∞ against four models.
3. [`cw_effectiveness.ipynb`](cw_effectiveness.ipynb) — the CW attack against four models.
4. [`sigma_zero_effectiveness_and_tuning.ipynb`](sigma_zero_effectiveness_and_tuning.ipynb) — σ-zero against five models, plus the parameter tuning for the detectors.
5. [`adaptive_attack_effectiveness.ipynb`](adaptive_attack_effectiveness.ipynb) — the main event: the σ-binary attack, adaptive (the attacker knows the defence), against all eight models, with the cross-model comparison.
6. [`mimicry_effectiveness.ipynb`](mimicry_effectiveness.ipynb) — the mimicry baseline against all eight models.
7. [`oblivion_attack_robustness.ipynb`](oblivion_attack_robustness.ipynb) — the complement of the adaptive runs: σ against the five detectors with an *unaware* attacker, scored conservatively and deferred. Together with the adaptive notebook, it brackets what the detectors are worth.
8. [`visualizing_adaptive_attack.ipynb`](visualizing_adaptive_attack.ipynb) — what the adaptive adversarial examples actually look like.
9. [`comparisons.ipynb`](comparisons.ipynb) — the reporting layer: attacks against each other from the archived tensors, and the rounding comparison (none / thresholded / probabilistic / prioritised) that the method's binarisation choice rests on.

**Before:** [`04-defenses/`](../04-defenses/) builds what is measured here. **After:** the method itself, in [sigma-binary](https://github.com/mostafa-ja/sigma-binary).
