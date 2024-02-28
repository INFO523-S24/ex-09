# Ex-08: Analyzing Egg Production Trends

## Objective:

Analyze the impact of different housing conditions on egg production using regression models, focusing on understanding the relationship between cage-free percentages and overall production.

**Prerequisites:** Ensure Python, Jupyter Notebook, and necessary libraries (**`pandas`**, **`numpy`**, **`scikit-learn`**, **`matplotlib`**, **`seaborn`**) are installed. The datasets **`egg-production.csv`** and **`cage-free-percentages.csv`** should be accessible in the **`data`** directory.

## Dataset:

The data this week comes from [The Humane League's US Egg Production dataset](https://thehumaneleague.org/article/E008R01-us-egg-production-data) by [Samara Mendez](https://samaramendez.github.io/). Dataset and code is available for this project on OSF at [US Egg Production Data Set](https://osf.io/z2gxn/).

This dataset tracks the supply of cage-free eggs in the United States from December 2007 to February 2021. For TidyTuesday we've used data through February 2021, but the full dataset, with data through the present, is available in the [OSF project](https://osf.io/z2gxn/).

> In this project, they synthesize an analysis-ready data set that tracks cage-free hens and the supply of cage-free eggs relative to the overall numbers of hens and table eggs in the United States. The data set is based on reports produced by the United States Department of Agriculture (USDA), which are published weekly or monthly. They supplement these data with definitions and a taxonomy of egg products drawn from USDA and industry publications. The data include flock size (both absolute and relative) and egg production of cage-free hens as well as all table-egg-laying hens in the US, collected to understand the impact of the industry's cage-free transition on hens. Data coverage ranges from December 2007 to February 2021.

We'll use two datasets: **`egg-production.csv`** and **`cage-free-percentages.csv`**, which include monthly observations of egg production types, housing conditions, and the percentages of cage-free eggs. These datasets provide a unique opportunity to explore the effects of production practices on egg production volumes.

### Metadata for **`egg-production.csv`:**

| Variable             | Class     | Description                                                          |
|-----------------|-----------------|---------------------------------------|
| **`observed_month`** | double    | Month in which observations were collected                           |
| **`prod_type`**      | character | Type of egg product: hatching, table eggs                            |
| **`prod_process`**   | character | Production process and housing: cage-free (organic/non-organic), all |
| **`n_hens`**         | double    | Number of hens                                                       |
| **`n_eggs`**         | double    | Number of eggs produced                                              |
| **`source`**         | character | Original USDA report source                                          |

### **Metadata for `cage-free-percentages.csv`:**

| **Variable**         | **Class** | **Description**                                                    |
|----------------|----------------|----------------------------------------|
| **`observed_month`** | double    | Month in which observations were collected                         |
| **`percent_hens`**   | double    | Percentage of cage-free hens relative to all table-egg-laying hens |
| **`percent_eggs`**   | double    | Percentage of cage-free eggs relative to all table eggs            |
| **`source`**         | character | Original USDA report source                                        |

(Source: [TidyTuesday](https://github.com/rfordatascience/tidytuesday/blob/master/data/2023/2023-08-15/readme.md))

## **Question:**

How do cage-free production practices influence overall egg production?

## **Step 1: Setup and Data Preprocessing**

1.  Begin by importing necessary libraries and loading the datasets.

2.  Merge the datasets on the **`observed_month`** variable and preprocess the data by encoding categorical variables and handling missing values if any.

## **Step 2: Exploratory Data Analysis (EDA)**

1.  Conduct EDA to understand the distribution of cage-free percentages and their relationship with egg production volumes.

2.  Utilize visualizations like scatter plots and histograms to illustrate these relationships.

## **Step 3: Model Training**

1.  Train regression models to predict **`n_eggs`** using **`percent_hens`** and other relevant variables as predictors.

2.  Consider linear regression, ridge regression, and lasso regression for this task. Evaluate the models based on training data.

## **Step 4: Model Evaluation and Interpretation**

1.  Use metrics such as R-squared, Mean Squared Error (MSE), and coefficients analysis to evaluate the performance of your models.

2.  Discuss the significance of cage-free percentages in predicting egg production volumes.

## **Assignment:**

1.  Implement the data preprocessing, model training, and evaluation steps.

2.  Explore the relationship between cage-free percentages and egg production, utilizing the models trained.

3.  Reflect on the implications of your findings for the poultry industry, particularly concerning cage-free housing practices.

## **Submission:**

-   Submit your Jupyter Notebook via the course's learning management system, including your code, visualizations, and a brief discussion of your findings regarding the impact of cage-free practices on egg production.
