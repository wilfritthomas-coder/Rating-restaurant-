# 🍽️ Restaurant Ratings Analysis

## Project Overview

This project performs a structured data analysis on a restaurant dataset to examine the distribution of aggregate ratings and quantify user engagement through vote counts. The analysis uncovers patterns in how restaurants are rated and highlights which rating segments attract the most customer feedback.

---

## Task Objectives

| # | Objective |
|---|-----------|
| 1 | Analyze the distribution of aggregate ratings across all restaurants |
| 2 | Determine the most common rating range |
| 3 | Calculate the average number of votes received by restaurants |

---

## Dataset

| Property | Details |
|----------|---------|
| File | `dataset.csv` |
| Records | 9,551 restaurants |
| Features | 21 columns |
| Key Fields | `Aggregate rating`, `Rating text`, `Votes` |

---

## Project Structure

```
restaurant_ratings_analysis/
│
├── dataset.csv                         # Source dataset
│
├── Restaurant_Ratings_Analysis.ipynb   # Jupyter Notebook (full analysis)
│
├── README.md                           # Project overview (this file)
├── Task_Explanation.txt                # Detailed task description
│
├── fig1_rating_histogram.png           # Histogram of aggregate ratings
├── fig2_rating_range_bar.png           # Bar chart — restaurants per rating range
├── fig3_rating_pie.png                 # Pie chart — proportional rating share
├── fig4_rating_category.png            # Horizontal bar — rating text categories
├── fig5_votes_boxplot.png              # Box plot — votes across rating ranges
└── fig6_avg_votes_bar.png              # Average votes per rating range
```

---

## Key Findings

### Rating Distribution

| Rating Range | Count | Share |
|-------------|-------|-------|
| 0 – 1 | 2,148 | 22.49% |
| 1 – 2 | 10 | 0.10% |
| 2 – 3 | 1,891 | 19.80% |
| **3 – 4** | **4,388** | **45.94%** ← Most Common |
| 4 – 5 | 1,114 | 11.66% |

- **Mean Aggregate Rating:** 2.67
- **Median Aggregate Rating:** 3.20
- **Most Common Rating Range:** **3–4** (45.94% of all restaurants)

### Votes Analysis

| Metric | Value |
|--------|-------|
| Average Votes per Restaurant | **156.91** |
| Median Votes per Restaurant | 31.00 |
| Total Votes in Dataset | 1,498,645 |
| Maximum Votes (single restaurant) | 10,934 |

> **Note:** The large gap between mean (156.91) and median (31.00) indicates a right-skewed distribution — a small number of highly popular restaurants receive disproportionately high vote counts.

---

## Visualizations

| Figure | Description |
|--------|-------------|
| `fig1_rating_histogram.png` | Full distribution of aggregate ratings with mean and median markers |
| `fig2_rating_range_bar.png` | Count of restaurants in each rating range with percentage labels |
| `fig3_rating_pie.png` | Proportional share of each rating range |
| `fig4_rating_category.png` | Restaurant count per qualitative rating category |
| `fig5_votes_boxplot.png` | Spread of votes across rating ranges (outlier detection) |
| `fig6_avg_votes_bar.png` | Average votes per rating range vs. overall average |

---

## How to Run

```bash
# Open the notebook
jupyter notebook Restaurant_Ratings_Analysis.ipynb

# Or run the analysis directly
python3 analysis_script.py
```

**Requirements:** Python 3.8+, pandas, numpy, matplotlib, seaborn

---

## Insights

1. **The 3–4 rating band dominates** — nearly half of all restaurants fall here, suggesting a clustering of above-average performance in the dataset.
2. **Highly rated restaurants attract significantly more votes** — restaurants in the 4–5 range average 637 votes, vs. just 39 for the 2–3 range.
3. **Vote distribution is heavily skewed** — the median is 31 while the mean is 157, indicating popular outlier restaurants pull the average upward.
4. **"Not rated" is significant** — 2,148 restaurants (22.5%) carry a rating of 0, likely due to insufficient data, which impacts the distribution analysis.
