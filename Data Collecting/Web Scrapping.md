Web scraping, web harvesting, or web data extraction is data scraping used for extracting data from websites. Web scraping software may directly access the World Wide Web using the Hypertext Transfer Protocol or a web browser.

## Beautiful Soup

>Beautiful Soup is a Python package for parsing HTML and XML documents. It creates a parse tree > for parsed pages that can be used to extract data from HTML, which is useful for web scraping.

#### Custom attributes

To set custom attributes like `data-seller-is-safe-deal="True"` or `data-wholesale="0"` you should use dictionaty: 
`attributes = { 'data-seller-is-safe-deal': 'True', 'data-wholesale': '0' }`
and pass is as an argument to find method:
`soup.find('element', attrs=attributes)`

#### Example

Здесь я брал список товаров с заранее загруженной страницы
```python
from bs4 import BeautifulSoup
with open("html/parts/hyundai_accent.html", "r", encoding="utf-8") as file:
    soup = BeautifulSoup(file.read(), 'html.parser')
    colgroup = soup.find('colgroup')
    attributes = { 'data-seller-is-safe-deal': 'True', 'data-wholesale': '0' }
    trs = soup.find_all('tr', attrs=attributes)
    products = [{
        'code': tr.find('td', attrs={'data-type': 'code'}).text.strip(),
        'maker': tr.find('td', attrs={'data-type': 'maker'}).text.strip(),
        'price': float(tr.find('td', attrs={'data-type': 'price'}).get('data-value'))
    } for tr in trs]
```
