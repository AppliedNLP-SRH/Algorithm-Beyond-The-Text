# The Anna Karenina Paradox — A Digital Reading of Tolstoy

**Short title:** The Anna Karenina Paradox 
**Author(s):** Joranas Cigas, Jakhongir Erkinov, Tawdros Daved, Chriswin Baiju

---

## Project description (TL;DR)

This project uses lightweight NLP methods to compare two Tolstoy novels —  *Anna Karenina* — with an eye toward **character findings**. The motivating question is

1. **How similar or different is Leo Tolstoy’s style across these two long novels?**  
2. **How does book length and internal structure affect measures of predictability (compressibility, repeated phrases, sentence patterns, etc.)?**

One narrative angle — *“The Anna Karenina paradox”* — asks whether Anna is the clear central figure when other major characters (e.g., Levin) share narrative weight. We use quantitative measures (compression ratio, n-grams/PMI, sentence patterns, paragraph compressibility) to provide data-driven context for such literary readings.

This repository contains source data, Jupyter notebooks for analysis, and exported visualizations.

---

## Research question

**Primary:** How do *War and Peace* and *Anna Karenina* compare in terms of textual predictability and repetition, at book and sub-book (segment / paragraph) levels?

**Secondary / interpretive:** Do measures of redundancy correlate with narrative features (dialogue vs description, repeated phrases, or long lists), and what does that tell us about Tolstoy’s stylistic choices?

---

## What’s in this repo (folder structure)


---

## 📑 Session Outline

### Topic: Phrases & Collocations

This session explores multi-word expressions and phrase patterns in literary texts. Using two works by the same author (as an example Alice's Adventures in Wonderland and Through the Looking-Glass), you'll learn to:

1. **Bigrams & Trigrams** ([`1_AppliedNLP_Session2_Bi_Trigrams.ipynb`](./notebooks/1_AppliedNLP_Session2_Bi_Trigrams.ipynb))
   - Compute frequent bigrams and trigrams across two texts
   - Compare phrase frequencies using normalized rates
   - Identify distinctive phrases for each work
   - Visualize most characteristic multi-word expressions

2. **Pointwise Mutual Information (PMI)** ([`2_AppliedNLP_Session2_PMI.ipynb`](./notebooks/2_AppliedNLP_Session2_PMI.ipynb))
   - Measure collocation strength using PMI scores
   - Identify strongly associated word pairs beyond raw frequency
   - Compare PMI-based collocations across works
   - Export reproducible analysis artifacts

3. **POS Pattern Frequency** ([`3_AppliedNLP_Session2_POS_Patterns.ipynb`](./notebooks/3_AppliedNLP_Session2_POS_Patterns.ipynb))
   - Analyze grammatical patterns in bigrams (ADJ+NOUN, VERB+NOUN, etc.)
   - Apply spaCy POS tagging for syntactic analysis
   - Visualize distribution of POS patterns
   - Compare syntactic phrase structure across texts

4. **Phrase Diversity (n-gram TTR)** ([`4_AppliedNLP_Session2_Phrase_Diversity.ipynb`](./notebooks/4_AppliedNLP_Session2_Phrase_Diversity.ipynb))
   - Measure phrase variety using Type-Token Ratio (TTR)
   - Compare lexical/phrasal diversity across works
   - Analyze diversity trends by section/chapter
   - Interpret TTR as indicator of stylistic formulaicity vs. variety

5. **Collocation Network** ([`5_AppliedNLP_Session2_Collocation_Network.ipynb`](./notebooks/5_AppliedNLP_Session2_Collocation_Network.ipynb))
   - Visualize word collocations as network graphs
   - Identify hub words and collocation clusters
   - Explore phrase structure through network topology
   - Compare collocation patterns between texts

### Key Concepts
- **N-grams**: Contiguous sequences of n tokens (bigrams, trigrams)
- **Collocations**: Words that frequently co-occur in predictable patterns
- **PMI**: Statistical measure of association between words in bigrams
- **TTR**: Ratio of unique to total n-grams, measuring diversity
- **POS patterns**: Grammatical templates underlying phrases

### Data
All notebooks work with Project Gutenberg text in the [`data/`](./data/) folder:
- `The Project Gutenberg eBook of Anna Karenina, by Leo Tolstoy.txt` — Anna Karenina by Leo Tolstoy.

Notebooks include robust preprocessing to strip Gutenberg headers, normalize quotes, and handle encoding artifacts. For your texts, you should implement different preprocessing steps if needed.

---
- Read more about this project on Medium: <Medium_Article_link>
---

---
## 🚀 Environment Setup

Before starting, please **fork this repository** and create a fresh Python virtual environment.  
All required libraries are listed in `requirements.txt`.

> ⚠️ If you encounter errors during `pip install`, try removing the version pinning for the failing package(s) in `requirements.txt`.  
> On Apple M1/M2 systems you may also need to install additional system packages (the “M1 shizzle”).

---

### macOS / Linux (bash/zsh)

```bash
# Select Python version (if using pyenv)
pyenv local 3.11.3

# Create and activate virtual environment
python -m venv .venv
source .venv/bin/activate

# Upgrade pip and install dependencies
pip install --upgrade pip
pip install -r requirements.txt
```

### Windows (PowerShell)
```bash
# Select Python version (if using pyenv)
pyenv local 3.11.3

# Create and activate virtual environment
python -m venv .venv
.venv\Scripts\Activate.ps1

# Upgrade pip and install dependencies
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### Windows (Git Bash)
```bash
# Select Python version (if using pyenv)
pyenv local 3.11.3

# Create and activate virtual environment
python -m venv .venv
source .venv/Scripts/activate

# Upgrade pip and install dependencies
python -m pip install --upgrade pip
pip install -r requirements.txt
```

You’re now ready to run the session notebooks!

Deactivate the environment when you’re done:
```bash
deactivate
```
