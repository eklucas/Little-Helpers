Intro to Geocoding
=======================
```by Liz Lucas```

- [**What is geocoding?**](https://github.com/eklucas/Little-Helpers/blob/master/Intro_to_geocoding.md#what-is-geocoding) 
- [**Why geocode?**](https://github.com/eklucas/Little-Helpers/blob/master/Intro_to_geocoding.md#why-geocode)
- [**When to geocode**](https://github.com/eklucas/Little-Helpers/blob/master/Intro_to_geocoding.md#when-to-geocode)
- [**Things to consider**](https://github.com/eklucas/Little-Helpers/blob/master/Intro_to_geocoding.md#things-to-consider)
- [**Things to look out for**](https://github.com/eklucas/Little-Helpers/blob/master/Intro_to_geocoding.md#things-to-look-out-for)
- [**Available tools**](https://github.com/eklucas/Little-Helpers/blob/master/Intro_to_geocoding.md#available-tools)


###_What is geocoding?_
Most of us have gotten data at one point or another that includes addresses; small business loans, lottery ticket winners, school test scores, and parking tickets are just a few examples of data that almost always include an address. Less often we get fields labeled "latitude" and "longitude."

In order to put addresses on a map, any mapping software needs those lat and long coordinates. When you enter an address into Google Maps, it quickly calculates the coordinates for that address and plots it on the map: that's *_geocoding_*.

Unfortunately, as reporters dealing with 1 million records (or even 100 records), entering addresses into a map one at a time isn't an option. Thankfully there are geocoding services out there that will geocode hundreds or thousands of addresses very quickly, and plenty will do it for free. These geocoding services take our data, geocode the addresses and tack on latitude and longitude to the end of our data file. From there we can load the data into a mapping program and map away!

[Take me back to the top](https://github.com/eklucas/Little-Helpers/blob/master/Intro_to_geocoding.md#intro-to-geocoding)
###_Why geocode?_
If you've got addresses and you want to create a map, you'll need to geocode. But why create a map at all? 

Creating a map from your data _may_ enable a type of analysis that can't be done in a spreadsheet or a database manager. If you're looking at parking ticket data, you can use SQL to group the number of tickets by street or zip, but those results will miss clusters that don't conform to streets or zips. By mapping those tickets, you might be see spatial relationships that aren't apparent by just looking at the columns and rows.

Another good reason to map is to post your mapped data online and let your viewers look through the data themselves, by zooming to their own streets and neighborhoods. When it comes to things like parking tickets, potholes, sewer systems and car accidents, most of us want to know how these problems relate to where we live, or the routes we regularly travel. 

[Take me back to the top](https://github.com/eklucas/Little-Helpers/blob/master/Intro_to_geocoding.md#intro-to-geocoding)
###_When to geocode_
You may find yourself with data that would benefit greatly from being plotted on a map, but you should answer a few questions about it before you try to geocode. 

1. What pieces of information do you have? The most important pieces of information are the street number, the street name and suffix (such as "St" or "Rd"), the street direction (such as "N"), and the zip code. If you're missing the zip code but you have city and state, your geocode _might_ work. Unfortunately street names are often repeated within cities, so to avoid confusion having the zip code is best.
2. How dirty is the data? If street names are commonly misspelled, or suffixes left off, then you may need to do some cleanup before you geocode. It's usually not helpful if you can only geocode half of your data because the other half is too messy. Save yourself some time and frustration and try to get your data as clean as possible before you attempt geocoding. 
3. Are addresses repeated in your data? If there are three parking tickets at one address, you don't want to geocode that address three times. The geocoding services we discuss below will often do some geocoding for free, but there are limits. Usually it's helpful to create a list of unique addreses from your data, and then join that list (after it has acquired latitude and longitude from the geocoder) back to your data.

[Take me back to the top](https://github.com/eklucas/Little-Helpers/blob/master/Intro_to_geocoding.md#intro-to-geocoding)
###_Things to consider_
Geocoding services are never perfect, and there are some things you should keep in mind when you're deciding whether to geocode and what service to use: 
 - Some geocoders won't geocode intersections (usually written this way: "9th St and Elm St" or "9th St / Elm St").
 - Sometimes geocoders can't get accurate coordinates for an address, so they'll [place addresses in the middle of a wider geography](http://www.vox.com/2014/4/21/5636040/whats-the-matter-with-kansas-and-porn), such as a county, state or even the country.
 - Sometimes geocoders are just not accurate. As Jacob Harris once put it: [_geocoding is often rubbish_](https://source.opennews.org/en-US/learning/distrust-your-data/). Don't be discouraged, just be careful. 

[Take me back to the top](https://github.com/eklucas/Little-Helpers/blob/master/Intro_to_geocoding.md#intro-to-geocoding)
###_Things to look out for_


[Take me back to the top](https://github.com/eklucas/Little-Helpers/blob/master/Intro_to_geocoding.md#intro-to-geocoding)
###_Available tools_


[Take me back to the top](https://github.com/eklucas/Little-Helpers/blob/master/Intro_to_geocoding.md#intro-to-geocoding)
