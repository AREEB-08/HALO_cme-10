# HALO-CME Detection using Aditya-L1 Particle Data  
**ISRO Hackathon 2024 – Problem Statement 10**

## Abstract
This project presents a method to identify **HALO Coronal Mass Ejection (CME)** events using particle flux data from the **SWIS-ASPEX payload** onboard the **Aditya-L1** spacecraft. HALO CMEs are large-scale solar ejections that appear to surround the solar disk and have the potential to cause significant space weather effects. The approach involves time-series data analysis, signal processing, and threshold-based detection techniques to isolate CME signatures.

---

## Problem Statement
**Problem 10**: Develop a data-driven approach to identify HALO-CME events using particle data from the SWIS-ASPEX payload, part of India's Aditya-L1 solar mission.

---

## Project Goals
- Analyze solar wind ion spectra and flux variations to detect anomalies consistent with HALO CMEs.
- Develop a repeatable, interpretable detection pipeline suitable for scientific use.
- Provide visualization and data export capabilities for further study and validation.

---

## Dataset Description
- **Source**: Simulated or real data from the **SWIS-ASPEX** payload.
- **Variables**:
  - Proton and alpha particle energy levels
  - Particle flux (particles/cm²·s·sr·MeV)
  - Time-stamped spectral readings
  - Derived velocities and average energy

---

## Methodology

1. **Data Preprocessing**
   - Interpolation and forward-fill for missing data
   - Time normalization and unit consistency

2. **Feature Extraction**
   - Calculate energy flux trends
   - Derive sudden gradient shifts in particle behavior

3. **Detection Pipeline**
   - Apply rolling averages and smoothing filters
   - Identify sharp rises in proton/alpha flux
   - Validate against time-localized patterns known to match CME dynamics

4. **Rule-Based Classification**
   - Thresholds selected based on known CME benchmarks
   - Detection of sustained, multi-feature anomalies flagged as potential HALO-CMEs

---

## Tools & Libraries
- **Python 3.10**
- **Pandas** – Data cleaning and manipulation  
- **NumPy** – Numerical operations  
- **Matplotlib / Seaborn** – Scientific plotting  
- **SciPy** – Signal processing  
- **Jupyter Notebook** – Analysis environment

---

## Results
- Successfully identified multiple CME-like events from the provided dataset
- Visual confirmation through flux and velocity anomaly graphs
- Low false positive rate due to conservative threshold tuning

---

## How to Run

```bash
git clone https://github.com/AREEB-08/HALO_cme-10.git
cd HALO_cme-10
pip install -r requirements.txt
jupyter notebook
