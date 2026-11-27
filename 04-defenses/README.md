# 04 — Defences

**The question:** once the attacks work, what can be done about them — and how much of each defence survives a serious attack?

This section builds the defence suite that the paper evaluates: adversarially trained classifiers, and detectors (KDE, DLA, DNN+, ICNN, PAD) that try to catch adversarial examples rather than classify through them. It also builds the σ-zero attack — the stress test the suite is measured with here, before the full evaluation in `06-thesis-evaluation/`.

## Reading order

1. [`sigma_zero_attack.ipynb`](sigma_zero_attack.ipynb) — the σ-zero attack: the yardstick for the rest of the section.
2. [`adversarial_training_defenses.ipynb`](adversarial_training_defenses.ipynb) — hardening the classifiers themselves (AT-rFGSM, AT-MaxMA and relatives).
3. [`detection_defenses.ipynb`](detection_defenses.ipynb) — the detection idea and the combined detector builds, including ICNN and PAD.
4. [`kde_defense.ipynb`](kde_defense.ipynb) — the KDE detector, from the first version to the GKDE arc.
5. [`rbf_defense.ipynb`](rbf_defense.ipynb) — the RBF-network defence: build, visualisation, and attacking it.
6. [`mimicry_and_ddn_vs_defenses.ipynb`](mimicry_and_ddn_vs_defenses.ipynb) — mimicry and DDN attacks run against the defences.
7. [`sigma_tuning_and_comparison.ipynb`](sigma_tuning_and_comparison.ipynb) — tuning σ, and σ-zero head-to-head against CW.
8. [`tsne_model_comparison.ipynb`](tsne_model_comparison.ipynb) — a t-SNE look at how the models' representations differ.

**Before:** the attacks these defend against are in [`03-attacks/`](../03-attacks/). **Next:** a detour — [`05-contrastive-learning/`](../05-contrastive-learning/) asks whether a different training objective helps at all; then [`06-thesis-evaluation/`](../06-thesis-evaluation/) measures everything in this section under one protocol.
