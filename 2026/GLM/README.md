# Deep Learning Methods: Genomic Language Models

**BMI 511 — Spring 2026**  
**Instructor:** Pratik Dutta, Ph.D. | Department of Biomedical Informatics, Stony Brook University

---

## Lecture Materials

| Material | Description |
| --- | --- |
| `GLM_Lecture.pptx` *(to be added)* | Lecture slides (~30–35 min presentation) covering transformers for DNA, tokenization, DNABERT-2 / Nucleotide Transformer / HyenaDNA, fine-tuning recipe, and variant effect prediction |

## Google Colab Notebooks

| # | Notebook | Topics | Open in Colab | Time |
| --- | --- | --- | --- | --- |
| 1 | [Introduction to Genomic Language Models](https://github.com/duttaprat/BMI_511/blob/main/2026/GLM/NB1_Intro_to_Genomic_Language_Models.ipynb) | What is a gLM; character vs k-mer vs BPE tokenization; loading DNABERT-2; first forward pass; per-token and sequence embeddings | [Open In Colab](https://colab.research.google.com/github/duttaprat/BMI_511/blob/main/2026/GLM/NB1_Intro_to_Genomic_Language_Models.ipynb) | ~25 min |
| 2 | [Sequence Embeddings & Visualization](https://github.com/duttaprat/BMI_511/blob/main/2026/GLM/NB2_Sequence_Embeddings_Visualization.ipynb) | Batched embedding extraction; PCA / t-SNE / UMAP projection; cosine similarity heatmap; linear-probe logistic regression on frozen embeddings | [Open In Colab](https://colab.research.google.com/github/duttaprat/BMI_511/blob/main/2026/GLM/NB2_Sequence_Embeddings_Visualization.ipynb) | ~30 min |
| 3 | [Fine-tuning DNABERT-2 for Promoter Classification](https://github.com/duttaprat/BMI_511/blob/main/2026/GLM/NB3_Finetune_DNABERT2_Promoter.ipynb) | Full fine-tuning with HuggingFace `Trainer`; train/val/test split; accuracy, F1, MCC, confusion matrix; comparison against linear-probe baseline | [Open In Colab](https://colab.research.google.com/github/duttaprat/BMI_511/blob/main/2026/GLM/NB3_Finetune_DNABERT2_Promoter.ipynb) | ~40 min |
| 4 | [Variant Effect Prediction](https://github.com/duttaprat/BMI_511/blob/main/2026/GLM/NB4_Variant_Effect_Prediction.ipynb) | Non-coding variant scoring; embedding shift; masked-LM log-likelihood ratio; connection to DeepVRegulome pipeline | [Open In Colab](https://colab.research.google.com/github/duttaprat/BMI_511/blob/main/2026/GLM/NB4_Variant_Effect_Prediction.ipynb) | ~30 min |
| 5 | [Comparing Embeddings Across GLMs](https://github.com/duttaprat/BMI_511/blob/main/2026/GLM/NB5_Comparing_Embeddings_Across_GLMs.ipynb) | Side-by-side DNABERT / DNABERT-2 / Nucleotide Transformer / HyenaDNA; UMAP + t-SNE; silhouette score; linear-probe accuracy; tokenization + PCA analysis; Evo/Evo2 as exercises | [Open In Colab](https://colab.research.google.com/github/duttaprat/BMI_511/blob/main/2026/GLM/NB5_Comparing_Embeddings_Across_GLMs.ipynb) | ~40 min |

## Suggested Teaching Flow (3 hours)

```
[0:00–0:35]   Lecture slides (presentation)
[0:35–1:00]   Notebook 1 — Intro to gLMs (tokenization + first forward pass)
[1:00–1:35]   Notebook 2 — Embeddings & visualization (PCA/UMAP + linear probe)
[1:35–1:45]   Break
[1:45–2:20]   Notebook 3 — Fine-tuning DNABERT-2 (main hands-on lab)
[2:20–2:40]   Notebook 4 — Variant effect prediction (capstone + DeepVRegulome link)
[2:40–3:00]   Notebook 5 — Model comparison (assign as take-home if short on time)
```

## Concepts Covered

* **Transformers for DNA**: encoder architecture, attention, masked-language-model objective
* **Tokenization**: character, overlapping k-mer, Byte-Pair Encoding (BPE)
* **Pretrained models**: DNABERT, DNABERT-2, Nucleotide Transformer, HyenaDNA, Enformer
* **Embeddings**: mean vs `[CLS]` pooling, dimensionality reduction, linear probing
* **Fine-tuning**: HuggingFace `Trainer`, learning rate, epochs, evaluation metrics (Accuracy, F1, MCC)
* **Variant effect prediction**: embedding shift, log-likelihood ratio, regulatory variant prioritization

## Requirements

All notebooks run in Google Colab with a **T4 GPU** (Runtime → Change runtime type → T4 GPU). Core libraries:

* `transformers`, `datasets`, `accelerate`, `torch`
* `scikit-learn`, `umap-learn`
* `numpy`, `pandas`, `matplotlib`, `seaborn`

Notebook 1 runs without a GPU; Notebooks 2–4 strongly benefit from one; Notebook 3 requires a GPU.

## Further Reading

* **DNABERT** (Ji et al., *Bioinformatics* 2021) — original gLM with overlapping k-mer tokenization
* **DNABERT-2** (Zhou et al., *ICLR* 2024) — BPE-tokenized, multi-species, efficient
* **Nucleotide Transformer** (Dalla-Torre et al., *Nature Methods* 2024) — 500M–2.5B parameters, 850 species
* **HyenaDNA** (Nguyen et al., *NeurIPS* 2023) — 1 Mb context via Hyena operators
* **DeepVRegulome** (Dutta et al., arXiv:2511.09026) — interpretable regulatory variant impact prediction on top of fine-tuned DNABERT models  
  Project: [`DavuluriLab/DeepVRegulome`](https://github.com/DavuluriLab/DeepVRegulome) · Package: `pip install deepvregulome` · Demo: [deepvregulome.streamlit.app](https://deepvregulome.streamlit.app)
