# Spam Email Classifier

## Problem
Can simple text-based features reliably distinguish spam from 
legitimate emails, and which machine learning model performs 
best for this task?

## Data
- Source: TidyTuesday (2023) spam dataset
- 4,601 labeled emails (spam / not spam)
- Key variables: consecutive capital letters (crl.tot), 
  dollar sign frequency, exclamation mark frequency, 
  money keyword occurrence, string "000" occurrence

## Approach
- Removed duplicate rows to rebalance dataset from 60/40 
  to near-parity (53/46)
- Applied min-max normalization across all features
- Removed "make" variable due to low correlation (0.04) 
  with target
- Trained and evaluated 3 models with 10-fold cross-validation:
  - Logistic Regression
  - Decision Tree
  - SVM with RBF kernel
- Computed permutation importance to assess feature contributions

## Results
| Model               | Accuracy | Spam Recall | Specificity |
|---------------------|----------|-------------|-------------|
| Logistic Regression | 76.5%    | 66.4%       | 88.2%       |
| Decision Tree       | 74.2%    | 78.7%       | 69.0%       |
| SVM (RBF kernel)    | 82.0%    | 75.0%       | 89.0%       |

## Key Finding
SVM with RBF kernel outperformed all models — exclamation marks 
were the strongest spam signal (importance: 2.19), outranking 
dollar signs (1.84) and money keywords (1.50), revealing 
non-linear relationships missed by correlation analysis alone.

## Files
- `spamemails.R` — full analysis and model training script
- `spamemails_report.pdf` — full project write-up with results
