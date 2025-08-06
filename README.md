# Statistical-Analysis-of-Historic-MLB-Hitting-Metrics

# Introduction

In this project, I intend to dive deeper into the statistical relationships between some of today's top sluggers in the MLB. With analysts putting a heavy emphasis on bat speed and coaches prioritizing a high swing rate, there are several factors that play a crucial role in a batter's success when they step into the batter's box. Are players like Oneil Cruz and Junior Caminero who lead the league in bat speed (78.7 & 78.4 mph, respectively) deemed to be more impactful hitters than Luis Arraez and Steven Kwan (62.6 & 63.6 mph, respectively), the two slowest players in terms of bat speed? While Arraez and Kwan may be at the bottom in terms of bat speed, the two All-Stars often find themselves with the lowest strike-out rate across the league and a remarkably high batting average. Additionally, does the handedness of a batter play a role in the successes of batters? Certain ballparks are definitely deemed to be friendlier to certain handed players but does it actually matter?

Research Question 1: Do left handed batters tend to hit more home runs and have a higher OPS (on-base percentage + slugging) than their right handed counterparts?

This question brings up an interesting topic that relates to the successes of left handed batters in comparison to their right handed counterparts, especially given that many ballparks are left-hand friendly, as seen with the Boston Red Sox field having a distance of 302 feet down the right field line as opposed to the 37 foot tall Green Monster located in left-field. While many athletes can only stick to one side of the plate, this question can be particularly useful for switch hitters, those who bat both left and right handed, because of it allowing them to choose a side according to the ballpark they are playing in or the pitcher they face.

Research Question 2: How does a batter's average swing speed and swing percentage affect their strikeout percentage and slugging?

When it comes to baseball, there are often two kinds of batters, those who swing and swing hard, and those who are more passive but tactical with their swings. Both have their pros and cons, but which type of batter on average generates the better results? Is it better to swing at every pitch with all your might or is it smarter to just try and make contact with the ball, not caring about how far it may travel? Over time, slugging has become a more commonly used measure for a batter's success because of it taking into account not only whether or not the batter reached base, but also how effective they hit the ball (i.e. did it result in a double? triple? home run?).

# Dataset Discussion

This dataset was acquired from Baseball Savant's custom leaderboard:
https://baseballsavant.mlb.com/leaderboard/custom?year=2024&type=batter&filter=&min=q&selections=pa%2Ck_percent%2Cbb_percent%2Cwoba%2Cxwoba%2Csweet_spot_percent%2Cbarrel_batted_rate%2Chard_hit_percent%2Cavg_best_speed%2Cavg_hyper_speed%2Cwhiff_percent%2Cswing_percent&chart=false&x=pa&y=pa&r=no&chartType=beeswarm&sort=xwoba&sortDir=desc
This dataset consists only of qualified batters from the 2024 MLB season and contains data such as the number of plate appearances each player had along with advanced statistics such as barrel rate and bat speed. The data is updated and scraped live alongside the games, with this dataset containing data updated up until 5:00 PM on Wednesday, September 18, 2024, the time the data was downloaded.

As a dataset containing batting statistics of all qualified MLB players during the 2024 MLB season, the unit of observation for this dataset would be a single MLB player that meets the minimum qualifying plate appearances. For an MLB player to be considered "qualified", they must record at least 3.1 plate appearances per scheduled league game.

Throughout this project, I will be focusing on the categorical variable of handedness and the quantiative variables of home runs and OPS. Handedness consists of Left, Right, and Switch hitters. OPS (On base percentage + slugging) is a general metric used in baseball to determine how often players are getting on base as well as how many bases they are getting on a single at bat (i.e. Single, Double, Triple, Home Run).

Limitations that exist within this data include the fact that I am unable to tell each player's difficulty of schedule as well as the pitchers they faced. If players face up against CY Young worthy superstar pitchers, it would be expected that their stats would be deflated due to the competition compared to another player who verses an ordinary, non-established pitcher. Therefore, it is possible that some players have lower stats due to the competition they face. Some information that is not included in the data that would have been helpful include the home stadium of these players because that can help explain why some batters perform better than others. Especially in Colorado with the high altitudes, players tend to hit the ball further because of the altitude, thus positively influencing the batting statistics of players.


# Data Visualization

## Research Question 1: Do left handed batters tend to hit more home runs and have a higher OPS (on-base percentage + slugging) than their right handed counterparts?

<img width="567" height="432" alt="output" src="https://github.com/user-attachments/assets/36f0a8d4-eaed-4fd5-a589-c3ae43a623ca" />

Analysis: From the violinplot shown above, the distribution between right-handed and left-handed batters seems to be relatively similar, although there does seem to be a somewhat higher Q1, median, and Q3 for left-handed batter's OPS. When considering extreme values, right-handed batters do have a higher maximum. Switch hitters have a comparably higher median OPS compared to both right-handed and left-handed hitters, showing some evidence that switch hitters might benefit from being able to switch according to the ballpark or pitcher they face.

Since the distributions between left and right handed batters is not significant, we can not neccesarily say that this plot provides much evidence that left-handed batters perform better. However, the distribution for switch hitters is somewhat exciting because of it providing just a little bit of evidence that switch hitters benefit from hitting from both sides of the plate.

<img width="576" height="432" alt="output2" src="https://github.com/user-attachments/assets/cc97b7ba-c6f2-46cd-bcb8-2198208c385e" />

Analysis: From the violinplot shown above, there is once again not much of a difference between the distributions of home runs per plate appearance among right handed and left handed batters. In fact, it seems that right handed batters actually have a higher Q1, median, and Q3 than left handed batters. Additionally, switch hitters once again are performing better than their right handed and left handed counterparts, achieving a higher minimum, Q1, median, and Q3. While this data is not enough to make a conclusive stance that switch hitters benefit from hitting on both sides of the plate, the evidence does show some level of support for the claim.

Results: Given the data, it seems that there is no conclusive evidence that left-handed batters perform better than their right-handed counterparts. In fact, it seems that right-handed batters might even perform better than left-handed batters in certain categories such as the number of home runs they hit per plate appearance. However, some data that was exciting was the performance of switch hitters in comparison to the other two groups. While their distribution was not necessarily significantly higher, there was a reasonable gap between their OPS and home runs per plate appearance compared to the other two.


## Research Question 2: How does a batter's average swing speed and swing percentage affect their strikeout percentage and slugging?

<img width="490" height="489" alt="output3" src="https://github.com/user-attachments/assets/36cadb99-e82e-4426-909d-33284061c6cd" />

From the histplot above, there seems to be a relatively high positive correlation between a batter's swing speed and their slugging percentage.

<img width="490" height="490" alt="output4" src="https://github.com/user-attachments/assets/855cf038-724f-4a17-bb69-3b5d955ff4a7" />

From this histplot, it seems that there is some level of positive correlation between swing speed and strikeout percentage.

<img width="576" height="433" alt="output5" src="https://github.com/user-attachments/assets/e27e71d0-f315-4a81-ac2e-9ccbde0cd99b" />

While there was a positive correlation between swing speed and slugging, there seems to be only a very slight negative between swing percentage and slugging.

<img width="563" height="436" alt="output6" src="https://github.com/user-attachments/assets/38db4aa0-b10e-4ec6-b27b-15eed25a8cd9" />

There seems to be no correlation between swing percentage and strikeout percentage.

Reults: From the above visualizations and correlation chart, it seems that a batter's swing percentage has little to no correlation with their slugging and strikeout rate whatsoever. However, there does seem to be a correlation between a batter's swing speed and slugging/strikeout rate. Therefore, while this data is not necessarily conclusive evidence, there does seem to be a trend for batters who swing faster to play the game at a higher risk (either a strikeout or a hit).

# Conclusion

Using data acquired from Baseball Savant's custom leaderboard, I was able to use data from qualifed batters in the 2024 MLB season to compare trends between a batter's handedness and their home run rate and OPS. My research question: "Do left handed batters tend to hit more home runs and have a higher OPS (on-base percentage + slugging) than their right handed counterparts?" was designed to see whether or not left-handed batters had a competitive advantage over their right-handed counterparts due to the structure and design of certain ballparks being left-handed friendly. Additionally, I was curious as to whether or not this would play a role in a switch hitter's success because of them being able to choose which side of the plate they swung from depending on the ballpark they played in. After cleaning the data and creating a new data frame with my variables of interest (handedness, home runs, OPS), I was able to create data visualizations and summary statistics comparing the home runs per plate appearance and OPS for lefties, righties, and switch hitters. Unfortunately, the data seemed to show relatively no relationship between a batter's handedness and their performance. Statistics were relatively even across the board, although switch hitters did seem to perform slightly better than the other two groups. Therefore, while there was not much evidence to support the research question, there was some evidence to show that switch hitters do benefit from being able to switch which side of the plate they swing from.

Limitations: Some limitations that I faced in my results are that although I have 135 total players in my dataset, only 14 of them are switch hitters, so this generates a lower sample size that can greatly influence the spread of their statistics if one player were to perform amazingly or if one performed poorly. Some contextual information that is important for these results are that this data does not take into account the health of the player or the level of competition they faced. For instance, if a player were to play while sick or injured, their statistics would likely be deflated due to worse performance. Additionally, the level of competition and ballparks played at is a crucial missing factor that would play an immense role in the performance of players. This would affect the way these results can be used because it means that these results cannot be generalized to all baseball players, nor can it be generalized to all MLB players because of it not sampling all players, but only those who met the minimum plate appearances threshold.

Future work: If someone were to conduct future work based on these analyses, some research questions that might arise include finding the relationship between a batter's handedness and other variables such as batting average to see whether or not there is actually a difference between handedness and other variables. Additionally, these analyses could be used to consider the relationships between the swing speed of batters of different dominant hands and how slower swinging left handed batters may compare with slower swinging right handed batters.
