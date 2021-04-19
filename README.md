# EndSars_Twitter_analysis

The #EndSARS movement appears to be one of the most powerful movements in Africa over the last two decades. In this analysis, I seek to quantify the impact and provide data-informed answers to some questions.

### Methodology

* Data gathering
* Data cleaning
* Data analysis
* Sentiment analysis

## Data gathering

* Data was collected using the official Twitter API.
* Keywords relevant to the movement were passed in as query parameters.
* The time period of data collected was Jan. 2020 to Feb. 2021

## Sentiment analysis

**Approach:**
Three models used
* Vader lexicon: uses a lexicon based approach
* Textblob: uses a rule based approach
* FastText: Supervised learning. Model was trained on tweets that do not necessarily represent the context of our data. (Precision and recall on validation set was about 0.8)

*Challenge: Difficulty is getting labelled dataset with similar context to train on.*

**Outcome:**
* Sentiments varied across the three models.
* FastText seemed to generalize on the dataset best.
* Positive sentiments mostly constitute tweets in favor of the movement, jokes, adverts.
* Negative sentiments were mostly captured by tweets expressing anger towards SARS and the government. Some adverts and jokes were also classified as negative sentiment.
* Many false negatives and false positives were captured by all three models. 

## Next steps

* Improve on the existing model with hyper-parameter tuning.
* Calculate sentiment with respect to top accounts.
* Calculate change in sentiment with respect to time.
* Perform network analysis.
* Deploy an interactive dashboard where visitors can get insights about the movement.
* Turn model into an API.


*Need the dataset? Happy to share. Reach me on tochiebby@gmail.com*
