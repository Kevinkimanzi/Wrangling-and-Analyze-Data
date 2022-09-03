# Wrangling and Analyze Data

## Dataset

Directly download the WeRateDogs Twitter archive data (twitter_archive_enhanced.csv)

## Quality issues
##### twitter_archive_enhanced

1.There are many column with misssing value like In_reply_to_status_id, in_reply_to_user_id, retweeted_status_id, retweeted_status_user_id, retweeted_status_timestamp and expanded_urls

2.Erroneous data types - timestamp & retweeted_status_timestamp column(also needs to be split into two date and time); dog_stage column(should be categorical); tweet_id, in_reply_to_status_id, in_reply_to_user_id, retweeted_status_id, retweeted_status_user_id columns(should be str)

3.rating_numerator column has some exceptionally high values which leads to exceptionally high rating which can be inaccurate

4.Rating_denominator is other than assumed standard value of 10 at some places which can be Inaccurate data

5.Some names in the name column are invalid data like such, quite, a, an, the, none

6.name, doggo, floofer, pupper and puppo columns have value with the name None

7.some of expanded_urls rows has 2 url and we just need tweeter link

##### image_predictions

1.tweet_id should be "string" not "int"

2.names p columns have some upper letter and some lower letter

json_df

1.tweet id title is different, id here tweet_id in others. 2.tweet_id should be "string" not "int"

## Tidiness issues
1.doggo, floofer, pupper, and puppo should be in one column not 4

2.Change tweet_id to type int64 in order to merge with the other 2 tables

## cleaning data
1. Dropping all missing columns
2. Replacing NaNS with empty string for columns in doggo, floofer, pupper and puppo then combining it as one column
3. Tweet id title is different, id here tweet_id in others
4. Merge the tables json_df_clean and twitter_archive_enhanced_clean
5. Converting Erroneous data types to their right type

## Summary of Findings
1. Golden_Retriever is the most common blreed in this twitter archiver with 150 tweets followed by Labrador_retriever and Pembroke. respectively. cocker_spaniel had the least tweets followed by Pomeranian respectively

2.Pupper is the most popular Dog stage followed by doggo,puppo, multiple and the least is floofer.

3.Number of tweets decreases as months progresses.

