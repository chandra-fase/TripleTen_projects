## Project description

You work as an analyst for the telecom operator Megaline. The company offers its clients two prepaid plans, Surf and Ultimate. The commercial department wants to know which of the plans brings in more revenue in order to adjust the advertising budget.
You are going to carry out a preliminary analysis of the plans based on a relatively small client selection. You'll have the data on 500 Megaline clients: who the clients are, where they're from, which plan they use, and the number of calls they made and text messages they sent in 2018. Your job is to analyze clients' behavior and determine which prepaid plan brings in more revenue.

## Description of the data

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

## General conclusion

Comparing users enrolled in Megaline’s two plans, Surf and Ultimate, we can see several similarities and differences. In terms of calling, users in both seem to be pretty similar in their distribution of call duration per month. Internet traffic per month for users in both plans is also very similar to each other. When comparing the average payments per month for users in both plans, the users enrolled into the Surf plan has a wider range of payment amount compared to those enrolled in the Ultimate plan.

When testing the hypothesis that the average revenue from Users of the Ultimate and Surf calling plans differ, we found that we can reject the null hypothesis because the average profits for the plans are different.

When testing the hypothesis that the average revenue from users in the NY-NJ area is different from that of the users from the other regions, we found that we cannot reject the null hypothesis as the average profits comparing the two populations in the NY/NJ area are not the same.
