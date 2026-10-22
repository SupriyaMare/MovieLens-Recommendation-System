# 🎬 MovieLens Recommendation System

A movie-rating prediction project using the **MovieLens 10M dataset**, developed in R as a data science and machine learning project. The goal is to predict user ratings for movies and evaluate model performance using Root Mean Squared Error (RMSE).

## 📌 Project Overview

Movie recommendation systems help users discover movies based on rating patterns and preferences. This project explores rating data, develops progressively more advanced prediction models, and compares their performance to identify an effective approach.

The analysis covers exploratory data analysis (EDA), rating distributions, movie and user effects, regularization, and matrix factorization.

## 🎯 Objectives

- Explore the MovieLens dataset and understand user-rating patterns.
- Analyze movie ratings, user activity, genres, and rating trends.
- Build and compare baseline and advanced rating-prediction models.
- Apply regularization to reduce overfitting.
- Evaluate model performance using RMSE.
- Identify a model that improves rating predictions over a simple baseline.

## 📊 Dataset

The project uses the **MovieLens 10M dataset**, containing millions of movie ratings from users.

The report describes the following data partitions:

| Dataset | Approximate records |
|---|---:|
| Training dataset (`edx`) | 9,000,055 |
| Validation dataset | 999,999 |

The data includes user IDs, movie IDs, ratings, timestamps, and movie-related information used for exploratory analysis.

**Data source:** [GroupLens MovieLens datasets](https://grouplens.org/datasets/movielens/)

Note: The figures above are reported in the project documentation. Confirm them against the actual data files before claiming that the analysis has been reproduced.

## 🛠️ Technologies Used

- **R** — data analysis and model development
- **R Markdown** — analytical reporting
- **Data visualization** — exploratory analysis and model evaluation
- **`recosystem`** — matrix-factorization modeling using stochastic gradient descent
- **RMSE** — model-performance evaluation

## 🔍 Methodology

### 1. Exploratory Data Analysis

- Examined rating distributions and user activity.
- Investigated movie popularity and genre patterns.
- Explored rating trends over time.
- Created visualizations to understand the dataset.

### 2. Baseline Model

Established a baseline using the global average rating. This provided a reference point for evaluating more advanced models.

### 3. Movie and User Effects

Introduced movie-specific and user-specific rating effects to capture differences in movie popularity and individual rating behavior.

### 4. Regularization

Applied regularization to the movie and user effects model to help control overfitting and improve generalization.

### 5. Matrix Factorization

Explored matrix factorization to learn latent user and movie representations from rating patterns. The report describes an implementation using the `recosystem` package and stochastic gradient descent.

### 6. Model Evaluation

Compared model predictions using Root Mean Squared Error (RMSE). Lower RMSE indicates that predicted ratings are closer to actual ratings on the evaluated dataset.

## 📈 Results

The following results are transcribed from the project report and have **not been independently reproduced**.

| Model | Reported RMSE |
|---|---:|
| Global average baseline | 1.0599 |
| Movie effects | 0.9437 |
| Movie and user effects | 0.8659 |
| Regularized movie and user effects | 0.8652 |
| Matrix factorization — development evaluation | 0.7965 |
| Final matrix factorization — validation | **0.7867** |

The final reported matrix-factorization RMSE is approximately **25.8% lower than the global-average baseline**, based on the values in the report.

These values should be treated as report-reported results until the source code and evaluation procedure have been run successfully. The development and validation figures should not be assumed to represent the same evaluation split.

## 📂 Project Structure

Organize your GitHub repository like this, adjusting filenames to match the files you actually have:

```text
MovieLens-Recommendation-System/
├── README.md
├── report/
│   └── MovieLens-Recommendation-System-Project.pdf
├── src/
│   └── movielens_model.R
├── notebooks/
│   └── exploratory-analysis.Rmd
├── results/
│   └── visualizations/
├── data/
│   └── README.md
└── LICENSE
```

**Important:** Only include files that actually exist. If you currently have only the PDF report, upload it under `report/` and remove or clearly mark the source-code, notebook, and visualization paths as planned additions. Do not create placeholder files that imply the implementation is available.

## 🚀 How to Reproduce the Project

Reproduction requires the original R source code, the required dataset partitions, and the relevant package dependencies.

1. Install [R](https://cran.r-project.org/) and [RStudio](https://posit.co/download/rstudio-desktop/).
2. Obtain the MovieLens dataset from [GroupLens](https://grouplens.org/datasets/movielens/).
3. Prepare the training and validation datasets using the procedure required by your implementation.
4. Install the R packages used by the source code, including `recosystem` if the matrix-factorization implementation requires it.
5. Run the R script to train the model, generate predictions, and calculate RMSE.
6. Render the R Markdown report, if available, to regenerate the analysis and visualizations.
7. Compare the reproduced metrics with the values documented above.

The steps cannot be completed from the PDF alone. Exact reproduction also depends on the original preprocessing, random seeds, package versions, data partitions, and evaluation procedure.

## ⚠️ Limitations and Future Improvements

- Reproduce and verify the reported metrics using the original source code.
- Compare the model against additional collaborative-filtering approaches.
- Investigate cold-start problems for new users and movies.
- Explore recommendation ranking and top-N recommendations in addition to rating prediction.
- Develop an interactive interface for users to explore movie recommendations.

## 📚 Reference

The repository [altaflab/movielens](https://github.com/altaflab/movielens) was consulted as a reference for organizing a MovieLens capstone project around R, R Markdown, a PDF report, and model evaluation.

This repository is a reference, not the source of the results presented above. The results in this README are based on the supplied project report.

## 👩‍💻 Project Status

**Status:** Report documented; source-code reproducibility should be verified before describing the project as fully reproducible.

