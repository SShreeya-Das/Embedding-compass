# 🌍 The Embedding Compass: Cultural Geometry in Multilingual AI

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> **Research Question:** Do multilingual embedding models encode culturally-specific semantic relationships between abstract moral concepts?

**Answer:** Yes. The geometric relationships between moral concepts vary significantly across languages, suggesting that embedding models absorb cultural values from training data.

---

## 🔬 **Key Finding**

The relationship between **justice, mercy, and punishment** differs by **21%** across languages: This difference is statistically significant (F=48.0, p<0.0001).

| Language | Ratio* | Interpretation |
|----------|--------|----------------|
| 🇯🇵 Japanese | 1.279 | Justice and mercy closely related |
| 🇬🇧 English | 1.290 | Balanced relationship |
| 🇨🇳 Chinese | 1.308 | Moderate separation |
| 🇸🇦 Arabic | 1.476 | Greater conceptual distance |
| 🇮🇳 Hindi | 1.549 | Justice and mercy are distinct concepts |

**\*Ratio = distance(justice→mercy) / distance(justice→punishment)**

**Statistical Validation:**
- **ANOVA:** F = 48.0, p < 0.0001
- **Effect Size:** 21% variation across languages
- **Conclusion:** Language is a statistically significant predictor of concept geometry

**Methodology**

**Model**: `paraphrase-multilingual-mpnet-base-v2` (768-dimensional embeddings)

**Languages**: English, Hindi, Japanese, Arabic, Chinese

**Concepts**: 10 abstract moral terms (justice, mercy, duty, honor, forgiveness, punishment, law, freedom, loyalty, sacrifice)

**Metric**: Cosine distance = 1 - cosine_similarity

**Statistical Test**: One-way ANOVA with bootstrap resampling (n=20 per language)

**Visualization**: Interactive Plotly HTML charts

## 📊 **What This Means**

### Cultural Insight
- **Japanese embeddings** show integrated moral concepts (balance, harmony)
- **Hindi embeddings** show distinct moral categories (dharma, karma, daya as separate)
- This aligns with cultural scholarship on Eastern vs Western moral philosophy

### AI Implications
- Multilingual models are **not culturally neutral**
- Training data cultural context is **encoded in embedding geometry**
- Implications for **AI fairness, cross-cultural NLP, moral reasoning systems**
## 📊 Visualizations

### Key Charts

#### Justice-Mercy Ratio Comparison
![Ratio Comparison](https://raw.githubusercontent.com/SShreeya-Das/Embedding-compass/main/results/screenshots/ratio_comparison.png)
*Shows the 21% variation in concept relationships across languages*

#### Hindi Concept Heatmap
![Hindi Heatmap](https://raw.githubusercontent.com/SShreeya-Das/Embedding-compass/main/results/screenshots/heatmap_hindi.png)
*Visualizes how moral concepts cluster in Hindi embeddings*

#### Japanese Concept Heatmap
![Japanese Heatmap](https://raw.githubusercontent.com/SShreeya-Das/Embedding-compass/main/results/screenshots/heatmap_japanese.png)
*Visualizes how moral concepts cluster in Japanese embeddings* 

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SShreeya-Das/Embedding-compass/blob/main/embedding-compass.ipynb)


## 🚀 **Quick Start**

### **Option 1: Run in Google Colab** (Recommended)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SShreeya-Das/Embedding-compass/blob/main/embedding-compass.ipynb)

1. Click the badge above
2. Click **Runtime** → **Run all**
3. Results appear in ~5 minutes

### **Option 2: Run Locally**

```bash
# Clone repository
git clone https://github.com/SShreeya-Das/Embedding-compass.git
cd embedding-compass

# Install dependencies
pip install -r requirements.txt

# Run analysis
python analysis.py  # (if you created this file)
# OR open the notebook in Jupyter

📚 **Related Work**
Ahia et al. (2023). "All Languages Are Not Created (Tokenized) Equal." ACL Findings
Hofstede, G. (2001). Culture's Consequences. Sage Publications.
Sapir, E. (1929). "The Status of Linguistics as a Science." Language
🛠️ **Technical Details**
Model: paraphrase-multilingual-mpnet-base-v2 (Sentence Transformers)
Metric: Cosine distance (1 - cosine similarity)
Languages: English, Hindi, Japanese, Arabic, Chinese
Concepts: 10 abstract moral terms (justice, mercy, duty, honor, forgiveness, punishment, law, freedom, loyalty, sacrifice)
