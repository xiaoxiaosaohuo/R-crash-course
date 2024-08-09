## What is Boxplot

A boxplot gives a summary of one or more numeric variables, A boxlot is composed of several elements:
1. Median: there is a line in the box, it represents the median of the data, if the median is 10, it means that there are the same number of data points below and above 10.
2. Min and Max: They represent the smallest and largest data point int hte dataset excluding outliers, min is the bottom whisker of the boxplot, while max is the top. 
3. First Quartile(Q1): This is the 25th percentile of the data, below which 25% of the data points fall, it's the bottom edge of the box.
4. Third Quartile(Q3): This is the 75th percentile of the data, below which 75% of the data points fall, it's the top edge of the box.
5. Outliers: Data points that fall below the lower bound or above the upper bound are considered outliers. They are typically depicted as individual points.

## Interpreting a Boxplot

1. Identify the Interquartile Range (IQR): this is the distance between Q1 and Q3, it represents the middle 50% of the data.
2. Observe the median: the median line inside the box shows the central tendency of the dataset.
3. Check for Outliers: Outliers are data points that fall outside the whiskers, they might indicate variability in the data, measurement errors, or other factors.
4. Assess Symmetry: If the median is in the center of the box and the whiskers are of similar length, the data is approximately symmetric, if not, the data might be skewed.
5. Range and Spread: The overall range can be observed from the smallest to the largest values (excluding outliers), and the spread of the middle 50% of data is given by the IQR.

## Code 
```
# Creating a data frame
data_frame <- data.frame(
  group1 = c(10, 15, 14, 20, 21, 18, 30, 22, 25, 17, 15, 19),
  group2 = c(8, 5, 8, 15, 12, 14, 20, 25, 18, 13, 20, 14)
)

# Plotting a boxplot
boxplot(data_frame, main = "Boxplot of Data Frame", ylab = "Values", names = c("Group 1", "Group 2"))
```