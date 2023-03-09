# Stats 201 Final Project -- Sentiment Analysis and Topic Modeling Using Machine Learning

## Project information
- **Author**: Colden Johnson, Political Economy and Data Science, Class of 2026, Duke Kunshan University
- **Instructor**: Prof. Luyao Zhang, Duke Kunshan University
- **Disclaimer**: Submissions to the Final Problem Set for STATS201 Introduction to Machine Learning for Social Science, 2022 Autumn Term (Seven Week - Second) instructed by Prof. Luyao Zhang at Duke Kunshan University.
- **Acknowledgments**: I am very greatful to professor Luyao Zhang for her great instruction in class, as well as to Michael Cornell for his helpful comments and suggestions throughout the peer review process.
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
| Contents | File Type |
|--------|--------|
| [Queried Data](https://github.com/Rising-Stars-by-Sunshine/ColdenJohnson-stats201-Final-Project/blob/main/data/Queried_Data/Trump_Twitter_CausalityTimePeriod.csv)|CSV File|
| [Clipped Data (Preliminary Analysis)](https://github.com/Rising-Stars-by-Sunshine/ColdenJohnson-stats201-Final-Project/blob/main/data/Queried_Data/Final_Project_ExpandedCausalityTimePeriod.csv) |CSV File|
| [Final Data](https://github.com/Rising-Stars-by-Sunshine/ColdenJohnson-stats201-Final-Project/blob/main/data/Queried_Data/Final_Project_ExpandedCausalityTimePeriod.csv) |CSV File|

Retreived using snscrape library. Documentation [available](https://github.com/JustAnotherArchivist/snscrape)
### Data Overview
| File Name  | Variable Name | Description | Unit | Type |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| [Trump_Twitter_CausalityTimePeriod.csv](https://github.com/Rising-Stars-by-Sunshine/ColdenJohnson-stats201-Final-Project/blob/main/data/Queried_Data/clipped_trump_data_2018.csv)  | Tweet_number  | Unique Identifier Assigned to each Tweet during scraping (using for loop) | None | int |
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
![Stats201_FinalPoster](https://user-images.githubusercontent.com/118926209/224045116-262038cd-102e-4c40-93b0-50fe786f1ef6.png)

- Figures

![Sentiment_PieChart](https://user-images.githubusercontent.com/118926209/223123994-7ef301c9-92d5-48d8-9b26-760f778fef38.png)

**Fig. 1**: Piechart showing sentiment distribution over the entire queried timespan. Tweet sentiment is overwhelmingly negative, with less than 6% being labelled as positive. This is not necessarily surprising, as negativity has been shown to be more common on Twitter than positive Tweets. However, negative Tweets are on average only about 15% more prevalent than positive (Goldenberg et. al). Therefore, this result shows a substantially more negative public opinion than would usually be expected on sentiment analysis of this type.

![Tweet_Volumes_By_Hour](https://user-images.githubusercontent.com/118926209/223124393-650d8c6e-054a-45b0-9b7b-5c4ca911bbd8.png)

**Fig. 2**: Tweet volume of reply counts and retweet accounts, grouped by day. These two metrics closely track each other on both high and low days. The green vertical line indicates the date of the capitol riots, where there was a spike in activity. This activity remains elevated for the next several days, and another retweet spike can be seen on the day Trump's account was banned.

![Tweet_Volume](https://user-images.githubusercontent.com/118926209/223124431-c8fc638c-ebfe-41bb-984e-b695643b9865.png)

**Fig. 3**: Tweet volume over time. Tweet volume spikes during the capitol riots (Jan. 6) and remains elevated for several days.

![Average_Sentiment_By_Day](https://user-images.githubusercontent.com/118926209/223124480-e5298f4f-d8f5-4971-af3b-48f35d75a703.png)

**Fig. 4**: Average tweet sentiment over time visualized in a stacked line chart. The lowest sustained negative opinion (indicating a substantial trend) can be seen on the 3 day period surrounding Jan. 6, and the all-time high public opinion appears on Jan. 20 (Trump's concession speech).

![Tweet_Sentiment_LineGraph](https://user-images.githubusercontent.com/118926209/223124584-fd1c531e-c3f3-4b82-a583-94f4ce1f0cab.png)

**Fig. 5**: Graphed visualization of average Tweet sentiment over time, on a scale from -1.0 to + 1.0. The first two vertical lines (local min and local max) mark the passage of a covid relief package through congress. The sentiment around these two lines correctly tracks the predicted sentiment as recorded by polls, giving validity to the metric as a general barometer of public opinion. The green line (Jan. 6) indicates the capitol riots, and marks the 3-day lowest sustained negative public opinion during the queried timespan. The yellow line (Jan. 20) marks Trump's concession speech, in which he committed to peacefully transferring power, and is the absolute maximimum for public sentiment.


![WordCloud](https://user-images.githubusercontent.com/118926209/223124608-0b95b5ac-16bd-4679-be0c-d191d05df227.png)

**Fig. 6**: Word cloud of all scraped text data over the timespan, after removing stopwords.

## More About the Author
![SeniorPhoto_JohnsonColden - Copy](https://user-images.githubusercontent.com/118926209/224054174-bac3c0b5-1883-4863-b1fd-09365b2f8574.jpg)


Colden Johnson is a freshman at Duke Kunshan University. He is interested in majoring either in political economy or data science, and is interested in studying at the intersection of these two fields. He has experience working with a variety of programming languages, including R, Python, and Java.

## Final Reflections

This course has helped me understand the broad utility of machine learning, and helped train me to use a wide variety of techniques as they apply to each problem type. Prior to taking this course, I had a basic understanding of machine learning concepts and coding applications. However, this course has broadened my knowledge and skills in the field significantly. I specifically learned about machine learning applications in blockchain and Twitter, and completing my final project offered many problem solving opportunities. For my professional growth, I am hopeful that this class will help me continue conducting meaningful and practically interesting research. Broadly applicable skills, such as proficiency using Google Collab and Github, will also be valuable in my future career. In the future, I want to conduct research in the field of 'computational humanities', and continue employing the same text-based machine learning techniques (sentiment analysis and topic clustering) as I used in my final project. The application of machine learning techniques to the humanities is not only pioneering, but also a valuable research contribution which I would like to bring greater attention to in the future.

## A Special Note on Peer Evaluations

Thank you again to Michael Cornell for the great discussions we had during the peer evaluation process. I would specifically like to thank him for several of the suggestions he gave on my final analysis. First, I have introduced a more complete causal analysis surrounding the Jan. 6 capitol riots, with greater validity, thanks to his comments. I have also been able to run my analysis on much larger data thanks to his suggestion to use a virtual machine. Finally, I have reworked many of my figures and graphs to be more simplistic and coherent to a general audience.

## References
### Articles
 Abdullah, Malak, and Mirsad Hadzikadic. “Sentiment Analysis of Twitter Data: Emotions Revealed Regarding Donald Trump during the 2015-16 Primary Debates.” In 2017 IEEE 29th International Conference on Tools with Artificial Intelligence (ICTAI), 760–64, 2017. https://doi.org/10.1109/ICTAI.2017.00120.

  Andersen, Torben G., Tim Bollerslev, Francis X. Diebold, and Paul Labys. “Modeling and Forecasting Realized Volatility.” Econometrica 71, no. 2 (March 2003): 579–625. https://doi.org/10.1111/1468-0262.00418.
  
  Bollen, Johan, Huina Mao, and Xiaojun Zeng. “Twitter Mood Predicts the Stock Market.” Journal of Computational Science 2, no. 1 (March 1, 2011): 1–8. https://doi.org/10.1016/j.jocs.2010.12.007.
  
  Elbagir, Shihab, and Jing Yang. “Twitter Sentiment Analysis Using Natural Language Toolkit and VADER Sentiment.” Hong Kong, 2019.
  
  Giachanou, Anastasia, and Fabio Crestani. “Like It or Not: A Survey of Twitter Sentiment Analysis Methods.” ACM Computing Surveys 49, no. 2 (June 30, 2016): 28:1-28:41. https://doi.org/10.1145/2938640.
  
  Hong, Liangjie, and Brian D. Davison. “Empirical Study of Topic Modeling in Twitter.” In Proceedings of the First Workshop on Social Media Analytics, 80–88. SOMA ’10. New York, NY, USA: Association for Computing Machinery, 2010. https://doi.org/10.1145/1964858.1964870.

  Hu, Yuheng, Ajita John, Fei Wang, and Subbarao Kambhampati. “ET-LDA: Joint Topic Modeling for Aligning Events and Their Twitter Feedback.” Proceedings of the AAAI Conference on Artificial Intelligence 26, no. 1 (2012): 59–65. https://doi.org/10.1609/aaai.v26i1.8106.
  
  Jianqiang, Zhao, and Gui Xiaolin. “Comparison Research on Text Pre-Processing Methods on Twitter Sentiment Analysis.” IEEE Access 5 (2017): 2870–79. https://doi.org/10.1109/ACCESS.2017.2672677.
  
  “Journal of Medical Internet Research - Characterizing Twitter Discussions About HPV Vaccines Using Topic Modeling and Community Detection.” Accessed March 9, 2023. https://www.jmir.org/2016/8/e232/.
  
  Kayesh, Humayun, Md Saiful Islam, and Junhu Wang. “On Event Causality Detection in Tweets.” arXiv, January 11, 2019. https://doi.org/10.48550/arXiv.1901.03526.
  
  Liu, Yinhan, Myle Ott, Naman Goyal, Jingfei Du, Mandar Joshi, Danqi Chen, Omer Levy, Mike Lewis, Luke Zettlemoyer, and Veselin Stoyanov. “RoBERTa: A Robustly Optimized BERT Pretraining Approach.” arXiv, July 26, 2019. https://doi.org/10.48550/arXiv.1907.11692.
  
  Poth, Clifton, Jonas Pfeiffer, Andreas Rücklé, and Iryna Gurevych. “What to Pre-Train on? Efficient Intermediate Task Selection.” arXiv, September 10, 2021. http://arxiv.org/abs/2104.08247.
  
  Ramteke, Jyoti, Samarth Shah, Darshan Godhia, and Aadil Shaikh. “Election Result Prediction Using Twitter Sentiment Analysis.” In 2016 International Conference on Inventive Computation Technologies (ICICT), 1:1–5, 2016. https://doi.org/10.1109/INVENTIVE.2016.7823280.
  
  Resnik, Philip, William Armstrong, Leonardo Claudino, Thang Nguyen, Viet-An Nguyen, and Jordan Boyd-Graber. “Beyond LDA: Exploring Supervised Topic Modeling for Depression-Related Language in Twitter.” In Proceedings of the 2nd Workshop on Computational Linguistics and Clinical Psychology: From Linguistic Signal to Clinical Reality, 99–107. Denver, Colorado: Association for Computational Linguistics, 2015. https://doi.org/10.3115/v1/W15-1212.

  Sahu, Kalyan, Yu Bai, and Yoonsuk Choi. “Supervised Sentiment Analysis of Twitter Handle of President Trump with Data Visualization Technique.” In 2020 10th Annual Computing and Communication Workshop and Conference (CCWC), 0640–46, 2020. https://doi.org/10.1109/CCWC47524.2020.9031237.
  
  Schoen, Harald, Daniel Gayo-Avello, Panagiotis Takis Metaxas, Eni Mustafaraj, Markus Strohmaier, and Peter Gloor. “The Power of Prediction with Social Media.” Edited by Daniel Gayo-Avello, Panagiotis Takis Metax. Internet Research 23, no. 5 (October 14, 2013): 528–43. https://doi.org/10.1108/IntR-06-2013-0115.
  
  Schöne, Jonas Paul, Brian Parkinson, and Amit Goldenberg. “Negativity Spreads More than Positivity on Twitter After Both Positive and Negative Political Situations.” Affective Science 2, no. 4 (December 1, 2021): 379–90. https://doi.org/10.1007/s42761-021-00057-7.
  
  Severyn, Aliaksei, and Alessandro Moschitti. “Twitter Sentiment Analysis with Deep Convolutional Neural Networks.” In Proceedings of the 38th International ACM SIGIR Conference on Research and Development in Information Retrieval, 959–62. SIGIR ’15. New York, NY, USA: Association for Computing Machinery, 2015. https://doi.org/10.1145/2766462.2767830.
  
  Somula, Ramasubbareddy, K. Dinesh Kumar, S. Aravindharamanan, and K. Govinda. “Twitter Sentiment Analysis Based on US Presidential Election 2016.” In Smart Intelligent Computing and Applications, edited by Suresh Chandra Satapathy, Vikrant Bhateja, J. R. Mohanty, and Siba K. Udgata, 363–73. Smart Innovation, Systems and Technologies. Singapore: Springer, 2020. https://doi.org/10.1007/978-981-13-9282-5_34.

  
