## Project description

You work for the online store Ice, which sells video games all over the world. User and expert reviews, genres, platforms (e.g. Xbox or PlayStation), and historical data on game sales are available from open sources. You need to identify patterns that determine whether a game succeeds or not. This will allow you to spot potential big winners and plan advertising campaigns.
In front of you is data going back to 2016. Let’s imagine that it’s December 2016 and you’re planning a campaign for 2017.
(The important thing is to get experience working with data. It doesn't really matter whether you're forecasting 2017 sales based on data from 2016 or 2017 sales based on data from 2016.)
The dataset contains the abbreviation ESRB. The Entertainment Software Rating Board evaluates a game's content and assigns an age rating such as Teen or Mature.

## Description of the data

- `Name` - Name of the game
- `Platform` - Platform game was developed for
- `Year_of_Release` - Year game was released
- `Genre` - Category
- `NA_sales` - (North American sales in USD million)
- `EU_sales` - (sales in Europe in USD million)
- `JP_sales` - (sales in Japan in USD million)
- `Other_sales` - (sales in other countries in USD million)
- `Critic_Score` - (maximum of 100)
- `User_Score` - (maximum of 10)
 -`Rating` - (ESRB)

## Answer these questions:

- Look at how many games were released in different years. Is the data for every period significant?
- Look at how sales varied from platform to platform. Choose the platforms with the greatest total sales and build a distribution based on data for each year. 
- Find platforms that used to be popular but now have zero sales.  
- How long does it generally take for new platforms to appear and old ones to fade?
- Determine what period you should take data for. To do so, look at your answers to the previous questions. The data should allow you to build a prognosis for 2017.
- Work only with the data that you've decided is relevant. Disregard the data for previous years.
- Which platforms are leading in sales? Which ones are growing or shrinking? Select several potentially profitable platforms.
- Build a box plot for the global sales of all games, broken down by platform. Are the differences in sales significant? What about average sales on various platforms? Describe your findings.
- Take a look at how user and professional reviews affect sales for one popular platform (you choose). Build a scatter plot and calculate the correlation between reviews and sales. Draw conclusions.
- Keeping your conclusions in mind, compare the sales of the same games on other platforms.
- Take a look at the general distribution of games by genre. What can we say about the most profitable genres? Can you generalize about genres with high and low sales?

## General conclusion

After analyzing the data, I concluded:
- Top selling platforms did not become popular until after 1995.
- Platforms released before 2005 have pretty much become obsolete with the rest slowing declining.
- We have decided data collected prior to 2013 is irrelevant.
- Using the example of Playstation platforms, the user scores have little correlation and the critic scores have moderate correlation with the total sales.
- Although the Wii is an older system, many of the most popular games were released for the Wii platform
- Overall, the most popular genre of games was action followed by sports, but the Shooter genre has the highest median.
- The NA region generates the highest number of sales per platform
- The EU and NA regions are similar in their top platforms, genre and ESRB rating. The JP region generates the smallest number of sales per platform and varies quite a bit from the other two regions in top platforms, genres and ESRB ratings.
- We found that the user rating vary from the action and sports genres but are similar between Xbox One and PC platforms by testing the following hypotheses:
  - Average user ratings of the Xbox One and PC platforms are the same.
  - Average user ratings for the Action and Sports genres are different.
