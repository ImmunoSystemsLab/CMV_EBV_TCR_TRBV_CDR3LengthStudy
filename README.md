# 🧬 TCR-BAP  
### Baseline-Aware Analysis of Antigen-Specific TCR Repertoires

---

## 📌 Overview

Understanding T-cell receptor (TCR) specificity requires more than identifying frequent patterns — it demands distinguishing true biological signals from baseline repertoire biases.

**TCR-BAP** provides a computational framework for analyzing antigen-specific TCR repertoires (e.g., CMV) by comparing them against healthy baseline repertoires to uncover *true enrichment signals*.

---

## 🎯 Key Idea

Most observed patterns in TCR data (e.g., V gene usage, motifs) are influenced by **inherent repertoire structure** rather than antigen specificity.

👉 This project focuses on:

- Baseline correction  
- Enrichment analysis  
- Interpretable specificity profiling  

---

## 🧩 Features

### 1️⃣ TRBV Gene Enrichment
- Normalized V gene frequency calculation  
- log2 enrichment vs baseline  
- Identification of truly overrepresented genes  

---

### 2️⃣ CDR3 Length Profiling
- Comparison of length distributions across conditions  
- Detection of structural constraints in antigen recognition  

---

### 4️⃣ Visualization Module
- Enrichment barplots  
- Distribution comparisons  
- Clean, interpretable biological figures  

---

## 📊 Example Insights

- Selective enrichment of TRBV genes (e.g., TRBV29-1)  
- Preference for shorter CDR3 lengths (~11–14 amino acids)  


---

## 🧠 Biological Interpretation

CMV-associated repertoires show subtle, broadly distributed deviations from the human baseline, consistent with chronic immune engagement and long-term immune adaptation. In contrast, EBV-associated repertoires exhibit more pronounced and selective deviations, suggesting stronger antigen-driven clonal expansion rather than global repertoire remodeling.

---

## 🛠 Tech Stack

- Python 🐍  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  

---

## 🚀 Workflow

### Step 1: Load Data
- Antigen-specific TCR dataset (e.g., CMV)
- Baseline healthy repertoire dataset

---

### Step 2: Normalize Frequencies
Convert raw counts into comparable frequencies across datasets.

---

### Step 3: Compute Enrichment

log2 enrichment:

log2(CMV frequency / baseline frequency)

---

### Step 4: Visualization & Interpretation
- Identify enriched vs depleted features  
- Interpret biological relevance in context of baseline  

---

## 🧠 Why This Matters

Traditional TCR analyses often:

❌ Over-rely on raw frequency signals  
❌ Misinterpret ubiquitous motifs as antigen-specific  

This framework:

✅ Separates signal from baseline bias  
✅ Improves interpretability of repertoire studies  
✅ Strengthens biological conclusions  

---

## 🔬 Future Directions

- Alpha vs Beta chain comparative modeling  
- Cross-reactivity prediction across epitopes  
- Structural integration (e.g., AlphaFold-informed TCR analysis)  
- Development of scoring frameworks for specificity (TEMPO-like models)  

---

## 📎 Data Sources

- VDJdb  
- Public TCR repertoire datasets  

---

## 🤝 Contributing

Contributions, suggestions, and collaborations are welcome.

---

## 📬 Contact

Mohamed Esmat  
Bioinformatics & Immunology

---

## ⭐ Acknowledgment

Inspired by advances in interpretable TCR modeling and baseline-aware immune repertoire analysis.
