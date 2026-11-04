# Titanic Survival Prediction with SEMMA

## Sample and Explore

The Titanic dataset provides a compact example of supervised classification. Survival was explored by passenger class, missingness, and class balance.

## Modify and Model

Passenger class, sex, age, family counts, fare, and embarkation port were retained. Numeric values were imputed and standardized; categorical values were imputed and one-hot encoded. Logistic regression was trained on a stratified split.

## Assess

The notebook reports accuracy, precision, recall, F1, and a confusion matrix on unseen passengers. The assessment emphasizes that accuracy alone does not describe all error types.

## Limitations

This historical sample is not a causal explanation of survival and should not be used for real-world individual decisions. More robust work would compare multiple models and use cross-validation.

## Why SEMMA fits this project

SEMMA emphasizes an analytical workflow: sample the data, explore patterns, modify variables, model the target, and assess performance. The notebook reflects that sequence while documenting why variables were retained or excluded. This is important because a good score without a clear transformation history is difficult to reproduce or defend.

## Findings and responsible interpretation

Passenger class, sex, age, fare, and family structure provide useful predictive information in this historical sample. These relationships describe the recorded dataset; they do not establish that changing one characteristic would cause a different outcome. The model is therefore useful as a classroom demonstration of classification, not as a system for evaluating real people.

## Future work

A stronger study would use nested cross-validation, compare calibrated probabilities, inspect subgroup error rates, and test whether the results remain stable across different samples.
