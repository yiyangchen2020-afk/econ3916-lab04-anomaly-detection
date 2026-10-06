# Robust Statistics -- Automated Anomaly Detection

## Objective
I used the California Housing dataset to compare different summary statistics and outlier detection methods, and to see how they respond to extreme values and data contamination.

## Methodology
- Computed the mean, median, 10% trimmed mean, standard deviation, IQR, and MAD using 20,640 observations.
- Used Tukey Fences to identify unusually high or low housing values.
- Applied Isolation Forest to detect unusual observations using multiple variables at the same time.
- Compared the observations flagged by Tukey Fences and Isolation Forest.
- Ran a contamination experiment by replacing 5% of the housing values with extreme values.
- Compared how the mean, median, and trimmed mean changed after contamination.

## Key Findings
Tukey Fences and Isolation Forest did not flag exactly the same observations because they identify different types of unusual values. Tukey Fences focus on extreme values in one variable, while Isolation Forest can detect unusual combinations across several variables.

After 5% contamination, the mean increased by 67.13%, while the median increased by only 3.56%. The trimmed mean increased by 6.88%. This shows that the median and trimmed mean were much less affected by the extreme values than the mean.
