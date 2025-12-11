# The Anna Karenina Paradox — A Digital Reading of Tolstoy
Short title: The Anna Karenina Paradox

## Project members: Joranas Cigas, Jakhongir Erkinov, Daved Tawdros, Chriswin Baiju

## 📖 Project Description 
This project uses computational literary analysis to investigate a central question in Leo Tolstoy's Anna Karenina:
## Why is the book named after Anna when Konstantin Levin has just as much narrative weight?

This is the "Anna Karenina Paradox":

### Quantity: Levin appears in just as many chapters and has nearly equal "screen time" as Anna.

### Structure: The novel is famously a "double-plot" structure (Anna’s tragedy vs. Levin’s spiritual journey).

## The Question: Is Anna the true protagonist, or is she just the more dramatic half of a balanced equation?

To solve this, we applied four specific quantitative measures to the text. Our results revealed a fascinating 2-2 split, proving that the novel relies on a perfect structural tension between its two leads.

## 🏆 The Scorecard: Anna vs. Levin

We tested "Protagonist Status" using four distinct NLP metrics. The results show exactly how Tolstoy balanced the novel.
1. Total Mentions (Levin won)   .It measures frequency of name occurrences.  Levin is technically the most present character.   He is the steady "background radiation" of the novel.
2. Network Centrality (Anna won). It measures "Hub" status in the social graph.  Anna connects more distinct social groups (Karenin, Vronsky, Oblonskys).  She is the social gravity of the book.
3. Timeline / Sentiment(Levin won). It measures Presence across the full narrative arc.  Anna vanishes (dies) before the end.  Levin carries the narrative through to the final philosophical conclusion.
4. Semantic Coherence (Anna won). It measures Paragraph-level topical focus.  Anna's sections have lower entropy/higher focus (high drama/action).  Levin's are more "wandering" (philosophy/farming). Anna drives the plot; Levin drives the theme.

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
