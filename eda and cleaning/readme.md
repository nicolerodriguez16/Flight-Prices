# Milestone:  Exploratory Data Analysis(EDA)

For the third milestone, the exploratory data analysis was performed on the Flight Prices dataset from Kaggle.  This included, understanding the data(viewing columns, rows, min/max/count (1) of numeric and date columns, relationships amongst features and the label etc) as well as cleaning the data by removing null/missing values.



A correlation matrix,  was created which demonstrated a low correlation between ‘elapsedDays’ and a high correlation with ‘baseFares’, both were removed due to its low correlation and high dependency of the label.



 Moving forward in feature engineering, I see issues with the dates as I believe that it also may play a role in determining the total fare price, considering shorter leadtimes would most likely result in a higher price. A solution to this could be creating the new column “leadTime” by using datediff between “searchDate” and “flightDate”.