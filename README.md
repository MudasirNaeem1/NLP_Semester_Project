# Domain-Specific Medical Spell Correction using Context-Sensitive NLP

A research-oriented Natural Language Processing (NLP) project focused on **context-aware spell correction of medication names in clinical text**, addressing a critical gap in healthcare NLP systems.

---

## 📌 Project Overview

Clinical text is inherently noisy, containing abbreviations, shorthand, and frequent spelling errors. Among all entities, **medication names** are particularly challenging due to their length, rarity, and domain-specific nature.  
Traditional spell checkers and general NLP models often fail to correct such terms accurately, which may lead to serious downstream consequences in healthcare systems.

This project proposes a **domain-specific, context-sensitive spell correction framework** inspired by recent research, with enhancements tailored specifically for **medication name correction** in low-resource clinical settings.

---

## 🎯 Objectives

- Address the limitations of general-purpose spell correction for **medical terminology**
- Focus specifically on **medication name correction**
- Leverage **contextual language understanding** instead of surface-level similarity only
- Design a solution suitable for **low-resource and real-world clinical environments**

---

## 🧠 Research Foundation

This work is inspired by the following research paper:

> **Kim, Y., Weiss, R., & Ravikumar, P. (2022)**  
> *Context-Sensitive Spelling Correction of Clinical Text via Conditional Independence*  
> Proceedings of Machine Learning Research (PMLR)

🔗 **Paper Link:**  
https://pmc.ncbi.nlm.nih.gov/articles/PMC11044887/

The paper introduces a **Conditional Independence Model (CIM)** that separates:
- **Context modeling** (language model)
- **Noise modeling** (corruption process)

Our project extends this idea with a stronger focus on **drug names**, improved candidate generation, and practical deployment considerations.

---

## 🔍 Identified Research Gap

Despite strong results, existing approaches:
- Underemphasize **medication names**
- Struggle with **severely misspelled drug terms**
- Rely on **computationally heavy models**
- Lack adaptability for **hospital-scale, low-resource systems**

This project directly targets these limitations.

---

## 🛠️ Proposed Approach (High-Level)

### 1️⃣ Tokenization & Filtering
- Clinical sentences are tokenized
- Non-alphabetic and irrelevant tokens are filtered out

### 2️⃣ Domain-Specific Medication Lexicon
- A curated dictionary of medication names is used
- Prevents incorrect corrections to non-medical terms

### 3️⃣ Robust Candidate Generation
- **Edit-distance based matching** for surface similarity
- **BK-Tree indexing** for efficient approximate search
- **Phonetic similarity** to handle pronunciation-based errors

### 4️⃣ Corruption Modeling
- Estimates how a correct medication name may transform into a misspelled variant
- Models real-world clinical typing errors

### 5️⃣ Contextual Scoring
- Uses a **clinical language model** (e.g., BioClinicalBERT)
- Scores candidates based on sentence-level context

### 6️⃣ Final Candidate Selection
- Combines corruption probability and contextual likelihood
- Selects the most contextually appropriate correction

---

## 📊 Evaluation Summary

- Focused on **token-level accuracy**
- Tested against heavily corrupted medication names
- Demonstrated strong correction performance despite:
  - Limited dictionary size
  - No supervised training
  - Severe spelling noise

---

## 🚀 Key Contributions

- Highlights an **underexplored problem** in medical NLP
- Proposes a **medication-focused spell correction framework**
- Extends CIM with:
  - Improved candidate generation
  - Domain constraints
  - Practical deployment considerations
- Suitable for **low-resource clinical environments**

---

## 🤝 Team Members

| Name | Roll Number |
|-----|------------|
| **Mudasir** | 22K-8732 |
| **Nihal Ali** | 22K-4054 |
| **Basim Baqai** | 22K-4062 |


---

## 👩‍🏫 Course Teacher

**Miss Saeeeda Kanwal** | saeeda.kanwal@nu.edu.pk

---

## 📚 Future Work

- Integration with larger medical ontologies (RxNorm, UMLS)
- Learning real-world typo patterns from clinical logs
- Semantic-type constraints to reduce over-correction
- Model compression for real-time clinical deployment

---

## 📄 License & Academic Use

This project is developed for **academic and research purposes**.  
Proper citation is required if this work or its concepts are reused.

---

⭐ *If you find this project useful, feel free to star the repository and share feedback.*
