# Multi-Elves Analysis for the Pierre Auger Observatory
> Author: Adriana Vásquez Ramírez adrianacvr67@gmail.com

This repository hosts the data and codes developed for the analysis of elves detected at the [Pierre Auger Observatory](https://www.auger.org/news/scientific-highlights/356-quasi-constant-time-gap-in-multiple-rings-of-elves). It focuses on the preprocessing, feature extraction, and classification of transient luminous events (elves) for Atmospheric Research. 

---

## 📂 Primary Analysis
* The curated dataset and the final classification code developed for this research are archived and publicly available on Zenodo:
>  **Vásquez-Ramírez, A. (2024).** Python Notebook and Dataset for Multi-Elves Analysis at the Pierre Auger Observatory [Data set]. Zenodo. [DOI: 10.5281/zenodo.14224794](https://doi.org/10.5281/zenodo.14224794)

Please access the link above to download the dataset and core notebook: `multi-elves.ipynb`. For local setup and execution guidelines, refer to the README.md file in that repository.

* The classification results were used to validate hypotheses regarding the physical origin of multiple rings in elves. These findings provided key insights into the underlying atmospheric mechanisms, and the main results of this research are published in:
> **The Pierre Auger Collaboration (2025).** *Quasi-constant time gap in multiple rings of elves.* **Earth and Space Science**, 12, e2025EA004321. [DOI: 10.1029/2025EA004321](https://doi.org/10.1029/2025EA004321)

## 📂 Supplementary Analysis
This repository contains supplementary analysis of this investigation: 

* `examples/`: Running examples with the `multi-elves.ipynb` notebook to visualize signal characteristics for double and triple-ring elves.
* `seasonal_distribution/`: Preprocessing of the data and seasonal distribution of elves.
* `lightning_waveform_analysis/`: Correlation between elves and lightning external data from Earth Networks. 

## 🛠️ Tech Stack
* **Languages:** `Python`, `C++` and `ROOT` (CERN framework)
* **Data Acquisition**: Remote ingestion of large-scale atmospheric event data (~10 GB/day) from the Pierre Auger Observatory servers via secure remote protocols `SSH`
* **Preprocessing:** `C++` pre-classification to scan raw data and identify "Multi-Elves" candidates
* **Data Selection**: Implemented a Python-based ingestion layer using `uproot` to transition from ROOT TTree structures to `numpy` arrays.
* **Data Analysis:** `pandas`, `numpy`, `scipy` (Signal Processing)
* **Modeling:** `scikit-learn`, `KMeans` (Event Classification)
* **Visualization:** `Matplotlib` and `ROOT`


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
