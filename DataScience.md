## Data Science in the MLB

Nowdays most of the teams use data to make decissions about their players, they use stats like avg, ops, rbi's to create the most optimal team. 
However this stats were ignored most of the time until one team use them to transform one Athletic  Oklands in one of the best teams in the league. 

In the 2002 season Paul DePodesta devised a method to find and make use of undervalued players, based on statistical variables that had largely been ignored earlier. His goal was to create a framework which would increase the likelihood of the Oakland A’s making it to the playoffs. He began by stating the somewhat intuitive claim that the probability of any team making it to the playoffs depended on the number of games they won in their regular season. Hence, in order to make it to the playoffs, he had to devise a method to not only discover how many games the team needed to get to that point but also to find the optimal team structure that would give the Oakland A’s just enough wins to make it through.


## What does he had in mind? 
He used estimates of the necessary variables and created that optimal team structure. In terms of statistical tools, this can be explained in terms of linear regression models, which are used to predict how many games a team will win in future regular seasons using the difference between runs scored (based on the right batting statistical variables) and runs allowed (based on the right fielding and pitching variables). Hence, grounded on the pre-2002 data, Paul DePodesta estimated that the Oakland A’s needed at least 95 wins to make it to the playoffs. If we use the pre-2002 MLB data and create the following simple linear regression model, we arrive at the same number as Paul DePodesta i.e. the Oakland A’s needed to score approximately 135 more runs than their opposition to make it to the playoffs:

Wins = 80.8814 + 0.1058*RunDifference

95 ≤ 80.8814 + 0.1058*RunDifference

RunDifference ≥ 133.4 (which DePodesta approximated to 135)

## And what about the team?

Now to form the right combination of players, within a limited budget, the Oakland A’s made use of 2001 player statistics. Here, Paul DePodesta (somewhat controversially) placed emphasis on the player On-base percentage statistics as opposed to the traditional batting average variables. The following multiple linear regression model now helps us understand why:

RunsScored = c + b1*OBP + b2*SLG + b3*BA

When this model is created for pre-2001 MLB game data, it clearly indicates the correlation of the player’s OBP, SLG, and the Batting Average with the runs a batting side scores. 

RunsScored = -788.5 + 2917.4OBP + 1637.9SLG + -369BA

As it turns out, using the data from 2001, the coefficient of BA is highly negative, whereas the other two variables have positive correlations with the runs scored, indicating that baseball scouts were placing far too much money and attention on the wrong statistical variable when judging whether to recruit a player for a team or not. This discovery of the over-valuation of the batting average, though straight forward today, had major repercussions on baseball analytics at the time.

Ultimately, Paul DePodesta formulated a team of players with a 0.339 team OBP, a 0.430 team SLG, a 0.307 team OOBP, and a 0.373 team OSLG. Disregarding the batting average variable, the runs scored and runs allowed can then be calculated using the following models:

RS = -804.6 + 2737.8OBP + 1584.9SLG

RS = 805 (approximately)

RA = -837.4 + 2913.6OOBP + 1514.3OSLG

RA = 622 (approximately)

## Results
By making use of the OBP and SLG statistics for calculating runs scored (using player data available before 2002) and by making use of OOBP and OSLG statistics for calculating runs allowed, Paul DePodesta assembled a team of players, estimating their collective worth as enough to secure approximately 100 wins using the simple linear regression model:
