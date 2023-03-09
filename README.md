# Stats 201 Final Project -- Sentiment Analysis and Topic Modeling Using Machine Learning

## Project information
- **Author**: Colden Johnson, Political Economy and Data Science, Class of 2026, Duke Kunshan University
- **Instructor**: Prof. Luyao Zhang, Duke Kunshan University
- **Disclaimer**: Submissions to the Final Problem Set for STATS201 Introduction to Machine Learning for Social Science, 2022 Autumn Term (Seven Week - Second) instructed by Prof. Luyao Zhang at Duke Kunshan University.
- **Acknowledgments**: I am very greatful to professor Luyao Zhang for her helpful instruction in class, as well as to Michael Cornell for his helpful comments and suggestions throughout the peer review process.
- **Project Summary**: As one of the largest social media platforms, Twitter can be used as one barometer of public sentiment. In this project, I explore the impact of Trump's actions on Twitter discourse through sentiment analysis and topic modeling using machine learning. Twitter data containing the keyword 'Trump' was queried between the years of 2020 and 2022. The data was preprocessed before applying supervised machine learning sentiment analysis, including the ROBERTA sentiment analysis AI. All Tweets were classified into one of three categories, 'positive', 'negative', and 'neutral'. Results were visualized as timeseries data by grouping average tweet sentiment by day and hour. Linear regression was also used to identify 2 major events of interest during this time period (fig. 5) Causal inference machine learning techniques were used to find a strong causal effect from specified events (including Trump's actions during the capitol riots on Jan. 6 and Trump's Jan. 20 Concession Speech). However, due to the complex nature of events and limited dimensionality of the data, this machine learning technique has limited effectiveness in the face of confounding variables. In general, Twitter sentiment reached its lowest during the capitol riots, and thereafter climbed to its absolute maximum when Trump conceded defeat in the election. I also performed unsupervised machine learning techniques including topic modeling, identifying several common topic clusters during the studied timeframe. Common topics of discourse can be grouped in the categories: discussion about implications of the election, debate over vote validity, and Tweets broadly referencing the 'wants' and 'needs' of the American people. This research helps contribute to understanding how Donald Trump's actions were perceived by the American public, providing a more complete picture of events during this important time period. It is also worth noting that Trump's Twitter ban had little impact on Tweet volume, topic, or sentiment, and was largely overwhelemed by other topics. This has implications when attempting to understand the limited impact of social media bans on public discourse. In the future, the research scope can be expanded to include a variety of public figures, in order to create a more generalizable predictive model for how Twitter discourse takes shape.

## Table Of Contents
| Contents | Description |
|--------|--------|
| [Data](https://github.com/Rising-Stars-by-Sunshine/ColdenJohnson-stats201-Final-Project/blob/main/README.md#Data) | View Raw and Processed Data Files |
| [Code](https://github.com/Rising-Stars-by-Sunshine/ColdenJohnson-stats201-Final-Project/blob/main/README.md#Code) | View Jupyter Notebook Code Files |
| [Spotlight](https://github.com/Rising-Stars-by-Sunshine/ColdenJohnson-stats201-Final-Project/blob/main/README.md#Spotlight) | View Generated Spotlight Figures |
| [About the Author](https://github.com/Rising-Stars-by-Sunshine/ColdenJohnson-stats201-Final-Project/blob/main/README.md#more-about-the-author) | Read Author Bio and Project Background |
| [References](https://github.com/Rising-Stars-by-Sunshine/ColdenJohnson-stats201-Final-Project/blob/main/README.md#References) | View Refereces CSV File |



## Data
### Meta Data Information
| Contents | Data Type |
|--------|--------|
| [Queried Data](https://github.com/Rising-Stars-by-Sunshine/ColdenJohnson-stats201-Final-Project/blob/main/data/Queried_Data/Trump_Twitter_CausalityTimePeriod.csv)|CSV File|
| [Clipped Data (Preliminary Analysis)](https://github.com/Rising-Stars-by-Sunshine/ColdenJohnson-stats201-Final-Project/blob/main/data/Queried_Data/Final_Project_ExpandedCausalityTimePeriod.csv) |CSV File|
| [Final Data](https://github.com/Rising-Stars-by-Sunshine/ColdenJohnson-stats201-Final-Project/blob/main/data/Queried_Data/Final_Project_ExpandedCausalityTimePeriod.csv) |CSV File|

Retreived using snscrape library. Documentation [available](https://github.com/JustAnotherArchivist/snscrape)
### Data Dictionary

| File Name  | Variable Name | Description | Unit | Type |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| [literature.csv]()  | Tweet_number  | Unique Identifier Assigned to each Tweet during scraping (using for loop) | None | int |
|   | rawContent  | Tweet Raw Content Text Abstract | None | str |
|   | timestamp  | Datetime object of tweet timestamp | unit time  | DATETIME |
|   | ID  | Twitter generated unique identifier | None  | int |
|   | replyCount  | Total replies to Tweet | # of occurences | int |
|   | retweetCount  | Total retweets of Tweet | # of occurences  | int |
|   | likeCount  | Total likes of Tweet | # of occurences  | int |

## Code
- Final Project
[Jupyter Notebook Process Data](https://github.com/Rising-Stars-by-Sunshine/ColdenJohnson-stats201-Final-Project/blob/main/code/Final_Project_TwitterData%20(1).ipynb)
[Jupyter Notebook Analyze Data](https://github.com/Rising-Stars-by-Sunshine/ColdenJohnson-stats201-Final-Project/blob/main/code/Final_Project_TwitterData%20(1).ipynb)

- Prior Exploratory Work: Problem Sets 1 and 2
[Jupyter Notebook Process Data PS2](https://github.com/Rising-Stars-by-Sunshine/stats201-prediction-Colden/blob/main/code/Colden_Johnson_Process_Data_Prepare_X_and_Y_for_Classification_and_Regressions.ipynb)
[Jupyter Notebook Analysis PS2](https://github.com/Rising-Stars-by-Sunshine/stats201-prediction-Colden/blob/main/code/Colden_Johnson_Data_Machine_Learning_for_Predicting_Tweet_Reach.ipynb)
[Jupyter Notebook PS1](https://github.com/Rising-Stars-by-Sunshine/stats201-PS1-ColdenJohnson/blob/main/code/Problem%20Set%201.ipynb)

## Spotlight
- Poster

- Figures
![Sentiment_PieChart](https://user-images.githubusercontent.com/118926209/223123994-7ef301c9-92d5-48d8-9b26-760f778fef38.png)

![Tweet_Volumes_By_Hour](https://user-images.githubusercontent.com/118926209/223124393-650d8c6e-054a-45b0-9b7b-5c4ca911bbd8.png)

![Tweet_Volume](https://user-images.githubusercontent.com/118926209/223124431-c8fc638c-ebfe-41bb-984e-b695643b9865.png)

![Average_Sentiment_By_Day](https://user-images.githubusercontent.com/118926209/223124480-e5298f4f-d8f5-4971-af3b-48f35d75a703.png)

![Tweet_Sentiment_LineGraph](https://user-images.githubusercontent.com/118926209/223124584-fd1c531e-c3f3-4b82-a583-94f4ce1f0cab.png)

![WordCloud](https://user-images.githubusercontent.com/118926209/223124608-0b95b5ac-16bd-4679-be0c-d191d05df227.png)

## More About the Author


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


