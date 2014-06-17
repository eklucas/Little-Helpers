Web scraping with Helium Scraper
=================================
```by Liz Lucas```

- [**Intro to web scraping and Helium**](https://github.com/eklucas/NICAR-Help/blob/master/Intro_to_Helium_Scraper.md#intro-to-web-scraping-and-helium)
- [**Planning your scrape**](https://github.com/eklucas/NICAR-Help/blob/master/Intro_to_Helium_Scraper.md#planning-your-scrape)
- [**Helium terminology: Kinds, Actions and Data**](https://github.com/eklucas/NICAR-Help/blob/master/Intro_to_Helium_Scraper.md#helium-terminology-kinds-actions-and-data)
- [**Translating your plans into a scraper**](https://github.com/eklucas/NICAR-Help/blob/master/Intro_to_Helium_Scraper.md#translating-your-plans-into-a-scraper)
- [**Legal and ethical considerations**](https://github.com/eklucas/NICAR-Help/blob/master/Intro_to_Helium_Scraper.md#legal-and-ethical-considerations)

###_Intro to web scraping and Helium_

We've all visited websites that contain valuable information we want to analyze, such as [inspections reports](http://www.gocolumbiamo.com/webapps/cfforms/health/health_inspections.cfm), [lobbying expenditures](http://ethics.la.gov/LobbyistData/SearchByFinancialDisclosure.aspx), or a [list of jail inmates](https://www.showmeboone.com/sheriff/JailResidents/JailResidents.asp). 

We're grateful for the [growing movement](http://theodi.org/about-us) among [government agencies](https://nycopendata.socrata.com/) (particularly [federal](www.consumerfinance.gov/hmda) ones) to provide what we all want to see: the **DOWNLOAD** button. 

But not everyone is there yet. 

So when we can't download or copy and paste what's there, we have to give up or figure out how to literally _scrape_ the info off the website and into a database, a spreadsheet, or something we can actually use.

Imagine tackling this site: [https://apps.sd.gov/st12odrs/LobbyistViewlist.asp?cmd=resetall](https://apps.sd.gov/st12odrs/LobbyistViewlist.asp?cmd=resetall). If you wanted to end up with a spreadsheet of registered lobbyists, how would you do it? 

A web scraper is simply a [piece of software](http://www.heliumscraper.com/), a [bit of code](http://docs.python-guide.org/en/latest/scenarios/scrape/), or a [browser plugin](https://chrome.google.com/webstore/detail/scraper/mbigbapnjcgaffohmbkdlecaccepngjd?hl=en) that does the work for us, preferably while we go have a beer. 

[Helium Scraper](http://www.heliumscraper.com/) is a $99 piece of software (for Windows only) that provides a point-and-click interface for web scraping so that you don't have to write something like this: 

```python
soup = BeautifulSoup(html)
results_table = soup.find('table', attrs={'class': 'resultsTable'})
output_list = []
for tr in results_table.findAll('tr'):
    row_list = []
    for td in tr.findAll('td'):
        row_list.append(td)
    output_list.append(row_list)
```

###_Planning your scrape_

So back to that question: how would you do it? 

On [this page](https://apps.sd.gov/st12odrs/LobbyistViewlist.asp?cmd=resetall) we can search for a particular lobbyist, but to get information on ALL of the lobbyists we need to click "Show All." We immediately get a page full of information: Year, Lobbyist Name, Address, etc. If we want to create a spreadsheet of these lobbyists, we'd probably try copying and pasting these rows into Excel. When we scroll to the bottom of the page we notice that this is one of 406 pages. That's a lot of copying and pasting. 

With Helium, though, we can create a simple program to do all that automatically. First we'll make it click "Show All", then scrape all the data. Then it will click the little arrow leading to the next page, and scrape all _that_ data. And so on, 406 times. 

When you're getting ready to set up a web scraper, think through what steps you would do and then figure out how to make the computer do those things. 

###_Helium terminology: Kinds, Actions and Data_

Helium Scraper helps you build a web scraper using a point-and-click interface that operates with two general concepts: kinds and actions. **"Kinds"** are the pieces of the website you'll need the scraper to act on. Think of them as building blocks. **"Actions"** are what we create to arrange those building blocks in a particular order. 

For example, we need the scraper to click "Show All" before it can scrape any data. First we have to tell the scraper how to recognize the "show all" button by creating a `kind`, and we tell it to actually click the button by creating an `action`. 

Additionally, we want to create a `kind` for each column of data we want: year, name, address, etc. That way the scraper can recognize the pieces of data we want. The `action` we'll create is to take those `kinds` and extract them to a table. 

The result of the scrape is the **data**, which Helium Scraper stores in a database that you can query. You can also export the data as a Microsoft Access database.

These are the basic steps, but Helium Scraper has a lot of additional functionality. For example, you can make the program wait between each click, which is helpful because certain web browsers or web pages won't allow you to make too many requests too quickly. You can also send the results of your scrape to different tables if you want to create a relational database. 

###_Translating your plans into a scraper_


###_Legal and ethical considerations_

