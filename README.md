# Pre-Thesis Adversarial ML

The work before the paper: the notebooks that led to my M.Sc. thesis and to **sigma-binary**, the method published in *"Evaluating the Robustness of Adversarial Defenses in Malware Detection Systems"* (Computers & Electrical Engineering, 2026).

The final method lives in its own repository — [sigma-binary](https://github.com/mostafa-ja/sigma-binary). This repository is the road to it, told as one story in seven chapters.

*A note on dates: the notebooks date from the thesis work itself. They were gathered from ten earlier repositories and consolidated into this edition in November 2026; the executed originals remain in those (now archived) repositories.*


## The story

Malware detectors are machine-learning models, and machine-learning models can be fooled. This repository follows one question through the whole arc of the research: **how robust are Android malware detectors and their defences against adversarial examples — perturbations that change a malware sample's features without changing what it does?**

1. **Data** — Android apps become feature vectors: the Drebin dataset is built, features are extracted, ranked, and mapped to what an attacker is actually allowed to change.
2. **Detectors** — the baseline classifiers (DNN, CNN, and early explorations) that everything else attacks or defends.
3. **Attacks** — PGD, genetic algorithms, and the CW-sine lineage: the long search for an attack that works in the binary, constrained feature space of malware. This search is where sigma-binary comes from.
4. **Defences** — the defence suite from the paper: adversarial training, the KDE/DLA/DNN+/ICNN detectors, PAD, and the σ-zero attack used to stress them all.
5. **A contrastive detour** — a separate study: can contrastive learning make a detector harder to fool? (Attacked with the same CW machinery, it could not.)
6. **The thesis evaluation** — everything brought together under one protocol: eight models, five attacks, clean/PGD/CW/σ-zero/adaptive/mimicry/oblivion, and the comparisons the paper's tables are built from.
7. **Coursework** — the tutorial chapters and side studies the work grew out of, kept for completeness and labelled as such.

## How it is organised

| Section | What is in it |
|---|---|
| [`01-data-and-features/`](01-data-and-features/) | Dataset building, Drebin feature extraction, feature importance, manipulation maps |
| [`02-detectors/`](02-detectors/) | The baseline DNN/CNN malware detectors everything else attacks or defends |
| [`03-attacks/`](03-attacks/) | The attack library, PGD builds and analysis, the genetic-algorithm attack, and the CW sine lineage that became sigma-binary |
| [`04-defenses/`](04-defenses/) | The defence suite: adversarial training, KDE, DLA, ICNN, DNN+, PAD, RBF, σ-zero |
| [`05-contrastive-learning/`](05-contrastive-learning/) | The contrastive-learning study and the CW attacks run against it |
| [`06-thesis-evaluation/`](06-thesis-evaluation/) | The final thesis experiments: effectiveness, robustness, comparisons, tuning |
| [`07-coursework-and-side-studies/`](07-coursework-and-side-studies/) | Coursework and side studies, kept for completeness and labelled as such |

Each section has its own README that introduces its question and lists its notebooks in reading order. Every notebook opens with its purpose, where it fits in the story, and where its material came from.

## How this repository was made

Gathered in November 2026 from ten earlier repositories (`thesis`, `PGD_form_attacks`, `Adversarials`, `CW-CL`, `contrastive-learning`, `a_malware`, `a_malware2`, `mal_adv3`, `mal_adv4`, `mal_adv5` — all now archived, originals untouched). Of 141 notebooks found, 111 were kept; those 111 were then **consolidated by topic into the 49 notebooks here**: repeated runs of one configuration are shown once, duplicate code is merged, and every notebook is structured into numbered steps with explanations. Outputs are cleared in these consolidated notebooks — the executed originals remain in the archived source repositories. Datasets are not included — see [`DATA.md`](DATA.md).

## A note on credentials

Two notebooks from `a_malware` originally contained a hard-coded GitHub token, and two others a VirusTotal API key; all were replaced with placeholders before this repository was published, and the repository's history was built clean, so no credential appears in any revision. If you forked an early version, rotate those credentials.
