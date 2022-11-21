# Web scraping

## Description
The objective of this project is to scrap the job opportunities posted [here](https://www.jobinrwanda.com) using the requests library to interact with the API. A library called BeautifulSoup to extract the meaningful content from the html which is obtained when the request library interacts with the API.


## Code
Below is the code that is used to extract the required information from the jobs posts:

* Title of each job
`content.find('span').getText()`
* Link to the content of each job title
`content.find('a')['href']` 
* Link to the institution that has posted the advert
`content.find('p').find('a')['href']` 
* Name of the company
`content.find('p').find('a').getText()`
* Type of advert
`content.find('p').find('span').getText()`
* Company description
`content.find_all('div', class_='employer-description')[0].getText()`

## Output
Below is the dataframe that was created from the scrapped data
![Company](https://user-images.githubusercontent.com/60528574/203159813-a73e32a1-7e57-476d-8e9e-6c9735df4df1.PNG)

# Text to features
The other objective of the project was to convert a list of sentences to features. Text to features is the process of converting tokens to numbers. This is because the machine only works with numbers. Moreover, for manipulation of text, the tokens need to be in digit form to apply any transformations.

The input of the function will be the matrix of tokens and output will be matrix with digits.

## Simplest form of featurization
The simplest way is to assign each unique text a number starting from 0 and increase by one until all the text has been assigned numbers

## Bag Of Words (BoW)
* Split the sentences into words
* Create a dictionary with all unique words and their indices
* Create a vector, size same as the total number of unique words
* For every word in a sentence, get the index and add 1.
* The result will be a vector for each sentence with length same as all the unique words in all sentences, with frequency of each word in one particular sentence. If a word is not in that sentence, the frequency is 0
