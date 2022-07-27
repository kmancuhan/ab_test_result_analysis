# Date Created

July 27, 2022

# Project: AB Test Result Analysis

## Objective

The objective of this project is to analyze the impact of a new version of an existing web page on the conversion rate. The data has two groups, control and treatment. Control group should see the old version of the page whereas treatment group should see the new version of the page.

## Description

The impact analysis is done via the hypothesis testing. The data is first cleaned to make sure that some inconsistencies don't exist in the computed statistics. For example, we wouldn't want people who landed on the old page in the treatment group. We also compute some statistics to get a sense of the data.

After cleaning, we compute the conversion rate on treatment and control groups and compute the difference between the treatment and the test groups. Then, I apply both non parametric and parametric techniques on the computed statistics in order to compute the P-value under the null hypothesis.

In non parametric method, bootstrapping is used to compute the same statistics 10000 times and derive a standard deviation for it. Then, under a null hypothesis of a normal distribution with mean 0 (no observed difference); the P value is computed as in a one sided test.

In parametric method, paired z-test is applied to compute the P-value; again, for a one sided test.

Last, logistic regression is also applied as an alternative method for computing the significance of landing on a new page on the conversion rate.

## Main Findings

In both parametric and non-parametric methods, the P-values are computed and found to be pretty high (almost 90%). Hence, we failed to reject the null hypothesis. In other words, there is no significant improvement of using new page on the conversion rate. The result is also confirmed when Logistic regression is also applied. The relevant features for landing on a new page failed to be statistically significant.

# Files

## Source Files
  - Analyze_ab_test_results_notebook.ipynb

## Data Files
  - ab_data.csv
  - countries.csv

# Running Instructions

As long as you have the Jupyter Notebook with a python kernel and the necessary libraries, you should be able to download the code and run the scripts on your local. I am using an Anaconda virtual environment; however, it isn't necessary.

# Requirements
  - conda==4.12.0 (optional)
  - jupyter notebook==6.4.11
  - python==3.9.12
  - pandas==1.4.2
  - numpy==1.21.5
  - matplotlib==3.5.1
