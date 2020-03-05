# DS1  
This README will explain my thought process in choosing the model that I did and my methodology if I would have had quantifiable comments. 

## THE_GOAT  
This file contains some basic exploration of the keras imdb dataset for sentiment analysis. I was able to successfully train an embedded 
list of comments on the imdb rating system. After which I was able to run sentiment analysis on self made reviews and I was satisfied with 
the outcome.  


The biggest flaw with this way of running sentiment analysis on the Hacker News comments was that Hacker News doesn't have a scaled ranking
system like imdb, yelp, spotify, etc. I needed to use a pretrained model on my data because I was not able to train the comments themselves.


## HN_SA_Model  
Thanks to the suggestion of my Team Lead and Section Lead, I was able to find vaderSentiment. Vader proved to be a very useful application 
in this problem because it didn't need to be pretrained on anything and the words didn't even need to be embedded for the model to recognize 
them. I wrote custom functions to give a score on a string of words and it worked perfectly.  


The model was a great fit for the problem because it didn't need embeddings or training. I was able to implement the model in the flask app 
as a hn-utils.py file and then the main app called in the functions I wrote.
