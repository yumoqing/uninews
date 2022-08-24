# uninews
a universal news feed api for all news provider

## Installation
```
pip install uninews
```

## Supported providers

* [TheNewsApp](https://TheNewsApi.com)
* [NewsCatcherApi](https://newscatcherapi.com)
* [NewsData.io](https://newsdata.io)
* [GoogleNews](https://pypi.org/project/pygooglenews)

## Usage
Using thenewsapi provider
```
from uninews import NewsFeed
from TheNewsApi import set_app_info

set_app_info(appkey=mykey)
nf = NewsFeet('TheNewsApp')
x = nf.last_news()
print(x)
x = nf.hist_news()
print(x)
x = nf.sources()
print(x)
```

## Features

NewsFeed provide four type news get methods:
last_news:
	get last news from the specified provider

hist_news:
	get history news from the specified provider

sources:
	get the provider's sources of news

if the provider do not provide the method, it will return None

## Return data structure

### News data
The news data return by last_news() and hist_news() methods are the same, t is a dictionary data which contains:
1. total
	total record returned
2. articles
	a array contain all the articles

### Article data
article is a dict contains following keys:
1. title
	the article's title
2. description
	the summary description
3. content
	the article body
4. link
	the url address to the article
5. img_link
	the article image url address
6. video_link
	the video url address of article
7. publish_date
	the article publish date
8. countries
	countries of the article
9. categories
	categories of the article
10. author
	article's author
11. source_id
	source id of the article
12. language
	article's language

### sources data
1. total
2. sources

### source data
1. id
2. name
3. link
4. language
5. categories
6. description
7. countries


## provider
the following provider is tested
* [newsdataio](https://pypi.org/project/newsdataio) for https://newsdata.io
* [news_yapi](https://pypi.org/project/news_yapi) for [newsapi](https://newsapi.org)
* [thenewsapi](https://pypi.org/project/thenewsapi) for [thenewsapi](https://thenewsapi.com)

## working on provider
* google feed news provider




