# NCAA Draft Classification

The objective of this classification project is to get an insight of how the NBA has changed in relation to the players that are drafted. Using Supervised Machine Learning models we try to predict if NCAA players are able to make it to the next level based on their stats such as Points, Assist, Rebounds, etc. 


# Data

[NCAA_players_career_data.csv](Data/NCAA_players_career_data.csv)

- Over **30,000** NCAA D1 Basketball players statistics were collected from the [SPORTSREFERENCE](https://www.sports-reference.com/cbb/) Database. Players stats include career accumulated Points,Assists,Rebound, and more.

[NBA_Full_Draft_Draft_1947-2018.csv](Data/NBA_Full_Draft_Draft_1947-2018.csv)

- This Dataset was downloaded from [Kaggle](https://www.kaggle.com/hrfang1995/nba-drafts-of-19472018) containing every player drafted into NBA from 1947 to 2018.

[NBA_3PA_perseason.csv](Data/NBA_3PA_perseason.csv)

- This Dataset was downloaded from [BasketballREFERENCE](https://www.basketball-reference.com/leagues/NBA_stats_per_game.html) containing 3 point attempts & made averages ranging from 1979 too 2019.


# Exploratory Data Analysis

From the beginning of the century 'til 2018 over 30,000 people played in the NCAA and only a small percentage are able to make it to the NBA.

![DraftedVunDrafted](https://i.imgur.com/XovJv9D.png)

Breaking this down by position we see a discrepancy in the pool of players position. In the past 18 years less than 10% of the total College players were Centers. The label Center is traditionally given to the tallest players on the team and they usually play close to the basket in the low post.

![#ofplayersdraftedbyposition](https://i.imgur.com/qCek5yN.png)

When we mention a true center, as an NBA fan, we think of players like Bill Russel, Shaquille O'Neal, Hakeem Olajuwon. These Hall of famers dominated the low post giving their team high percentage shots and grabbed every rebound due to them towering over the other players. On the other hand, they were infamous for their lack of shooting abilities and in that era this was okay because teams preferred closer shots. Nowadays because of analytics players are given a green light to shoot as many 3s as they like, simply put it the 3 is a more efficient shot than a mid-ranged 2.

![Average3pMakesAttempts](https://i.imgur.com/xUf1fC9.png)

Since 2012, the NBA average for three point attempts and makes has increased year over year to record breaking numbers. As the league catches on to the trend of shooting  further from the basket we begin to see Centers being drafted less and less

![#playersdraftedbyposition_yearly](https://i.imgur.com/20BCoG1.png)

A great way to understand the projection of the NBA is to study the players entering it. Although general managers may sometimes draft players simply based on potential or their own bias and not just statistics we won't ever be able to predict the outcome of a draft with 100% certainty but more than likely we can come to a percentage of accuracy that we are comfortable with.

# Classification Models

- Logistic Regression
- Decision Tree
- Support Vector Machine

## Logistic Regression

### Percision :  27%

### Confusion Matrix :

![LogisticRegression_cf_test](https://i.imgur.com/TgEIo6R.png)

TP : 148 Correctly predicted as Drafted\
TN : 21784 Correctly predicted as Undrafted\
FP : 397 Incorrectly predicted as Drafted\
FN : 613 Incorrectly predicted as Undrafted

#### AUC : 0.8711130698036186

![LogisticRegression_ROC](https://i.imgur.com/CVHY3wp.png)



## Support Vector Machine

### Percision :  28%

### Confusion Matrix :

![svm_cf_test](https://i.imgur.com/aUx8i3e.png)

TP : 156 Correctly predicted as Drafted\
TN : 21781 Correctly predicted as Undrafted\
FP : 400 Incorrectly predicted as Drafted\
FN : 605 Incorrectly predicted as Undrafted

#### AUC : 0.865149885889837

![svm_ROC](https://i.imgur.com/JdnKZ7w.png)


# Future Work and Areas of Improvement

- How are positions given to players? Players like Anthony Davis, Demarcus Cousin who are almost 7 feet tall were labeled as Fowards instead of Centers. Maybe because they had the ability to shoot?, which traditional centers cannot do. 

- Whats next?, Now that we have this informing on drafted basketball players what can we do with it?

- Applying unsuperived model to see the similarity between players.

- Multi-class, instead of just a binary Drafted or not the target can be expanded to draft position

- Gather more data


# Conclusion

In a landscape where the style of play is evolving at such a rapid pace, the ability to understand the players of the upcoming generation becomes integral. The barrier being the NBA Draft where players who are capable are inaugurated to the next stage of competition. To separate the capable and incapable is a big decision amongst those that run multi-million dollar teams, and can be a huge deciding factor of winning the championship. There is still a lot of further research needed before the models can be deemed useful/actionable but I think it a great place to learn and understand the problem. With that being said my attempts at classifying the drafted versus undrafted had an very low accuracy of 27/28%. Basing the models off ROC curve Logistic Regression Model was the better of the 2.

