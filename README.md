# NBA Sports Betting Using Machine Learning

This project uses machine learning to predict the outcomes (winners and over/under) of NBA games. By analyzing historical team data from the 2007-08 season to the current season, alongside the odds for these games, the model forecasts the outcomes for today's games. The model achieves approximately 69% accuracy on money lines and 55% accuracy on over/under bets.

The project also calculates the expected value for money line bets to provide deeper insights and incorporates  for optimal bankroll management. A safer betting approach is also supported by using 50% of the recommended stake.

## Packages Used

Use Python 3.11. In particular the packages/libraries used are...

* Tensorflow - Machine learning library
* XGBoost - Gradient boosting framework
* Numpy - Package for scientific computing in Python
* Pandas - Data manipulation and analysis
* Colorama - Color text output
* Tqdm - Progress bars
* Requests - Http library
* Scikit_learn - Machine learning library



```bash
$ git clone https://github.com/rohitq1/Betting_nba.git
$ cd NBA
$ pip3 install -r requirements.txt
$ python3 main.py -xgb -odds=fanduel
```

Odds data will be automatically fetched from sbrodds if the -odds option is provided with a sportsbook.  Options include: fanduel, draftkings, betmgm, pointsbet, caesars, wynn, bet_rivers_ny

If `-odds` is not given, enter the under/over and odds for today's games manually after starting the script.

Optionally, you can add '-kc' as a command line argument to see the recommended fraction of your bankroll to wager based on the model's edge



```
cd Flask
flask --debug run
```

## Getting new data and training models
```
# Create dataset with the latest data for 2023-24 season
cd src/Process-Data
python -m Get_Data
python -m Get_Odds_Data
python -m Create_Games

# Train models
cd ../Train-Models
python -m XGBoost_Model_ML
python -m XGBoost_Model_UO
```
