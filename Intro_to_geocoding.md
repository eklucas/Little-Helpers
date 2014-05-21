Intro to Geocoding
=======================


- [**What is geocoding?**](https://github.com/eklucas/Little-Helpers/blob/master/Intro_to_geocoding.md#what-is-geocoding) 
- [**Why geocode?**](https://github.com/eklucas/Little-Helpers/blob/master/Intro_to_geocoding.md#why-geocode)
- [**When to geocode**](https://github.com/eklucas/Little-Helpers/blob/master/Intro_to_geocoding.md#when-to-geocode)
- [**Things to consider**](https://github.com/eklucas/Little-Helpers/blob/master/Intro_to_geocoding.md#things-to-consider)
- [**Available tools**](https://github.com/eklucas/Little-Helpers/blob/master/Intro_to_geocoding.md#available-tools)
- [**Our recommendation**](https://github.com/eklucas/Little-Helpers/blob/master/Intro_to_geocoding.md#our-recommendation) 


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


[Take me back to the top](https://github.com/eklucas/Little-Helpers/blob/master/Intro_to_geocoding.md#intro-to-geocoding)
###_Things to consider_


[Take me back to the top](https://github.com/eklucas/Little-Helpers/blob/master/Intro_to_geocoding.md#intro-to-geocoding)
###_Available tools_


[Take me back to the top](https://github.com/eklucas/Little-Helpers/blob/master/Intro_to_geocoding.md#intro-to-geocoding)
###_Our recommendation_


[Take me back to the top](https://github.com/eklucas/Little-Helpers/blob/master/Intro_to_geocoding.md#intro-to-geocoding)
