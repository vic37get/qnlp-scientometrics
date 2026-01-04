# Scientometric Analysis of Quantum Natural Language Processing (QNLP)

This repository contains the **code, data processing scripts, and analysis pipelines** used in the article:

> **A Scientometric Review of Practical Applications in Quantum Natural Language Processing (QNLP): Trends, Gaps, and Research Opportunities**
> *Victor R. Silva et al., IEEE Access, 2025*

The goal of this repository is to ensure **reproducibility, transparency, and extensibility** of the scientometric study, enabling other researchers to replicate the analyses, adapt the pipeline to other domains, or extend the results with new data.

---

## 📌 Overview

Quantum Natural Language Processing (QNLP) is an emerging interdisciplinary field at the intersection of **quantum computing**, **machine learning**, and **natural language processing**. Despite rapid growth, research remains fragmented.

This repository supports a **large-scale scientometric and bibliometric analysis** of QNLP literature, including:

* Temporal evolution of publications
* Author productivity and collaboration networks
* Core journals and sources (Bradford’s Law)
* Country-level scientific production
* Keyword co-occurrence, thematic maps, and research gaps
* Identification of underexplored application domains (e.g., healthcare)

The analyses follow **PRISMA guidelines** and rely on data collected from **Scopus** and **Web of Science** (2014–2024).

---

## 🧠 Repository Structure

```text
scientometric_qnlp/
├── data/
│   ├── raw/                  # Raw bibliographic data (Scopus & WoS exports)
│   ├── processed/            # Cleaned and merged datasets
│   └── metadata/             # Auxiliary files (keywords, filters, mappings)
│
├── notebooks/
│   ├── preprocessing.ipynb   # Data cleaning, deduplication, PRISMA filtering
│   ├── analysis.ipynb        # Core scientometric indicators
│   └── visualization.ipynb  # Plots, networks, and thematic maps
│
├── scripts/
│   ├── prisma_filter.py      # Automated PRISMA-based filtering
│   ├── keyword_cleaning.py   # Keyword normalization and pruning
│   └── metrics.py            # Bibliometric indicators
│
├── results/
│   ├── figures/              # Final plots and network visualizations
│   └── tables/               # Summary tables used in the article
│
├── requirements.txt
├── LICENSE
└── README.md
```

---

## 🔧 Tools and Technologies

The study combines **Python-based data processing** with **specialized bibliometric tools**:

* **Python** (pandas, numpy, matplotlib, seaborn)
* **Bibliometrix / Biblioshiny (R)** – descriptive indicators and thematic maps
* **VOSviewer** – co-authorship, co-citation, and keyword networks
* **PyBIBix** – bibliographic data parsing

> ⚠️ Some visualizations (e.g., VOSviewer maps) are generated externally and imported into this repository.

---

## ▶️ How to Reproduce the Analysis

1. **Clone the repository**

```bash
git clone https://github.com/vic37get/scientometric_qnlp.git
cd scientometric_qnlp
```

2. **Install dependencies**

```bash
pip install -r requirements.txt
```

3. **Add bibliographic data**
   Place Scopus and Web of Science exports (`.bib`, `.csv`, or `.txt`) into:

```text
data/raw/
```

4. **Run preprocessing and analysis notebooks**
   Execute the notebooks in order:

* `notebooks/preprocessing.ipynb`
* `notebooks/analysis.ipynb`
* `notebooks/visualization.ipynb`

5. **(Optional) Run Biblioshiny**

```r
biblioshiny()
```

Then upload the processed datasets from `data/processed/`.

---

## 📊 Main Outputs

The pipeline produces:

* Annual publication growth curves
* Lotka’s Law author productivity analysis
* Bradford’s Law core journals
* Country-level SCP vs MCP analysis
* Keyword co-occurrence networks
* Thematic evolution and thematic maps
* Application-focused keyword networks (after concept pruning)

These outputs directly support the figures and tables presented in the paper.

---

## 📎 Citation

If you use this repository or build upon this work, **please cite the article**:

```bibtex
@article{silva2025qnlp,
  title   = {A Scientometric Review of Practical Applications in Quantum Natural Language Processing (QNLP): Trends, Gaps, and Research Opportunities},
  author  = {Silva, Victor R. and Barbosa, F{\'a}bio R. and Silva, Jasson C. and Santos, Francisco J. and Rabelo, Ricardo A. L. and Rodrigues, Joel J. P. C.},
  journal = {IEEE Access},
  volume  = {13},
  year    = {2025},
  pages   = {210169--210179},
  doi     = {10.1109/ACCESS.2025.3638646}
}
```

---

## 📄 License

This repository is released under the **Creative Commons Attribution 4.0 (CC BY 4.0)** license, consistent with the IEEE Access publication.

You are free to:

* Share and adapt the material
* Use it for academic and commercial purposes

As long as proper attribution is given.

---

## 👤 Contact

**Victor R. Silva**
Federal University of Piauí (UFPI)
📧 [victor.silva@ufpi.edu.br](mailto:victor.silva@ufpi.edu.br)

For questions, suggestions, or collaborations, feel free to open an issue or get in touch directly.

---

*Science is a map, not the territory — this repository is a compass.*
