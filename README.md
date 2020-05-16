# MLSP-Hackathon
### 4th Place Solution for DataHack's Machine Learning Starter Program Hackathon 
Link to leaderboard: https://datahack.analyticsvidhya.com/contest/machine-learning-starter-program-hackathon/#LeaderBoard

The aim of this hackathon was to predict if a trainee will pass the examination for a particular program.

Given dataset had demographic details about the trainee as well the course.

### Approach:
* Final model was a weighted average blend of bagged CatBoost and Xgboost models
* Both models were trained on seperate datasets
* For CatBoost:
  * User **SelectFromModel** from sklearn to obtain import features
  * Created interactions amongst these features
  * Fed categorical features as it is to model
* For Xgboost:
  * Created interactions among intuitively selected features
  * Frequency encoded categorical feats
  
### Things that can improve score:
* Intuitive label encoding of categorical features
* Droping "Age" feature which has considerable missing values
