## Project Description

At Ice, an international online video game store, your role involves leveraging user and expert reviews, along with various game attributes such as genres, platforms (e.g., Xbox, PlayStation), and historical sales data, all obtained from open sources. The objective is to discern discernible patterns that significantly influence a game's success or failure in the market.

The aim of this project, set in December 2016, is to glean insights that can guide future advertising campaigns and identify potential blockbuster games for the upcoming year (2017). Although the dataset encompasses information dating back to 2016, the goal isn't solely to predict 2017 sales based on this historical data, but to gain valuable experience in data analysis and trend identification.

Key Project Objectives:
- **Success Determinants:** Analyze the provided dataset to identify key patterns or factors that correlate with a game's success. This includes exploring relationships between user reviews, expert ratings, genres, platforms, ESRB ratings, and historical sales data.
- **Campaign Planning:** Use the insights garnered from the analysis to formulate strategic advertising campaigns for the upcoming year (2017). Tailor these campaigns to maximize the potential success of identified games or genres with promising indicators.
- **ESRB Ratings Analysis:** Examine the influence of ESRB ratings (such as Teen or Mature) on game success. Understand how these ratings impact sales and reception among target audiences.

Your analysis will involve data exploration, feature engineering, and potentially predictive modeling to discern and interpret the intricate relationships between various attributes and a game's performance in the market. The ultimate goal is to equip Ice with actionable insights that will aid in optimizing advertising efforts, foreseeing potential blockbuster games, and making informed decisions regarding the store's inventory and promotional strategies for the upcoming year.

## Description of the Data

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

## Answer These Questions:

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

## General Conclusion

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

## Suggestions for the Company

**Strategic Inventory Management:**
 - Platform-Specific Stock Management: Considering the trend that top-selling platforms gained popularity post-1995, focus on optimizing inventory for these platforms, ensuring a robust selection of games tailored to their popularity. Minimize investments in obsolete platforms released before 2005, aligning stock levels with declining demand.

 **Data Relevance and Focus:**
 - Focused Data Analysis: Acknowledging the irrelevance of data collected prior to 2013, concentrate future analyses and predictions on more recent and pertinent data sets. This can streamline analysis efforts and lead to more accurate forecasting for forthcoming years.

 **Advertising and Promotional Strategies:**
 - Targeted Marketing for Successful Platforms: Capitalize on the correlation between critic scores and sales for platforms like PlayStation. Design marketing campaigns that highlight critical acclaim to potentially boost sales further.
Highlighting Wii's Success: Despite being an older system, promote popular games released for the Wii platform to leverage its historical success, potentially attracting nostalgic gamers and expanding the customer base.

 **Genre-Specific Strategies:**
 - Focus on High-Median Genres: Given the popularity and high median of Shooter games, consider spotlighting this genre in advertising campaigns or expanding the available Shooter game selection to capitalize on its potential.
Diversified Genre Offerings: While action and sports games are popular, diversify the game catalog to include a range of genres, catering to varying user preferences and potentially increasing overall sales.

 **Regional Market Targeting:**
 - Regional Sales Optimization: Considering that the NA region generates the highest sales per platform, prioritize marketing efforts and inventory selections tailored to this region's preferences. Optimize the game selection based on regional preferences to maximize sales potential.

 **Region-Specific Strategies:**
 - Tailored Offerings for Different Regions: Recognize the disparities in sales trends and preferences between regions (EU, NA, JP). Develop region-specific marketing strategies, game selections, and ESRB-rated content to better resonate with the unique preferences of each region.

 **User Rating Insights:**
 - Platform and Genre-Specific User Rating Analysis: Acknowledging the differences in user ratings between genres and platforms, tailor user engagement strategies accordingly. Consider enhancing user experience or offering incentives for genres with varying user ratings to improve overall customer satisfaction.
 
Implementing these strategies derived from the analysis can assist Ice in optimizing inventory, refining advertising campaigns, targeting regional markets more effectively, and improving user engagement, ultimately leading to increased sales and enhanced customer satisfaction.
