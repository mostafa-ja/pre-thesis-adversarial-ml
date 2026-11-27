# 07 — Coursework and side studies

**What this is:** the study material behind the thesis work — kept for completeness, and clearly *not* part of the pipeline in sections 01–06.

The core is the four chapters of the [adversarial-ml-tutorial.org](https://adversarial-ml-tutorial.org) course, worked through with notes: the theory the malware work applies in a feature space, learned here in the image domain where the examples are easier to see. Around it are the image-domain experiments and the malware-as-images side track (transfer learning and knowledge distillation on Malimg).

## Reading order

1. [`tutorial_ch1_introduction.ipynb`](tutorial_ch1_introduction.ipynb) — fooling a ResNet50; adversarial risk; Danskin's theorem.
2. [`tutorial_ch2_linear_models.ipynb`](tutorial_ch2_linear_models.ipynb) — adversarial examples for linear models, where the attack has a closed form.
3. [`tutorial_ch3_adversarial_examples.ipynb`](tutorial_ch3_adversarial_examples.ipynb) — FGSM and PGD in depth; bound propagation, MILP and convex relaxations for exact answers.
4. [`tutorial_ch4_adversarial_training.ipynb`](tutorial_ch4_adversarial_training.ipynb) — adversarial training and relaxation-based robust training.
5. [`image_domain_experiments.ipynb`](image_domain_experiments.ipynb) — side experiments: do deltas transfer between models? forging a confident "5"; an autoencoder under FGSM; "parallel models" trained to be parameter-distant; saliency.
6. [`malware_images_transfer_learning_and_distillation.ipynb`](malware_images_transfer_learning_and_distillation.ipynb) — malware as images: the PyTorch transfer-learning tutorial, then Malimg with VGG16 features and classical classifiers, knowledge distillation on Malimg, and a first look at Kaggle IoT-malware images.
7. [`decision_boundary_demos.ipynb`](decision_boundary_demos.ipynb) — presentation notebooks: FGSM and PGD drawn on 2-D decision boundaries.

**The main line** starts at [`01-data-and-features/`](../01-data-and-features/).
