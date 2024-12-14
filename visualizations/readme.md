# Milestone 5:  Exploratory Data Analysis(EDA)

For milestone 5 we were instructed to create visualizations for the data and prediction results that have allowed for a deeper understanding of the data at hand. Through these visualizations, a story can be created.

Visualization 1: a correlation matrix that would depict the relationship between my label, “TotalFare”, and features, “‘'totalFare', 'seatsRemaining', 'totalTravelDistance', 'leadTime', 'isRefundable_binary', 'isNonStop_binary', 'isBasicEconomy_binary', 'segmentsCabinCodeIndex', 'startingAirportIndex', 'destinationAirportIndex', 'travelDurationIndex'”. The correlation can be depicted as the following 3 features, “‘total travel distance’, ‘travel duration index’, and ‘starting airport index’’” having a stronger correlation with total fare compared to other features


Visualization 2 &3: Demonstrates the number of flights by starting and destination airport, and side by side comparison with its visualization and count on a chart after using .head(16)



Visualization 4: uses seaborn to create a distribution plot, randomly sampling 1% of the large flight dataset. The plot shows the total fare distribution among the dataset.  This insight allows us to create an idea on the different deviations for the fare in our dataset and a possibility on the max and min fare that will be worked on, in this case using the .describe() on totalFare and the visualization it can be noted that the count of 1% is 741048.000000, mean 341.784517, standard deviation is 171.434373, lowest total fare (min) is 23.970000, and the deviations of the distributions are: 25% as 202.600000, 50% as  312.600000, 75% as 458.600000, highest total fare (max) is 942.100000



Visualization 5:  uses seaborn to create a relationship plot between the totalFare and totalTravelDistance.  The following plot shows a positive correlation between both, demonstrating that as the travel duration increases so does the total fare, using 0.0001% randomly selected from the flight price data. The percentage was lowered, after attempting to work with 1%, 0.01%, and 0.001% to see a clear picture without seeing a blob of clusters. With this in mind, this can also be relevant when looking for flights on google from NYC to Los Angeles, California, compared to NYC to Nashville, Tennessee in April. Where the average duration according to distance calculator for JFK to LAX is 2,469.45 mi (3,974.20 km) flight distance apart and it’s cheapest flights (currently as of 12/13/24 10:24 PM) at $387 and according to Air Miles Calculator JFK to BNA is 65 miles / 1232 kilometers flight distance apart and it’s cheapest flights (currently as of 12/13/24 10:25 PM) at $278.




Visualization 6: uses seaborn again to create a relationship plot between the totalFare and prediction, using again 0.0001% randomly selected points for the clear visualization.  The column prediction was created after making the machine learning regression model to be able to predict the flight prices, through this visualization, one can see how far the predictions are off from the actual total fare.  Although we received a high root mean squared error and a low R squared result, indicating poor predicting outcomes, the visualizations make the picture a bit clearer. 