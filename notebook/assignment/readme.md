
**Designing a model to identify time segments of a label (e.g., ACTIVE, IDLE, OFF) in time-series data rather than classifying individual data points involves segmenting the time series into contiguous labeled intervals**

-> Enter another label in the data: time_segment
-> Treat the problem as a sequence labeling task.
-> Instead of classifying each data point, use a model to detect change points where the label transitions.
-> Combine contiguous points with the same label into a single segment
-> Define transition rules to avoid unrealistic segments (e.g. short bursts of ACTIVE in the middle of OFF).

**Cost-Sensitive Learning**

Penalize misclassifications of the minority class by using class weights (e.g. hyper-parameter class_weight = 'balanced' in scikit-learn).

**Ensemble Methods**

Algorithms like Random Forest or Gradient Boosting often perform better with imbalanced datasets when properly tuned.

