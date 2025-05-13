# Dissertation
*"It's that time of the degree"*

# To-do
- [x] Finish literature review
- [x] Finish methodology
- [x] Practice finBERT model
- [ ] Write Discussion of Results

## Important Structure

*  Restate the main result
*  Compare it to the literature
*  Explain differences between results and previous researchers' results (maltese papers can work well for this)
*  Interpret findings to explain the main takeaway message

## Things to Keep in Mind

*  Explain why I many have got certain results
*  Do my findings support my hypothesis?
*  Address limitations (data collection, sample size, methodology)
*  What should I recommend for future work?
-----
## Quick Guide

| Section                                                             | Description                                                                              | Estimated Words |
| ------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | --------------- |
| 1. Introduction                                                     | Brief restatement of aims, methodology, and structure of discussion                      | 200–300         |
| 2. Key Findings (with and without sentiment, per model, per source) | Detailed analysis of all your results (MAE, R², test loss), supported by literature      | 1,200–1,500     |
| 3. Comparison with Previous Studies                                 | Explain how your findings align or differ from literature (e.g., Sousa, Sigodi, Pirotta) | 800–1,000       |
| 4. Cross-Validation Analysis                                        | Deep dive into time-series CV results and why they differ                                | 500–700         |
| 5. Source Comparison (Malta Independent vs. Malta Business Weekly)  | Discuss publication frequency, article style, and impact on sentiment accuracy           | 300–500         |
| 6. Critical Evaluation of Methods                                   | Reflect on FinBERT, model selection, overfitting, data quality, sentiment accuracy       | 300–400         |
| 7. Limitations and Implications                                     | Talk about computational issues, FinBERT’s limitations, etc.                             | 200–300         |
| 8. Recommendations & Future Work                                    | Suggest model refinements, more data, other sources (e.g. social media), new metrics     | 200–300         |
| 9. Conclusion                                                       | Final synthesis of findings, contribution to knowledge                                   | 150–200         |
----
## How to Expand 2–3 Bullet Points into 500+ Words

#### 🔹 Take Each Metric Seriously
Don’t just say “MAE dropped by X” — explore:

- Why it dropped  
- What it means in real-world terms  
- How it compares to similar studies  
- Whether it was expected  
- How sentiment specifically helped  

> “The drop in MAE from 31.6 to 14.8 in the LSTM model with sentiment represents not only a substantial numerical improvement but also reflects a stronger ability of the model to capture short-term market movement patterns. This echoes findings by Sousa, who found a similar trend when incorporating financial sentiment using FinBERT…”

#### 🔹 Quote and Evaluate Previous Studies
Quote their findings and critically engage:

- Do your results confirm, contradict, or add nuance?  
- Did you replicate their method but get a different result?  
- Were your models more complex? Your data smaller?

> “While Pirotta achieved a relatively modest 62.09% accuracy using TextBlob and VADER, this study demonstrates that FinBERT can achieve significantly lower error rates on a much smaller dataset. This suggests that domain-specific NLP models may outperform general-purpose ones even when data volume is limited.”

#### 🔹 Evaluate the Models Themselves
Go model-by-model and do a performance and design reflection:

- Was LSTM more stable?  
- Did CNN do better with short-term shifts?  
- Did the hybrid overfit or generalize poorly?

> “Despite being the most complex, the CNN-LSTM model did not always outperform simpler architectures. In fact, the hybrid model exhibited reduced accuracy when sentiment was included. This contrasts with assumptions in previous research that hybrid models provide a balanced strength of temporal and spatial learning…”

#### 🔹 Time Series Cross-Validation: A Whole Section
This part underperformed. Unpack that:

- Talk about why traditional splits and time-series behave differently  
- Discuss non-stationarity, data sparsity, sentiment delays, etc.  
- Discuss the risk of overfitting vs. underfitting  
----
## Discussion Structure Guide

#### 1. Restate the Purpose Briefly
Begin with a short reminder of your study’s aim:

> “This study aimed to evaluate the impact of sentiment analysis on stock price prediction using FinBERT and deep learning models applied to Maltese financial news.”

---

#### 2. Key Findings and Their Interpretation

##### A. Impact of Sentiment on Predictive Accuracy
> “Across both datasets and multiple models, incorporating sentiment data consistently improved predictive accuracy under the 80:20 split. For instance, the LSTM model on the Malta Independent dataset showed a notable drop in MAE from 31.61 to 14.83 and a rise in R² from 0.85 to 0.95. This aligns with Sousa’s findings, where FinBERT improved stock prediction accuracy, and with Pirotta’s recommendation to use ensemble or deep models with sentiment input.”

**This shows:**
- Your results support claims by Sousa and Sigodi (re: FinBERT’s strength).
- Your use of domain-specific sentiment (FinBERT) had measurable value.

##### B. Model Comparison
> “Among the tested models, the LSTM-CNN hybrid generally produced the lowest errors. However, when sentiment was included, its performance sometimes declined. This suggests potential model overfitting or challenges in integrating FinBERT-derived features into convolutional architectures—echoing Shobayo’s concerns about computational load and model complexity when using FinBERT.”

**This shows:**
- Hybrid models had benefits (as expected in the literature).
- But they also experienced unexpected declines — possibly due to FinBERT’s computational weight, as discussed by Shobayo.

##### C. Differences Between News Sources
> “Malta Independent produced better predictive outcomes than Malta Business Weekly. This may be due to its more frequent publication, which offered more sentiment signals. This supports Grech’s observation that high-frequency, slang-heavy social media data can affect sentiment models, suggesting a similar dynamic may apply to high-frequency news vs. sparse reports.”

**This shows:**
- Frequency and style of news matter.
- More frequent signals → better performance.

---

#### 3. Performance Under Time-Series Cross-Validation
> “In contrast, results under rolling time-series validation were significantly weaker, with most models yielding negative R² scores. This divergence indicates limited generalizability, potentially due to shifts in the sentiment-price relationship over time, sparse data, or limited market reactivity in the Maltese index. Hanna and Pirotta both noted that sentiment is only one of many market drivers, and this result reinforces the need to account for broader economic context.”

**This shows:**
- Sentiment helps in static 80/20 splits, but struggles with temporal splits.
- Volatility, event-driven noise, or dataset size may explain the decline.

---

#### 4. Limitations
Be transparent:

- Small dataset (only Maltese news)
- Sentiment scoring may miss nuance/sarcasm (as Grech noted about slang)
- Models might overfit due to limited data

---

#### 5. Implications and Future Work
> “The results suggest that financial sentiment analysis can significantly improve stock price forecasting for small markets like Malta when applied correctly. However, performance varies by model architecture and data volume. Future research should explore more robust models like RoBERTa or FinBERT-light and expand datasets to include international news and social media sentiment.”

**Wrap-up takeaways:**
- FinBERT has measurable value but clear limits.
- Improvements can come from larger datasets, better temporal handling, o
