# Code for paper "ChatGPT-4 outperforms experts and crowd-workers at annotating political Twitter messages with zero-shot learning"

## Abstract 
This paper assess  the accuracy, reliability, and bias of the Large Language Model (LLM) ChatGPT-4 on the text analysis task of identifying the political affiliation of Twitter posters based on tweet content, compared to manual annotation by expert classifiers and crowd workers. Twitter messages from politicians in 11 countries provide ground truth data. The paper finds that ChatGPT-4 achieves significantly higher accuracy and reliability, and equal or lower bias than human classifiers, with the highest accuracy for the US but high accuracy for all included countries and languages. The LLM is able to correctly annotate messages with implicit or unspoken references, that require reasoning on the basis of contextual knowledge or assumptions of the author's intentions -- traditionally seen as uniquely human capacities. These results suggest that LLMs will have paradigm-shifting impact on the use of textual data in the social sciences.

## Description
### CODE
- LLM.ipnyb runs ChatGPT on the data and stores the result
- MTURK.ipnyb carries out MTurk analysis
- Analysis and graphs.ipnyb analyzes the resulting data and outputs figures for paper

### DATA
- data/expert/Expert[1-3].csv contain the expert coding of the US senator tweets.
- data/mturk/MTURK.csv contain the MTURK coding of the US senator tweets.

- data/regular/RegularPeopleExpert[1-2].csv contain the expert coding of regular people's tweets.

- data/country/[COUNTRY]_sample_tweets.csv contains the sample of tweets for a given country.
- data/country/tweet_process_[COUNTRY].pkl contains the sample of tweets for a given country, classified by the LLM

(Note that as CSV files with dataframes do not support arrays in columns, the code uses pickles.)
