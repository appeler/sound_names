## Sound Names: Using the Sequence of Sounds to Classify Names

Building on prior [work](https://github.com/appeler/ethnicolr) that classifies names based on the sequence of characters, we create a model that capitalizes on sequence of sounds to classify names.   

To capture the phonetic similarity of different names, we first produce sound encodings of names using https://pypi.org/project/Metaphone/#contents
and then use LSTM on top to test classification accuracy. We find that the accuracy is substantially lower than what we can achieve when we just apply LSTM to the name strings. This suggests that there is some information in the spellings (aside from the sound) and very plausibly that the sound encoding algorithms do not capture the way a name is read completely.

In the future, we plan to ensemble the two models. 

### Scripts

1. [Download FL Voter Data](scripts/01_download_fl_voter.ipynb)
2. [Prepared FL Voter Data](scripts/02_prepare_fl_voter.ipynb)
3. [LSTM Model Based on Metaphone Encoding](scripts/03_metaphone_lstm_fl_voter_name.ipynb)
4. [Comparison Between Ethnicolr and Soundnames and Naive Average of the two models](scripts/04_metaphone_lstm_fl_voter_name-evaluation.ipynb)

### Authors

Suriyan Laohaprapanon and Gaurav Sood
