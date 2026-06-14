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

Baseline-aware analysis revealed that several apparent TCR signals can be misleading when interpreted without comparison to healthy repertoire background.

### 🔬 Example 1 — TRBV Gene Enrichment (CMV)

| TRBV Gene | Human Baseline | CMV Frequency | log2 Enrichment | Interpretation |
|---|---:|---:|---:|---|
| TRBV29-1 | 0.0117 | 0.0507 | +2.12 | Relative enrichment after baseline correction |
| TRBV12-3 | 0.0133 | 0.0465 | +1.80 | Low baseline gene showing increased usage |
| TRBV20-1 | 0.0392 | 0.0867 | +1.15 | Expanded but requires biological validation |
| TRBV7-9 | 0.1743 | 0.0551 | -1.66 | High baseline gene depleted in CMV |
| TRBV4-1 | 0.1622 | 0.0276 | -2.55 | Apparent loss due to baseline comparison |

**Observation:**  
High-frequency human repertoire genes may appear as antigen-associated changes if baseline usage is ignored.

---

### 🔬 Example 2 — TRBV Gene Enrichment (EBV)

| TRBV Gene | Human Baseline | EBV Frequency | log2 Enrichment | Interpretation |
|---|---:|---:|---:|---|
| TRBV12-3 | 0.0133 | 0.1242 | +3.22 | Strong enrichment relative to baseline |
| TRBV29-1 | 0.0117 | 0.0708 | +2.60 | Enriched but requires validation |
| TRBV7-9 | 0.1743 | 0.2511 | +0.53 | Amplification of common gene usage |
| TRBV6-5 | 0.0471 | 0.0038 | -3.65 | Strong depletion relative to baseline |

**Observation:**  
Large fold changes can result from low baseline frequency rather than true antigen specificity.

---

### 🔬 Example 3 — CDR3β Length Bias (CMV)

| CDR3β Length | Human Baseline | CMV Frequency | log2 Enrichment | Interpretation |
|---|---:|---:|---:|---|
| 11 aa | 0.0117 | 0.0412 | +1.82 | Short CDR3 enrichment signal |
| 18 aa | 0.0150 | 0.0293 | +0.97 | Increased usage |
| 15 aa | 0.2052 | 0.2370 | +0.21 | Common repertoire length |
| 17 aa | 0.1435 | 0.0703 | -1.03 | Reduced relative usage |

**Observation:**  
CDR3 length shifts must be evaluated against natural length distributions.

---

### 🔬 Example 4 — CDR3α Length Bias (EBV)

| CDR3α Length | Human Baseline | EBV Frequency | log2 Enrichment | Interpretation |
|---|---:|---:|---:|---|
| 13 aa | 0.3288 | 0.4477 | +0.45 | Expansion of dominant baseline length |
| 10 aa | 0.0136 | 0.0163 | +0.26 | Mild enrichment |
| 9 aa | 0.0314 | 0.0009 | -5.08 | Strong depletion |

**Observation:**  
The most common CDR3 lengths in humans can dominate antigen datasets without representing unique specificity.

---

### 🧠 Main Conclusion

Baseline comparison prevents false interpretation by distinguishing:

**Natural repertoire architecture**  
from  
**Potential antigen-driven selection**

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
