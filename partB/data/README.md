# Dataset Information

## Dataset Used
**Wine Dataset** from scikit-learn (`sklearn.datasets.load_wine`)

## Source
- Originally from the UCI Machine Learning Repository
- Available directly via `sklearn.datasets.load_wine()`
- No manual download required

## Description
- **Samples:** 178
- **Features:** 13 (chemical analysis measurements of wines from three different cultivars)
- **Classes:** 3 (class 0, class 1, class 2)
- **Task:** Multiclass classification (used as multiclass cost-sensitive classification with a custom cost matrix)

## How It Is Used
1. Loaded directly via scikit-learn in each notebook — no external files needed.
2. Features are standardized using `StandardScaler`.
3. A custom non-uniform cost matrix is defined to create a cost-sensitive classification problem.
4. Train/test split: 70/30, random seed = 42.

## Why This Dataset
- The original paper (Tu & Lin, ICML 2010) uses UCI datasets including Wine for evaluation.
- We use the same dataset but with a custom cost matrix (not identical to the paper's) to demonstrate the method on a genuine cost-sensitive problem.
- 178 samples and 3 classes keep experiments CPU-friendly and fast to iterate.

## Limitations vs. Original Paper
- The paper tests on datasets with up to 10+ classes and thousands of samples.
- Our cost matrix is manually designed, whereas the paper uses structured cost matrices from the literature.
