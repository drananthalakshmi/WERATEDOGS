# #WeRateDogs Twitter Data Analysis
## Data Gathering
>* Tweets Data: Sourced from a csv file
>* Image Predictions Data: Sourced from an API
>* Tweet Stats: Sourced from Twitter API using Tweepy library

## Data Assessment

>### Quality issues

>#### df_enhanced_data
1. The name column has values starting with lowercase and has values like 'a', 'an', 'the' and there are 79 rows with name less than or equal to 2 characters

2. retweeted_status_timestamp, timestamp column is in object datatype, can be datetime

3. None values are present in name, doggo, floofer, pupper, puppo columns when should add to null count

4. in_reply_to_status_id, in_reply_to_user_id, retweeted_status_id, retweeted_status_user_id can be int like tweet_id. These are the tweets which are not original tweets

5. Rating numerator ranges to high tens and thousands which seems to be invalid

6. Rating denominator is zero for a value and also has some other invalid values than 10

7. HTML in source column and can also be a category

8. There are double links in exapnded_urls

>#### df_image_predictions

9. There are values in p1, p2, p3 which are not dogs like ice_bear, doormat, ibex, tub, etc., and the values are not in consistent case
10. The confidence and names can be grouped

>### Tidiness issues
1. The dataframes are of different lengths. 

2. The dataframes df_enhanced_data, df_image_predictions, df_public_metrics should be combined together

## Finally, data is cleaned for all the issues stored and visualized.