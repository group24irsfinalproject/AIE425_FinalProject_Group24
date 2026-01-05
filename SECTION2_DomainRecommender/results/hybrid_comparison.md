
    ## Comparison of Hybrid Methods
    
    | Hybrid Method | Advantages | Disadvantages |
    |---------------|------------|---------------|
    | **Weighted** (alpha=0.5) | Balances relevance (CB) and serendipity (CF). Smooth transition. | Hard to tune alpha. CF scaling issues. |
    | **Switching** | Handles Cold Start perfectly (Uses CB). Optimizes for data-rich users (CF). | Hard threshold (10 ratings) can be abrupt. |
    | **Cascade** | Computationally efficient (CF only ranks subset). High precision. | 'Zero-hit' problem: if CB misses, CF can't recover it. |
    
    ## Choice of Best Hybrid: **Switching Hybrid**
    **Justification**:
    1.  **Cold Start Handling**: Our dataset likely has many users with few ratings. Switching ensures they get decent CB recommendations immediately.
    2.  **Quality Cap**: For heavy users, SVD (Item-Based CF) typically outperforms CB in capturing latent tastes. Switching leverages this.
    3.  **Simplicity**: It avoids the complex normalization and weighting issues of Weighted Hybrid and the 'Zero-hit' risk of Cascade.
    