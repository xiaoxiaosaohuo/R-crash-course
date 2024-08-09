## Scatterplot

## Key Components of a Scatterplot
1. Data points: Each point represents a pair of values from your dataset.
2. X-axis: This axis typically represents the independent variable.
3. Y-axis: This axis represents the dependent variable.
4. Title: A descriptive title often summarizing what the scatterplot is about.
5. Labels: Descriptive labels for the X and Y axis to indicate what each axis represents.

## Interpreting a Scatterplot
1. Overall Pattern
- Positive Relationship: If the points tend to rise from the bottom-left to the top-right, this suggests a positive relationship between the variables; as the X value increases, the Y value tends to increase.
- Negative Relationship: If the points fall from the top-left to the bottom-right, this suggests a negative relationship; as the X value increases, the Y value tends to decrease.
- No Relationship: If there is no discernible pattern (the points are randomly scattered), this suggests no relationship between the variables.

2. Strength of Relationship:

- Strong Relationship: Points closely clustered to a line indicate a strong relationship.
- Weak Relationship: Points widely scattered indicate a weak relationship.
3. Form of Relationship:

- Linear: Points roughly form a straight line.
- Non-linear: Points form a curve or some other non-linear pattern.
4. Clusters: Identify any clusters (groups of points) which may indicate subgroups within your data.

5. Outliers: Individual points that fall far from the general pattern of data. These might indicate variability, experimental errors, or special cases requiring further investigation.

## Code
1. Basic
```
# Sample data
x <- rnorm(100)  # 100 random numbers from a normal distribution
y <- rnorm(100)  # 100 random numbers from a normal distribution

# Basic scatterplot
plot(x, y, main="Scatterplot of Random Data", xlab="X-axis Label", ylab="Y-axis Label", pch=19)  # pch=19 plots solid circles
```
2. scatterplot with grouping

```
# Sample data with two groups
group <- sample(c("Group 1", "Group 2"), 100, replace=TRUE)
colors <- ifelse(group == "Group 1", "blue", "green")

# Scatterplot with grouping
plot(x, y, main="Scatterplot with Groups", xlab="X-axis Label", ylab="Y-axis Label", pch=19, col=colors)
legend("topright", legend=c("Group 1", "Group 2"), col=c("blue", "green"), pch=19)
```