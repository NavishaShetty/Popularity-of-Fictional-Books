# Popularity-of-Fictional-Books
The project is to analyse how information revelation affects the popularity of English-language fiction books

1.	Analyzing the role of information revelation in the popularity of English-language fiction books:

The analysis aimed to investigate the role of information revelation measured by KLD scores in the popularity of English-language fiction books. We used book-level measures of KLD, such as mean, variance, skewness, kurtosis, and slope and regressed against book downloads, alongside genre controls and additional variables like sentiment and word count and have drawn a few key insights as follows: 

The Regression analysis indicates that the slope of KLD scores and average sentiment scores are significant predictors of book downloads. 
•	A steeper slope is negatively associated with downloads, while higher average sentiment scores are positively associated. 
•	Variance in sentiment (sentiment volatility) also shows a significant positive relationship with downloads. 
•	The analysis suggests that genre and sentiment measures have some impacts on downloads, with certain genres like romance and horror, and sentiment volatility have higher downloads, while others like biography, history, other, and average sentiment have fewer downloads.

The LASSO regression further refines these findings by identifying the most predictive variables. 
•	The identified features highlight the importance of author-related characteristics, genre, sentiment, and book length in predicting book downloads.
•	Longer books might tend to be more popular, potentially due to offering more content to readers. 
•	The variable "authoryearofdeath" significantly decreases the number of downloads.
•	Variables such as "subj2_horror", "sentiment_vol", and "wordcount" positively influence the number of downloads.

In summary, the findings underscore the importance of narrative dynamics in driving reader engagement and book popularity. By quantifying information revelation through KLD scores, the study provides a novel way to understand reader preferences and suggests that authors and publishers can enhance a book's appeal by strategically managing the flow of information within the narrative.

2. Descriptions of Variables

1.	avg_kld: The average of the KLD scores for each book calculated by applying the np.mean function to the list of KLD scores for each book.

2.	var_kld: The variance of the KLD scores for each book calculated by using the np.var function on the KLD score lists.

3.	trend_kld: The trend of the KLD scores over the course of the narrative calculated as the difference between the last and first KLD values divided by the length of the list.

4.	slope: The slope of a linear regression line fitted to the KLD scores, representing another measure of the trend in KLD. Determined using LinearRegression from sklearn to fit a linear model to the KLD scores.

5.	kld_skew: The skewness of the KLD scores for each book. Constructed using the skew function from scipy.stats to measure the asymmetry of the distribution.

6.	kld_kurtosis: The kurtosis of the KLD scores for each book. Constructed using the kurtosis function from scipy.stats to measure the tailedness of the distribution.

7.	sentiment_avg: A control variable representing the average sentiment score of the book taken directly from the extra_controls.csv dataset.

8.	Wordcount: A control variable representing the total word count of the book taken directly from the extra_controls.csv dataset.

9.	Control 1: Example: subj2_war: A control variable representing the presence of "war" as a genre attribute of the book taken directly from the extra_controls.csv dataset.

10.	Control 2: Example: subj2_romance: A control variable representing the presence of "romance" as a genre attribute of the book taken directly from the extra_controls.csv dataset.
![image](https://github.com/user-attachments/assets/bf8bc503-fc7d-47e4-abff-f935e089cc4f)
