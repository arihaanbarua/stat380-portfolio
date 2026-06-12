# Machine Learning Portfolio

A [Quarto book](https://quarto.org/docs/books/) collecting a series of **statistical modeling and machine-learning projects** in R and Python, from my time at Penn State. Each chapter takes a real dataset, builds and evaluates models, and rebuilds every figure as an interactive [plotly](https://plotly.com/) visualization with a plain-language explanation of the analysis.

📖 **Live book:** https://arihaanbarua.github.io/machine-learning-portfolio/

## Contents

### Part I — Data Analysis & Regression (R)
- **Data Wrangling** — querying baseball career records with `dplyr` (grouping, joining, filtering)
- **Linear Regression & Model Selection** — insurance charges, used-car pricing, NOVA housing EDA & multiple regression
- **Regularization & kNN** — MLB salary (LASSO & backward elimination), linear regression vs k-nearest-neighbors, housing prediction

### Part II — Machine Learning (Python)
- **Gaussian Naïve Bayes** — Iris classification implemented from scratch
- **Neural Networks** — Dry Bean variety classification with `MLPClassifier`
- **Random Forests** — Gini impurity & feature-importance comparison
- **ROC & Cross-Validation** — corporate bankruptcy prediction with stratified k-fold
- **Decision Trees** — breast-cancer diagnosis & information gain

## Project structure

```
.
├── _quarto.yml            # Book configuration
├── index.qmd              # Landing page / overview
├── chapters/              # One self-contained chapter per topic
│   ├── 01-data-wrangling.qmd
│   ├── 02-linear-regression.qmd
│   ├── 03-regularization-knn.qmd
│   ├── 04-naive-bayes.qmd
│   ├── 05-neural-network.qmd
│   ├── 06-random-forest.qmd
│   ├── 07-roc-kfold.qmd
│   └── 08-decision-trees.qmd
├── Files/                 # Datasets + original source notebooks & PDFs
└── _book/                 # Rendered HTML output (git-ignored)
```

## Building locally

This book mixes **R** (via the knitr engine) and **Python** (via [reticulate](https://rstudio.github.io/reticulate/)). You'll need:

- **Quarto** ≥ 1.4
- **R** with: `dplyr`, `tidyr`, `Lahman`, `glmnet`, `MASS`, `FNN`, `ggplot2`, `plotly`, `scales`, `reticulate`
- **Python** with: `numpy`, `pandas`, `scikit-learn`, `plotly`, `statistics`, and optionally `ucimlrepo`

Render the whole book:

```bash
quarto render
```

Preview with live reload:

```bash
quarto preview
```

The machine-learning chapters pull benchmark datasets from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/); each includes a `scikit-learn` or direct-download fallback so the book still renders if the UCI API is unreachable.

## Author

**Arihaan Barua**
