### Group 24

Shiref Khaled Elhalawany -  221100944

Ahmed Anis Hassan - 221100101 

Karim Ashraf Elsayed - 221100391

Kareem Shaheen - 221101524

# Section 2: Domain-Specific Hybrid Recommender System

## 📖 Overview
This section implements a comprehensive Recommender System for the Book domain (Amazon Books dataset). It explores multiple recommendation strategies including:
- **Collaborative Filtering (CF)**: User-User/Item-Item KNN and Matrix Factorization (SVD).
- **Content-Based Filtering (CB)**: TF-IDF vectorization of book metadata (Titles, Descriptions, Categories).
- **Hybrid Methods**: Weighted, Switching, and Cascade hybrid strategies combining CF and CB.

## 📂 Repository Structure

### `code/`
- **`main.ipynb`**: The entry point for the project. Orchestrates the entire pipeline by executing the other notebooks in sequence. Run this notebook to reproduce all results.
- **`data_preprocessing.ipynb`**: Handles data loading, cleaning, missing value imputation, rating scaling, and dataset splitting.
- **`content_based.ipynb`**: Implements the Content-Based Filtering logic using TF-IDF on item metadata.
- **`collaborative.ipynb`**: Implements Collaborative Filtering models (KNN and SVD) using the `scipy` and simple linear algebra/similarity approaches.
- **`hybrid.ipynb`**: Implements Hybrid recommendation strategies (Weighted, Switching, Cascade) and contains the final evaluation and cold-start simulation logic.
- **`evaluation.ipynb`**: (Currently Empty) Placeholder for future modularization of evaluation metrics.

### `results/`
Contains generated CSV files for recommendations and evaluation metrics (e.g., `hybrid_weighted.csv`, `cold_start_evaluation.csv`).

## 📊 Dataset
This project uses the **Amazon Reviews 2023** dataset.
- **Source**: [https://amazon-reviews-2023.github.io/](https://amazon-reviews-2023.github.io/)
- **Category**: Books

### Setup Instructions
1. Download the **"Books"** subset from the source (both User-Item-Rating and Metadata files).
2. Place the files in the `data/` directory.
3. Rename the files to match the expected format:
   - Ratings File: `data/Books.csv`
   - Metadata File: `data/meta_Books.jsonl`

## 🚀 Usage
1. Ensure the dataset (`Books.csv` and `meta_Books.jsonl`) is located in `../data/` (relative to the code directory) or `data/` (relative to this README).
2. Open **`code/main.ipynb`**.
3. Run all cells. This will:
   - Load and preprocess the data.
   - Train Content-Based and Collaborative models.
   - Execute Hybrid strategies.
   - Run Cold-Start simulations.
   - Generate evaluation comparisons.

## Key Features
- **Cold-Start Handling**: Simulates user cold-start by masking ratings and evaluating performance using a Switching Hybrid (CB -> CF).
- **Hybrid Comparisons**: Compares Weighted, Switching, and Cascade hybrids to determine the best approach for this domain.

---
*Group [X] - AIE425 Final Project*
