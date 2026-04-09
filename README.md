# MLB Analytics & Betting Disparity Platform

An end-to-end data science project analyzing **45,000+ MLB games across 10 seasons (2012–2021)** to surface systematic disparities between pregame betting lines and actual outcomes. Built with Python, scikit-learn, and NLP-generated game summaries.

---

## What This Project Does

- Converts American moneyline odds into normalized implied win probabilities
- Engineers features to measure how strongly a team is favored relative to the market
- Trains a logistic regression model to predict game outcomes
- Generates natural language summaries for every game using NLP techniques
- Identifies where betting lines are systematically miscalibrated across probability ranges

---

## Key Finding

Betting lines are most miscalibrated at the extremes.

| Implied Probability Range | Actual Win Rate vs. Implied | Interpretation |
|---|---|---|
| 40–50% | Slight underperformance | Lines slightly overprice underdogs |
| 50–60% | Slight outperformance | Mild favorites deliver on expectations |
| 60–65% | Underperformance | Market overprices moderate favorites |
| **65–70%** | **Strongest outperformance** | **Best-calibrated range in the dataset** |
| 70%+ | Underperformance | Extreme favorites underperform implied odds |

> Teams priced at 70%+ implied probability consistently underperform — suggesting the market overreacts to dominant matchups. The 65–70% range is where implied probability most accurately reflects actual outcomes.

---

## Tech Stack

- **Python** — pandas, NumPy, matplotlib, scikit-learn
- **NLP** — rule-based narrative summary generation per game
- **Modeling** — Logistic Regression with engineered features (implied prob differential, line gap)
- **Data** — 45,530 game records, 2012–2021 MLB seasons

---

## Project Structure

```
mlb-analytics-dashboard/
│
├── 4050_Project.ipynb        # Full analysis notebook
├── mlb_game_summaries.csv    # Processed dataset with NLP summaries
├── disparity_chart.png       # Betting line disparity visualization
└── README.md
```

## Disparity Chart

<img width="989" height="490" alt="disparity-chart" src="https://github.com/user-attachments/assets/aff58b16-b32c-4e1e-a9d0-0827c898a9ce" />


---

## How to Run

1. Clone the repo
2. Upload `oddsDataMLB.csv` to your working directory
3. Open `4050_Project.ipynb` in Google Colab or Jupyter
4. Run all cells in order

---

## Author

**Christopher Alford**  
Senior, B.S. Data Science — University of North Texas  
[linkedin.com/in/alford-christopher](https://linkedin.com/in/alford-christopher) | [github.com/christopher-alford](https://github.com/christopher-alford)
