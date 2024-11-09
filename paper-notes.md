# Key points of papers

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

### News sentiment and international equity markets during BREXIT period: A textual and connectedness analysis

* analysed over 34000 news articles and categorised them into 3 clusters (positive, negative and neutral)
* used time varying connectedness of Diebold and Yilmaz
* no differentiation was made between positive and negative sentiment in news articles
* scope of analysis could be broadened to largere equities such as bonds
* 5 year timeframe
* spillover increased when articles were on topics relevant to investors
* news sentiment can be used as a good indicator of the financial markets during times of higher uncertainty
* financial market sentiment in news articles are better indicators rather than general ones
* investors saw brexit as a smaller threat to EU-based companies and therefore, less threat for EU economies
* estimating spillover effects couild capture market movements as well as market structre in terms of returns

### Stock market prediction using machine learning classifiers and social media, news
* markets can be driven by volitle factors being microblogs and news
* predict accuracy for 10 subsequent days
* feature selections and spam tweets resuction were performed
* highest prediciton score was achieved using social media and financial news
* RF was found to be consistent and achieving its highest accuracy in social media, financial news
* social media overall has more influence on stock price prediciton
* positive effect on prediciton performance when applying feature selection and spam tweet reduction
* other social media data could be used to compare effects (facebook)
* RF also works well since the dataset had a mix of numerical and categorical features

### The effect of international media news on the global stock market
* 35 countries were used
* International news sentiment positively influences stock market returns globally.
* The effect of news sentiment is weaker in countries with higher financial development and stronger financial institutions.
* Increased access to international media amplifies the effect of news sentiment on stock markets.
* The impact is more pronounced in countries with high levels of economic openness.
* The influence of news sentiment grew stronger after the 2008 financial crisis, especially in emerging markets relative to developed ones.
* The effect on stock markets is mitigated by recent deglobalization trends and the COVID-19 pandemic.
* Robust regressions, alternative sentiment and return estimation methods, and exogenous shocks (e.g., World Cup Soccer Matches) confirm the study’s findings.

### News sentiment and company reports impact on stock returns
- **Objective**: Analyzes the incremental effect of sentiment from MD&A sections in 10-K and 10-Q reports on predicting next-quarter stock returns.
  
- **Data**: 
  - U.S.-based companies' filings over the past 20 years.
  - MD&A sections extracted with regular expressions for accuracy.

- **Sentiment Scoring**: 
  - TF-IDF assigns weights to words in specific emotional categories from the Harvard IV-4 General Inquirer.
  - Scores for each sentiment category are calculated by summing these weights.

- **Modeling Approach**:
  - CatBoost model tested with and without sentiment features, using AUC for evaluation.
  - Binary classification used for robustness; regression models avoided.

- **Findings**:
  - Model significantly outperforms random guessing.
  - Specific categories (e.g., “Weak & Underst”) are more informative than general positive/negative scores.

- **Future Research**:
  - Consider incorporating accounting fundamentals to refine the model.
  - Explore other dictionaries for financial sentiment beyond positive/negative categories.

- **Data and Extraction Challenges**:
  - Missing quarterly reports, possibly due to SEC data issues.
  - MD&A extraction needs improvement due to varying keywords and section labels.
  - HTML unavailability in some filings complicates parsing.

- Weak emotional category tops the ranking, outweighing the importances of all previous quarters' returns.
- **Adding sector and month features was explored to enhance model performance.**
- Sector feature notably improves the model, pushing the AUC above 0.56.
- Month feature has a minimal impact, adding just 0.4 percentage points over the sentiment-augmented model.

### How does Chinese stick market react to breaking news about covid-19?
- period was 2020-2023
- event study method from first declaration to classifying to catrgory B
- The impact of negative news was generally stronger than that of positive news.
- overall intensity of reactions to bad news is stronger than that to good news
- Small-sized stocks react more positively to good news and more negatively to bad news (market level)
- Materials, health care, and energy sectors experienced positive impacts during the pandemic.
- Consumer discretionary, utilities, and real estate sectors were the most adversely affected by COVID-19 in China.
- Sectoral reactions aligned with COVID-19 profitability patterns, with sectors benefiting from pandemic-driven demand performing better
- Implications for Investors:
   - For Small Firms: Special attention should be given to COVID-19 news, especially negative announcements.
- Methodology Constraints: The event study methodology may yield different results with varied event windows or sample periods. Future studies could expand these parameters.
- Geographic Scope: This study is China-specific; similar studies in other countries could provide comparative insights.

### Stock market prediction using machine learning tools
- Investors can now trade easily using internet-connected devices, increasing accessibility and appeal in stock trading.
- Online trading has transformed how people buy and sell stocks, creating a globally interconnected marketplace and new investment opportunities.
- Stock markets have become sensitive to social media sentiment and susceptible to cyber-attacks, highlighting the need for secure and adaptive trading frameworks.
- Studies were analyzed based on the type of data input (market data and textual data), data pre-processing approaches, and machine learning techniques used.
- Common performance metrics used across studies were reviewed, with SVM emerging as the most widely applied SMP technique.
- Techniques like Artificial Neural Networks (ANN) and Deep Neural Networks (DNN) showed greater accuracy and faster predictions, especially when combining market data with textual data from online sources.
- Extracting predictive features from financial data is complex due to the variety of predictive variables and the noisy nature of financial datasets, which affects prediction quality.
- While many SMP methods work in controlled settings, live testing presents difficulties due to real-time price fluctuations, noise, and unpredictable events (e.g., the Knight Capital Tragedy, which caused a $440 million loss).
- Market volatility, influenced by factors like inflation, uncertainty, and algorithmic trading, heightens risks and complicates price prediction. Examples include flash crashes, where $860 billion was erased from U.S. stock markets within 30 minutes.
- Political events can also intensify volatility, further complicating market behavior analysis.
- Social media sentiments significantly impact stock predictions, yet the presence of bots introduces noise, requiring bot detection for more accurate sentiment analysis.
- Events such as the 2013 Associated Press Twitter hack, which triggered a market crash, highlight the influence and volatility associated with social media data.
- The rise of fake news and bot-generated data complicates the extraction of reliable insights from social media platforms, making it essential to filter high-quality data for accurate sentiment analysis. (sentiment analysis challenge)

### Financial sentiment analysis: techniques and applications
- **Evolving Scope of FSA:**
  - FSA research has expanded significantly with the rise of financial textual data from sources like public news and social media.
  - Modern FSA examines not only sentiment within financial texts but also how this sentiment influences market predictions.

- **Distinct Goals of FSA Techniques and Applications:**
  - **FSA Techniques:** Focus on improving sentiment analysis tasks (e.g., targeted aspect-based FSA) using human-annotated data to enhance analytical accuracy.
  - **FSA Applications:** Use sentiment data for practical financial applications, such as causality and correlation testing, and market forecasting based on market-driven, real-world data.

- **Role of Financial Sentiment as Investor Sentiment Proxy:**
  - Financial sentiment acts as a stand-in for investor sentiment, which in turn influences market dynamics and reflects collective investor behaviors.

- **Interconnections Among FSA, Investor Sentiment, and Market Sentiment:**
  - Market sentiment is shaped by aggregated investor sentiment, which is reflected in their investment decisions.
  - Investor sentiment can be inferred from multiple sources, including financial text sentiment, sentiment surveys, and actual market data, providing a theoretical basis for using diverse data sources for financial forecasting.

### Using news articles to predict stock price movements
- **Data Sources and Approach:**
  - The approach utilizes **two key information sources**: stock prices and related news articles, aligning news articles with stock price movements to analyze their impact.
  - Stock prices are analyzed within a **specific window of influence**, scoring news articles based on how stock prices move shortly after publication.

- **Classification and Findings:**
  - A **naïve Bayesian text classifier** was trained to categorize stock price movements into three classes, though the classifier’s predictive accuracy was low.
  - A significant correlation was observed between news articles and stock price behavior **within a 20-minute window before and after** the news release.

- **Implications and Market Hypothesis Challenge:**
  - This correlation challenges the **efficient market hypothesis**, suggesting that short-term indicators for predicting stock behavior exist immediately surrounding news publication.
  - The findings imply that timely analysis of news articles could potentially be leveraged for profitable stock predictions within a brief time frame following their release.
- **Low Predictive Power Despite Significant Classification Results:**
  - The classifier showed significant results for stock price alignments in the [-20, 0] and [0, 20] minute windows relative to news release times.
  - Despite this, the classifier’s overall predictive power remained low, indicating limitations in accurately predicting stock price movements based on news.

- **Possible Reasons for Low Predictive Power:**
  - **Index Price Volatility Approximation:** The B-value measure used to gauge stock price movement relative to an index was sometimes ineffective. Accurate prediction may require a more realistic and precise index price to better model individual stock movements.
  - **Redundant News Reporting:** Often, important news is repeatedly reported by multiple sources, but only the first release significantly impacts stock prices, reducing predictive accuracy when subsequent articles are included in the analysis.
- These findings suggest that refining index modeling and filtering repeated news reports could enhance predictive accuracy for stock price behavior.

### Sentiment analysis of financial news
   - The study applies the VADER tool for sentiment classification on highly liquid stocks, categorizing news headlines as negative, neutral, or positive based on their sentiment values.
   - Sentiment scores are calculated as percentages (positive, neutral, negative) that sum up to 1 per sentence, and a compound score is derived by normalizing lexicon ratings.
   - Sentiment values for stocks (e.g., Apple) are tabulated and visualized (e.g., in green, red, yellow) for daily analysis.
   - A compound sentiment score over time helps users assess market sentiment, with negative scores suggesting a potential decrease in stock prices, as seen in visual comparisons of Tesla and Apple.
   - While sentiment scores are informative, external economic factors (like national and global economic conditions) may occasionally disrupt the correlation between market sentiment and actual stock performance, introducing variability.
  Here are the key findings from the study:
   - Minor lexicon adjustments could tailor the methodology for specific market sectors (e.g., pharmacy, healthcare, e-commerce) or stock classifications (e.g., large-cap, mid-cap, small-cap).
   - Such sector-specific customization could support forecasting trends in stock values within particular industries or market segments.
   - Here are the key insights from the provided text:
   - A strong correlation is noted between shifts in sentiment and subsequent stock price changes.
   - For example, a positive sentiment change for Tesla on 10/26/2019 preceded a stock price increase on the first trading day after the weekend (10/28/2019).
   - Similarly, a negative sentiment on 10/29/2019 coincided with a price drop, which stabilized the following day as sentiment improved.
   - While sentiment generally correlates with stock price movement, external factors can influence this relationship. These include the bandwagon effect, market overvaluation corrections, the impact of related markets, and broader economic conditions (both national and global).
