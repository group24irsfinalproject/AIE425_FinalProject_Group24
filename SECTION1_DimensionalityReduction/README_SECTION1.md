### Group 24

Shiref Khaled Elhalawany -  221100944

Ahmed Anis Hassan - 221100101 

Karim Ashraf Elsayed - 221100391

Kareem Shaheen - 221101524

# Dimensionality Reduction for Collaborative Filtering
### A Comparative Analysis on the MovieLens 20M Dataset

## 📖 Overview
This project module, **Section 1**, investigates the application of dimensionality reduction techniques to address the challenges of data sparsity and scalability in Collaborative Filtering (CF) systems. By transforming high-dimensional user-item interaction matrices into lower-dimensional latent feature spaces, we aim to uncover hidden patterns in user preferences and improve recommendation efficiency.

The analysis focuses on three primary techniques:
1.  **Principal Component Analysis (PCA)** with Mean Imputation.
2.  **PCA with Maximum Likelihood Estimation (MLE)** for robust covariance estimation.
3.  **Singular Value Decomposition (SVD)** for latent factor extraction.

## 📊 Dataset
**Source**: [MovieLens 20M Dataset](https://grouplens.org/datasets/movielens/20m/)

The dataset contains 20 million ratings and 465,000 tag applications applied to 27,000 movies by 138,000 users. Due to computational constraints, a sampled subset is generated for analysis ensuring minimum density requirements.

### Setup Instructions
1. Download the **MovieLens 20M** dataset from the source.
2. Extract the contents.
3. Place `ratings.csv` in the directory: `../data/ml-20m/ml-20m/`.


## 📂 Repository Structure

The project is organized efficiently to separate source code, data, and analytical results.

### `code/`
*   **`statistical_analysis.ipynb`**
    *   *Purpose*: Data Preprocessing & Exploratory Analysis.
    *   *Key Actions*: Loads raw data, filters for dense user/item subsets, and visualizes rating distributions. Generates the canonical `sampled_scaled_ratings.csv`.
*   **`pca_mean_filling.ipynb`**
    *   *Purpose*: Standard PCA Implementation.
    *   *Key Actions*: Implements Item-Mean filling for missing entries, computes covariance, and identifies similar items (peers) in the reduced space.
*   **`pca_mle.ipynb`**
    *   *Purpose*: Robust PCA via MLE.
    *   *Key Actions*: Estimates covariance using overlapping ratings (handling NaNs without imputation) and projects items into a latent space.
*   **`svd_analysis.ipynb`**
    *   *Purpose*: Matrix Factorization.
    *   *Key Actions*: Performs full and truncated SVD, analyzes singular value decay (Scree Plots), and evaluates reconstruction error (RMSE/MAE).
*   **`utils.ipynb`**
    *   *Purpose*: Shared Library.
    *   *Key Actions*: Centralizes configuration (paths, constants), plotting utilities, and common computation logic to ensure consistency across notebooks.

### `data/`
*   Contains the raw MovieLens dataset and intermediate processed files.

### `results/`
*   **`tables/`**: Exported CSVs including sampled datasets, similarity matrices, and error metrics.
*   **`plots/`**: analytical visualizations such as Scree plots, Cumulative Variance curves, and heatmap distributions.

## 🚀 Usage

To replicate the analysis, execute the notebooks in the following sequential order to ensure data dependencies are met:

1.  **Likelihood & Sampling**: Run `statistical_analysis.ipynb` to generate the processed dataset.
2.  **Analysis**: Run `pca_mean_filling.ipynb`, `pca_mle.ipynb`, and `svd_analysis.ipynb` in any order to perform the specific dimensionality reduction tasks.
3.  **Utilities**: `utils.ipynb` is a dependency module and does not need to be run directly; it is referenced by the other notebooks (conceptually).

---
*Group [X] - AIE425 Final Project*
