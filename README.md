# 🧠 Hyperscanning EEG Analysis with EEGLAB, MATLAB and Python

[![GitHub issues](https://img.shields.io/github/issues/sccn/eeglab?color=%23fa251e&logo=GitHub)](https://github.com/sccn/eeglab/issues)  
![Twitter Follow](https://img.shields.io/twitter/follow/eeglab2?style=social)

This project extends the functionality of [**EEGLAB**](https://sccn.ucsd.edu/eeglab/index.php), an open-source MATLAB toolbox for EEG analysis, by building a complete pipeline for **EEG hyperscanning**, **video generation**, **isosurface visualization**, **perceptual similarity analysis**, and **blob detection** using both **MATLAB** and **Python**.

---

## 📘 Contents

- EEG Video Generation using EEGLAB & custom MATLAB code
- EEG Normalization using Z-scores
- 3D Volume Isosurface Visualization (Video to 3D)
- Perceptual Hashing & Hamming Distance between videos
- Highlighting synchronized vs desynchronized EEG frames
- Blob Detection & Annotated Video Output
- Comparison using Subject 5 & Subject 6 (4 trials each)

---

## 🧠 What is EEGLAB?

[EEGLAB](https://sccn.ucsd.edu/eeglab/index.php) is an open-source MATLAB toolbox for electrophysiological signal processing. It supports data loading, preprocessing, ICA decomposition, time-frequency analysis, and more.

> _Delorme, A., & Makeig, S. (2004). [EEGLAB: an open source toolbox for analysis of single-trial EEG dynamics including independent component analysis](http://sccn.ucsd.edu/eeglab/download/eeglab_jnm03.pdf)._ *Journal of neuroscience methods, 134(1), 9–21.*

---

## 🧠 Based On EEGLAB

This project builds upon [EEGLAB](https://sccn.ucsd.edu/eeglab/) — an open-source MATLAB toolbox for EEG signal processing by Delorme & Makeig et al., UCSD.

**Original EEGLAB components** are used under the GNU GPL license and credited to the authors. See `LICENSE` and original source headers (e.g., `eeglab.m`) for full attribution.

We have added:
- MATLAB-based blob processing for hyperscanning EEG
- EEG-based video generation using perceptual hashing
- Python post-processing utilities for CNN classification of EEG blobs

