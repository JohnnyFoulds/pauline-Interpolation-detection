# Detecting Pauline Interpolations Using Cross-Translation LLM Consensus: A Data-Driven Approach to Textual Criticism 

## Thesis Synopsis

---

#### **What I Am Doing**  
This thesis pioneers a computational framework to identify interpolations—later textual additions—in the Pauline epistles (e.g., 1–2 Corinthians, Romans) by analyzing stylistic anomalies across English Bible translations. Using large language models (LLMs), I fine-tune two `roberta-base` models on formal (ESV) and dynamic (NLT) translations of undisputed Pauline texts (Romans, Galatians) to flag inconsistencies in contested passages. By requiring **cross-translation consensus** for anomaly detection, the method mitigates translation-specific biases and isolates signals of potential scribal edits.  

---

#### **Why I Am Doing It**  
Traditional textual criticism relies on subjective analysis of Greek/Hebrew manuscripts, a process inaccessible to non-specialists and prone to scholarly bias. Meanwhile, modern translations often obscure or amplify textual anomalies through their phrasing choices. This work addresses these gaps by:  
1. **Democratizing Scholarship**: Using English Bibles to enable broader participation in textual criticism.  
2. **Empirical Rigor**: Introducing data-driven metrics (e.g., perplexity scores) to complement manual analysis.  
3. **Novelty**: Bridging NLP and theology—no prior work applies cross-translation LLM consensus to Pauline interpolations.  

The project has ethical urgency: interpolations like *1 Corinthians 14:34–35* (mandating women’s silence) shape doctrines with real-world consequences, demanding rigorous scrutiny.  

---

#### **Methodology**  
1. **Data Collection**:  
   - **Training Data**: Romans and Galatians (ESV/NLT), chosen for undisputed authenticity.  
   - **Test Data**: 1–2 Corinthians, Pastorals (ESV/NLT).  
   - **Validation Data**: Known interpolation candidates from Ehrman (2006) and Nestle-Aland’s critical apparatus.  

2. **Model Design**:  
   - Fine-tune separate `roberta-base` models on ESV and NLT training corpora.  
   - Calculate **perplexity scores** for test verses to quantify stylistic deviations.  
   - Flag anomalies with Z-scores >2σ in both translations.  

3. **Validation**:  
   - **Statistical**: Benjamini-Hochberg correction for false discovery rate (FDR).  
   - **Scholarly Alignment**: Precision/recall against Fee’s and Ehrman’s interpolation catalogs.  
   - **Manuscript Evidence**: Cross-reference anomalies with Codex Fuldensis placements.  

---

#### **Research Questions**  
1. **Detection Validity**: Can LLMs detect interpolation candidates in English translations with statistical significance?  
2. **Translation Impact**: Does cross-translation consensus (ESV/NLT) reduce false positives compared to single-model approaches?  
3. **Scholarly Alignment**: Do flagged anomalies align with debates in textual criticism (e.g., 1 Cor 14:34–35)?  
4. **Failure Analysis**: If anomalies are undetected, what methodological or textual factors explain this?  

---

#### **Expected Contributions**  
1. **Technical**: A reproducible NLP framework for interpolation detection, adaptable to other contested texts.  
2. **Scholarly**: Empirical validation of long-debated anomalies (e.g., 2 Cor 6:14–7:1) and identification of novel candidates.  
3. **Ethical**: Challenging doctrinal traditions rooted in interpolations (e.g., gender roles) through data-driven critique.  

By bridging computational linguistics and theology, this thesis advances both fields while democratizing access to biblical scholarship.
