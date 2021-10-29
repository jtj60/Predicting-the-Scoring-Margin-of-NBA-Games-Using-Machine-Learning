# Machine Learning Model to Predict the Point Spread of NBA Games

**Authors** 
Johnson, Jacob Thomas
Owen, Brett
Sharma, Juhi
Sayson, Christian Noel


**Abstract** :
The goal of this project is to achieve a reasonable accuracy in predicting the outcomes of individual NBA games. This is a lofty objective, and to meet it we will create a machine learning model. The model will be developed from testing various algorithms on the primary dataset (individual NBA games of the past 3 seasons), and then choosing the algorithm that performed the best. The NBA - and independent observers - track and record a large quantity of statistical data for every game. Everything from 3-Point Shooting Percentage to Personal Fouls and even Average Shot Distance is documented and easily found. This data will be fed into the model, and the model will unbiasedly decide what stats are important (the number of isolation plays a team runs) and what is not important (the amount of timeouts a team calls). After the model has decided which stats to prioritize or discard; we will feed it a structured dataset of teams and matchups (made up primarily of historical player statistics) and attempt to predict the point margin of any given game.

## Introduction

The National Basketball Association, more commonly known as the NBA, is a professional basketball league in North America consisting of 30 teams. Each team has 15 players on it’s roster, and they play 82 games every season (1230 league-wide total games). Given the huge amount of statistical categories catalogued for every single game, the NBA has a plethora of historical data. What is all this data used for? Outside of using it as talking points when debating the eternal question: Lebron James vs. Michael Jordan… many teams employ data scientists and statisticians to give their players an edge on the court. In fact, it’s these people that are primarily responsible for the extreme shift in playstyle over the past decade. Basketball used to be ruled by verticality, or to be more descriptive: a 7-foot tall guy shooting over another 7-footer in close proximity to the rim. But now, it’s ruled horizontally. Why? Because it took 70 years for everyone to realize that usually, a 3 point shot was more efficient than a 2 point shot. But that realization is very old news. To gain any advantage now, teams require more cutting edge analytics. But data science and analytics and advanced stats have not only revolutionized the NBA. Their rise in prevalence and popularity have also transformed the way the NBA is seen externally.

Vegas - and sports gambling in general - has seen a dramatic surge recently. This is mostly due to more widespread legalization across the United States, and the popularity of sports betting platforms such as DraftKings or FanDuel that provide convenience and accessibility to their patrons. Which makes Vegas very happy. But Vegas isn’t happy about a small subset of the population; a subset that is doing what has long been considered impossible: beating the House. How are they doing it? Among other things, using Machine Learning. It’s not a simple task, of course. Beating the House never is. Why NBA games? The NBA is considered the least variable league. Any given game is more likely to go as expected than the other major leagues. This is largely due to the nature of the sport; there are less players on the court, and the best players get the vast majority of minutes. Furthermore, there is virtually no luck in Basketball, it’s almost entirely skill based. The less random something is, the easier it is to predict. And therefore to build and develop models upon. But it’s still not easy. Even achieving a 45% accuracy would put a model in the upper echelon. 55% is considered professional. Anything greater than 60%, and you’re essentially a millionaire. We’re not aiming to be millionaires - or to do any betting at all, but we are aiming to achieve a decent accuracy. 

How are we going to predict the point spread of NBA games? It starts with the data. Collecting, formatting, and shaping the extensive supply of stats is a formidable undertaking. Fortunately, we can use the efforts of those who came before us. This dataset, based on the official NBA stats website, contains 5 csv’s of game, team, and player stats from 2004-2020; which should be more than substantial enough for our model. A useful data set is required in building a successful model. It needs to contain all the relevant stats the model could prioritize while being formatted correctly and efficiently so the model can retain precision. 

<-------- Project has not yet advanced past the data collection stage. -------->

## Problem Statement

We are attempting to predict the point spread of individual NBA games using a model that has decided what statistics are most important in determining the spread.

For the accuracy benchmark, we will be using the actual results of the games versus what our model predicted.

We are hoping to achieve an accuracy in the 30-40% range, based on our current assumptions. The most prolific models generally achieve 52-58%, with almost no models going above 60% for any given stretch of time. Such models are usually developed by professionals with far more experience and resources, obtaining an accuracy remotely close to that would be an achievement.

### Related Work

Vegas cares about this problem quite a bit, as do the people who attempt to do this exact thing for a living. It’s impact is minimal outside of sports betting and the NBA, but in those spheres it’s effect is substantial. Implications of better solutions would include possibly changing how NBA teams view players. And if those better solutions were better enough, their creators could become quite wealthy off of them. 

Speaking of better solutions and wealthy creators, this problem has already been ‘solved’. At the least, people have created models that have granted them success in the Vegas Markets. Particularly, Bob Voulgaris created the ‘Ewing’ model back in 2007-2010 with ‘The Whiz’ (his anonymous partner, evidently a math/comp sci/data science prodigy). It was one of the first such models, and an extraordinarily successful one. It’s exact accuracy is unknown, but Voulgaris (at least claims) to have made millions using it. There are other various models we have researched, but none are as notable. Furthermore, predicting the points spread of NBA games or even just the binary Win/Loss is a popular Machine Learning project, so there are plenty of resources at our disposal. 

## Data Management 

The important questions of interest are centered upon what data to include. There might be statistics that we think are irrelevant, but the model finds to be correlated. 
* Should we subjectively take out certain variables beforehand to clean up the dataset? Or should we only let the model decide what’s truly important? 
* Player driven data vs. team driven data is another question of interest. Player driven data would undoubtedly be more precise and accurate, but is also more unwieldy to work with. 
* How many seasons back should we feed the model? The NBA playstyle and ‘meta’ has changed significantly over the years, even as close as 2012 the game was far different. Does this matter for model integrity? 

### Data Gathering

We have collected CSV files containing historical game, player, and team stats from 2004-2020. This should be more than enough data to test and complete our model, barring a need for more advanced or obscure statistics to increase model quality.

Most advanced stats have formulas derived from the statistics in our current CSV’s, but if it’s easier to pull them from elsewhere than calculate them ourselves, we will do so. Other potential data needed is rosters throughout the season, if individual games don’t provide the nessecary information or it is not convenient enough to use. 

### Data Pre-processing, Cleaning, Labeling, and Maintenance 

### Exploratory Data Analysis 

## Machine Learning Approaches

### Describe the ML methods that you used and the reasons for their choice. 

### Justify ML algorithms in terms of the problem itself and the methods you want to use. 

### Tools and Infrastructure Tried and Not Used

## Experiments

## Conclusion

## References

## Appendix## 
