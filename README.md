# Multi-Elves Analysis for the Pierre Auger Observatory

**Signal Processing & Classification of events for Atmospheric Research**

This repository hosts the data and codes developed for the analysis of elves for the **Pierre Auger Collaboration**. It focuses on the preprocessing, feature extraction, and classification of transient luminous events (Elves) detected between 2014 and 2020. 

For further information feel free to reach out: Adriana Vásquez Ramírez, adrianacvr67@gmail.com

---

## 🔬 Scientific Context
The classification results were used to validate hypotheses regarding the physical origin of multiple rings in Elves. These findings provided key insights into the underlying atmospheric mechanisms, and the main results of this research are published in:
> **The Pierre Auger Collaboration (2025).** *Quasi-constant time gap in multiple rings of elves.* **Earth and Space Science**, 12, e2025EA004321. [DOI: 10.1029/2025EA004321](https://doi.org/10.1029/2025EA004321)

The curated dataset and the final classification code developed for this research are archived and publicly available on Zenodo:
>  [DOI: 10.5281/zenodo.14224794](https://doi.org/10.5281/zenodo.14224794)

## 🛠️ Tech Stack
* **Languages:** Python, C++ and ROOT (CERN framework)
* **Data Acquisition**: Remote ingestion of large-scale atmospheric event data (~10 GB/day) from the Pierre Auger Observatory servers via secure remote protocols (SSH)
* **Preprocessing:** C++ pre-classification to scan raw data and identify "Multi-Elves" candidates
* **Data Selection**: Implemented a Python-based ingestion layer using Uproot to transition from ROOT TTree structures to numpy arrays.
* **Data Analysis:** Pandas, NumPy, SciPy (Signal Processing)
* **Modeling:** Scikit-learn, K-means (Event Classification)
* **Visualization:** Matplotlib and ROOT

## 📂 Repository content
* `notebooks/`: Final Python notebooks for analysis and visualization.
* `src/`: Core preprocessing and classification scripts.
* `data/`: (Refer to Zenodo DOI for full dataset access).

## 📝 Citation
If you use this work, please cite both the publication and the dataset:

```bibtex
@article{https://doi.org/10.1029/2025EA004321,
author = {The Pierre Auger Collaboration},
title = {Quasi-Constant Time Gap in Multiple Rings of Elves},
journal = {Earth and Space Science},
volume = {12},
number = {10},
pages = {e2025EA004321},
keywords = {multi-elves, temporal resolution, ground reflection model, lightning waveform},
doi = {https://doi.org/10.1029/2025EA004321},
url = {https://agupubs.onlinelibrary.wiley.com/doi/abs/10.1029/2025EA004321},
eprint = {https://agupubs.onlinelibrary.wiley.com/doi/pdf/10.1029/2025EA004321},
note = {e2025EA004321 2025EA004321},
year = {2025}
}

@dataset{vasquez_ramirez_2024_14224794,
  author = {Vásquez-Ramírez, Adriana},
  title = {{Python Notebook and Dataset for Multi-Elves Analysis at the Pierre Auger Observatory}},
  month = nov,
  year = 2024,
  publisher = {Zenodo},
  version = {1.0.0},
  doi = {10.5281/zenodo.14224794},
  url = {https://doi.org/10.5281/zenodo.14224794}
}
```

