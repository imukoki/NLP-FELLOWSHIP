# Web scraping

## Description
The objective of this project is to scrap the job opportunities posted on ([here] (https://www.jobinrwanda.com)) using the requests library to interact with the API. A library called BeautifulSoup to extract the meaningful content from the html which is obtained when the request library interacts with the API.


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
