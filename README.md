# 🧬 TCR-BAP  
## Baseline-Aware Analysis of Antigen-Specific TCR Repertoires

## 📌 Overview

T-cell receptor (TCR) repertoire analysis often relies on identifying frequent V genes, CDR3 patterns, or sequence features.

However, high-frequency patterns do not always represent antigen-driven selection. Many observed signals are shaped by the natural architecture of the human TCR repertoire.

**TCR-BAP (Baseline-Aware Profiling)** is a computational framework designed to distinguish potential antigen-associated enrichment from normal repertoire background variation by comparing antigen-specific repertoires against healthy baseline repertoires.

---

## 🎯 Key Idea

A TCR feature can appear enriched simply because it is naturally common in human repertoires.

Therefore, this framework focuses on:

✅ Baseline correction  
✅ Frequency normalization  
✅ Enrichment estimation  
✅ Interpretable repertoire profiling  

The goal is to separate:

**Repertoire architecture → from → antigen-associated selection**

---

## 🧩 Features

### 1️⃣ V Gene Enrichment Analysis

- Calculates normalized TRBV/TRAV gene frequencies
- Compares antigen-specific repertoires against healthy baseline
- Computes:

`log2(Antigen frequency / Baseline frequency)`

- Identifies genes truly overrepresented relative to background usage

---

### 2️⃣ CDR3 Length Landscape Analysis

- Compares CDR3α and CDR3β length distributions
- Detects structural repertoire shifts
- Evaluates whether observed patterns exceed baseline expectations

---

### 3️⃣ Baseline-Aware Interpretation

The framework helps identify misleading signals:

❌ Frequent V genes mistaken as antigen markers  
❌ Low-frequency genes showing artificial enrichment  
❌ Common CDR3 lengths interpreted as specificity signals  

Instead:

✅ Enrichment is evaluated relative to normal repertoire structure

---

## 📊 Example Insights

Analysis of CMV and EBV repertoires showed that:

- Some apparent V gene signals disappear after baseline correction
- Highly abundant genes may reflect repertoire architecture rather than antigen specificity
- True antigen-associated enrichment requires comparison against background usage

---

## 🛠 Tech Stack

🐍 Python

- Pandas
- NumPy
- Matplotlib
- Seaborn

---

## 🚀 Workflow

### Step 1 — Load Data

Input:

- Antigen-specific TCR repertoire (CMV / EBV)
- Healthy baseline repertoire

### Step 2 — Normalize Frequencies

Convert raw counts into comparable frequencies.

### Step 3 — Compute Enrichment

Calculate enrichment relative to baseline.

### Step 4 — Visualization

Generate:

- V gene enrichment plots
- CDR3 length profiles
- Baseline-adjusted repertoire comparisons

---

## 🧠 Why This Matters

Traditional repertoire analysis can:

❌ Overinterpret frequent clonotypes  
❌ Confuse public repertoire features with antigen specificity  
❌ Ignore background V gene bias  

TCR-BAP provides:

✅ Baseline-aware interpretation  
✅ Reduced false discovery  
✅ More biologically meaningful repertoire analysis

---

## 🔬 Future Directions

- Alpha/Beta chain joint modeling
- Motif-level CDR3 analysis
- Public clone detection
- Epitope-specific prediction
- Structural TCR–pMHC integration
- Explainable machine learning models

---

## 📎 Data Sources

- VDJdb
- Public human TCR repertoire datasets

---

## 🤝 Contributing

Contributions, suggestions, and collaborations are welcome.

---

## 📬 Contact

Mohamed Esmat  
Bioinformatics & Immunology

---

## ⭐ Acknowledgment

Inspired by advances in:

- Interpretable TCR modeling
- Immune repertoire analysis
- Baseline-aware computational immunology
