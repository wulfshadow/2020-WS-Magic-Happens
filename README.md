# Web Scraper Magic Happens Documentation
[Full Web Scraper Repository](https://github.com/wulfshadow/2020-Group-Web-Scraper)

## Magic Happens Code
```
#MAGIC HAPPENS
def get_count():
    page_response = requests.get(page_link, timeout=5)
    page_count = BeautifulSoup(page_response.content, "html.parser")
    count = len(page_count.find_all('br'))
    print count
    return(count)

current_count = get_count()

while True:
    page_count = get_count()
    if(current_count != page_count):
        print("Changed")
```     
### Explanation of Code
- Page is requested by requests.get function
- BeautifulSoup scrapes page under page_response variable
- page_count.find_all function searches for specified HTML tag, len function returns amount of tag
- New variable current_count is set equal to get_count()
- While loop begins, page_count becomes equal to get_count()
- if current_count variable (which was earlier set equal to get_count()) does not equal page_count varaible (the original variable that the scraper data is stored under) "Changed" is printed in the terminal.
- While loop continues into Output section.

## Tools 
- HTMLParser
- BeautifulSoup

## Techniques
- While Loop (first part of it, second part becomes output)
- len function
- find.all function

## Reference sites
- [https://docs.python.org/2/library/htmlparser.html](https://docs.python.org/2/library/htmlparser.html)
- [https://kite.com/python/examples/1734/beautifulsoup-find-all-tags-with-some-given-name-and-attributes](https://kite.com/python/examples/1734/beautifulsoup-find-all-tags-with-some-given-name-and-attributes)
- [https://stackoverflow.com/questions/4302027/how-to-open-a-url-in-python](https://stackoverflow.com/questions/4302027/how-to-open-a-url-in-python)
- [https://docs.python-guide.org/scenarios/scrape/](https://docs.python-guide.org/scenarios/scrape/)
- [https://www.pluralsight.com/guides/web-scraping-with-beautiful-soup](https://www.pluralsight.com/guides/web-scraping-with-beautiful-soup)
