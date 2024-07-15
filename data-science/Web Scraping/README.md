`pip install beautifulsoup4`

`pip install lxml` - Praser
`pip install html5lib` - Praser

`pip install requests`

```python
from bs4 import BeautifulSoup
import requests
url = "https://timesofindia.indiatimes.com/rssfeedstopstories.cms"
document = requests.get(url)
soup = str(BeautifulSoup(document.content,"lxml-xml"))
print(soup)
print(soup.prettify())
```

```
```