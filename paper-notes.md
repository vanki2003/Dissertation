# Milestone 2 - Key Points

[THE IMPACT OF ECONOMIC EVENTS ON STOCK MARKET RETURNS: EVIDENCE FROM INDIA](https://archive.aessweb.com/index.php/5002/article/view/2011/3206)

* Stock market can be used as a metric for a country/region’s economic health therefore its returns are expected to be affected by global economic events.
* unexpected economic events exert a greater impact than those expected
* USA trades with plenty of countries therefore any American economic event will have a global affect (subprime mortgages 2008)
* Macroeconomic on trade volume and stock prices lead to a significant response in trading and price.
* Information based stock trading positively affected the stock prices and enhanced the market efficiency.
* Romanian stock market volatility was caused by effects of global events.
* In Thailand, an expected rather than unexpected change in interest rates affected stock prices.
* neither a company’s characteristics nor the macroeconomic conditions could explain the reaction of stock prices.
* very few announcements by the US Federal Reserve exerted any significant impact on stock returns in India.
* Methodology was done by examining 13 economic crises and 5 bank frauds between 2008-2018.
* Regression analysis was performed.
* The realty and private banking sector were affected the most by the US subprime mortgage crisis
* Despite the instantaneous reactions to economic events be it positive or negative from investors, their responses are short-term.
* More of the unexpected events of dramatic effect led to opportunities for investors and traders to earn short-term profits.
* Study could be enhanced by incorporating volatility analysis.
___

[Impact of Macroeconomic Factors and Political Events on the Market Index Returns at Palestine and Amman Stock Markets (2011–2017)](https://deliverypdf.ssrn.com/delivery.php?ID=803090114088007108005121101068028103016052085015079029126116071027126070064115118030006052013006037046016118078068004089114012048011066061044002098021124102111102025091015052086118007014070099121123114091100076080096112014077067092105098020102121111098&EXT=pdf&INDEX=TRUE)

* Used event study methodology.
* CPI, GDP and exchange rate had a significant impact on stock market returns.
* Political events had a significant impact on stock market returns:
    * Abnormal positive returns before and after the event date
    * New political information affected Nepalese prices 2-3 days from the event date
* The real GDP is the greatest determinant of stock market returns.
* Positive relationship between balance of trade and stock market returns.
* Study made use of time series monthly data.
* Events tested were ones that caught the media's attention.
* Palestine and Amman stock markets are inefficient and do not absorb uncertain information and noisy events.
* The author encourages studying the impacts of other macroeconomic factors on a wider scale:
    * Unemployment rate and interest rates, for example
* The author also recommends extending the study to include other markets, both in advanced and developing countries, for comparison.
___

[Stock Closing Price Prediction using Machine Learning Techniques](https://www.sciencedirect.com/science/article/pii/S1877050920307924?fr=RR-2&ref=pdf_download&rr=85dbf0b53cfe4be7)
* Artificial Neural Network and Random Forest techniques were used to predict the next day closing price.
* Most of the previous work in this area use classical algorithms like linear regression, RWT, MACD and also using some linear models like ARMA and ARIMA
* This can be enhanced by using SVM and/or RF
* ANN, CNN, RNN and LSTM have shown promising results
* Data was collected through yahoo finance:
    * Over a 10 year period
    * Stocks observed were Nike, Goldman Sachs, Johnson and Johnson, Pfizer and JPMorgan Chase and Co.

* High, Low, Open, Close, Adjacent close and Volume was the information that was used
* New variables were created for training the model
    * Stock High minus Low price (H-L)
    * Stock Close minus Open price (O-C)
    * Stock price’s seven days’ moving average (7 DAYS MA)
    * Stock price’s fourteen days’ moving average (14 DAYS MA)
    * Stock price’s twenty-one days’ moving average (21 DAYS MA)
    * Stock price’s standard deviation for the past seven days (7 DAYS STD DEV)

* The author’s objective is to compare prediction accuracy between ANN and RF.
    * Predicted closing prices are subjected to finding the final minimalized errors in the predicted price.
        * Root Mean Square Error (RMSE)
        * Mean Absolute Percentage Error (MAPE)
        * Mean Bias Error (MBE)
* ANN proved to be a better technique
* For future work, deep learning models could be developed by adding external variables to the dataset for better results.
    * financial news articles
    * financial parameters
        * closing price
        * traded volume
        * profit and loss statements
___

[Comparison of Support Vector Machine (SVM) and Linear Regression (LR) for Stock Price Prediction](https://ieeexplore.ieee.org/document/10381982)
* author will be comparing the performance between SVM and LR models for sock price prediction
* obtained data from yahoo finance
    * Stock used was PT. Vale Indonesia
    * 9 year period (June 2014 – June 2023)
* Variables that make up the dataset were the date, open, high, low and close
* Data cleaning was done manually by deleting missing values
* Normalisation was done
    * Method used was min-max normalisation
* Data was split for 3 different scenarios
    * Scenario 1 – 70:30
    * Scenario 2 – 80:20
    * Scenario 3 – 90:10

* RMSE evaluation was carried out for comparison of results
 
* 70:30 test
    * SVM obtained an RMSE of 76.28 -> not good
    * LR obtained an RMSE of 45.61 -> not good

* 80:20 test
    * SVM obtained an RMSE of 66.05 -> not good
    * LR obtained an RMSE of 43.06 -> quite good

* 90:10 test
    * SVM obtained an RMSE of 64.32 -> not good
    * LR obtained an RMSE of 42.82 -> quite good

* LR algorithm is better than SVM for predicting the stock price
* The more training data used, the better the prediction results obtained
* Best LR performance was during the 90:10 test
    * Therefore, split data affects the prediction value obtained by an algorithm
* Suggestions that can be given for further research are to conduct research using deep learning algorithms or combining machine learning and deep learning as a comparison to obtain better prediction results.
___

[Russia–Ukraine crisis: The effects on the European stock market](https://onlinelibrary.wiley.com/doi/epdf/10.1111/eufm.12386)

* fear of political instability has a significant negative effect on stock market return and the risk profiles offinancial assets 
* inverse relationship betweeen political risk and stock returns 
* political risk influences currency carry trade returns 
* future tension levels are related to reductions incurrent stock returns 
* GPR has significant impactson corporations and financial markets by the adverse effects on investment, employment and downside risks equity returns and bond spreads and volatility in the stock markets 
* geopolitical threats have a greater significant effect on stock returns than geopolitical acts 
    * military build ups, threats of war, terrorism  
* the impact of this crisis is considerably broader and deeper than the impact of previous political events 
* author used firms belonging to the STOXX Europe 600 index
    * collected from Refinitiv Datastream
    * represents publicly traded firms with large, medium and small capital from major european countries
    * dropped 13 firms since daily stock price or market value data were not available for the entire estimation period
* findings demonstrate significantly negative average abnormal returns (AARs) surrounding the short‐event windows 
    * -3 to +3 days 
* Negative and significant cumulative abnormal returns (CARs) around the event days, pre‐event days and post‐event days was observed 
* seven out of eleven industries experienced negative and significantAAR on the event day 
    * industries were viz, the basic materials, consumer staples, financials, healthcare, industrials, telecommunications and utilities sectors 
* consumerstaples industry had the worst AAR on the event day meanwhile the energy industry experienced aninsignificant positive AAR 
* financial sector had the most severe effect 
* important to note that the author's sample countries are not ‘direct’ participants in the war, although they are providing humanitarian and military support to Ukraine and imposing restrictions on Russia 
* findings suggest that country‐level variation cannot be explained solely by geographic proximity to Russia or Ukraine; rather, the extent of trade and economicties affect stock prices significantly 
* Utilized event study methodology
* Noted that small- and median-cap firms were more heavily affected by the crisis compared to large-cap firms
* Encouraged further research to comprehensively examine the outcomes and repercussions of the crisis, including its effects on global stock markets and the broader geopolitical landscape
___
# Tabulated Format

| Paper Title and Link | Key Findings | Methodology |
|----------------------|--------------|-------------|
| [THE IMPACT OF ECONOMIC EVENTS ON STOCK MARKET RETURNS: EVIDENCE FROM INDIA](https://archive.aessweb.com/index.php/5002/article/view/2011/3206) | - Economic events significantly affect stock market returns <br> - Unexpected events have a greater impact <br> - Macroeconomic factors and information-based trading influence prices <br> - US Federal Reserve announcements have limited impact on Indian stock returns | - Examination of 13 economic crises and 5 bank frauds (2008-2018) <br> - Regression analysis |
| [Impact of Macroeconomic Factors and Political Events on the Market Index Returns at Palestine and Amman Stock Markets (2011–2017)](https://deliverypdf.ssrn.com/delivery.php?ID=803090114088007108005121101068028103016052085015079029126116071027126070064115118030006052013006037046016118078068004089114012048011066061044002098021124102111102025091015052086118007014070099121123114091100076080096112014077067092105098020102121111098&EXT=pdf&INDEX=TRUE) | - CPI, GDP, and political events significantly impact stock returns <br> - Study suggests inefficiency of Palestine and Amman stock markets <br> - Encouragement for wider macroeconomic factor study | - Event study methodology <br> - Analysis of time series monthly data |
| [Stock Closing Price Prediction using Machine Learning Techniques](https://www.sciencedirect.com/science/article/pii/S1877050920307924?fr=RR-2&ref=pdf_download&rr=85dbf0b53cfe4be7) | - Use of ANN and RF for stock price prediction <br> - New variables created for model training <br> - ANN showed better prediction accuracy <br> - Future recommendation for deep learning models | - Collection of stock data from Yahoo Finance (10-year period) <br> - Creation of new variables for training <br> - Comparison of ANN and RF prediction accuracy <br> - ANN gives better prediction of stock prices as compared to RF|
| [Comparison of Support Vector Machine (SVM) and Linear Regression (LR) for Stock Price Prediction](https://ieeexplore.ieee.org/document/10381982) | - Comparison of SVM and LR for stock price prediction <br> - LR outperformed SVM <br> - Data split affects prediction accuracy <br> - Suggestions for future research on deep learning algorithms | - Data collection from Yahoo Finance (9-year period) <br> - Manual data cleaning and normalization <br> - Comparison of RMSE for different data split scenarios |
| [Russia–Ukraine crisis: The effects on the European stock market](https://onlinelibrary.wiley.com/doi/epdf/10.1111/eufm.12386) | - Geopolitical crises negatively impact European stock returns <br> - Small and median-cap firms more heavily affected <br> - Impact extends beyond direct participants in the crisis | - Utilization of event study methodology <br> - Examination of STOXX Europe 600 index firms <br> - Analysis of abnormal returns surrounding crisis events |
___
