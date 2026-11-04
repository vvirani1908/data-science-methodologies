# Discovering Mall Customer Segments with KDD

## Knowledge discovery goal

The project uses the KDD process to discover customer groups from annual income and spending score without a predefined target.

## Preparation and mining

Duplicates and missing values were checked, the numerical attributes were standardized, and candidate cluster counts were compared using elbow and silhouette diagnostics. K-means clustering with five groups was then fitted.

## Interpretation

The resulting groups can support marketing hypotheses such as high-income/high-spend loyal customers, high-income/low-spend opportunities, and value-focused shoppers. The segment summary and scatter plot appear in the notebook.

## Limitations

K-means depends on scaling and the selected number of clusters. The dataset does not include purchase recency or frequency, so segments must be validated with richer transaction data and tested through campaigns.

## Why KDD fits this project

KDD is appropriate because the project begins with a knowledge objective rather than a labeled prediction target. Selection defines the business question, preprocessing checks quality, transformation makes distance calculations meaningful, data mining discovers groups, and interpretation converts clusters into testable knowledge.

## Findings and actionability

Income and spending score produce distinct customer profiles that can support exploratory marketing hypotheses. For example, high-income/low-spend customers may need engagement research, while high-income/high-spend customers may respond to loyalty programs. These are hypotheses, not conclusions; controlled campaigns are required before allocating resources.

## Governance and future work

Segment labels should not be used to deny service or make decisions based on protected characteristics. Future work should add recency, frequency, monetary value, product categories, and campaign responses, then test cluster stability over time.
