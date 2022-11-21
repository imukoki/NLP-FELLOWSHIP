# Text to features
The objective of the project was to convert a list of sentences to features. Text to features is the process of converting tokens to numbers. This is because the machine only works with numbers. Moreover, for manipulation of text, the tokens need to be in digit form to apply any transformations.

The input of the function will be the matrix of tokens and output will be matrix with digits.

Two ways of converting text to features were used in the project which are the simplest form of featurization and bag of words (BOW)

## Simplest form of featurization
The simplest way is to assign each unique text a number starting from 0 and increase by one until all the text has been assigned numbers

## Bag Of Words (BoW)
* Split the sentences into words
* Create a dictionary with all unique words and their indices
* Create a vector, size same as the total number of unique words
* For every word in a sentence, get the index and add 1.
* The result will be a vector for each sentence with length same as all the unique words in all sentences, with frequency of each word in one particular sentence. If a word is not in that sentence, the frequency is 0

The list of sentences that were used for this project are:
`list_sentences = ['this is a list of sentences example', 'second sentence in list of sentence', 'a word for complexity']`
This the dictionary that was created for the entire word corpus:
`{'word': 0, 'for': 1, 'list': 2, 'sentence': 3, 'sentences': 4, 'in': 5, 'this': 6, 'is': 7, 'second': 8, 'a': 9, 'example': 10, 'complexity': 11, 'of': 12}`

## Output
This is the result that is obtained when the text has been converted to features for the 3 sentences that were provided:
![Matrix](https://user-images.githubusercontent.com/60528574/203168858-f9c5e5d4-bc39-4ca2-b63c-9b2a4d5bf421.PNG)




