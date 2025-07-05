# 🧠 Hyperscanning EEG Analysis with Blob Detection and Hamming Distance

This project explores **EEG hyperscanning** — simultaneous EEG recordings from two subjects — to analyze synchrony and desynchrony of neural activity through **video generation, 3D visualization**, and **perceptual hashing-based comparison**.

## 📁 Project Overview

This pipeline is part of the _Neural and Cognitive Systems_ coursework and includes:

- Normalized EEG-based video generation for multiple subjects
- Isosurface rendering of EEG video in 3D (space × time)
- Comparison using perceptual hashes and Hamming distance
- Threshold-based blob detection on synchronized/desynchronized frames
- Final combined output video highlighting major differences

---

## 🧠 Key Components

### 1. **Data**
- Source: `Subjects_08` EEG dataset (zipped)
- Format: Cleaned `.mat` EEG recordings for 8 subjects
- Tools: EEGLAB Toolbox (`EEGLAB_Tutorial.zip`)

### 2. **EEG Video Generator (MATLAB)**
- Uses bandpass filtering (Theta: 4–8 Hz)
- Global normalization (`z = (x - μ) / σ`)
- Generates `.avi` EEG videos for Subjects 5 & 6, Trials 1–4
- Frame rate: 20 fps, duration: 180 seconds

### 3. **Isosurface 3D Visualization (MATLAB)**
- Converts EEG videos into 3D volumes
- Applies Gaussian smoothing
- Extracts isosurface with adjustable transparency
- Plots 3D structure using `patch()` and `isonormals()`

### 4. **Perceptual Hashing & Hamming Analysis (Python)**
- Compares pairs of EEG videos (Subject 5 vs 6)
- Computes **normalized Hamming distance** per frame
- Thresholds:
  - **< 0.15** → Synchronized
  - **> 0.35** → Desynchronized
- Significant frames are labeled and stored

### 5. **Blob Detection & Comparison Video (Python + OpenCV)**
- Applies blob detection on synced/desynced frames
- Combines both subject videos side-by-side
- Overlays Hamming score, color-coded blobs
- Exports comparison video (e.g., `blob_comparison_output_5-04_6-04.avi`)



