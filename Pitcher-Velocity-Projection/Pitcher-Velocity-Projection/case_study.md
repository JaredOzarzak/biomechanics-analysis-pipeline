# Five-Year Velocity Projection: 2025 FCL Pitchers

## Overview
The question: which 2025 FCL pitcher is most likely to throw the hardest fastball five years from now? The 2025 FCL file contains pitching biomechanics but no measured velocity, so I trained a model on a separate dataset that has both and used it to estimate velocity for the FCL pitchers. This was completed as a technical assessment.

## Data
- **Training set:** 8,981 pitches from 203 pitchers, with measured velocity and 66 biomechanical metrics
- **2025 FCL set:** 5,450 pitches from 71 pitchers after filtering out 2024 rows from the raw file (6,893 rows)

## Methods
- Audited both datasets (missing values, dates, overlapping columns) and kept only the 66 columns present in both. Removed pitcher ID and date so the model couldn't use them as shortcuts, and filled missing values with training-set medians
- Looked at correlations with velocity and compared the top 10% of pitches against the rest
- Validated with 5-fold grouped cross-validation by pitcher ID, so no pitcher appears in both the training and test folds
- Compared a baseline mean model, ridge regression, and a small random forest, and used the random forest
- Predicted velocity for every FCL pitch, corrected for the model's average over-prediction in validation, and aggregated to the pitcher level
- Only ranked pitchers with at least 20 fastballs (20 of the 71 had fewer), since small samples are noisy
- Checked how stable the ranking was with a bootstrap (25 runs of resampling the training pitches, refitting the model, and re-ranking)
- Used pitchers who appeared at two levels (2024 FCL and 2025 FSL) as a rough reference for how velocity develops: about +1 mph per level

## Model performance
| Model | RMSE (mph) | MAE (mph) | R² |
|---|---|---|---|
| Small random forest | 2.58 | 2.06 | 0.07 |
| Baseline (mean) | 2.68 | 2.12 | -0.00 |
| Ridge regression | 2.77 | 2.11 | -0.07 |

The model does only slightly better than guessing the average. Biomechanics alone explains a small share of pitch velocity, and the data has no age, strength, health, or training history. Because of that, I treated the rankings as tiers rather than exact predictions.

## Results
- The most influential features were torso side-bend at maximum external rotation, maximum torso rotation velocity, and player height, followed by throwing-arm and glove-side shoulder and elbow measures
- **Pitcher 119** came out on top: about 94 mph projected on 212 fastballs, and in the top five in all 25 bootstrap runs
- Pitchers 265, 96, 94, 171, and 195 sat in a close group around 93 mph, within the model's error, so I treated them as a tier
- Pitcher 16 ranked very high on raw results but only had 15 fastballs, so I excluded him as a likely small-sample spike

## Limitations
- Low R² means the individual projections have wide error
- No birthdates or body-composition data, so the development estimate is a general reference and not an aging curve for each pitcher
- Bootstrap used 25 runs to keep the notebook fast

## Technical Stack
Python, Google Colab, pandas, NumPy, scikit-learn, Matplotlib

## Reference
Aguinaldo, A. L., & Escamilla, R. F. (2019). Segmental Power Analysis of Sequential Body Motion and Elbow Valgus Loading During Baseball Pitching. *American Journal of Sports Medicine, 47*(7), 1600-1608.
