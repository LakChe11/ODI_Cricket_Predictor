# ODI Cricket Winner Predictor

## Overview
Predicts the winner of One Day International (ODI) cricket matches using historical match data and feature engineering.  
This project demonstrates **data cleaning, feature engineering, machine learning**, and **predictive modeling** for sports analytics.

## Dataset
- Source: Kaggle  
- Contains 4500+ ODI matches with details such as teams, venue, toss, runs, and results.  
- Placed in `data/raw_matches.csv`  

## Features
The model uses the following features:

1. **Toss winner** (`toss_winner_team1`) – whether Team1 won the toss  
2. **Home advantage** (`team1_home`) – whether Team1 is playing in its own country  
3. **Team1 historical win %** (`team1_win_pct`) – win percentage of Team1 in past matches  
4. **Team2 historical win %** (`team2_win_pct`) – win percentage of Team2 in past matches  
5. **Head-to-head record** (`head2head_team1`) – Team1 win percentage vs Team2  
6. **Team1 recent form** (`team1_recent_form`) – win percentage in last 5 matches  

## Model
- **Baseline**: Logistic Regression  
- **Upgraded**: Logistic Regression with advanced features  
- **Accuracy**: ~60–65% on test set  
- Features can be extended for more advanced models like **Random Forest** or **Gradient Boosting**

## Usage
1. Open the Jupyter notebook: `notebooks/1_ODI_predictor.ipynb`  
2. Run all cells from top to bottom  
3. Predict new matches using the function:

```python
predict_match(team1, team2, toss_winner, venue_country)
