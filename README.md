# Flight-Prices

Source: Kaggle: 
[Flight Prices] (https://www.kaggle.com/datasets/dilwong/flightprices/data)

The research I have chosen for the semester-long machine learning project is “Flight Prices One-way flights found on Expedia between 2022-04-16 and 2022-10-05”(31.09 GB) from Kaggle. The dataset contains information and background about “CSV file where each row is a purchasable ticket found on Expedia between 2022-04-16 and 2022-10-05, to/from the following airports: ATL, DFW, DEN, ORD, LAX, CLT, MIA, JFK, EWR, SFO, DTW, BOS, PHL, LGA, IAD, OAK.”

The data was 31.09 GB and would have to undergo exploratory data analysis, feature engineering, modeling and visualizations. With its large file size, google cloud storage, data-proc, compute engine, PySpark, and hadoop were among the many tools and libraries used to conduct the project.

 Through my findings, it was concluded that with the use of linear regression one can see that:
    Root Mean Squared Error: “119.36465702019076”
    R-Squared:  “0.5151452061893984” ,
    
With these values in mind, I was suggested on changing the parameter grid with some variations in regularization and elastic net, but the Root Mean Squared Error and R squared remained consistent with minor changes. The regression model was not able to fully accurately predict the flight price, however conclusions regarding the effect of travel duration on total price and its correlation among other features was notable during the visualization process. 