# Online News Popularity — Multi-Class Classification

**Module:** MSIN0097 Predictive Analytics — UCL School of Management, 2025–26

## Project Overview

Predicts the popularity level (Low / Medium / High) of Mashable articles using a PyTorch MLP trained on 58 pre-publication features. Final model achieves **macro F1 = 0.4883** and **accuracy = 50.1%** on the held-out test set (vs 33% random baseline).

## Repository Structure

```
├── README.md                     ← This file
├── requirements.txt              ← Python dependencies with versions
├── notebook.ipynb                ← Main Jupyter notebook (all 6 sections)
├── data/
│   └── OnlineNewsPopularity.csv  ← Dataset (download instructions below)
```

## Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/mewwmewie/predictive-analytics.git
cd online-news-popularity
```

### 2. Install dependencies

Requires Python 3.10+ and Java 8+ (for PySpark).

```bash
pip install -r requirements.txt
```

### 3. Download the dataset

Download from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/332/online+news+popularity):

```bash
mkdir -p data
# Option A: Direct download
wget -O data/OnlineNewsPopularity.zip https://archive.ics.uci.edu/static/public/332/online+news+popularity.zip
unzip data/OnlineNewsPopularity.zip -d data/
mv data/OnlineNewsPopularity/OnlineNewsPopularity.csv data/

# Option B: Manual download
# 1. Visit https://archive.ics.uci.edu/dataset/332/online+news+popularity
# 2. Click "Download" → extract OnlineNewsPopularity.csv into data/ folder
```

### 4. Run the notebook

```bash
jupyter notebook notebook.ipynb
```

Run all cells sequentially. Expected runtime: ~15–20 minutes (mostly MLP training).

## Reproducibility

- **Global random seed** (`SEED = 42`) is set at the start of the notebook for `random`, `numpy`, `torch`, and all PySpark operations.
- All file paths are **relative** (no absolute paths).
- Python package versions are pinned in `requirements.txt`.

## Citation

Fernandes, K., Vinagre, P., Cortez, P., & Sernadela, P. (2015). Online News Popularity [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5NS3V.
