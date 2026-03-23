# Chapter 4 Sample Code
## Word Embeddings

In `embedding.py`, there is an example of how to build a word-to-vector embedding in Tensorflow.  We train it as a classifier, determining if the text, a movie review from IMDB, is a positive review of the movie it is reviewing, or a negative review.  Just that process, of training the model (including the embedding) to predict if a review is positive or negative, provides enough information for the embedding to learn a substantial amount about the language involved.

The function `find_closest()`, which runs at the end of the program, finds the 10 words whose distance from "excellent" and "awful", and the results are surprisingly good.

In this model, the tokens are words, the only character other than letters and spaces that is kept is the apostrophe ('), to keep words like "didn't" intact.  We give up on all other punctuation, since it is not important to the classification.

If you want to run this code, make sure you follow the Google Drive link in the docstring at the top of embedding.py to download my combined version of the dataset.

Notice that the input strings are all set to 100 words, the rest of each review is discarded.  This is a feature of CNNs and CNN-like models (like this one) -- the input size must be fixed for all inputs.  To deal with variable-length inputs, you need to go with something like an RNN (Recurrent Neural Networks) or a Transformer model.  Coming soon!