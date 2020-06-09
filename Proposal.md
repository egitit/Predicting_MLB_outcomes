# Predicting_MLB_outcomes
Leveraging machine learning in order to try and predict the outcome of a Major League Baseball game. 

# What are you trying to do?
Prior to 2018, Nevada was the only state where one could bet on sports legally. In May of 2018, the US Supreme Court decided to strike down the PASPA (Professional and Amateur Sports Protection Act of 1992) allowing states to make their own calls when it came to sports betting. Since then, 21 states have legalized sports betting resulting in roughly $10-$15 billion dollers being bet on sports in 2019. I've had my up's and down's when it comes to betting on baseball but I'd like to create a model that will help me predict the outcome of a baseball game which will hopefully lead to some extra cash going into my pocket.

# How has this problem been solved before?
There have been attempts by individuals and teams to try and predict the outcome of a baseball game. These individuals gave a diverse approach to solving this problem, mainly through feature engineering and understanding their importances. These teams have tried Regression models as well as Classifications models. According to another project from Stanford, Las Vegas sports book accruately predicted 56.87% of the 2012 baseball games while they were able to accurately predict 59% of the games with a random forest model (http://cs229.stanford.edu/proj2013/JiaWongZeng-PredictingTheMajorLeagueBaseballSeason.pdf). Tim Elfrink leveraged a generalized linear model, random forest, XGBoost, and a boosted logistic regression model. His XGBoost model along with a certain set of features was able to generate a 55.5% accuracy. My goal is to achieve 55-60% accuracy from my model.

# What is new about your approach, why do you think it will be successful?
While these teams were able to generate decent results, I felt like they focused on some of the more common statistics to leverage as features for their models. There were only a few features that were engineered that really caught my attention. I'd like to focus my efforts on leveraging the statistics that most teams did not consider. These statistics would directly influence a players productivity as far as generating offense, or defense from both teams. 

# Who cares? If you're successful, what will the impact be?
Producing an accurate model would be ideal, but I'd like to put my money where my mouth is. For the sake of simplicity, I'm going to ignore odds for teams and simplify it to $10 a game. Winning a game gives +$10, and losing a game is -$10 from an overall balance. There is a total of 2,430 games in a season and I'd like to predict on the 2018 & 2019 seaons while training my model on the 2010-2016 seasons.

# How will you present your work?
I'd like to present my findings in the matter of how much money I could hypothetically make from the 2018 & 2019 season. 

# What are your data sources? What is the size of your dataset, and what is your storage format?
RetroSheet has detailed information of each game played from 2010-2019. I'd like to combine these stats along with MLB.com's regular and expanded statistics to help my models prediction. 

# What are potential problems with your capstone?
The biggest challenge will be how I'll be able to combine these datapoints into one cohesive dataframe that my model can predict on while also figuring out new features for my model to leverage. 

# What is the next thing you need to work on?
Determine a way to leverage more real-time data. Usually teams will annouce starting lineups the day of, which my model won't necessarily account for. My model is going to leverage individual players and teams past preformances and will not account for any last minute lineup changes. 
