# Data Science recruitment challenge
## Recruitment task carried out for the Surfer company, branch in Wrocław
### Author: Michał Hetmańczuk
#### Task: Phrase scoring
Task theme — data science and coding skills.

##### For each scrape find 10 most prominent phrases.

Consider phrases up to 4 words.

###### Dataset

[scrapes.csv](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/610644d8-ce87-408f-8c25-84268b3ca151/scrapes.csv)

###### Dataset description

This dataset contains data from 14 different scrapes. Each scrape has multiple crawled pages. Each crawled page has multiple words.

- `scrape` - collection of crawled pages which were returned in the Google SERP
- `scrape_keyword` - keyword used in given Google Search
- `words` - vector of words extracted from given crawled page
- `scores` - vector of integer word prominence scores. Each word should have a corresponding score.

#### Solution
The prominence of each phrase was calculated as the average prominence of its words. 
The measure defining the significance of phrases with a specific word pattern was based on the tfidf measure at the scrape level,
 but instead of the term frequency, the average phrase score was calculated.