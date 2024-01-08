# Walmart Sales Forecasting
# Problem :
Sales can vary greatly from the average during different seasons, and not being aware of these fluctuations can result in significant financial losses for a company. The ability to predict future sales is essential for any business, as it allows for proper stock management, revenue calculation, and informed decision-making regarding investments. Furthermore, being able to anticipate sales can positively impact stock prices and investor confidence by meeting or exceeding predetermined targets. Conversely, failing to reach projected sales targets can have a detrimental effect on stock prices, particularly for a large company like Walmart. Therefore, understanding and forecasting sales is crucial for the success and stability of a business.
# My Goal:
My main goal in this project is to construct a model that can accurately forecast the sales of the stores. By utilizing this model, Walmart executives will be able to make informed decisions about their future strategies, a crucial aspect in managing inventory, projecting revenue, and determining whether to pursue new investments.
# Plan :
1. Understanding the data
2. Cleaning the data
3. Exploring data
4. Preparing for modelling
5. Create SARIMA model
# Findings :
1. Exploratory Data Analysis
   - There are a total of 45 stores, encompassing 81 departments, and offering 3 different types of stores.
   - This dataset contains information on the weekly sales of Walmart from February 5, 2010, to October 26, 2012. In 2010, there were 48 weeks, in 2011, there were 52 weeks, and in 2012, there were 43 weeks.
   - Store 20 is widely regarded as the top-performing store, achieving the highest weekly sales of 301.4 million. Following closely behind are store 4 and store 14, securing the second and third positions, respectively. On the other hand, store 5, store 44, and store 33 occupy the bottom three spots in terms of weekly sales.
   - Department 92 is the best department in getting weekly_sales througout timeseries in this dataset with 483.8 M
   - Weekly sales data by year indicates that 2010 was the top-performing year, with an average of 16318. When examining sales by month, it is clear that December stood out as the best month, with an average of 19425. This is unsurprising, given that December is a holiday month when people are more likely to shop. Looking at the monthly sales line plot, it is apparent that sales follow a consistent pattern each year, with a steady increase in sales during November and December. This trend is consistently observed year after year. The weekly sales line plot also reveals a consistent pattern, with peak sales occurring in the 50th week each year.
   - On holidays, average weekly sales are 51.7% higher than non-holidays, which have sales at 48.3%. Thanksgiving sales consistently exceed those of other holidays, with an average of 22,269. This indicates the strong popularity and demand for Thanksgiving products compared to other holidays.
   - Weekly sales for type A and type B follow a similar pattern, but type A consistently has higher sales than type B. Type C, on the other hand, has the lowest sales compared to types A and B. The peak sales for types A and B were observed during Thanksgiving, whereas type C experienced its highest sales during the Superbowl.
2. SARIMA Modelling
   - After we determine the optimal order for the SARIMA model, we proceed with forecasting on the initial dataset and draw the following conclusions:
our SARIMA model's optimal order is (1,1,1)(1,1,0)52
The SARIMA forecast visualization indicates that the model can make reasonably accurate predictions on the training data. This is further supported by the MAPE score of 6.3
In the test data, the forecast in the visualization demonstrates favorable outcomes with a superior MAPE score compared to the training data at 2.97
3. auto-arima Modelling
   - We used auto-arima for modeling and reached the following conclusions:
The auto ARIMA model indicates that the best model order is (1,0,2)(2,0,0)[52].
The graph data shows that the prediction closely matches the testing data, with a MAPE score of 5.61. This indicates that the model's accuracy is dependable and consistent.
