# Exploring YouTube recommendations

This is a fork of Guillaume Chaslot's YouTube reccommendation explorer used in his excllent [Algotransparency](https://algotransparency.org/) project. It's been ported to Python 3 from 2.

Only minor changes were made:

* Using urllib instead of urllib2
* Decoding byte-strings to utf-8

-------------------------------

Where does YouTube's recommendation algorithm bring the user if he follows the recommendations?
This robot follows the recommendations on YouTube from a given search query to find out where they bring you.
After searching on YouTube and following the recommendations, it prints the 50 most recommended videos.

## Installation

To install the project's python dependencies, you can use pip:

```
pip install -r requirements
```

Used dependencies:

* [BeautifulSoup4](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)

## Example of usage:

python follow-youtube-recommendations.py  --query="global warming,vaccines,nasa" --searches=4 --branch=4 --depth=4 --name="science"

* --query: query that is made on youtube
* --searches: number of search results from the query to start with
* --branch: branching factor = number of recommendations that are followed
* --name: name under which it will be saved
* --alltime: add this option if you want to start from the most viewed videos for the query (using the option filter by viewcount on youtube)
