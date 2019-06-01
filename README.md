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
stored in 4 different columns , these columns are removed and one column named dogStage stores this data


Storing data 

After cleaning data is stored in twitter_archive_master.csv
