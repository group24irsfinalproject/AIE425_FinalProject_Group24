### Group 24

Shiref Khaled Elhalawany -  221100944

Ahmed Anis Hassan - 221100101 

Karim Ashraf Elsayed - 221100391

Kareem Shaheen - 221101524

# AIE425 Final Project: Recommender Systems Analysis

This repository contains the final project for AIE425, focusing on advanced recommender system techniques. The project is divided into two main sections: Dimensionality Reduction Analysis and a Domain-Specific Hybrid Recommender System.

## Project Structure

### [Section 1: Dimensionality Reduction Analysis](./SECTION1_DimensionalityReduction/README_SECTION1.md)
**Dataset**: MovieLens 20M

This section explores the fundamental techniques of dimensionality reduction in the context of recommender systems. It includes:
- **PCA Analysis**: Principal Component Analysis for latent feature extraction and mean-filling strategies.
- **SVD Analysis**: Singular Value Decomposition for matrix factorization, including sensitivity analysis on hyperparameters ($k$).
- **Statistical Analysis**: Deep dive into the MovieLens dataset properties.

[View Section 1 Documentation](./SECTION1_DimensionalityReduction/README_SECTION1.md)

### [Section 2: Domain-Specific Hybrid Recommender](./SECTION2_DomainRecommender/README_SECTION2.md)
**Dataset**: Amazon Books (2023)

This section implements a comprehensive hybrid recommender system tailored for the book domain. Key components include:
- **Content-Based Filtering**: TF-IDF vectorization of book metadata (titles, descriptions).
- **Collaborative Filtering**: SVD Matrix Factorization and KNN approaches.
- **Hybrid Methods**: Implementation and comparison of Weighted, Switching, and Cascade hybrid strategies.
- **Cold-Start Simulation**: Robust evaluation of recommendation performance for new users.

[View Section 2 Documentation](./SECTION2_DomainRecommender/README_SECTION2.md)

## Setup and Installation

1.  **Environment**: Ensure you have Python installed (Python 3.8+ recommended).
2.  **Dependencies**: Install the required packages using the provided requirements file:
    ```bash
    pip install -r requirements.txt
    ```
3.  **Data**: 
    - **Section 1**: Uses MovieLens 20M.
    - **Section 2**: Uses Amazon Books. Please follow the download instructions in the [Section 2 README](./SECTION2_DomainRecommender/README_SECTION2.md#setup-instructions) to acquire the Amazon Books dataset.

## Execution

Navigate to the respective code directories for each section to run the Jupyter Notebooks.
- **Section 1**: `SECTION1_DimensionalityReduction/code/`
- **Section 2**: `SECTION2_DomainRecommender/code/`
