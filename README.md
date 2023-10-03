# (Dataset Exploration Title)
## by (your name here)


## Dataset

The dataset is from a bike sharing company. The data was obtained from the following source: https://www.kaggle.com/datasets/dcshah/bay-wheels-2019-data/data

The data is organized in separate csv files for each month and contains data for all months 2019. Each row constitutes a bike ride where information about the bike ride has been recorded (e.g. start and end time/location of bike trip, bike ID, destination name, etc.).


## Summary of Findings

Findings from univariate analysis:
1. Unusual points were mostly related to extremely high rental times and travel distances. Some of these most extreme outliers have been removed since they could be clearly attributed to erroneous data. However, the distributions of distances and durations are unimodal and still right skewed (log normal distributions) but the remaining values which are responsible seem legit and reasonable have, hence, not been removed. Hence, these were plotted on a logarithmic x-scale.
2. There were also some unreasonably small values in the distance and duration columns which partially could be removed since they were probably corresponding to some default database entries. However, the remaining small values were kept.
3. The time dependent data were the most interesting since they lead to the conclusion that most people use the bike service mostly to commute to and from work. Furthermore, it was found that the service is mostly used during week days.
4. The customer type data did ot hold any surprises. They clearly show that most rides are performed by subscribers and the subsidised service is only used by a small fraction of the people.

Findings from bivariate analysis:
1. Travel distance and duration are almost almost identical for each hour of day and day of week. These properties seem to not be very correlated with time. => Bike service seems to be used for similar purposes at any given time.
2. A much larger fraction of subscribers seem to use the service for commuting to work. The main use cases of the service seem to be identical for both user types. However, the uniform distribution for day of week and the flatter distribution for hour of day indicate that a larger fraction of customers tend to use the service also for free time activities.

Findings from multivariate analysis:
1. We have found that the the customer travel distance and duration are systematically higher than the corresponding values of the subscribers across all metrics of our summary.
2. Additionally, the comparison of customer data to subscriber data suggests that customers tend to use the bike more often and for longer travels during the middle of the day (during regular working hours) and on weekends than subscribers.
3. The most surprising and most important finding was that it seems like subscribers are converting to regular customers at the end of the year. This could have a multitude of reasons, which we don't have the data to pin down, but it might be a concern for the company. Hence, while our initial goal was to find ways to make customers convert to subscribers, the more urgent issue to prevent subscribers to convert to customers.




## Key Insights for Presentation

The presentation's main goal will be to lead the audience to the concern of the decrease in subscribers and users and additionally show the the differences in user behavior throughout the day. For this, the following
findings/graphs will be presented:
1. Start from the bivariate distribution of users on an hourly basis to make the point that most users seem to use the service for work commuttes.
2. Show the multivariate plot indicating the differences in travel durations for users as function of the time of day (we could have also used the distance plot or the day of week plot but this plot shows the point we wanna make the strongest and is consistent with the previous plot) to show that that customers tend to use the service for much longer travel durations/distances and use the service especially longer during working hours. => Probably more freetime or student use of customers.
3. However, even though there are differences in customer behavior which could be used for marketing and converting customers to subscribers, there are more urgent issues with our service which should have a much higher priority. To introduce this problem we start by showing the graph of the univariate user distribtuion as function of the month of the year. The point here is that the bike trips decrease towardsDecember. This is not unusual but expeced but there is a twist:
4. Show the bivariate graph of the user distribution per month divided according to user type: The problem is that the number of customers increases while the number of subscribers decreases which seems odd. This could of course just be coincidence but we have some indications that our idea is correct:
5. Show the graph which shows the median travel distance and duration for each user: From this graph it can be seen that both user types are usually unaffected in their usage behavior throughout the year and both show clear distinctions. However, this graph clearly shows that during the November/December the user behavior of the customer group converges towards the subscribers group. In combination with the previous graph this suggests that subscribers convert to regular customers.
