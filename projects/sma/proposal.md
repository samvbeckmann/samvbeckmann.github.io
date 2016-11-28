---
layout: page
title: Social Media Analysis Proposal
permalink: /projects/sma/proposal
---

{:.center-focus}
Work of Sam Beckmann and Nate Beckemeyer

## Data Analysis

Our data sources will be the Twitter & Reddit datasets currently being collected by the machine in the intelligent agents lab.[^1]

[^1]: I'll fill in this section later

### Part 1: Social Network or Communication Topology

#### Question 1: Hashtag Cross-Pollination

>If an individual uses a pro-Trump hashtag, what is the probability that the same individual will use a pro-Clinton hashtag? Similarly, if an individual uses a pro-Clinton hashtag, what is the probability they will use a pro-Trump hashtag? That is, given a certain political hashtag, what is the probability that the user who tweeted that hashtag also tweeted a hashtag associated with the opposite political alignment—or another hashtag of the same political alignment?
{:.indent}

This analysis will be performed using the Twitter dataset, and the hashtags `#MakeAmericaGreatAgain`, `#MAGA`, `#Trump2016`, `#TrumpPence2016`, `#deplorables`, `#VoteTrump`,  `#Trump`, `#TrumpsArmy`, `#TRUMPTRAIN`, and `#Trump2016` as the pro-Trump dataset, and `#HillaryClinton`, `#Hillary2016`, `#ImWithThisBitch`, `#ImWithHer`, `#TrumpIsALiar`, `#NeverTrump`, `#StrongerTogether`, `#DumpTrump`, `#HillarysArmy`, and `#LoveTrumpsHate` as the pro-Clinton dataset.

#### Question 2: Subreddit Cross-Pollination

> If a user comments in a pro-Trump subreddit, what is the probability that the same user will comment in a pro-Clinton subreddit? Similarly, if a user comments in a pro-Clinton subreddit, what is the probability they will comment in a pro-Trump subreddit? That is, given a certain political subreddit, what is the probability that the user who commented in that subreddit also commented in a subreddit associated with the opposite political alignment—or another subreddit of the same political alignment?
{:.indent}

This analysis will be performed using the Reddit dataset, and the subreddits `r/HillaryClinton`, `r/HillaryForAmerica`, `r/AskHillarySupporters`, `r/EnoughTrumpSpam`, `r/progressive`, and `r/liberal` as the pro-Clinton subreddits, and `r/The_Donald`, `r/trump`, `AskTrumpSupporters`, `r/HillaryForPrison`, `r/conservative`, and `r/Republicans` as the pro-Trump subreddits.

### Part 2: Information Flow & Diffusion

#### Question 1: Politicized Influence on Twitter

> Do Twitter users who use multiple hashtags, especially those of different candidates, find themselves in more influential positions when they tweet?
{:.indent}

Using the Twitter dataset, we will create a set of political hashtags mentioned by each user, as well as calculate the average influence of the user’s tweets, based on the average number of likes and retweets their tweets get. Is the average tweet influence score correlated with the number of political hashtags used? We may also look at nonpolitical hashtags to generate a control group, in case using multiple hashtags naturally raises a user’s average tweet influence.

#### Question 2: Politicized Influence on Reddit

> Do Reddit users who frequent multiple political subreddits, especially those of different candidates, find themselves in more influential positions when they make comments?
{:.indent}

Using the Reddit dataset, we will create a set of subreddits commented on for each user, as well as calculate the user’s average comment score. (as well as the average comment score excluding comments with less than net votes, to exclude comments which received no attention) Is the average comment score correlated with the number of political subreddits commented in? We may also look at nonpolitical subreddits to generate a control group, in case commenting on multiple subreddits naturally raises a user’s average comment score.

### Part 3: Content Analysis

#### Question 1: Hashtag Adoption

> Are Twitter users prone to being early or late adopters to hashtag trends in general, or does a user’s adoption depend on the hashtag in question, not general early or late adoption habits?
{:.indent}

This question will use the Twitter dataset. Early adoption will be defined as the first 10% of users to use the hashtag in our dataset, and late adopters will be defined as users who did not use the hashtag until after it’s maximum popularity

#### Question 2: Subreddit Opinion Adoptions

> What is the falloff between the most adopted opinion, and the second most adopted opinion on a political subreddit? Does this falloff vary between different political subreddits, or between candidates?
{:.indent}

This question will use the Reddit dataset. For each successful Reddit post from a political subreddit, (successful posts being defined as receiving 100 or more up-votes) we will consider the two “most highly adopted” comments for the post — the comments which received the most up-votes. Then, we will compare the difference in magnitude of votes between the two comments, as well as the average distance for each subreddit, and each candidate.
