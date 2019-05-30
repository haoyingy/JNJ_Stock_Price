# JNJ_Stock_Price
The project objective is to forecast the stock price of JNJ at the end of 2019 based on contextual factors

**Qual Narrative:**
1.	Overview about JNJ (Johnson & Johnson)
JNJ is one of the world’s largest healthcare company. Its products fall into three segments:
•	Pharmaceutical, with 39% of total sales
•	Medical device and diagnostic, with 36%
•	Consumer product, with 25%

2.	Factors analysis
There are external factors and internal factors which will influence JNJ stock price. As internal factors are highly related to JNJ stock price, it’s hard to make time series prediction on it, so I focused on external factors to make prediction. 
External factors for JNJ, there are two types:
Competitive: 
As JNJ is world’s top Pharmaceutical company, and barriers to ‘Pharmaceutical, Medical device and diagnostic’ entry is very high, so new entrants or existing competitors have very small impact on JNJ, this type can be ignored. 
Contextual: 
Politics, Economic (GDP, income, expenditure), sociocultural (aging population, surging rate of various health problem), technological, medical industries, health care cost, etc. So contextual factors will be my main focus. 

3.	Model building process
I used linear regression to build the model, ARIMA and ETS to predict time series data. Then I put time series prediction data into linear model to forecast the stock price of JNJ for each month in 2019. At linear regression model, I used log (stock price) as target variable, and log each independent variables as predictor variables. 

Dependent variable: 
JNJ stock price (monthly)
Independent variables:
GDP per capita (quarterly)
Income per capita (monthly)
Health care construction cost (monthly)
Consumer Price Index for medical care (monthly)
Medical care commodities price index (monthly)




**Quant Narrative:**

Model 1: 
Models used: Linear regression, ARIMA, ETS
Dependent variable: JNJ Stock Price
Independent variable 1: Income per capita
Independent variable 2: CPI of Medical Care
Data Sources: Yahoo Finance, U.S. Bureau of Economic Analysis, U.S. Bureau of Labor Statistics

Adjusted R-Squared: 0.836
negative influence: ‘Income per capita’ 
positive influence: ‘CPI of medical care’ 
Scenario 1A(ARIMA) Predictive Output: $155.71 
Scenario 1B(ETS) Predictive Output: $156.67

Model 2: 
Models used: Linear regression, ARIMA, ETS
Dependent variable: JNJ Stock Price
Independent variable 1: GDP per capita
Independent variable 2: Health Care Construction Spending 
Independent variable 3: Medical care commodities price index
Data Sources: Yahoo Finance, U.S. Bureau of Economic Analysis, U.S. Bureau of Labor Statistics

Adjusted R-Squared: 0.802
negative influence: ‘GDP per capita’
positive influence: ‘Health Care Construction Spending’, ‘Medical care commodities price index’ 
Scenario 1A Predictive Output: $145.39
Scenario 1B Predictive Output: $143.15

Model 3: 
Models used: Linear regression, ARIMA, ETS
Dependent variable: JNJ Stock Price
Independent variable 1: Income per capita
Independent variable 2: CPI of Medical Care
Independent variable 3: GDP per capita
Independent variable 4: Health Care Construction Spending
Data Sources: Yahoo Finance, U.S. Bureau of Census, U.S. Bureau of Labor Statistics

Adjusted R-Squared: 0.841
negative influence: ‘Income per capita’, ‘GDP per capita’
positive influence: ‘CPI of medical care’, ‘Health Care Construction Spending’
Scenario 1A Predictive Output: $151.25
Scenario 1B Predictive Output: $153.19

Final predictive output from ensemble model: $150.89
