---
layout: post
title: MTA Data Analysis
---


My first week at Metis Data Science Bootcamp began with a group project. Our team was tasked to identify the ideal subway entrances to spread awareness for a fictional organization called WomenTechWomenYes. Our recommendation focused on stations with high rider volume, favorable demographics, and locations near major tech centers in NYC.

 Our Team began the analysis by pulling MTA data over a three-month period. The data set counted the cumulative number of exits and entries for different turnstiles throughout the city. The data was granular enough where we could identify the not only the ideal station but also the ideal entrance to stand outside. However the dataset did have some irregularities. The turnstile counters would randomly reset at times. Also, the turnstiles would frequently count an unreasonable number of entrances over a given period of time such as 5000 entrances in 4 hours (over 20 people a minute for 4 hours straight). Our team accounted for the data discrepancies and outliers prior to analyzing the data.

Our exploratory data analysis began with a look at the top station entrances by volume of riders. The results were predictably the major transportation hubs in New York City. Penn Station, Herald Square, and Grand Central were among the stations with highest entrance volume. While this data was useful, our team realized volume might not be solution to our project. We wanted to consider areas whose residence may show interest in WomenTechWomenYes. 

To supplement our data, we pulled US census bureau demographic information about the different zip codes of New York City. Specifically, we wanted to know the proportion of women in the workforce, median income, and education level of the various neighborhoods in the city. We used this information to create a demographic ‘score’ and weighted the score of the areas located in the subway stations. If a station had a high demographic score, it received a higher value in our model. After incorporating demographic score with our rider volume data, we identified some new stations to target. Grand Central and Penn Station were still the top locations but now 86th street on the Upper East Side entered our model.

Finally, we wanted to identify stations with close proximity to major tech areas in the city. Through qualitative research, our team identified areas of lower manhattan and came up with the following subway stations: Union Square, West 4th Street, and Herald Square.

After careful review of the data, our team came up with the following recommendation: Target the highly educated working women in the morning by stationing teams at Grand Central, Penn Station, and 86th street. Then target members of the tech community on their evening commute by stationing teams at Union Square, West 4th street, and Herald Square.
