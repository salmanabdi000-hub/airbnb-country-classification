# Airbnb Country Classification

Practice machine learning project evaluating whether recorded age and gender can predict the COUNTRY category in a supplied Airbnb user dataset.

## Methods

- Dataset audit and exploratory analysis
- Fixed 80/20 stratified training/test split
- Preprocessing fitted inside model pipelines
- Majority-class baseline, Logistic Regression, and Random Forest
- Five-fold cross-validation and grid-search hyperparameter tuning

## Initial results

All three evaluated models predicted US for every test record:

| Model | Accuracy | Balanced accuracy | Macro-F1 |
|---|---:|---:|---:|
| Majority baseline | 79.54% | 10.00% | 0.0886 |
| Logistic Regression | 79.54% | 10.00% | 0.0886 |
| Random Forest | 79.54% | 10.00% | 0.0886 |

Neither trained algorithm improved on the baseline. The results illustrate why accuracy alone can be misleading for imbalanced classification.

## Data and limitations

The supplied file contains 50,098 records and five columns: ID, DATE_DIFF, GENDER, AGE, and COUNTRY.

ID was excluded as an identifier. DATE_DIFF was excluded because its definition and availability at prediction time remain unverified. Ages outside the provisional 18–100 range were treated as missing and imputed within training pipelines.

The original source, usage permissions, and exact COUNTRY definition remain under investigation. Raw data is not included in this repository.

## Project status

Initial experiments are complete. The reviewed notebook, execution instructions, and supporting files will be added after final checks.

## AI assistance

ChatGPT/Codex assisted with planning, code generation, debugging guidance, and interpretation. Verification completed so far includes inspection of the saved notebook and exported results; a fresh execution check remains outstanding.
