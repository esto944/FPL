# Fantasy Premier League (FPL) Player Price Tier Analysis

## Overview

This project analyzes Fantasy Premier League (FPL) player performance across different price tiers and playing positions. The main objective is to explore how player cost relates to total fantasy points and whether certain positions provide better value within low, middle, and premium price categories.

The analysis uses Python data science tools to clean, categorize, and visualize FPL player data.

---

# Project Goal

Create a box plot visualization showing the distribution of total fantasy points for different player positions across three price tiers:

* Low
* Middle
* Premium

This helps identify:

* Which positions perform best at different price levels
* How consistent player performance is within each tier
* Potential value picks in Fantasy Premier League

---

# Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Plotly
* Jupyter Notebook / Google Colab

---

# Dataset

The dataset contains Fantasy Premier League player statistics, including:

* Player position
* Player cost
* Total fantasy points
* Team information
* Performance metrics

Typical positions include:

* Goalkeeper (GK)
* Defender (DEF)
* Midfielder (MID)
* Forward (FWD)

---

# Project Structure

```text
FPL-Analysis/
│
├── FPL.ipynb                # Main analysis notebook
├── README.md                # Project documentation
├── data/                    # Dataset files
├── images/                  # Visualizations and charts
└── requirements.txt         # Python dependencies
```

---

# Analysis Workflow

## 1. Data Cleaning

* Load FPL dataset
* Handle missing values
* Prepare numerical columns

## 2. Price Tier Categorization

Players are grouped into three price categories based on cost:

| Tier    | Price Range |
| ------- | ----------- |
| Low     | Below $5.0  |
| Middle  | $5.0 – $7.5 |
| Premium | Above $7.5  |

## 3. Visualization

A box plot is generated to compare:

* Player positions
* Price tiers
* Distribution of total points

The visualization helps reveal:

* Median performance
* Performance spread
* Outliers
* Value efficiency by position

---

# Key Findings

* Premium players generally score higher total fantasy points.
* Midfielders and forwards tend to dominate the premium tier.
* Defenders in the middle tier may provide strong value relative to cost.
* Performance variability differs across positions and pricing categories.

---

# Example Visualization

The project includes box plots comparing:

* Goalkeepers
* Defenders
* Midfielders
* Forwards

across low, middle, and premium price brackets.

---

# How to Run the Project

## Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_LINK
```

## Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn plotly
```

## Open the Notebook

```bash
jupyter notebook FPL.ipynb
```

or open directly in Google Colab.

---

# Future Improvements

Possible extensions for this project:

* Predict player points using machine learning
* Build an FPL recommendation system
* Add interactive dashboards
* Analyze player consistency over time
* Compare expected points vs actual points

---

# Skills Demonstrated

This project demonstrates:

* Data cleaning
* Exploratory Data Analysis (EDA)
* Data visualization
* Feature engineering
* Python programming
* Sports analytics
* GitHub project organization

---

# Author

Created as part of a beginner data science portfolio project focused on sports analytics and Fantasy Premier League data analysis.

