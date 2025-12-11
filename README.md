The Anna Karenina Paradox — A Digital Reading of TolstoyShort title: The Anna Karenina ParadoxAuthor(s): Joranas Cigas, Jakhongir Erkinov, Tawdros Daved, Chriswin Baiju📖 Project Description (TL;DR)This project uses computational literary analysis to investigate a central question in Leo Tolstoy's Anna Karenina: Why is the book named after Anna when Konstantin Levin has just as much narrative weight?This is the "Anna Karenina Paradox":Quantity: Levin appears in just as many chapters and has nearly equal "screen time" as Anna.Structure: The novel is famously a "double-plot" structure (Anna’s tragedy vs. Levin’s spiritual journey).The Question: Is Anna the true protagonist, or is she just the more dramatic half of a balanced equation?To solve this, we applied four specific quantitative measures to the text. Our results revealed a fascinating 2-2 split, proving that the novel relies on a perfect structural tension between its two leads.🏆 The Scorecard: Anna vs. LevinWe tested "Protagonist Status" using four distinct NLP metrics. The results show exactly how Tolstoy balanced the novel.MetricWinnerWhat it MeasuresInterpretation1. Total MentionsLevinRaw frequency of name occurrences.Levin is technically the most present character. He is the steady "background radiation" of the novel.2. Network CentralityAnna"Hub" status in the social graph.Anna connects more distinct social groups (Karenin, Vronsky, Oblonskys). She is the social gravity of the book.3. Timeline / SentimentLevinPresence across the full narrative arc.Anna vanishes (dies) before the end. Levin carries the narrative through to the final philosophical conclusion.4. Semantic CoherenceAnnaParagraph-level topical focus.Anna's sections have lower entropy/higher focus (high drama/action). Levin's are more "wandering" (philosophy/farming). Anna drives the plot; Levin drives the theme.Conclusion: The book is named Anna Karenina not because she is the "main" character by volume, but because she provides the narrative intensity (Coherence/Centrality) that breaks the narrative stability (Mentions/Timeline) provided by Levin.📂 Repository StructureThis repository contains source data, Jupyter notebooks for analysis, and exported visualizations.data/ - Raw .txt files (Anna Karenina).notebooks/ - Analysis scripts (see below).results/ - Generated plots (Network graphs, Coherence density plots) and CSVs.📑 Analysis Modules1. The "Focus" Test (Semantic Coherence)Goal: Determine who drives the plot intensity.Method: We use sentence-transformers (S-BERT) to measure the semantic similarity of sentences within paragraphs.Finding: Anna's paragraphs are "tighter" and more focused (Action/Drama). Levin's are "looser" (Philosophy/Musing).Notebook: paragraph_coherence_anna_vs_levin.ipynb2. The "Social" Test (Network Centrality)Goal: Determine who is more essential to the character web.Method: We build a co-occurrence graph of all major characters.Finding: Anna has higher "Betweenness Centrality"—if you remove her, the novel's social network falls apart. Levin is more isolated.3. The "Volume" Test (Mentions & Frequency)Goal: Determine who dominates the page.Method: N-gram analysis and named entity counting.Finding: Levin actually "wins" on raw counts, supporting the idea that this is a dual-protagonist novel.

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
## Key Libraries used:

sentence-transformers (for semantic analysis)

spacy (for entity recognition)

networkx (for social graphs)

seaborn / matplotlib (for visualization)

## 📜 Session Outline (For Coursework)
In addition to the main project, this repo contains standard NLP session notebooks covering:

Bigrams & Trigrams (1_AppliedNLP_Session2_Bi_Trigrams.ipynb)

Pointwise Mutual Information (PMI) (2_AppliedNLP_Session2_PMI.ipynb)

POS Pattern Frequency (3_AppliedNLP_Session2_POS_Patterns.ipynb)

Phrase Diversity (n-gram TTR) (4_AppliedNLP_Session2_Phrase_Diversity.ipynb)

Collocation Network (5_AppliedNLP_Session2_Collocation_Network.ipynb)