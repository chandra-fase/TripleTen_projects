## Project Description

The project aims to analyze and compare music preferences between the cities of Springfield and Shelbyville using real Yandex.Music data. It involves testing hypotheses to understand user behavior in these locations. By examining and evaluating the data, the project seeks to determine if there are significant differences in music tastes between the two cities. The findings will enable better insights into user preferences and assist in making informed decisions regarding music content or marketing strategies tailored to each location.

## Hypotheses:

- User activity differs depending on the day of the week and from city to city.
- On Monday mornings, Springfield and Shelbyville residents listen to different genres. This is also true for Friday evenings.
- Springfield and Shelbyville listeners have different preferences. In Springfield, they prefer pop, while Shelbyville has more rap fans.

## Description of the Data

- `userID`: user identifier
- `Track`: track title
- `artist`: artist's name
- `genre`: song genre
- `City`: user's city
- `time`: the exact time the track was played
- `Day`: day of the week

## Steps Taken

- The data was cleaned and preprocessed by removing duplicate and missing values and replace wrong values.
- The data was then split into groups by city to prepare for hypothesis testing.
- Hypothesis 1 was tested by:
  - Grouping the data by city to find the number of tracks played in each group.
  - Grouping the data by day of week to find the number of tracks played on Monday, Wednesday, and Friday.
  - Creating a new function to calculate the number of songs played for a given day and city.
      <img width="375" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/2f4655f0-b6ec-4b3b-b96d-c715aaae2eed">
  - Creating a new table displaying the results.
      <img width="502" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/534a026a-3daa-48c6-8e4b-c75a5b2fcb5f">
- Hypothesis 2 was tested by:
  -  Creating a function to return info on the 15 most popular genres on a given day within the period of two timestamps.
      <img width="738" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/11ad6108-b818-4139-a8d5-4230ad2db6b1">
  -  Using the new function to compare the results for Springfield and Shelbyville on Monday morning from 7am to 11am and on Friday evening from 5pm to 11pm.
- Hypothesis 3 was tested by:
  - Grouping the `spr_general` and `shel_general` tables (separately) by genre and using the count method to find the number of songs played, displaying them in descending order for each city.
      <img width="524" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/5eea1900-fb16-4b60-a343-2791e02703bf">
      <img width="377" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/e39474f0-185e-4ea2-a383-b74b9922eacc">

## General Conclusion

After analyzing the data, I concluded:
- User activity in Springfield and Shelbyville depends on the day of the week, though the cities vary in different ways.
- Musical preferences do not vary significantly over the course of the week for both cities. There are small differences in order on Mondays, but for both cities the most popular genre is pop.
- Musical preferences of users from both cities are quite similar.

## Suggestions for the Company

Here are potential improvement ideas and business outcomes based on the conclusions drawn from the analysis of music preferences between Springfield and Shelbyville:

- **Localized Marketing Strategies:** While the musical preferences might be similar between the two cities, minor differences, such as the small variation in order on Mondays, can still inform targeted marketing efforts. Develop localized marketing campaigns that focus on promoting pop music or specific artists on Mondays in both cities. This targeted approach could potentially boost engagement and user activity on the platform.

- **Tailored Content Curation:** Utilize the knowledge that musical preferences do not significantly vary over the week to curate playlists or recommend music that aligns with the most popular genre (pop) for both cities. Develop and showcase playlists highlighting popular pop tracks to engage users consistently throughout the week, aiming to improve user satisfaction and retention.

- **Community-Based Initiatives:** Capitalize on the similarity in musical preferences by fostering a sense of community among users from both cities. Launch community-driven initiatives, such as collaborative playlists or local music events, where users from Springfield and Shelbyville can engage and share their favorite music. This can create a sense of belonging and strengthen user loyalty.

By implementing these strategies based on the conclusions drawn from the analysis, the music platform can enhance user engagement, satisfaction, and retention by catering to the preferences and behaviors of users in Springfield and Shelbyville, ultimately improving the overall user experience.
