# recommeder_app

Introduction

Over time, we rely more and more heavily on online platforms and applications such as Netflix, Amazon, Spotify etc. we are finding ourselves having to constantly choose from a wide range of options.

One may think that having many options is a good thing, as opposed to having very few, but an excess of options can lead to what is known as a “decision paralysis”. As Barry Schwartz writes in The Paradox of Choice:

“A large array of options may discourage consumers because it forces an increase in the effort that goes into making a decision. So consumers decide not to decide, and don’t buy the product. Or if they do, the effort that the decision requires detracts from the enjoyment derived from the results.”

Also resulting in another, more subtle, negative effect:

“A large array of options may diminish the attractiveness of what people actually choose, the reason being that thinking about the attractions of some of the unchosen options detracts from the pleasure derived from the chosen one.”

An obvious consequence of this, is that we end up not making any effort in scrutinising among multiple options unless it is made easier for us; in other words, unless these are filtered according to our preferences.

A major drive in the field is Netflix, which is continuously advancing the state-of-the-art through research and by having sponsored the Netflix Prize between 2006 to 2009, which hugely energised research in the field.

In addition, the Netflix’s recommender has a huge presence in the platform. When we search for a movie, we immediately get a selection of similar movies which we are likely to enjoy too:

Outline
This post starts by exposing the different paradigms in recommender systems, and goes through a hands on approach to a content based recommender. I’ll be using the well known MovieLens dataset, and show how we could recommend new movies based on their features.

This is the first in a series of two posts (perhaps more) on recommender systems, the upcoming one will be on Collaborative filtering.

Types of recommender systems
Most recommender systems make use of either or both collaborative filtering and content based filtering. Though current recommender systems typically combine several approaches into a hybrid system. Below is a general overview of these methods:

Collaborative filtering: The main idea behind these methods is to use other users’ preferences and taste to recommend new items to a user. The usual procedure is to find similar users (or items) to recommend new items which where liked by those users, and which presumably will also be liked by the user being recommended.
Content-Based: Content based recommenders will instead use data exclusively about the items. For this we need to have a minimal understanding of the users’ preferences, so that we can then recommend new items with similar tags/keywords to those specified (or inferred) by the user.
Hybrid methods: Which, as the name suggests, include techniques combining collaborative filtering, content based and other possible approaches. Nowadays most recommender systems are hybrid, as is the case of factorization machines.
The MovieLens Dataset
One of the most used datasets to test recommender systems is the MovieLents dataset, which contains rating data sets from the MovieLens web site. For this blog entry I’ll be using a dataset containing 1M anonymous ratings of approximately 4000 movies made by 6000 MovieLens users, released in 2/2003.

Let’s get a glimpse of the data contained in this dataset. We have three .csv files: ratings, users, and movies. The files will be loaded as pandas dataframes. We have a ratings file which looks like:


source: https://towardsdatascience.com/content-based-recommender-systems-28a1dbd858f5
App: http://ike360.herokuapp.com/

Special thanks goes to kishan for a remarkable contribute he is putting out the for those in the Data Science space and also this particular project.
