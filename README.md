# Text Mining Group Assignment:
### Sarah de Jong, Tom Klein Tijssink, Lukas Busch

## Abstract
The goal of this report is to explore different machine learning approaches to generate song lyrics. We use a dataset that contains 380.000 songs. First, we use a BERT model in order to add a positive or negative sentiment to each song. Then, we explore a simple N-gram model, a word-based LSTM, a character-based LSTM, and a GPT-2 model to generate song lyrics by using N-grams. After evaluating the results with a survey, it is found that the GPT-2 model performs best.

## Research questions
Can we create a song writing program that takes a number of words as well as a genre and sentiment (positive/negative) to generate lyrics?

## Dataset
For this project, we used the dataset 380000-lyrics-from-metrolyrics, because this dataset includes lyrics as well as genres. It was originally available on kaggle, but it currently is not anymore. We retrieved the data from a project from last year: https://github.com/ludovicaschaerf/TMCI_Project.
The dataset contains 380,000 different songs, which includes the artist, year, genre, and lyric. It can be downloaded in csv format.

## A tentative list of milestones for the project
- Week 1 - Determine topic
- Week 2 - Do sentiment analysis, determine method of evaluation, look at first model
- Week 3 - Try more models (see below for what we ended up looking at)
- Week 4 - Try more models (see below for what we ended up looking at)
- Week 5 - Try more models (see below for what we ended up looking at)
- Week 6 - Do survey for evaluation, clean up code, write report, prepare presentation

## Division of the work
We met about 10 times to discuss the progress and the project. In the first week, we determined the topic together. In the second week, Lukas did the sentiment analysis of the songs, Tom looked at an N-gram RNN model, and Sarah looked at ways to evaluate the songs. In the third week, Lukas looked at the GPT-2 model and Sarah tried to implement the N-gram RNN model for a larger number of songs, which used too many resources and which is therefore not in the final project. In the fourth and fifth week, Sarah looked at a basic N-gram model and Tom and Lukas both looked at an LSTM model. In the sixth week, we cleaned up the code and repository, did the evaluation of our songs with a survey, wrote the report, and prepared for the presentation.

## Documentation
The src folder in this repository contains our work. We did not put all our code in one notebook, because we thought it was a lot more organized to put every different model in a different notebook. Furthermore, we started out in separate files, and if we had wanted to put them all together at the end, we would have needed to rerun everything (or submit a notebook that was not run). Our repository contains the following files:
- data/lyrics.csv, which is our data-set
- data/lyrics_sentiments.csv, which is our data-set with the sentiments added
- data/popsongs.txt, which is our data-set in a text file
- data/negative_pop.txt, which contains the negative songs of our data-set in a text file
- data/positive_pop.txt, which contains the positive songs of our data-set in a text file
- sentiment_analysis/Sentiment_Analysis.ipynb, which contains the training of a BERT model to predict sentiments on a dataset of poetic verses.
- sentiment_analysis/predicting_sentiments.ipynb, which contains the predicting of sentiments of our songs with the BERT model.
- Ngram_model.ipynb, which contains the training and evaluation of our basic n-gram model
- Lstm_character_model.ipynb, which contains the training and evaluation of our character based lstm model
- lstm_model_training.ipynb, which contains the training of our word based lstm model
- lstm_model_evaluation.ipynb, which contains the evaluation of our word based lstm model (note that these are separate because we put them separate at first and did not want to rerun it due to time constraints)
- GPT_2_Text_generation.ipynb, which contains the training and evaluation of our GPT-2 model
