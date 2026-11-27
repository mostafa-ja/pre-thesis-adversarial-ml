# 01 — Data and features

**The question:** what does an Android app look like to a machine-learning model, and which parts of that description is an attacker allowed to change?

Everything later in this repository stands on this section: the Drebin feature vectors, the sparse-matrix form the models consume, and — crucially for the attacks — the *manipulation maps* that record which features can be added or removed without breaking the app. An adversarial example that ignores those maps is fiction; the attacks in `03-attacks/` are built on them.

## Reading order

1. [`building_the_dataset.ipynb`](building_the_dataset.ipynb) — assembling the dataset from the raw collections.
2. [`static_analysis_and_feature_sets.ipynb`](static_analysis_and_feature_sets.ipynb) — static analysis of the apps and the feature sets it produces.
3. [`drebin_to_sparse_matrices.ipynb`](drebin_to_sparse_matrices.ipynb) — the Drebin features in the sparse-matrix form the detectors train on.
4. [`feature_importance.ipynb`](feature_importance.ipynb) — which features matter, and to which model.
5. [`pca_feature_analysis.ipynb`](pca_feature_analysis.ipynb) — the feature space under PCA: structure, clusters, outliers.
6. [`manipulation_maps.ipynb`](manipulation_maps.ipynb) — the maps of manipulable features that constrain every attack in this repository.
7. [`virustotal_label_check.ipynb`](virustotal_label_check.ipynb) — cross-checking labels against VirusTotal reports.

**Next:** the detectors trained on this data are in [`02-detectors/`](../02-detectors/).
