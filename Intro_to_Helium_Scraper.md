Web scraping with Helium Scraper
=================================
```by Liz Lucas```

-- [**Intro to web scraping and Helium**](https://github.com/eklucas/NICAR-Help/blob/master/Intro_to_Helium_Scraper.md#)
-- [**Planning your scrape**](https://github.com/eklucas/NICAR-Help/blob/master/Intro_to_Helium_Scraper.md#)
-- [**Helium terminology: Kinds, Actions and Data**](https://github.com/eklucas/NICAR-Help/blob/master/Intro_to_Helium_Scraper.md#)
-- [**Translating your plans into a scraper**](https://github.com/eklucas/NICAR-Help/blob/master/Intro_to_Helium_Scraper.md#)
-- [**Legal and ethical considerations**](https://github.com/eklucas/NICAR-Help/blob/master/Intro_to_Helium_Scraper.md#)

###_Intro to web scraping and Helium_

We've all visited websites that contain valuable information we want to analyze, such as [inspections reports](http://www.gocolumbiamo.com/webapps/cfforms/health/health_inspections.cfm), [lobbying expenditures](http://ethics.la.gov/LobbyistData/SearchByFinancialDisclosure.aspx), or a [list of jail inmates](https://www.showmeboone.com/sheriff/JailResidents/JailResidents.asp). 

We're grateful for the [growing movement](http://theodi.org/about-us) among [government agencies](https://nycopendata.socrata.com/) (particularly [federal](www.consumerfinance.gov/hmda) ones) to provide what we all want to see: the **DOWNLOAD** button. 

But not everyone is there yet. 

So when we can't download or copy and paste what's there, we have to give up or figure out how to literally _scrape_ the info off the website and into a database, a spreadsheet, or something we can actually use.

Imagine tackling this site: [https://apps.sd.gov/st12odrs/LobbyistViewlist.asp?cmd=resetall](https://apps.sd.gov/st12odrs/LobbyistViewlist.asp?cmd=resetall). If you wanted to end up with a spreadsheet of registered lobbyists, how would you do it? 

A web scraper is simply a [piece of software](http://www.heliumscraper.com/), a [bit of code](http://docs.python-guide.org/en/latest/scenarios/scrape/), or a [browser plugin](https://chrome.google.com/webstore/detail/scraper/mbigbapnjcgaffohmbkdlecaccepngjd?hl=en) that does the work for us, preferably while we go have a beer. 

[Helium Scraper](http://www.heliumscraper.com/) is a $99 piece of software (for Windows only) that provides a point-and-click interface for web scraping so that you don't have to write something like this: 

```
soup = BeautifulSoup(html)
results_table = soup.find('table', attrs={'class': 'resultsTable'})
output_list = []
for tr in results_table.findAll('tr'):
    row_list = []
    for td in tr.findAll('td'):
        row_list.append(td)
    output_list.append(row_list)
```




