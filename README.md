# Project 3 subreddit classification Republican/Democrat

## Problem Statement

Politics in America are very divisive. At least that is how it is often portrayed.  Can we use data to try and prove if this division is as great as it seems or more overblown.

I have been assigned by Major News Network to try to find the level of division in discourse on the internet.  In particular using reddit posts from the Democrat and Republican subreddits to try and see the strength of the division. This will be through trying to classify the posts using natural language processing. In that way look for the common language used in each subreddit. 

In this way we can try to look at the political difference based on what people are saying not just polls or voting numbers.

|Feature|Type|Description|
|---|---|---|
|created_utc|int|The UTC timestamp that the post was created|
|subreddit|object|The subreddit that the post came from|
|title|object|The text of the title of the reddit post|
|char_count|int|Total number of characters in the title of the post|
|word_count|int|Total number of words in the title of the post|


## Summary
I pulled the data from the two subreddits to try and create a classification model that would try to judge the subreddit of a post.  The initial challenge with the posts was that most did not have much text to go along with them as they tended to be based on a news artice or video.  The titles of the posts were usually a good length so the titles became my method of judgement.

This also fits with the inital problem as it often corresponds with the narative of different media outlets and shows the current discourse around a subject.  

The data was vectorized and examined for points of interest.  What I found was that while the meaning of the posts could be different a lot of the same words were common between both subreddits.  This was going to present a problem when creating a model as most models would have trouble picking between the two when using the common words.

The initial models had to be very overfit to get good results.  I worked on the hyperparameters of the models to try and get a better result and while I could reduce the overfit it seemed like I was unable to get a better overall accuracy score.

It seems that the similar word choice between the titles makes it hard to determine which subreddit each came from.  

## Conclusion
This has resulted in some interesting data.  On the one hand, looking at the reddit and other outside information it would seem that the country is very divided politically.  The problem is that the models for classification do not seem to be able to find a similar result.  I can only get around 64% accuracy on the test data.

What seems to be happening is that although the meaning of an article might be clear to a person about their political leanings the language used is so similar that the computer models have trouble finding the difference. This seems in part due to the way the media tends to report on political news.  Different news sources say similar things but leave out some key words or phrases that might change the meaning of a statement.

This means that care needs to be taken when relaying the news to avoid partisan language.  It also shows the importance of nuance in the language and how it can be abused for an agenda.  As a media company the title of your piece can be as important as the body since it is the first thing people see and can direct the conversation.  Making sure you are not seen as partisan is important for informing the population.

With improvement the model can help to show bias in titles and try to help the company maintain a more neutral stance. Thsi can be done by avoiding sarcastic or misleading titles, or statement that use overly hyperbolic language.

### What Next
- expand to other subreddits like ones that might be less partisan
- enhance the vectorization by checking for more hyperparameters
- look into other models that might be better at picking up language nuance
- expand to the comments of the subreddits