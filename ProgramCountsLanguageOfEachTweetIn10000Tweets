'''
HW8
CIS 2532 NET01
Dr. Shamsuddin
Kostas Spyropoulos
Program counts the languages of 10,000 tweets
04/11/2022
Exercise 13.1
'''
import tweepy
import keys
from random_word import RandomWords
auth = tweepy.OAuthHandler(keys.consumer_key, keys.consumer_secret)
auth.set_access_token(keys.access_token, keys.access_token_secret)
api = tweepy.API(auth, wait_on_rate_limit=True, wait_on_rate_limit_notify=True)


# Exercise 13.1 


# dictionary containing language types as keys and amounts of tweets per language as values
countTweets = {}

# count counts amount of total tweets
count = 0

# for loop that counts the number of tweets per language in 10000 tweets
for iteration in range(100):
    for tweet in api.search(q="#china", count=100):
        if tweet.lang in countTweets:
            countTweets[tweet.lang] += 1
        else:
            countTweets[tweet.lang] = 1

# keys and values of the countTweets dictionary stored as lists
keys = list(countTweets.keys())
values = list(countTweets.values())

# for loop that counts total tweets analyzed
for value in values:
    count += value 
print("Total tweets: ", count)
    

# display counts of tweets of various languages from the 10,000 tweets
for index in range(len(countTweets)):
    print("Language: " + str(keys[index]) + " Count: " + str(values[index]))
