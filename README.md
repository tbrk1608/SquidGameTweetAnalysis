## Squid Game Netflix Tweet Analysis:

**Overview:**<br>
Squid Game, a South Korean survival drama television series, based on six games and a princely sum is awarded to the winner. The show became the most-watched show in September 2021 on Netflix. The series is about 456 players playing deadly games, all of whom are in deep financial debt. The players risk their lives to play children's games to win a prize of about 45.6 billion. 
There are numerous tweets and reactions related to the most trending show, some viewers in support of the show, a few against the show, saying it is overhyped.
This project uses the Squid Game tweets of one month to perform sentiment analysis and build a prediction model

**EDA**<br>
Episode 1, which had the highest mentions, followed by episodes 9 and 6. Similarly, out of the 456 players in the game, Player 001 and 456 have the highest tweets mentioned followed by player 067 and player 199. 

![EDA](https://github.com/tbrk1608/SquidGameTweetAnalysis/blob/main/viz/0.png?raw=true)


**Lecixon Sentiment Analysis:**<br>
Used two different lexicon-based approaches for sentiment analysis. TextBlob and VADER. Textblob in general is the most used library for analyzing text sentiment, whereas VADER is specifically designed to further understand the comments on social media platforms. VADER gives more weightage to words that are entirely upper case, highlighting the importance of the word in predicting the sentiment. As expected VADER gave us better results in classifying the tweets.

![Lex1](https://github.com/tbrk1608/SquidGameTweetAnalysis/blob/main/viz/1.png?raw=true)

![Lex2](https://github.com/tbrk1608/SquidGameTweetAnalysis/blob/main/viz/2.png?raw=true)

**Prediction Models:**<br>
Built a Classification model for Sentiment analysis. Used the output form lexicon analysis (only the positive and negative sentiments) and generated tf-idf vectors. 
The dimensions of tf-idf vectors are reduced from 20000 to 8000 features explaining 95% variance of the data. The reduced vectors are then used to train the prediction models - Random Forests and SVM algorithms. SVM gave better results compared to that of Random Forests with an accuracy of 92%, while with RF the accuracy was nearly 75%.

![Res](https://github.com/tbrk1608/SquidGameTweetAnalysis/blob/main/viz/3.png?raw=true)
