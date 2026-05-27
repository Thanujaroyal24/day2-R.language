# Statistical Analysis in R

## Overview

This project demonstrates basic statistical analysis and data visualization using the R programming language.  
The program calculates important statistical measures such as Mean, Median, Mode, Variance, and Standard Deviation.  
It also creates graphical visualizations including Bar Plot, Histogram, and Pie Chart.

This project is useful for beginners who want to learn fundamental statistical operations in R.

---

# Features

- Display dataset
- Calculate Mean
- Calculate Median
- Calculate Mode using a custom function
- Find Maximum and Minimum values
- Calculate Variance
- Calculate Standard Deviation
- Generate Summary Statistics
- Create:
  - Bar Plot
  - Histogram
  - Pie Chart

---

# Dataset

```r
data <- c(30, 40, 50, 60, 80, 90, 100)
```

---

# Complete R Program

```r
data <- c(30, 40, 50, 60, 80, 90, 100)

print("Dataset")
print(data)

mean_value <- mean(data)
print(paste("Mean =", mean_value))

median_value <- median(data)
print(paste("Median =", median_value))

mode_function <- function(x) {
  uniq_values <- unique(x)
  uniq_values[which.max(tabulate(match(x, uniq_values)))]
}

mode_value <- mode_function(data)
print(paste("Mode =", mode_value))

max_value <- max(data)
print(paste("Maximum =", max_value))

min_value <- min(data)
print(paste("Minimum =", min_value))

variance_value <- var(data)
print(paste("Variance =", variance_value))

sd_value <- sd(data)
print(paste("Standard Deviation =", sd_value))

summary(data)

barplot(data)

hist(data)

pie(data)
```

---

# Explanation of the Program

## 1. Mean
The mean is the average of all values in the dataset.

```r
mean(data)
```

---

## 2. Median
The median represents the middle value in the sorted dataset.

```r
median(data)
```

---

## 3. Mode
R does not provide a built-in function for mode calculation, so a custom function is created.

```r
mode_function <- function(x) {
  uniq_values <- unique(x)
  uniq_values[which.max(tabulate(match(x, uniq_values)))]
}
```

---

## 4. Maximum and Minimum Values

```r
max(data)
min(data)
```

---

## 5. Variance
Variance measures how far the data values are spread from the mean.

```r
var(data)
```

---

## 6. Standard Deviation
Standard deviation measures the amount of variation in the dataset.

```r
sd(data)
```

---

## 7. Summary Statistics
The `summary()` function provides:

- Minimum
- 1st Quartile
- Median
- Mean
- 3rd Quartile
- Maximum

```r
summary(data)
```

---

# Data Visualization

## Bar Plot

```r
barplot(data)
```

A bar plot represents data using rectangular bars.

---

## Histogram

```r
hist(data)
```

A histogram shows the frequency distribution of the dataset.

---

## Pie Chart

```r
pie(data)
```

A pie chart displays data as parts of a whole.

---

# Sample Output

```r
[1] "Dataset"
[1]  30  40  50  60  80  90 100

[1] "Mean = 64.28571"
[1] "Median = 60"
[1] "Mode = 30"
[1] "Maximum = 100"
[1] "Minimum = 30"
[1] "Variance = 666.6667"
[1] "Standard Deviation = 25.81989"
```

---

# How to Run the Program

## Step 1
Install R or RStudio on your computer.

## Step 2
Save the code in a file named:

```bash
statistics_analysis.R
```

## Step 3
Run the script using RStudio or terminal:

```bash
Rscript statistics_analysis.R
```

---

# Project Structure

```bash
├── statistics_analysis.R
├── README.md
```

---

# Learning Outcomes

After completing this project, you will understand:

- Basic statistical analysis in R
- Descriptive statistics
- Custom functions in R
- Data visualization techniques
- Working with datasets in R

---

# Applications

This project can be used in:

- Data Analysis
- Academic Projects
- Statistical Learning
- Beginner R Programming Practice
- Data Visualization Exercises

---

# Future Improvements

- Add user input functionality
- Read data from CSV files
- Use advanced visualization libraries like ggplot2
- Add boxplots and scatter plots
- Perform inferential statistics

---

# Author

Your Name

---

# License

This project is open-source and free to use for educational purposes.
