---
layout: post
title: The 2017 French Presidential Election
---

Predicting the Voting Patterns of French Towns during the 2017 Presidential Election


## Project Description:

Political science has always been of interest to me. For my third Metis project, I analyzed the 2017 French presidential election and built a model to determine the winner of individual towns throughout the country. I was able to build the model using voting and demographic data from INSEE, the French national statistics bureau. 

My analysis is based purely off the datasets I acquired so results may differ slightly from other publications or the media. I also focused my model on town predictions in mainland France; overseas departments and territories were not incorporated in the model.

I hope you enjoy! 



## Prologue:


Since the 1950s, France has always been governed either by a moderate left party such as the Socialist Party or a moderate right party such as the Republicans. The 2017 presidential election, however, marked a shift from the norm as a wave of populist movements swept its way through Western democracies. The results of the French election would not only impact the people of France but the European continent as a whole. Let’s take a look at France’s unique election cycle.



## French Presidential Election: How does it Work?

-	France elects a new president once every 5 years.
-	Anyone who secures 500 valid sponsorships from elected officials can run for office. 
-	The president is decided by popular vote.
-	A first round of voting is held. If a candidate fails to secure over 50% of the vote in the first round then the election moves to a second round where the top two candidates by popular vote face each other in a run-off. A candidate has never secured the presidency in the first round.
-	The second round of voting is held. The winner of the popular vote becomes president.



## Why Look at Towns?

With the president determined by popular vote, a presidential candidate gains no added value for winning an individual town or department. However, identifying the winners of individual towns across France provides us a unique view of the French voter that may otherwise be overlooked. The voting patterns of a given town may be tied to the demographics and characteristics of the town, which can help candidates better understand their constituents.



## Who were the Key Players?

**Jean-Luc Mélenchon:** A former member of the Socialist Party, Mélenchon started his own party, la France Insoumise, in the years leading up to the 2017 election. He is arguably the most far left politically of all the major candidates. With the Socialist Party divided on policy, Mélechon was able to take away most of the center left wing vote from the Socialist Party candidate Benoit Hamon. Mélenchon campaigned for pro-environmental policies and fought for the working class of France. He was anti-NATO and critical of the French government for its support of America’s wars in the Middle East.

**Emmanuel Macron:** Macron defined his party, En Marche!, as neither left nor right. As the former economy minister and the youngest candidate in the race, he was the most moderate of the major candidates. Macron wanted to focus on economic growth while maintaining a strong relationship with the European Union. He was also pro immigration.

**Francois Fillon:** Fillon, the Republican Party primary winner, represented the right of center. As the former Prime Minister, he was an early front runner until a series of scandals set him back in the polls. Fillon was fiscally conservative, wished to streamline the labor code, and wanted to reform the French healthcare insurance system.

**Marine Le Pen**: Le Pen represented the National Front, the far right political party of France. Marine Le Pen represented the populist wave of France with strong protectionist views. She was vehemently against the EU with plans to leave it and return France to the Franc, was anti-immigration, and wished to impose a 35% tax on goods from firms that relocated out of France.





## First Round Results:

The first round of voting took place on April 23rd with the final vote count announced on April 26th.  While the field contained 11 different candidates, the four major candidates took roughly 85% of the popular vote. 

![](https://github.com/bhdavie/bhdavie.github.io/raw/master/images/FirstRoundPopularVote.png)

Macron ultimately won the popular vote with 23.96% of the vote, edging out Le Pen who brought in 21.31% of the vote. As the top two candidates in the popular vote, Macron and Le Pen moved on to the second round of votes.

Macron and Le Pen were neck and neck in the first round but the way they got there varied tremendously. The disparity in voter demographics is amplified when we look at the winners of the first round by towns. Despite Macron winning the popular vote, Le Pen dominated every other candidate in the number of towns that voted for her.

![](https://github.com/bhdavie/bhdavie.github.io/raw/master/images/TownsWonByCandidateFirstRound.png)

Not only did she win nearly two thirds of the towns of France, Le Pen also dominated other candidates in percent margin of victory across every town in France.

![](https://github.com/bhdavie/bhdavie.github.io/raw/master/images/AverageMarginOfVictoryByCandidateFirstRound.png)

Macron was able to neutralize Le Pen’s victories and margins by winning in large metro areas such as Paris. The average population for towns that voted for Macron was twice the size as towns that voted for Le Pen.

![](https://github.com/bhdavie/bhdavie.github.io/raw/master/images/AverageTownSizeWonFirstRound.png)

The following graphic helps put everything together:

![](https://github.com/bhdavie/bhdavie.github.io/raw/master/images/FirstRoundHeatMap.png)

Each dot represents the location of an individual town in France. The size of the dot is proportional to the population of the town and the color represents the winner of the town. Blue represents Le Pen, red represents Macron, purple represents Fillon, green represents Mélenchon, and black represents everyone else. 



The contrast between urban and rural voting was a clear differentiator between Macron and Le Pen. However, there were other factors that played a significant role. These factors were prominent in my first round predictive model.



## First Round Predictive Model:


I decided to use a random forest classification model to predict the first round results. After fine-tuning the hyper parameters, I was able to predict the winner of an individual town with 59.5% accuracy. The following is information related to the precision and recall of the model relative to the candidates:

![](https://github.com/bhdavie/bhdavie.github.io/raw/master/images/FirstRoundModelResults.png)

There were several features that had a strong impact on model accuracy:

**Department Code:** The department (equivalent to a district or state in the US) a town was located in was a strong indicator of a town’s voting behavior. This suggested geography had a role to play in the election cycle. Departments in the northeast and French Riviera typically went to Le Pen while departments in the west or departments with large metro areas typically went to Macron.

**Proportion of single adults:** Towns with a larger proportion of single adults typically voted for Macron, Fillon, and Mélenchon. This reflected the contrast in urban and rural demographics as single adults typically live in cities. 

**Youth Population:** The average youth population (ages below 30) was slightly larger for Le Pen relative to other candidates. This includes all ages below 30, not just residents of voting age. The larger proportion of youth was likely connected to families located in suburban and rural areas.

**Proportion of registered voters who expressed an interest in voting:** The two candidates from the mainstream parties, Fillon of The Republicans and Hamon of the Socialist Party, won towns with a higher percent of registered voters who expressed an interest in voting. Towns with a larger proportion of interested registered voters were more likely to vote along traditional party lines.

**Proportion of registered voters who expressed an interest in abstention:** The political outsiders, Macron and Le Pen, won towns with a higher proportion of registered voters who expressed an interest in abstaining their vote. As registered voters are likely registered to traditional parties, towns with fewer interested registered voters give outsiders a better chance.

**Population of the town:** As I demonstrated in earlier graphics, population was a major factor in a town’s voting pattern.




## Second Round Results:


The second and final round of the presidential election was held on May 7th, just two weeks after the first round. Shortly after the first round results were released, Fillon and Hamon both pledged their support for Macron. Mélenchon opted not to reveal his opinions of either candidate, although more of his political views aligned with Macron relative to Le Pen. Only one candidate, Nicolas Dupont-Aignan, endorsed Le Pen in the second round.

Ultimately Emmanuel Macron won in a landslide with a little over 66% of the popular vote. 

![](https://github.com/bhdavie/bhdavie.github.io/raw/master/images/PercentPopularVoteByCandidateSecondRound.png)

Macron also dominated in the number of towns won:

![](https://github.com/bhdavie/bhdavie.github.io/raw/master/images/TownsWonByCandidateSecondRound.png)

Macron’s dominance, in the second round of voting, is evident through this nationwide voting map:

![](https://github.com/bhdavie/bhdavie.github.io/raw/master/images/SecondRoundHeatMap.png)

Again, red dots represent towns won by Macron and blue dots represent towns won by Le Pen. Not only did he take the vast majority of towns won by other candidates in the first round, Macron also won many towns won by Le Pen in the first round. 

The significant flip in town victories for Macron stemmed from the endorsements of Fillon and Hamon. Le Pen’s controversial stances on immigration and protectionism alienated much of the French vote. Macron’s moderate stances on most issues convinced members of both the mainstream left wing and right wing political parties to vote in his favor.


## Second Round Prediction Model:

Again I decided to use a random forest classification model to predict the second round results. I was able to predict the winner of an individual town with 88.3% accuracy. The following is information related to the precision and recall of the model relative to the candidates:

![](https://github.com/bhdavie/bhdavie.github.io/raw/master/images/SecondRoundModelResults.png)

While many features were incorporate, two features carried the greatest weight in the model:

**Margin of Victory in the First Round:** The percent difference in votes between the first place and second place candidate was the most predictive factor in the second round. If a race was close in the first round, the town almost always went to Macron in the second round. This was likely due to the endorsements from Fillon and Hamon. Below is a graph comparing the margin of victory in the first round and the candidate who won the town in the second round: Towns that were won by a margin below 5%, indicating a close race, are represented by the blue bars and towns that were won by a margin above 5%, indicating a more decisive win, are represented by the orange bars:

![](https://github.com/bhdavie/bhdavie.github.io/raw/master/images/TownWinsVsFirstRoundMarginVictory.png)

**Whether Le Pen Won the Town in the First Round:** The winner of the first round, specifically if Le Pen won the first round, was highly predictive in determining the winner of the second round. Again, Macron greatly benefited from the endorsements of Fillon and Hamon. The endorsements swayed a large number of citizens to vote Macron in the second round, allowing Macron to capture most of the towns won by other candidates in the first round. Not only did Le Pen struggle to pick up towns won by other candidates in the first round, Le Pen also struggled to hold on to many towns that voted for her in the first round. Below is a graph comparing whether the candidate did or did not win the town in the first round and how many towns they won in the second:

![](https://github.com/bhdavie/bhdavie.github.io/raw/master/images/TownWinsVsFirstRoundLePen.png)

As you can see, Le Pen picked up very few towns in the second round while Macron substantially increased the number of towns he won in the second round. 



## Conclusion:

After a decisive victory, Emmanuel Macron became the youngest president in the history of France. His party, ‘La République En Marche!’ went on to win a majority in the National Assembly in 2017, gaining control of 308 of the 577 seats. 

Marine Le Pen conceded her defeat to Macron shortly after the second round results. She was later elected as a member of the National Assembly. Her party, National Front, only acquired 8 of the 577 National Assembly seats in 2017.



## Final Remarks:

The 2017 French presidential election was an exciting race, and I’m glad I had the opportunity to analyze the results, but I would have liked to explore other demographics and their effects on the election. In particular, I’d like to acquire more demographic data related to ethnicity and employment. Immigration and employment were major issues throughout the election cycle but I didn’t have any data related to either of those issues. 

I’d also like to do a deep dive on two areas: Paris and the French Riviera. While Macron ultimately won the city of Paris, I want to take a closer look at how various areas of the city voted. I’m curious how demographics of certain areas of Paris would vote given the field of candidates. The French Riviera was interesting as it voted heavily in Le Pen’s favor in the first round, despite containing many towns with larger populations. Finally, I’d like to include the overseas departments and territories as well as the absentee voting from other countries around the world and draw insights from the voting patterns.

I hope you enjoyed the analysis! Please be on the lookout for additions over time.    
