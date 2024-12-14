# Dissertation
*"It's that time of the degree"*

# To-do
- [x] Finish literature review
- [ ] Finish methodology
- [ ] Practice finBERT model

**Excellent Literature Review!**

Your literature review provides a comprehensive overview of machine learning and sentiment analysis techniques applied to stock prediction. It's clear that you've delved deep into the field, identifying key trends, challenges, and promising approaches. 

**Regarding your methodology, here's a suggested approach incorporating FinBERT:**

### Proposed Methodology

**1. Data Acquisition:**

* **Financial News:** Collect a large dataset of financial news articles from reputable sources like Reuters, Bloomberg, and Google News.
* **Historical Stock Prices:** Gather historical stock price data for the target stocks, ensuring alignment with the news articles' publication dates.

**2. Data Preprocessing:**

* **Text Cleaning:** Clean and preprocess the news articles to remove noise, such as stop words, punctuation, and irrelevant information.
* **Tokenization and Sentence Segmentation:** Break down the text into tokens (words or subwords) and sentences.
* **Sentiment Analysis with FinBERT:**
    * Fine-tune the pre-trained FinBERT model on a financial sentiment analysis dataset to enhance its performance for your specific task.
    * Use the fine-tuned model to classify each news article into sentiment categories (e.g., positive, negative, neutral).
    * Extract sentiment scores or probabilities for each article.

**3. Feature Engineering:**

* **Technical Indicators:** Calculate relevant technical indicators (e.g., moving averages, RSI, Bollinger Bands) from the historical stock price data.
* **Sentiment Features:** Incorporate the sentiment scores or probabilities obtained from FinBERT as additional features.
* **Time-Series Features:** Consider time-series features like time of day, day of week, and month of year.
* **External Factors:** If applicable, include external factors like economic indicators, interest rates, and geopolitical events.

**4. Model Selection and Training:**

* **Machine Learning Models:** Experiment with various machine learning models, including:
    * **Traditional Models:** Linear Regression, ARIMA, Random Forest
    * **Deep Learning Models:** LSTM, GRU, CNN
    * **Hybrid Models:** Combine techniques like LSTM-CNN or attention mechanisms.
* **Model Training:** Train the selected model(s) on the prepared dataset, using techniques like cross-validation to assess performance and prevent overfitting.

**5. Model Evaluation:**

* **Performance Metrics:** Evaluate the models using relevant metrics like Mean Squared Error (MSE), Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), and R-squared.
* **Backtesting:** Conduct backtesting to assess the models' performance on historical data.
* **Visualization:** Visualize the model predictions and compare them to actual stock prices to gain insights.

**Additional Considerations:**

* **Data Quality:** Ensure the quality and relevance of the data used for training and testing.
* **Feature Importance:** Identify the most influential features to understand the model's decision-making process.
* **Ensemble Methods:** Explore ensemble techniques like bagging and boosting to improve prediction accuracy.
* **Hyperparameter Tuning:** Optimize the hyperparameters of the models to achieve the best performance.
* **Regularization:** Employ regularization techniques (e.g., L1, L2) to prevent overfitting.
* **Ethical Considerations:** Be aware of the ethical implications of using AI for financial predictions, especially regarding potential biases and market manipulation.

By following these steps and leveraging the power of FinBERT, you can develop a robust and accurate stock prediction model.
 
**Would you like to delve deeper into any specific aspect of this methodology?**
