Gathering Data
About the dataset - WeRateDogs
This data set is taken from Twitter account name WeRateDogs. WeRateDogs rates dogs and provides humorous comments It contains 2356 tweet data from 2015 to 2017.

There are 2 datasets named :
twitter-archive-enhanced.csv - contains tweet informations 
image_prediction.tsv - contains image predictions of the tweets

twitter-archive-enhanced.csv is downloaded from link provided by Udacity.

image_prediction.tsv is downloaded using the request library from the URL 

Tweet data is accessed via Twitter API and stored in tweet_json.txt

Accessing and Analyzing Data
Data is loaded into the dataframe to analyze the quality and tidiness issues . 
We can see below : 
Quality issues

'timestamp' does not have correct data type
Null in doggo , floofer , pupper and puppo is represented with None
Some 'names' are None instead of Null
Rating numerator is greater than the denominator
'rating_denominator' has value other than 10 also
text column has encoded data ,eg '&amp' for tweet_id = 758854675097526272
Some records donot have stage specified , for eg tweet_id = 758854675097526272
Some records have url and ranking mentioned in text column itself , for eg tweet_id 696886256886657024 and 715704790270025728
The source of some records are other than tweeter , for eg tweet_id=696886256886657024 or 715704790270025728
Retweet information is also present in dataframe of twitter-archive-enhanced.csv
'rating_denominator' has value zero

Tidiness issues 

The columns 'doggo', 'floofer', 'pupper','puppo' should be one variable in dataset df 
The columns 'rating_numerator' and 'rating_denominator' could be part of one variable
Cleaning Data
Rows having retweet information is removed
After removing the rows , retweet related columns are removed
Row having 'rating_denominator' as zero is removed
timestamp is converted to date time
Stage of dog is stored in 4 different columns , these columns are removed and one column named dogStage stores this data
Storing data 
After cleaning data is stored in twitter_archive_master.csv
