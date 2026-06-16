# Vietnamese Review Aspect-Based Sentiment Analysis

This repository contains a personal course project for aspect-based sentiment analysis on Vietnamese product reviews. The project compares single-task and multi-task learning approaches for classifying sentiment across multiple review aspects.

## Project Overview

The task is to identify sentiment labels for each review aspect:

- `Price`
- `Shipping`
- `Outlook`
- `Quality`
- `Size`
- `Shop_Service`
- `General`
- `Others`

Each review can contain sentiment for multiple aspects. Labels use `-1`, `0`, `1`, and `2` depending on the aspect annotation scheme used in the dataset.

## Repository Structure

```text
.
├── Dataset/
│   ├── train_data.csv
│   ├── val_data.csv
│   └── test_data.csv
├── Multi-Task Learning PhoBERT.ipynb
├── Multi-Task Learning Simple Models.ipynb
├── Multi-Task Learning VisoBERT.ipynb
├── Single-Task Learning Simple Models.ipynb
├── preprocess.py
├── report.pdf
├── presentation.pptx
├── requirements.txt
└── .gitignore
```

## Dataset

The dataset is split into:

| Split | Samples |
| --- | ---: |
| Train | 8,424 |
| Validation | 936 |
| Test | 2,340 |

Each CSV file contains one `Review` column and eight aspect-label columns.

## Experiments

The notebooks cover the following experiments:

- Single-task learning with simple neural models.
- Multi-task learning with simple neural models.
- Multi-task learning with PhoBERT.
- Multi-task learning with VisoBERT.

The preprocessing script includes utilities for Vietnamese text normalization, acronym normalization, emoji handling, and word segmentation.

## Setup

Create a Python environment and install the required packages:

```bash
pip install -r requirements.txt
```

Some notebooks were developed in Google Colab and may require path adjustments when running locally. Transformer-based experiments also require downloading pretrained models from Hugging Face.

## How to Run

1. Open one of the notebooks in Jupyter Notebook, JupyterLab, or Google Colab.
2. Make sure the `Dataset/` folder is available at the expected path.
3. Run the preprocessing cells.
4. Train and evaluate the selected model.

## Notes

- `report.pdf` and `presentation.pptx` are included as course submission materials.
- Large model checkpoints, generated artifacts, and local environment files are intentionally ignored.
- No open-source license has been specified yet.
