
# Feature Selection Rationale for Book Recommendation

## 1. Text Features (TF-IDF)
- **Source**: 'title' combined with 'categories'.
- **Method**: TF-IDF (Term Frequency-Inverse Document Frequency).
- **Reason**: Books are content-rich items. Title and categories provide strong semantic signals about the book's topic/genre. TF-IDF downweights common words ensuring unique keywords drive similarity.

## 2. Numerical Features
- **Features**: 'price', 'average_rating'.
- **Method**: Min-Max Scaling [0, 1].
- **Reason**: 
    - **Price**: Users often prefer books in specific price ranges. Normalization ensures it doesn't dominate the vector space.
    - **Average Rating**: Acts as a proxy for quality. Higher rated items might be more 'summable' with other high quality items.

## 3. Categorical Features
- **Method**: One-Hot Encoding (Top 20 frequent categories).
- **Reason**: While 'categories' are in the text indices, explicit dimensions for major genres (Fiction, Mystery, etc.) allow the model to strictly cluster items of the same 'type' even if titles are very different.

## 4. Combination
- We stack these vectors. The final representation mixes semantic similarity (Text) with property similarity (Price/Quality/Genre).
