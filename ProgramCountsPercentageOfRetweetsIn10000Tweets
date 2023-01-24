'''
HW8
CIS 2532 NET01
Dr. Shamsuddin
Kostas Spyropoulos
Program counts the amount of retweets in 10,000 tweets
04/11/2022
Exercise 13.2
'''
import tweepy
import keys
auth = tweepy.OAuthHandler(keys.consumer_key, keys.consumer_secret)
auth.set_access_token(keys.access_token, keys.access_token_secret)
api = tweepy.API(auth, wait_on_rate_limit=True, wait_on_rate_limit_notify=True)



# Exercise 13.2

# count of how many tweets with RT in the beginning
count = 0 

# count of total tweets analyzed
tweetTotal = 0

# for loop that counts retweets from the 10,000 tweets list
for iteration in range(100):
    for tweet in api.search(q="#china", count=100):
        tweetTotal = tweetTotal + 1
        tweetText = str(tweet.text)
        if tweetText.startswith("RT") == True:
            count = count + 1
            
            
# display percentage of retweets from 10,000 tweets list
print("Percent of Tweets that begin with RT out of 10,000 tweets: ",(count/10000)*100, "%")
print("Tweets analyzed: ",tweetTotal)
