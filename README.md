# Multi-Elves Analysis for the Pierre Auger Observatory
> Author: Adriana Vásquez Ramírez adrianacvr67@gmail.com

This repository provides data and code for the analysis of elves detected at the [Pierre Auger Observatory](https://www.auger.org/news/scientific-highlights/356-quasi-constant-time-gap-in-multiple-rings-of-elves). It focuses on the preprocessing, feature extraction, and classification of transient luminous events (elves) for Atmospheric Research. 


The classification results were used to test hypotheses on the physical origin of multiple rings in elves, providing key insights into the underlying atmospheric mechanisms. The main results are published in:
> **The Pierre Auger Collaboration (2025).** *Quasi-constant time gap in multiple rings of elves.* **Earth and Space Science**, 12, e2025EA004321. [DOI: 10.1029/2025EA004321](https://doi.org/10.1029/2025EA004321)
---

## 📂 Dataset and Code
* Dataset and full analysis code are available via Zenodo (see internal README for execution details):

>  **Vásquez-Ramírez, A. (2024).** Python Notebook and Dataset for Multi-Elves Analysis at the Pierre Auger Observatory [Data set]. Zenodo. [DOI: 10.5281/zenodo.14224794](https://doi.org/10.5281/zenodo.14224794)

* Clone this repository and run `multi-elves.ipynb` to visualize one example of each event type: a double elve, a triple elve, and an elve + halo event.

* The `examples/` directory contains the input data requiered for these examples. 

## 🛠️ Tech Stack
* **Languages:** `Python`, `C++` and `ROOT` (CERN framework)
* **Data Acquisition**: Remote ingestion of large-scale event data (~10 GB/day) from the Pierre Auger Observatory servers via `SSH`
* **Preprocessing:** `C++` pre-classification to scan raw data and identify "Multi-Elves" candidates (Not available in this repo; internal Observatory use)
* **Data Handling**: `uproot` for converting ROOT `TTree` data into `numpy` arrays.
* **Data Analysis:** `pandas`, `numpy`, `scipy` (Signal Processing)
* **Post-processing:** `KMeans` to refine classification results
* **Visualization:** `Matplotlib` and `ROOT`

## 📝 Citation
If you use this work, please cite both the publication and the dataset:

```bibtex
@article{VasquezRamirez_2025_elves,
  author = {The Pierre Auger Collaboration},
  title = {Quasi-Constant Time Gap in Multiple Rings of Elves},
  journal = {Earth and Space Science},
  volume = {12},
  number = {10},
  pages = {e2025EA004321},
  keywords = {multi-elves, temporal resolution, ground reflection model, lightning waveform},
  doi = {10.1029/2025EA004321},
  url = {https://agupubs.onlinelibrary.wiley.com/doi/abs/10.1029/2025EA004321},
  eprint = {https://agupubs.onlinelibrary.wiley.com/doi/pdf/10.1029/2025EA004321},
  note = {e2025EA004321 2025EA004321},
  year = {2025}
}

@dataset{VasquezRamirez_2024_dataset,
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
