# Time-Series-Price-Forecasting-on-Temperature

**Background**:

Energy prices are an inevitable expense for businesses, especially those that operate in a typical business setting. Additionally, energy markets tend to be highly volatile due to many factors, like weather, inflation, the prices of other similar commodities, etc. Some businesses attempt to hedge these risks through energy contracts with their suppliers. While there are a variety of ways to address these risks, there are two common contract types. The first being an indexed contract where companies can pay less, or can even be paid by decreasing their energy consumption while the energy grid is under high demand. The second is a fixed rate contract where the energy supplier agrees to charge the same rate, (cost per kilowatt hour), for a fixed amount of time regardless of how energy markets change. Spot prices, when taken over time in a specific area, are a key indicator of changing energy rates and overall grid demand.

-------

**Business Problem:**

For this energy advisor company, it would be extremely useful to have a tool that could be used to better advise clients on when the grid will likely be in high demand, when to best renew or enter into a fixed-rate contract, or what a profitable price for their contracts would be for a given year. The goal of this forecasting project was to devise a way to accurately forecast electricity spot prices in both the short and long term to advise existing clients how to manage their energy consumption if they are on an adjustable index contract and advising new/existing clients. It would also be extremely valuable to determine if temperature and the relationship it has with price could be used to forecast future prices, or if further information is necessary to make an accurate prediction.

---

**Model methodology:**

All three target variables (minprice, maxprice, avgprice) were tested using the Augmented Dickey-Fuller Unit Root Test to determine if the model were stationary. None of the variables showed significant seasonal pattern or trend; they also passed the unit root test indicating that the ARIMA model would be the best methodology to use, especially with the inclusion of two independent variables. We then decided to create nine total models, each with a target variable paired with an explanatory variable. The explanatory variables were also time series meaning these variables had to be prewhitened to reduce cross-correlations and determine the lag value that needed to be added to the SAS code to capture the most variation, which would lead to an effective use of the ARIMAX model.

---

**Business Recommendation:**

This model would have two major impacts on the energy market. First, for existing clients with indexed contracts, short-term average price forecasts would allow advisors to inform clients when best to reduce their energy consumption. Due to the conditions of their contracts this will cause drastic energy rate reductions as high energy spot prices are a result of high grid demand. The second application is for existing clients looking to renew their fixed rate contracts or new clients looking for the best time to start a contract inorder to hedge their consumption risks. A long-term forecast will allow advisors to identify when the most likely time would be to get a low fixed rate, this would prevent uncertainty when calculating budgets as the rate stays the same regardless of client usage or the energy market, however it would ruin customer relationships if they were locked in at a high fixed rate. Therefore this model will allow the advisors to identify when to enter their contracts, but also when not to sign a contract and to wait for a more certain time with a lower, more standard rate. There are more, but less common applications of this model as well. It can be used to estimate savings when consulting on green energy projects to lower client usage or renewable and energy storage initiatives.

----

**Tools/Technologies used :**

SAS Studio
