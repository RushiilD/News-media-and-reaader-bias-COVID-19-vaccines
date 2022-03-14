# News-media-and-reaader-bias-COVID-19-vaccines
An NLP project to determine the reporting bias of 5 major news outlets in the US and the impact of this reporting on readers.

## Overview
News sources in America are free to report any information they feel readers would want to consume, and they can insert as much or as little bias in their writing as they feel. Americans also tend to consume news from sources whose biases they view are aligned with their political leaning; for example a far-left reader might choose Huffington Post as their publication of choice, whereas a far-right reader might choose Breitbart. 
However, are readers’ political biases actually aligning with the published biases of a news source? That is what this project will attempt to address. 

## Reasons for undertaking project
A recent Gallup poll reported that only 36% of Americans have a great or fair amount of trust of media sources, the second lowest figure on record. 
Are there specific publications that are guilty of implanting bias in their reporting, or is it all media sources? If there are specific offenders, are Americans recognizing these biases or are they showcasing this mistrust on the wrong publications due to individual political bias given a perceived political leaning of a news source?

![image](https://user-images.githubusercontent.com/88729964/158274136-8e3c7fbd-1f61-4a52-a9e7-d8728e5a9f3b.png)

## Steps taken

### 1. Data Scraping
We sought our data from 2 different online mediums. We started by scraping articles about the COVID-19 vaccine using the newspaper library. The vaccine was one of the most relevant and polarizing topics in US politics recently, and a widely covered topic in mainstream media. The vaccine presented the perfect gauge for political leaning with the assumption that pro vaccine stances are liberal and anti vaccine stances are conservative. We chose 5 different news outlets that varied across the political spectrum. From left to right, we chose Huffpost, CNN, Reuters, FoxNews, and Breitbart, and in total we gathered 66 articles.

![image](https://user-images.githubusercontent.com/88729964/158275297-083c180e-3765-4e4e-b57e-43da45565607.png)

Next, we used Twitter. We scraped posts containing the names of our 5 publications as well as the specific word “vaccine” using tweepy, SnScrape and the twitter API. In total, we scraped around 7200 tweets. Additionally, we were able to obtain the location data of most of the users whose tweets we scraped.

![image](https://user-images.githubusercontent.com/88729964/158275737-de8bb255-23e2-43be-8666-0891e4260b8f.png)

### 2. Exploratory Data Analysis

We used the NLTK library for preprocessing of this data. We stemmed the words using the Lancaster Stemmer, and isolated keywords based on frequency counts and relevance to the topic at hand. Using these stemmed words, we created some MDS plots to understand the grouping of various terms by news source.

![image](https://user-images.githubusercontent.com/88729964/158274540-cd544c89-b055-4c00-855a-9f056ecdf9f5.png)

Our preliminary analysis of related words is as follows:

Reuters - Reporting on vax
Breitbart - Antifa and anti-vax
Fox - Dangers of vaccine
CNN - Importance of vaccine

### 3. Sentiment Analysis
We then used the VADER library in Python to perform sentiment analysis of the articles and group them by positive and negative sentiments around the vaccine.

![image](https://user-images.githubusercontent.com/88729964/158274717-85ba9e69-1909-454c-9f13-8aeb40049365.png)

Next, we analyzed the sentiments of Twitter responses to said articles to get an understanding of user sentiments and reactions.

![image](https://user-images.githubusercontent.com/88729964/158274811-f372fd59-ad4d-4ebb-ae3b-b7003c37f752.png)

FInally, we segmented the twitter responses by Geogrpahy and analyzed sentiments based on whether or not the states were conservative or liberal based on recent election results.

![image](https://user-images.githubusercontent.com/88729964/158274894-5e081ba6-c8e0-41db-a4d8-bb1fbf788b7d.png)

## Insights

Based on the insights generated above, we plotted the news articels on two scales: One for the articles themselves and the other for tweet replies. The left side of the scale represents positive sentiments about the vaccine while the right end of the scale represents negative sentiments about the vaccine.

![image](https://user-images.githubusercontent.com/88729964/158275060-e1a8d6ac-bc0c-4888-953a-9fb66a1f2e1f.png)

## Conclusion

We see the possible biases of these new sources both by the content in their articles and the sentiments of users interacting with said articles. Based on these insights, we conclude that user opinions of news sources are largely correct, however they can change subject to televised broadcasts while article content more or less remains as anticipated.













