# Predicting MLB game outcomes
Sports betting is a multi billion dollar industry that’s only growing larger YoY, but trying to predict an outcome is really a 50/50 chance. Some of the best teams in the MLB will only win 60% of their regular seaon games. For context, 98 wins is 60.4% out of 162 games and there were only 4 teams in the MLB that had more than 98 wins in 2019. 

My goal is to predict whether or not the Home team will win their game, and to hopefully beat Vegas.

# The Data
Player data was web scraped from MLB.com to examine individual player and pitcher statistics.
Game data was pulled from Retrosheet.org in order to evaluate individual game outcomes.

# Feature Engineering
My focus was on key offensive and defensive statistics that would either help or hinder a team from winning a game.

Offensively, I wanted to:
- Leverage teams prior season stats.
- Create a 3-day & 7-day rolling average trends for certain offensive metrics.

Defensively, I wanted to:
- Focus on the starting pitchers prior year stats, since a great startinng pitcher can greatly influence the games outcome.

# Modeling
I wanted to take a diversified approach to adding features to my models in order to try and gauge their feature importances and how it could ultimately affect my models performance. 

RandomForest:
- Created a model that leveraged teams prior season stats as well as the starting pitchers prior season stats.
- Created a model that looked at 3-day rolling averages and then 7-day rolling averages - both did not do well on their own.
- Created two more additional models that combined prior season stats and 3-day trends, then prior season stats and 7-day trends
- The prior season stats, prior season + 3-day, prior season + 7-day, all hovered around 55% accuracy in predicitng whether or not the home team would win. After conducting additional research on publsihed papers, I decded to try out a few other models to gauge their performances as well. 

AdaBoost:
- Leveraging the same engineered features as before, AdaBoost was able to lift my accuracy by a fraction of a percent. 

Gradient Boosted:
- My final model combined all 3 data combination into one. This model examined the prior seasons team & pitcher stats, the 3-day as well as the 7-day rolling averages.
- This led to roughly a 1.25% increase in my models accuracy

# Conclusion
Predicting sports outcomes is no easy task, but leveraging a Gredient Boosted Model achieved the best results. I was able to achieve:
- 56.77% Accuracy on predicitng the 2018 & 2019 baseball seasons
- 58.83% Accuracy on predicitng on the 2019 season alone

# Future Work
There is so much more work that I'd like to incorpate into this project, such as:

Engineer additional key features:
- Pitcher vs batter matchups
- Head-to-head results
- Situational features (RISP, runners on the corners, etc)
- Pitchers 3-start rolling averages on certain stats

Incorporate more aspects for betting
- betting odds - provide an actual ROI on betting on these games
- probability of teams success

Leverage MLB Advanced stats
- There are stats for Defensive, Offensive, Pitching, and Team categories
- They have potentially 45 additional feaures to look at between the 4
