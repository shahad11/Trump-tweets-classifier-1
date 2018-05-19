# Trump-tweets-classifier
Uses a Naive Bayes classifier to detect whether Trump has authored a given @RealDonaldTrump tweet.

#Background

Before becoming president, Donald Trump personally used a Samsung Galaxy, which runs the Android OS. Clever people quickly realized that tweets sent from an Android phone appeared "Trumpier" — a bit more angry and direct — than tweets sent from an iPhone.

This led folks to conclude that it probably was actually Trump tweeting in posts from the Android, while posts from the iPhone were from staffers.

Alas! Now that he's president, Trump is using his Android phone less and less. So we have to find a different to tell if it's him.

#The classifier

This script uses tweets from 2016 and part of 2017 (before Trump began switching over to using the iPhone almost exclusively) to fuel a bag-of-words Naive Bayes classifier. It parses tweet text into one of two categories: trump (similar to previous tweets posted by the Android) and staff (similiar to tweets posted by an other device).

It discards common words and narrows down the feature list to the top 500 words to prevent overfitting. Even so, I fear this model is biased to Campaign Trump, not Current Trump — it ranks highly terms like bernie and cruz, which are't quite as relevant today. (Update: I've now added 2016 campaign-y stuff to a custom list of stopwords.)

# The Data

The data comes from "The excellent Trump Twitter Archive" by Brendan Brown.
