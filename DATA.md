# Data

The datasets themselves are **not** stored in this repository — only the notebooks that build and use them.

- **Drebin** — the Android malware dataset used for most detector/attack experiments (feature extraction and the Drebin-specific builds live in `01-data-and-features/`). The original workspaces kept local copies under `data/` and `drebin/` folders; those raw files were not carried over.
- **VirusTotal** — `01-data-and-features/virustotal_label_check.ipynb` queries VirusTotal for sample reports/labels used while assembling the datasets. The API key in the original notebook has been replaced with a placeholder.
- **Malimg / Kaggle IoT malware** — image datasets used only by the side studies in `07-coursework-and-side-studies/`.

Paths inside the notebooks point at the original local/Colab locations; treat them as documentation of how the data was laid out at the time, not as runnable defaults.
