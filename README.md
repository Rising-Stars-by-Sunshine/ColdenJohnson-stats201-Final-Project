# Stats 201 Final Project

## Jupyter Notebook Files
[Jupyter Notebook Process Data](https://github.com/Rising-Stars-by-Sunshine/stats201-prediction-Colden/blob/main/code/Colden_Johnson_Process_Data_Prepare_X_and_Y_for_Classification_and_Regressions.ipynb)

[Jupyter Notebook Analysis](https://github.com/Rising-Stars-by-Sunshine/stats201-prediction-Colden/blob/main/code/Colden_Johnson_Data_Machine_Learning_for_Predicting_Tweet_Reach.ipynb)

## Project information
- **Author**: Colden Johnson, Political Economy and Data Science, 2026, Duke Kunshan University
- **Instructor**: Prof. Luyao Zhang, Duke Kunshan University
- **Disclaimer**: Submissions to the Problem Set 2 for STATS201 Introduction to Machine Learning for Social Science, 2022 Autumn Term (Seven Week - Second) instructed by Prof. Luyao Zhang at Duke Kunshan University.
- **Acknowledgments**: Thank you to Luyao Zhang for her helpful instruction in class, as well as to Michael Cornell for his help in setting up my virtual machine for this project.
- **Project Summary**: As one of the largest social media platforms, Twitter can be used as one barometer of public sentiment. In this project, I attempt to predict tweet sentiment as a function of total retweets. Twitter data containing the keyword 'Trump' was queried between the years of 2018 and 2023, and a random segment was chosen to run preliminary analysis on. The tweets text was cleaned (including removal of URLs and nonstandard characters) before applying sentiment analysis. All Tweets were classified into one of three categories, 'positive', 'negative', and 'neutral'. A variety of comparative machine learning algorithms were employed on the data to attempt to generate an accurate predictive model (Fig. 3, Fig. 4). The best model performs at a little above 47% accuracy. However, since Tweets were classified into three categories, this is higher than would be expected by random chance (33%). While the model is not currently refined enough to effectively predict Tweet sentiment outside of this testing environment, this project does help inform future research. It is likely that including more variables in the model will refine predictions, resulting in a much higher success rate. For subsequent research, I plan to add the variables 'total likes', 'total views', and additional text-based information, such as 'tweet length'. Additionally, I will attempt to run a larger dateset to further refine the models.

## Quick Links
| Contents | Data Type |
|--------|--------|
| [Data](https://github.com/Rising-Stars-by-Sunshine/stats201-prediction-Colden/blob/main/data/Queried_Data/scraped_data_trump_2018.csv)|CSV File|
| [Code Analyze Data](https://github.com/Rising-Stars-by-Sunshine/stats201-prediction-Colden/blob/main/code/Colden_Johnson_Data_Machine_Learning_for_Predicting_Tweet_Reach.ipynb) |Jupyter Notebook|
| [Code Process Data](https://github.com/Rising-Stars-by-Sunshine/stats201-prediction-Colden/blob/main/code/Colden_Johnson_Process_Data_Prepare_X_and_Y_for_Classification_and_Regressions.ipynb) |Jupyter Notebook|
| [Spotlight Figures](https://github.com/Rising-Stars-by-Sunshine/stats201-prediction-Colden/tree/main/spotlight) |Saved Figures (PNG)|



## Data
[Scraped Data 2018](https://github.com/Rising-Stars-by-Sunshine/stats201-prediction-Colden/blob/main/data/Queried_Data/scraped_data_trump_2018.csv)

Retreived using snscrape library. Documentation [available](https://github.com/JustAnotherArchivist/snscrape)

## Code
- Process Data
[Jupyter Notebook Process Data](https://github.com/Rising-Stars-by-Sunshine/stats201-prediction-Colden/blob/main/code/Colden_Johnson_Process_Data_Prepare_X_and_Y_for_Classification_and_Regressions.ipynb)

- Analyze Data
[Jupyter Notebook Analysis](https://github.com/Rising-Stars-by-Sunshine/stats201-prediction-Colden/blob/main/code/Colden_Johnson_Data_Machine_Learning_for_Predicting_Tweet_Reach.ipynb)

## Spotlight
- Figures
![WordCloud TrumpData](https://user-images.githubusercontent.com/118926209/220094960-cb03075d-5852-4249-a3c5-43ec2c0d1f7e.png)

Figure 1: wordcloud of words scraped from cleaned twitter raw content files.

![Tweet Analysis PieChart](https://user-images.githubusercontent.com/118926209/220094833-0b98c111-4fe3-42d8-a42a-695ff5b78eaf.png)

Figure 2: Tweet sentiment PieChart (before breaking into test and prediction datasets).

![ConfsuionMatrixFig 1](https://user-images.githubusercontent.com/118926209/220094985-5ef4d451-9386-456d-8c83-15083126fe66.png)

Figure 3: Confusion matrix for random forest classifier model. Note that this model is only slightly better than random chance, at 37% correct classifications.

![ConfusionMatrixFig 2](https://user-images.githubusercontent.com/118926209/220095008-b9ffe869-d3a4-438b-9a56-5127ed7a5656.png)

Figure 4: Confusion matrix for decision tree classifier model.

## References

### Data Source
- Data Source Title and URL
### Code Source
- Code Source Title and URL
### Articles
- Article Source Title and URL
### Literature
| Author | Title | Year |
|--------|-------|------|
| Bollen, Johan; Mao, Huina; Zeng, Xiaojun	 | Twitter mood predicts the stock market	 | 2011 |
| Ahmed, Ali Adnan Ahmed	 | Sentiment analysis for cryptocurrency prices prediction	 | 2020 |
| Salač, Adam	 | Forecasting of the cryptocurrency market through social media sentiment analysis	 | 2019 |


