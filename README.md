# EasyNMT Language Model

The purpose of this project was to come up with a list of sentences and to translate them to several languages using a pre-trained language model called EasyNMT.

## Code
The following code was used to translate the list of English sentences into several languages including Afrikaans, Albanian, Arabic and Armenian.
* Importing the easynmt library
`from easynmt import EasyNMT`
* Instantiating the EasyNMT object
`model = EasyNMT('opus-mt')`
* Translating the English sentences
`model.translate(df['en'], source_lang='en', target_lang=code)`

## Output
The dataframe below shows the translations for the English sentences
![Languages](https://user-images.githubusercontent.com/60528574/203166282-e3c41ce1-8601-4679-9ce6-086ae2859f1b.PNG)


