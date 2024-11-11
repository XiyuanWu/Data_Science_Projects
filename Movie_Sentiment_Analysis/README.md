# Movie Sentiment Analysis

**Movie Sentiment Analysis: Review Polarity Classification**


## Background

This project focuses on sentiment analysis of movie reviews, aimed at determining the underlying sentiment expressed within a body of text. By analyzing the content of movie reviews, we strive to classify each review as positive or negative automatically. 

Dataset can be found in [here](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews).


## Update

Before, we used Multilayer Perceptrons (MLP), a basic model, to predict movie sentiment. This time, we will use the LSTM model to make it even more robust.


## Result & Conclusion

For Multilayer Perceptrons (MLP), achieved:
- Accuracy: 0.8782
- Precision: 0.8683
- Recall: 0.8890
- F1 Score: 0.8786
- ROC AUC: 0.9477

For Bidirectional LSTM, achieved:
- Around 96% accuracy on the train
- Around 87% on the test/val set

Both model result are very similar. Interestingly, many people get the same result when I check someone else's notebook on Kaggle. It might be a dataset bias or some trends that are hard to catch by model. Overall, this model has shown the average level.

## Requirements

To run a Bidirectional LSTM notebook, you need a file `glove.6B.50d.txt` because it uses GloVe word embedding. To get this file, go to the [GloVe Website](https://nlp.stanford.edu/projects/glove/), download the file called `glove.6B.zip`, and unzip the file.