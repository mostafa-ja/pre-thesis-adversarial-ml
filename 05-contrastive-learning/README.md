# 05 — Contrastive learning

**The question:** does training a detector with a contrastive objective make it harder to fool?

A self-contained study from 2024: a supervised-contrastive (SupCon) malware detector is built, trained several ways, and then attacked with the same CW machinery used in `03-attacks/` — including boundary and mimicry attacks aimed at its embedding space. The answer the experiments give is no: the contrastive model falls to the same attacks, which is part of why the thesis returned to the defence suite of `04-defenses/`.

## Reading order

1. [`supcon_detector.ipynb`](supcon_detector.ipynb) — the supervised-contrastive detector itself.
2. [`contrastive_training_strategies.ipynb`](contrastive_training_strategies.ipynb) — four training strategies compared (Steps A–D).
3. [`adversarial_contrast_learning.ipynb`](adversarial_contrast_learning.ipynb) — adversarial training meets contrastive learning, in its versions.
4. [`cw_attacks_on_contrastive_model.ipynb`](cw_attacks_on_contrastive_model.ipynb) — the CW attack against the contrastive model.
5. [`cw_analysis_lr_loss.ipynb`](cw_analysis_lr_loss.ipynb) — analysing those attacks: learning rates and loss behaviour.
6. [`attacking_the_contrastive_model.ipynb`](attacking_the_contrastive_model.ipynb) — further attacks on the model.
7. [`boundary_and_mimicry_attacks.ipynb`](boundary_and_mimicry_attacks.ipynb) — boundary and mimicry attacks; the best adversarial confidences reached are recorded in the runs.

**Context:** the CW attack used here comes from [`03-attacks/`](../03-attacks/); the main line of the research continues in [`06-thesis-evaluation/`](../06-thesis-evaluation/).
