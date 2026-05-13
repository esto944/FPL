# Fantasy Premier League Data Analysis

This project analyzes Fantasy Premier League (FPL) player performance using Python, data analysis, and visualization tools.

The goal is to discover:
- Top-performing players
- Undervalued players
- Team trends
- Predictive insights for smarter FPL decisions

---

# Project Preview

## Top 10 Players by Total Points

![Top Players](images/top_players.png)

This graph shows the players with the highest total FPL points.

---

## Player Price vs Total Points

![Price vs Points](images/price_vs_points.png)

This scatter plot helps identify undervalued players by comparing player cost to points earned.

---

## Goals by Position

![Goals by Position](images/goals_by_position.png)

This graph compares goals scored by different player positions.

---

# Tools Used

- Python
- Pandas
- Matplotlib
- Jupyter Notebook

---

# Project Structure

```text
fpl-analysis/
│
├── data/
│   └── players.csv
│
├── images/
│   ├── top_players.png
│   ├── price_vs_points.png
│   └── goals_by_position.png
│
├── notebooks/
│   └── FPL_fixed.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

# How to Run the Project

## 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/fpl-analysis.git
```

## 2. Open the Project

```bash
cd fpl-analysis
```

## 3. Install Required Libraries

```bash
pip install pandas matplotlib jupyter
```

## 4. Start Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
FPL_fixed.ipynb
```

---

# How the Graphs Were Made

## Import Libraries

```python
import pandas as pd
import matplotlib.pyplot as plt
```

---

# Load the Dataset

```python
df = pd.read_csv("data/players.csv")
```

---

# Graph 1 — Top Players

## Code

```python
top_players = df.sort_values(by='total_points', ascending=False).head(10)

plt.figure(figsize=(10,5))

plt.bar(top_players['name'], top_players['total_points'])

plt.title('Top 10 FPL Players')
plt.xlabel('Player')
plt.ylabel('Total Points')

plt.xticks(rotation=45)

plt.savefig("images/top_players.png")

plt.show()
```

## Explanation

This graph:
- Sorts players by total points
- Selects the top 10 players
- Creates a bar chart
- Saves the graph as an image

The image is automatically stored inside:

```text
images/top_players.png
```

---

# Graph 2 — Price vs Points

## Code

```python
plt.figure(figsize=(8,6))

plt.scatter(df['now_cost'], df['total_points'])

plt.title('Player Price vs Total Points')
plt.xlabel('Player Price')
plt.ylabel('Total Points')

plt.savefig("images/price_vs_points.png")

plt.show()
```

## Explanation

This scatter plot compares:
- Player price
- Total points

It helps identify:
- Cheap high-performing players
- Expensive underperforming players

---

# Graph 3 — Goals by Position

## Code

```python
position_goals = df.groupby('position')['goals_scored'].sum()

position_goals.plot(kind='bar', figsize=(8,5))

plt.title('Goals by Position')
plt.xlabel('Position')
plt.ylabel('Goals')

plt.savefig("images/goals_by_position.png")

plt.show()
```

## Explanation

This graph:
- Groups players by position
- Adds total goals for each position
- Creates a bar chart

Useful for understanding:
- Which positions score the most goals

---

# How to Add Graphs to GitHub README

## Step 1 — Save Graphs

Always save graphs like this:

```python
plt.savefig("images/graph_name.png")
```

---

## Step 2 — Create an Images Folder

Inside your project:

```text
fpl-analysis/
└── images/
```

Put all graph images there.

---

## Step 3 — Add Images to README

Use this format:

```markdown
![Graph Name](images/graph_name.png)
```

Example:

```markdown
![Top Players](images/top_players.png)
```

GitHub will automatically display the graph.

---

# Future Improvements

Possible future features:
- Machine learning predictions
- Expected goals (xG) analysis
- Team strength analysis
- Weekly transfer recommendations
- Interactive dashboards

---

# Author

Est

Aspiring Data Scientist & Fantasy Premier League Analyst
