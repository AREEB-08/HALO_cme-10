# ☀️ HALO-CME Detection using Aditya-L1 Data  
*ISRO Hackathon 2024 — Problem Statement 10*

![Aditya-L1](https://upload.wikimedia.org/wikipedia/commons/thumb/7/7e/Aditya_L1_Spacecraft_-_ISRO.jpg/600px-Aditya_L1_Spacecraft_-_ISRO.jpg)

## 🚀 Overview
The goal of this project is to identify **HALO Coronal Mass Ejection (CME)** events using particle data collected from the **SWIS-ASPEX Payload** onboard ISRO’s **Aditya-L1** mission. These CME events are critical indicators of space weather patterns that can affect satellite operations, communication systems, and power grids on Earth.

Our solution analyzes **solar wind particle signatures** to distinguish HALO CMEs from normal variations in space plasma.

---

## 🔬 Problem Statement  
**Problem Statement 10 – ISRO Hackathon**  
> Design a data-driven solution to identify HALO-CME events using the particle data from the SWIS-ASPEX payload.

---

## 🧠 Core Idea  
We built a pipeline to:

- Preprocess time-series solar wind data (energy, velocity, charge, flux)
- Extract key patterns using moving averages, feature engineering, and smoothing
- Detect possible HALO-CME occurrences using peak detection and rule-based models
- Visualize the data and predictions in an interpretable way for scientists

---

## 🗂️ Dataset  
- **Source**: SWIS-ASPEX Payload (Aditya-L1)
- **Features**:
  - Proton energy spectra
  - Alpha particle counts
  - Particle velocities and fluxes over time

---

## ⚙️ Tech Stack
- **Python**
- **NumPy**, **Pandas**, **Matplotlib**
- **SciPy** for signal processing
- **Jupyter Notebook** for iterative analysis

---

## 📊 Methodology

1. **Data Cleaning**  
   Missing values were handled using forward filling and interpolation.

2. **Feature Engineering**  
   Key physical parameters like average energy flux and velocity thresholds were derived.

3. **Anomaly Detection**  
   Detected CME-like signatures based on:
   - Sudden spikes in proton/alpha flux
   - Sustained velocity shifts
   - Correlation with known CME events

4. **Threshold Logic**  
   Domain-specific thresholds were applied to detect potential HALO-CME instances.

---

## 📈 Sample Output  
Graphs generated showing spikes in particle activity corresponding to CME predictions:

![Sample Plot](https://raw.githubusercontent.com/AREEB-08/HALO_cme-10/main/plots/sample_plot.png)

---

## 🧪 How to Run

```bash
git clone https://github.com/AREEB-08/HALO_cme-10.git
cd HALO_cme-10
pip install -r requirements.txt
jupyter notebook
# Open and run 'main.ipynb'
