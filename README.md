# r/AITA Post Classification with NLP

This repository contains the code and methodology for classifying posts from [Reddit’s "Am I the Asshole" (AITA)](https://www.reddit.com/r/AITA/new/) forum into different verdict categories using various natural language processing (NLP) techniques. The project aims to uncover common themes within posts and predict community verdicts based on textual content.

## Overview 
Reddit is a vast network of communities based on people's interests. Here, people can post questions, share content, and comment on each other's posts in subreddit communities, which are specific to certain topics or themes.

The "Am I the Asshole?" (AITA) subreddit is one such community where users submit posts describing a situation where they may have been in conflict with someone else and ask the community to judge if they were in the wrong. The community then votes and comments, offering their judgment based on the subreddit's specific criteria (e.g., "You're the Asshole" (YTA), "Not the Asshole" (NTA), "Everyone Sucks Here" (ESH), "No Assholes Here" (NAH)). It's a platform for moral and ethical discussion where the focus is on the actions and decisions of individuals in specific scenarios, a semi-structured online forum that’s the internet’s closest approximation of a judicial system.

A vote is made using a set of initialisms, decided by a moderator for the channel:

- NTA - ‘not the asshole’: the OP (original poster) was not the asshole in the situation, while the others in the situation were
- NAH - ‘no assholes here’: nobody in the particular scenario is an asshole
- YTA - ‘you’re the asshole’: the OP (original poster) is the asshole, while the others are not
- ESH - ‘everyone sucks here’: the OP (original poster), and all others involved in the story are assholes


## Dataset Overview 

The dataset has 9 features:

- id, a unique string provided by Reddit's API to index every post timestamp of post creation, in epoch/Unix format
- title: title of post
- body: text of post
- edited: the timestamp at which a post was edited. If no edits occurred this field is False.
- verdict: verdict by the community ()"asshole", "not the asshole", "everyone sucks", "no assholes here")
- score: an integer corresponding to the difference between upvotes and downvotes
- num_comments: an integer corresponding to the total number of comments (including nested discussion) to the post
- is_asshole: a boolean (1/0) corresponding to whether the verdict is in the set {"asshole","everyone sucks"}, decided by a moderator of the subreddit
- 
The dataset was created and cleaned by Elle O’Brien, faculty at the University of Michigan, and can be accessed at her [GitHub](https://github.com/iterative/aita_dataset)
