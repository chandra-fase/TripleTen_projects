## Project Description

As an analyst at Megaline, a telecom operator offering Surf and Ultimate prepaid plans, your task is to conduct an initial analysis to ascertain which plan generates higher revenue. This analysis will guide adjustments to the advertising budget, optimizing promotional efforts for maximum returns.

You'll work with a dataset comprising information on 500 Megaline clients, including client demographics, geographical locations, plan subscriptions (Surf or Ultimate), and their 2018 usage metrics—specifically, the number of calls made and text messages sent.

The primary objectives of this analysis are:

- **Revenue Comparison:** Evaluate and compare the revenue generated from the Surf and Ultimate plans based on client behavior metrics. These metrics will include call and text message usage, allowing inference regarding the plan that contributes more to the company's revenue.

- **Client Behavior Analysis:** Analyze the behavior patterns of clients subscribed to each plan. This includes assessing the average usage of calls and text messages for both plans, identifying trends, and understanding any correlations between usage and plan selection.

Your analysis aims to provide insights into client behavior, highlighting which plan contributes more significantly to Megaline's revenue. This information will enable the commercial department to fine-tune the advertising budget, directing resources more effectively towards the plan with the higher revenue potential.

Your findings and recommendations will be crucial in optimizing advertising strategies, ensuring the allocation of resources aligns with the plan that proves to be more lucrative for Megaline.

## Description of the Data

There are five tables in the dataset, and you’ll need to use all of them to do your data preprocessing and EDA. Below is a data dictionary that lists the columns in each table and describes that data that hold.
- `users` table: data on users
  - `user_id`: unique user identifier
  - `first_name`: user's name
  - `last_name`: user's last name
  - `age`: user's age (years)
  - `reg_date`: subscription date (dd, mm, yy)
  - `churn_date`: the date the user stopped using the service (if the value is missing, the calling plan was being used when this database was extracted)
  - `city`: user's city of residence
  - `plan`: calling plan name
- `calls` table: data on calls
  - `id`: unique call identifier
  - `call_date`: call date
  - `duration`: call duration (in minutes)
  - `user_id`: the identifier of the user making the call
- `messages` table: data on texts
  - `id`: unique text message identifier
  - `message date`: text message date
  - `user_id`: the identifier of the user sending the text
- `internet` tabel: data on the plans
  - `plan_name`: calling plan name
  - `usd_monthly_fee`: monthly charge in US dollars
  - `minutes_included`: monthly minute allowance
  - 'messages_included`: monthly text allowance
  - `mb_per_month_included`: data volume allowance (in megabytes)
  - `usd_per_minute`: price per minute after exceeding the pakage limits
  - `usd_per_message`: price per text after exceeding the package limits
  - 'usd_per_gb`: price per extra gigabyte of data after exceeding the package limits

## Hypotheses

- The average revenue from users of Ultimate and Surf calling plans differs.
- the average revenue from users in the NY-NJ area is different from that of the users from other regions.

## Steps Taken

- Cleaned and preprocessed the data by removing duplicate and missing values, as well correcting column data types
- Aggregated the data per user per period in order to have just one record per period
- Built a function to calculate the monthly revenue for each user
- Created a plot graph to compare the average call duration per month average number of messages per month, average amount of internet traffic consumed and average amount of revenue, each per plan.
    <img width="329" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/896235cc-621d-4d11-a95f-f4fc85266349">
    <img width="254" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/0f0381c7-f3ff-4254-a92d-6d5fa39c0905">
- Box plots were also created to visualize the monthly distributions of each plan for each feature 
- Used an alpha value of 0.5 to test the two hypotheses

## General Conclusion

Comparing users enrolled in Megaline’s two plans, Surf and Ultimate, we can see several similarities and differences. In terms of calling, users in both seem to be pretty similar in their distribution of call duration per month. Internet traffic per month for users in both plans is also very similar to each other. When comparing the average payments per month for users in both plans, the users enrolled into the Surf plan has a wider range of payment amount compared to those enrolled in the Ultimate plan.

When testing the hypothesis that the average revenue from Users of the Ultimate and Surf calling plans differ, we found that we can reject the null hypothesis because the average profits for the plans are different.

When testing the hypothesis that the average revenue from users in the NY-NJ area is different from that of the users from the other regions, we found that we cannot reject the null hypothesis as the average profits comparing the two populations in the NY/NJ area are not the same.

## Suggestions for the Company

Here are potential improvement ideas and business outcomes based on the conclusions drawn from the comparison between Megaline's Surf and Ultimate plans, as well as the analysis of user behavior across different regions:

- **Tailored Marketing Strategies:**
  - Plan-Specific Promotions: Utilize the understanding that Surf plan users exhibit a wider range of payment amounts compared to Ultimate plan users. Develop targeted promotions or incentives tailored to Surf plan users to encourage more consistent spending or upselling opportunities.
  - Region-Based Campaigns: Considering the similarity in revenue across regions, devise region-specific marketing campaigns or offers that cater to the preferences or behavior patterns observed within each region. This could potentially improve customer engagement and revenue generation in specific areas.

- **Service Optimization and Personalization:**
  - Customized Service Offerings: Based on the similarity in call duration and internet traffic between Surf and Ultimate plan users, consider providing additional service features or add-ons that resonate with the observed usage patterns. For instance, offer specialized data packages or call-related benefits tailored to the specific needs of these user segments.
  - Personalized Plan Recommendations: Leverage the knowledge of differences in payment amounts between Surf and Ultimate plans to fine-tune personalized plan recommendations for users, ensuring that they are offered plans that align more closely with their spending preferences and usage behavior.

- **Customer Retention and Loyalty Programs:**
  - Plan Upgrade Initiatives: Develop targeted strategies to encourage Surf plan users to explore higher-tier plans or additional services, leveraging the wider range of payment amounts observed within this user group.

- **Market Segmentation and Product Development:**
  - Localized Service Enhancements: Based on the findings related to region-specific revenue, consider localized service enhancements or infrastructure improvements in the NY-NJ area to potentially attract more users or increase revenue in this particular market.

Implementing these strategies derived from the analysis can assist Megaline in enhancing its service offerings, refining marketing strategies, and fostering customer engagement and loyalty, ultimately leading to increased revenue and improved customer satisfaction.
