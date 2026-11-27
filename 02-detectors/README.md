# 02 — Detectors

**The question:** what does a straightforward malware detector look like, before anyone tries to defend or fool it?

These are the baseline classifiers — the models that the attacks in `03-attacks/` learn to evade and the defences in `04-defenses/` learn to protect. The DNN detector here is the direct ancestor of the classifiers used throughout the thesis evaluation in `06-thesis-evaluation/`.

## Reading order

1. [`first_dnn_md_nn.ipynb`](first_dnn_md_nn.ipynb) — the very first DNN experiments on the malware data.
2. [`dnn_detector.ipynb`](dnn_detector.ipynb) — the DNN detector in its two builds, merged; the learning-rate schedule difference between them is flagged where it matters.
3. [`cnn_detector.ipynb`](cnn_detector.ipynb) — the CNN variant (the BatchNorm version that actually ran is the one kept).
4. [`clustering_kde_exploration.ipynb`](clustering_kde_exploration.ipynb) — exploring the data with clustering and KDE — the seed of the KDE detector that becomes a full defence in `04-defenses/`.

**Before:** the data these train on is built in [`01-data-and-features/`](../01-data-and-features/). **Next:** attacking them, in [`03-attacks/`](../03-attacks/).
