# Trump’s Vast Expansion of Child Detention

# What is this about?
This analysis is to depict the situation of child detentions across the US boarder, particularly during Trump's administration, and to interpret how general public view upon the issues.

# Why you are doing this?
With the interest in human right and politics, the situation of child detentions in the US during the Trump administration is a niche and interesting topic to explore. This analysis is to explain the implication of journalism and social media in politics.

# Description of the dataset and Questions of the analysis
There are 2 cleaned datasets, namely detention_clean.csv and reddit_clean.csv . 

## The first dataset -- "detention_clean.csv" 
  - is to analyse the children detained more than 72 hours by grouping them on the basis of nationality and age group.  

### Questions involved of the first dataset:
1. Find the average number of hours the children were detained over time (The proportion of the children who were detained more than 72 hours and less than 72 hours). 
2. By how many hours did the detention exceed the 72 hours limit on average? 
3. By how much did the detention barrier increase by, over the past four years? 
4. Could we find any trajectory for the total detentions over the limit against time? What 
    would have been the number of wrong detentions in America in Jan 2020 if this case 
    wouldn't have come into the limelight in May 2019?  
    
### Cleaning Process: 
This dataset contains the date every child been detained in and out, the hours of detention in the  U.S. Customs and Border Protection Border Patrol during mid-January of 2017 until late January of  2020 and U.S. Customs and Border Protection Office of Field Operations during mid-January of 2017  until mid-June of 2020. So, we deleted the unnecessary columns and only kept the date_in,  date_out, hours_in_custody, citizenship and age_group. We then calclulate the missing values of  date_in, date_out and hours_in_custody using either of the columns, we then removed the rows  where gender and age_group were not available and lastly removed the rows which contained  outliers in the column hours_in_custody. 


 

## The second one -- "reddit_clean.csv" is to Analyze the sentiment of the people based on a reddit post which was posted after the news.
 
### Questions involved of the second dataset: 
1. What are the most important keywords? 
2. What are the sentiments of Redditors on this issues?

### Cleaning Process: 
The purpose of the second dataset is to understand of public sentiment on this issue using Natural  language processing. Therefore, we scrapped the data from Reddit, which is one of the biggest  online forums. The dataset has 18 variables, only 5 of which are needed, namely comment id,  comment date, user, comment score, comments. All values are not NA except the variable of  “post_text”. “comments” is the most important variable which is divided into uni-gram. After  removing the stopwords, every word is attached with lexicons of “AFINN”, “Bing”, and “Nrc”. It is  then found that lots of the values are of no emotion, thus removing them. 
