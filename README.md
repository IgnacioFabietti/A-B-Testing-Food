# A/B Testing for Fast Food Marketing Campaign

## Experiment Description

A fast-food chain plans to add a new item to its menu. However, they are still undecided between three possible marketing campaigns for promoting the new product. In order to determine which promotion has the greatest effect on sales, the new item is introduced at locations in several randomly selected markets. A different promotion is used at each location, and the weekly sales of the new item are recorded for the first four weeks.

### Experiment Goal 

Evaluate A/B testing results and decide which marketing strategy works the best.

### Hypothesis

We hypothesized that one of the three promotions has better effect than the two others, increasing revenue.

### Unit of Diversion 

The unit of diversion is _LocationID_, an unique identifier for store location.

### Evaluation Metrics

**SalesInThousands:** sales amount for a specific  _LocationID_,  _Promotion_, and  _week_

## Experiment Analysis

Compare the distribution of the whole markets (not subsetted by time or market size) for each Promotion.

### Normality
All three promotions fail the Shapiro-Wilk Test of normality.

### Variance Homogeneity 
The distributions pass the Lavene test of variance homogeneity.

### Sign Tests
We run  a right-tail Mann–Whitney  _U_  non- parametric test, for each pair of distributions, where for promotion #1 was proven statistically bigger than #2 and #3, and #3 was shown bigger than #2.

## Recommendation
The purpose of conducting this experiment was to test which of the three promotions had a better impact on sales.
The answer to the client is that the promotion # 1 is the best promotion and should be considered. Promotion # 2 was less effective than promotion # 1 and promotion # 3, whereas promotion # 3 isn't as effective as promotion # 1.

## Follow-Up Experiment
Further analysis could be done by grouping the _Week_ , _AgeOfStore_ or _MarketSize_ columns.
If the new subsets showcase normality, parametric tests could be carried out to observe differences.
