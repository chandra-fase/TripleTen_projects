## Project Description

As an analyst at Zuber, a burgeoning ride-sharing company launching in Chicago, your mission is to extract meaningful patterns from available data. Your objective is twofold: understanding passenger preferences and investigating the impact of external factors on rides.

You'll work extensively with a database, analyzing data from competing ride-sharing companies to test hypotheses concerning the correlation between weather conditions and ride frequency.

## Description of the Data

A database with info on taxi rides in Chicago:

`neighborhoods` table: data on city neighborhoods
- `name`: name of the neighborhood
- `neighborhood_id`: neighborhood code

`cabs` table: data on taxis
- `cab_id`: vehicle code
- `vehicle_id`: the vehicle's technical ID
- `company_name`: the company that owns the vehicle

`trips` table: data on rides
- `trip_id`: ride code
- `cab_id`: code of the vehicle operating the ride
- `start_ts`: date and time of the beginning of the ride (time rounded to the hour)
- `end_ts`: date and time of the end of the ride (time rounded to the hour)
- `duration_seconds`: ride duration in seconds
- `distance_miles`: ride distance in miles
- `pickup_location_id`: pickup neighborhood code
- `dropoff_location_id`: dropoff neighborhood code

`weather_records` table: data on weather
- `record_id`: weather record code
- `ts`: record date and time (time rounded to the hour)
- `temperature`: temperature when the record was taken
- `description`: brief description of weather conditions, e.g. "light rain" or "scattered clouds"

## Answer These Questions:

- Find the number of taxi rides for each taxi company for November 15-16, 2017. Name the resulting field trips_amount and print it along with the company_name field. 
Sort the results by the trips_amount field in descending order.
- Find the number of rides for every taxi company whose name contains the words "Yellow" or "Blue" for November 1-7, 2017. Name the resulting variable trips_amount. Group the results by the `company_name` field.
- In November 2017, the most popular taxi companies were Flash Cab and Taxi Affiliation Services. Find the number of rides for these two companies and name the resulting variable trips_amount. 
Join the rides for all other companies in the group "Other." Group the data by taxi company names. Name the field with taxi company names company. Sort the result in descending order by trips_amount.
- Retrieve the identifiers of the O'Hare and Loop neighborhoods from the neighborhoods table.
- For each hour, retrieve the weather condition records from the weather_records table. Using the CASE operator, break all hours into two groups: "Bad" if the description field contains the words "rain" or "storm," and "Good" for others. Name the resulting field weather_conditions. The final table must include two fields: date and hour (ts) and weather_conditions.
- Retrieve from the trips table all the rides that started in the Loop (neighborhood_id: 50) and ended at O'Hare (neighborhood_id: 63) on a Saturday. Get the weather conditions for each ride. Use the method you applied in the previous task. Also retrieve the duration of each ride. Ignore rides for which data on weather conditions is not available.


## General Conclusion

- Looking at the top ten companies based on the trip amount, we can see that Flash Cab is the leading company by over 8,000. After this large jump from the Flash Cab to Taxi Affiliation Services, the trip amount decreases less significantly between the rest of the top ten companies.
- Our graph of the average trip amount per drop-off location shows that Loop is the most popular drop-off location. The average trip amount for the bottom three of the top ten drop-off locations are very similar.
- After testing the hypothesis, we can see that the average duration of rides from the Loop to O'Hare International Airport changes on rainy Saturdays

## Suggestions for the Company

**Strategic Focus on Leading Companies:**
- Investing in Top Performers: Capitalize on Flash Cab's significant lead in trip amounts by forging strategic partnerships or exclusive deals. Consider tailored incentives or loyalty programs to retain their customers or attract them to Zuber's platform.
- Expansion and Collaboration: Explore possibilities for collaboration or acquisition with Flash Cab or other leading companies to expand Zuber's market reach and enhance service offerings.

**Enhancing Service to Popular Drop-off Locations:**
- Optimized Services to Loop: Given Loop's status as the most popular drop-off location, prioritize service enhancements, increased driver availability, or promotional offers specifically tailored to users frequenting this area. This can lead to improved customer satisfaction and increased brand loyalty.
- Improving Experience at Other Top Locations: While the bottom three drop-off locations show similarity in trip amounts, consider analyzing user preferences or pain points at these locations to provide targeted improvements or incentives to enhance customer experience and potentially increase ride frequency.

**Weather-Based Service Adjustments:**
- Adaptive Pricing or Service Enhancements: Based on the observed changes in ride duration from the Loop to O'Hare on rainy Saturdays, consider implementing dynamic pricing strategies or specific service enhancements during adverse weather conditions. This could potentially attract more riders or encourage flexibility in travel choices during inclement weather.

**Data-Informed Business Strategies:**
- Refined Marketing and Operations: Utilize insights on trip amounts and popular drop-off locations to optimize advertising efforts, focusing on highlighting Zuber's convenience or tailored services for these locations. Implement operational strategies or resource allocation based on customer demand patterns observed in the data.

**Customer-Centric Approach:**
- Customer Feedback and Experience Enhancement: Gather feedback or conduct surveys from users traveling from Loop to O'Hare during rainy Saturdays to understand their experience. Use these insights to refine services, potentially addressing pain points and improving customer satisfaction.

Implementing these strategies derived from the analysis can assist Zuber in optimizing service offerings, refining marketing campaigns, improving customer satisfaction, and ultimately increasing market share and profitability in the ride-sharing industry.
