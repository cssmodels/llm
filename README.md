# Code for paper "Large Language Models Outperform Expert Coders and Supervised Classifiers at Annotating Political Social Media Messages"

## Abstract 
Instruction-tuned Large Language Models (LLMs) have recently emerged as a powerful new tool for text annotation. As these models are capable of zero-shot annotation based on instructions written in natural language, they obviate the need of large sets of training data – and thus bring potential paradigm-shifting implications for text-as-data. While the models show substantial promise, their relative performance compared to human coders and supervised models remains poorly understood and subject to significant academic debate. This paper assesses the strengths and weaknesses of LLMs compared to both state-of-the-art supervised classifiers, and manual annotation by experts and crowd-workers. The task used is to identify the political affiliation of politicians based on a single X/Twitter message, focusing on data from 11 different countries. The paper finds that ChatGPT-4 achieves higher accuracy than both supervised models and human coders across all languages and country contexts. Examining the cases where the models fail, the paper finds that the LLM – unlike the supervised models – is able to correctly annotate messages that require understanding implicit or unspoken references, or reasoning on the basis of contextual knowledge – capacities that have traditionally been understood to be distinctly human. The paper thus contributes to our understanding of the revolutionary implications of LLMs for text analysis within the social sciences.

## Description
### CODE
- LLMAnalysis.ipnyb runs ChatGPT on the data and stores the result
- MTURK.ipnyb runs MTurk to collect data from crowd workers
- Results.ipnyb analyzes the resulting data
- Appendix1.ipnyb carries out analysis for Appendix 1: running a classification analysis on social media users for whom the labels are not a priori known.
- Appendix2.ipnyb carries out analysis for Appendix 2: measuring the reliability of the analysis to small variations in the prompt.


### DATA
- data/expert/experts.csv contain the expert coding of the US senator tweets.
- data/mturk/MTURK.csv contain the MTURK coding of the US senator tweets.

- data/regular/RegularPeopleExpert[1-2].csv contain the expert coding of regular people's tweets. Relating to Appendix 1.

- data/country/[COUNTRY]_sample_tweets.csv contains the random sample of tweets for a given country.
- data/country/tweet_process_[COUNTRY].pkl contains the sample of tweets for a given country, classified by the LLM.

(Note that as CSV files with dataframes do not support arrays in columns, the code uses pickles.)
