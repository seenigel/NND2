# NND2 Data, Fall 2018
## Finding, extracting, and working with hidden, messy, or non-existent data.
Permalink: 

## The hidden world of data
Last semester we talked about how data can enhance your story and and where you can go to find common data sources. 

This semester we're going to go deeper with our data analysis, but we're also going to look at what you do when data isn't readily available.

By the end of this semester you will know how to:

- File a Freedom of Information Act/Freedom of Information Law request 
- Pull simple website data into Google Sheets
- Convert simple PDFs into useable data
- Summarize a big dataset using a pivot table 

**Note**: These sessions will assume that you've learned the basics of data wrangling in Microsoft Excel or Google Sheets. If you need a refresher, last semester's notes are below:

- <a href="https://github.com/seenigel/NND1/tree/master/spring-2018/session2" target="blank">Basic Data Analysis in Google Sheets</a>

## Messy Data
In a perfect world, all the data we'd ever want to work with would be available in .xls (excel), .csv (comma separated value), or .tsv (tab separated values) formats. Those are files we can easily feed in to Excel or Google Sheets for data cleaning.

But we don't live in a perfect world. Often data will only be available on a website, with no option to download it at all. Other times, the only file that will be available for download is a .pdf file.

We can still work with those.

## Pulling Data Off A Website
The act of pulling data that's posted on a website off is called *scraping*. 

Whether or not you're allowed to scape a website's information comes down to that individual website's terms of service. (Make sure to read those!)

There are lots and lots of ways to scrape information off websites, with varying degrees of difficulty, but one of the easiest involves a simple command in Google Sheets: *importHTML*

What the importHTML command does is scan whatever website you're on for whatever type of HTML item you ask for and try to return it for you.

Here's the basic formula:

**=importHTML("URL", "ITEM-TYPE", NUMBER)**

- URL  = The url of the website you're trying to get data from
- ITEM - the HTML element you're trying to copy
- NUMBER - An actual number (from 0 to whatever), that represents the element. Because an HTML document contains lots of same items, you may have to experiment with the number until you get it right.

### Example:
- <a href="https://en.wikipedia.org/wiki/List_of_countries_by_population_(United_Nations)">Wikipedia Countries of the World list</a>

Let's say we wanted to get this list of countries into Google Sheets. This is pefect for the importHTML command.

Once we've got the data saved, copy all of it, open a new tab and select paste special > paste values only. 

Then go to work on your data analysis!

### Try on your own:
- <a href="https://www.basketball-reference.com/friv/free_agents.fcgi" target="blank">Here's a list of NBA Free Agents</a> 

I needed to use this data for the WSJ story the <a href="https://www.wsj.com/articles/nba-free-agency-billion-dollar-bear-market-1533048001" target="blank">NBA's Billion Dollar Bear Market</a>. Try pulling it into Google Sheets using importHTML.

## PDFs
PDF files are a pain in the neck. They're a data-presentation format, not a data analysis format, so they're not meant to get data pulled from them. And yet for some reason data is always given in PDF format. 

The NYPD, for years, only gave their <a href="https://www1.nyc.gov/site/nypd/stats/crime-statistics/borough-and-precinct-crime-stats.page" target="blank">weekly crime numbers</a> in PDF format.

Fortunately there is a good, free tool that can help us with that, as well.

<a href="http://tabula.technology" target="blank">Tabula</a> is a free app for Windows, Mac and Linux that lets you convert PDF tables into a useable format.

## Truly Hidden Data
These tools only work if the data is available on the web. What if it's not?

ASK FOR IT!

Remember, especially when dealing with a government agency, there are laws that require them to keep records of their official government activity. So if they have the records, you can ask to see them.

Example:
- DNAinfo Crime Blotter
The blotter is a precinct's arrest records. They don't show up in the compstat reports, but we were able to get them by building a good relationship with the police precinct and asking to see them each week. 

# What if they say no?
Well, then you can always file a Freedom of Information request.

Examples:

- <a href="https://www.dnainfo.com/new-york/20150422/bay-ridge/new-yorks-most-loud-sex-complaints-come-from-this-building-records-show/" target="blank">Loud Sex Complaints</a>

- <a href="https://www.dnainfo.com/new-york/20150202/washington-heights/map-see-how-often-green-cabs-stop-your-neighborhood/" target="blank">Green Cab Pickups</a>

- <a href="http://www.nydailynews.com/news/politics/lawsuit-forces-de-blasio-release-agents-city-emails-article-1.2885624" target="blank">de Blasio emails</a>

- <a href="https://www.dnainfo.com/new-york/20130919/inwood/troubled-la-marina-allowed-host-1800-people-shocking-neighbors" target="blank">La Marina occupancy</a>

## Next Data Session
We are going to talk more about FOILs and you're all going to file one.