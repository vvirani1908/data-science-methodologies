# KDD Operationalization Plan

Although KDD is primarily a knowledge-discovery process, the discovered segments can be operationalized carefully:

1. Run the approved preprocessing and clustering pipeline on a scheduled customer extract.
2. Store the segment label, scoring date, model version, and input-data version.
3. Present segment profiles in a dashboard for marketing analysis.
4. Use segments only to form testable campaign hypotheses.
5. Measure campaign lift with a controlled experiment.
6. Monitor segment sizes, feature drift, and assignment stability.
7. Refit or review the clusters when the data distribution changes materially.

No customer should be denied service or opportunity based only on an exploratory cluster. Protected characteristics should not be used for unfair targeting.
