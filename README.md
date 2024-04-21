## Sentiment Analysis of NBA Fans

### Abstract
This project investigates the sentiment of NBA fans through the analysis of social media data. Fans of sports teams are incredibly passionate, and their emotions can swing many times throughout a game, especially during a season. Each NBA subreddit has between 20,000 and 141,000 subscribers, so these forums are places where many fans are voicing their opinions. By collecting a dataset of fan content, this project aims to quantify the sentiments and trends in the aspects of the NBA. This project explores how sentiments vary across teams, and how it compares the sentiment to results and other statistics in the league. The findings show insights into the landscape of the NBA, and if the reactions of the fans are accurate. Passion from the fans can lead to more tickets and merch sales, which can lead to positive outcomes of the franchise, so this information could be key for front offices. 

### Data
The main source of data used in the current project was the Reddit API, specifically the Python Reddit API Wrapper. This package allows access to subreddits, including the posts and comments. 
<img width="649" alt="Screenshot 2024-04-21 at 1 33 00 PM" src="https://github.com/vivekdivakarla12/NBA-Sentiment-Analysis/assets/11672096/d0722190-6663-498e-9a9f-b1eafdf5e1a2">
This is an example of the last 15 reddit posts from the Cleveland Cavaliers subreddit, showing the titles. There are a variety of different topics shown, from coaches to game recaps to jokes about the team. Since there are many different types of conversations being held in the team subreddits, it will be interesting to see if there is a correlation between the sentiment and the team results. 
### Methods
After retrieving data for all thirty teams, the main method was to utilize the SentimentIntensityAnalyzer from vaderSentiment. For each comment, I calculated the polarity scores, and for each team, I created a happiness index to which calculates the average sentiment score over the posts from the team's subreddit. The second index was based on the most recent posts from each team's subreddit. Once the indexes were created for each team, I pulled different statistics as ways to categorize NBA teams, including Win%, Win% last 10 games, Total Cap Space, and Wins Above Expected. After creating this dataframe, I utilized the df.corr to measure the correlation on each feature.
### Results
WordCloud of the Cavs Subreddit
<img width="394" alt="Screenshot 2024-04-21 at 1 34 56 PM" src="https://github.com/vivekdivakarla12/NBA-Sentiment-Analysis/assets/11672096/221934ab-c23e-48aa-995d-d757c3530cde">
Happiness Index of NBA teams
<img width="503" alt="Screenshot 2024-04-21 at 1 35 31 PM" src="https://github.com/vivekdivakarla12/NBA-Sentiment-Analysis/assets/11672096/b59e0056-60b2-4e3f-bb69-101ddbd60e4b">
Happiness Index of NBA teams, more recently weighted
<img width="497" alt="Screenshot 2024-04-21 at 1 38 57 PM" src="https://github.com/vivekdivakarla12/NBA-Sentiment-Analysis/assets/11672096/8822e34c-8431-48a7-90dd-e500b6368441">
Correlation between features and Happiness Index
<img width="401" alt="Screenshot 2024-04-21 at 1 36 49 PM" src="https://github.com/vivekdivakarla12/NBA-Sentiment-Analysis/assets/11672096/9d49f29f-653d-4abb-9756-e6383b81804f">
Correlation between features and Happiness Index, more recently weighted
<img width="508" alt="Screenshot 2024-04-21 at 1 37 54 PM" src="https://github.com/vivekdivakarla12/NBA-Sentiment-Analysis/assets/11672096/8a8fcf95-34db-487e-8510-0017f6d13d07">

### Discussion
There are a lot of interesting insights between the features and the happiness indexes that are created. For the first index, which was done based on the whole season, the most important features were Wins vs Expected and Average Attendance. Expectations are a very crucial aspect that should be taken into account, as fans with low expectations will not be as mad compared to teams who underperformed. Attendance is also a factor, as fans who are happier will be more likely to attend games. The second index was based on more recent posts, so it was intriguing to explore how the correlations changed. Total Cap, which is money spent on players, becomes the highest correlation, followed by Win% over the team’s last 10 games. This is a smaller sample size, so the data may be skewed in these results. It is around playoff time, so the happier teams are the ones in the playoffs, who are typically the ones who spend more money on their players. 
One limitation of this data was that it was a smaller data set, and there were not any labels on the data. This made it difficult to utilize any machine learning models, and is the reason why I used the vaderSentiment. However, I still believe the results were insightful, and can bring value to NBA fans. 


