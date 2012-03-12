---
layout: page
title: "Unit 1: Understanding, finding, and making use of public data"
---
{% include JB/setup %}

# April 2 - 9, 2012


**Table of contents**

* This will become a table of contents (this text will be scraped).
{:toc}


## What exactly _is_ "public data"

You may already be familiar with this term, or it may be new to you. In either case, it will be helpful for us to come to a shared understanding of what "public data" means in the context of this course. 

The term public data is broadly understood to refer to information about the world around us that is made available for people to view and make use of. This could be information about our lives, or the lives of our neighbors -- such as court documents, vehicle registrations, election-related records like voting or campaign contribution history -- or knowledge about the world we live in, for example [cenus data](), environmental data like [historical weather information](), or geographic data like [bike paths]() or public parks. Typically, this information is "non-sensitive, unclassified, not copyrighted, and viewable by everyone."

In contemporary terms, public data has evolved to imply something more specific: information that is collected about "the public" or "in the public good" that is published or released in its rawest form. Examples of this are abundant today, and they encompass everything from large-scale efforts by national governments to publish the data they collect, like [Data.gov](), [Data.gc.ca](), and [Data.co.uk](), all the way down to municipal initiatives, like police forces releasing their [crime report data](http://data.dc.gov/), fire departments releasing their [incident data](http://data.sfgov.org/Fire/Fire-Incidents/i69v-qbqc), and transit organizations publishing [real-time information about vehicle arrival times](http://www1.toronto.ca/wps/portal/open_data/open_data_item_details?vgnextoid=4427790e6f21d210VgnVCM1000003dd60f89RCRD&vgnextchannel=6e886aa8cc819210VgnVCM10000067d60f89RCRD).

Public data is increasingly not limited to information collected by governments and public-benefit organizations; more and more public data is also being collected and published by private companies in the course of their work. Some obvious examples would be the micro-blog service [Twitter](), the photo-sharing site [Flickr](), the location-sharing site [Foursquare](), or the influence-measuring site [Klout](). Often this data is made available to software developers and computer programmers via an Application Programming Interface, or API, and benefits the company in some way when it's used by those developers, often in novel and creative ways that the company did not consider.

However, unlike these technology-centric companies that are providing data in the form of APIs that can be consumed easily by computer programs, much of the public data that is published by governments and their agencies is not provided in a format that is easy to explore or re-use. For example, until very recently -- the last two or three years -- a significant amount of public data was published as HTML pages, or -- worst yet -- put online as Microsoft Word or Excel documents, or as Adobe PDF documents. To many, the value of public data is greatly reduced -- or, at least, inhibited -- when the information is published in formats that are considered to be inaccessible. Further, a significant percentage of publicly available data provided by governments is still published in a summary, aggregate, or sanitized form, which can limit its usefulness if the line of inquiry requires the original documents or raw numbers.

So, while there have been huge advances in the world of public data over the last few years -- the organizations publishing it, the breadth of information published, frequency of updates, etc. -- there is still a lot of room for improvement in terms of how the data is provided, how easy it is to find, and how soon it is published. 

**Public data has the positive potential to open our eyes to the world around us, and the negative potential to give those who already have societal advantages the resources to outsmart those that are less savvy.**

FOIA / ATIP 
Public data that isn't published data.

## Public data vs. Open Data

There is another term that is often used synonymously with public data: [open data](https://en.wikipedia.org/wiki/Open_data). However, public data is not necessarily open data, by definition. The distinction is subtle, but important: 

> Open data is the idea that certain data should be freely available to everyone to use and republish as they wish, without restrictions from copyright, patents or other mechanisms of control. -- [Open Data on Wikipedia](https://en.wikipedia.org/wiki/Open_data)

There are many common understandings of the term open data, but the thematic consensus is roughly that open data is information that is _explicitly_ licensed in such a way that it bestows certain freedoms on the users of the information, specifically the freedom to republish and reuse the data.

There are a wide range of open licenses available for publishers to choose from, and each comes with its own nuances -- such as, the requirement to provide attribution or for the user of the data to "share alike" -- but generally, if the license provides the rights outlined above, it is considered open data. There's a good list of [open content licenses on Wikipedia](https://en.wikipedia.org/wiki/Open_licenses#Licenses) and the [Open Knowledge Foundation](http://okfn.org/) has [a helpful outline of the key freedoms](http://opendefinition.org/okd/) that should be a part of any such licenses.

To provide a concrete example, some of the "public data" in countries like Australia, Canada, and the United Kingdom is publicly _available_ but falls under [Crown Copyright](https://en.wikipedia.org/wiki/Crown_copyright). What this means in practice is that some information, like [looking up an electoral riding by postal code (zip code)](http://www.digital-copyright.ca/node/1060), is ostensibly "public" by its very nature, but can also be costly to obtain and provided under a very restrictive End User License Agreement (EULA). Historically, in Canada, to obtain an up-to-date database mapping postal codes to electoral ridings required one to license the data from Statistics Canada at a cost of $2900 CAD / annually. Many open-data advocates propose that all data collected by public agencies, in the public interest, and made possible by public tax dollars, should be both public in the general sense (available) and public in the open data context (free of limitation on its use).

Either way, it will be important for you to consider the license of the data that you encounter during this course, and to be able to make the distinction between open data and public data. 

<div class="alert alert-info">

<p><i class="icon-info-sign">&nbsp;</i>&nbsp;&nbsp;
The open-data movement is often considered to be part of a larger "[open everything]()" movement, which has roots in the [Free Software movement]() that started in the 1960s. To many, the crux of the movement is a question of licensing and freedoms -- and sometimes the format of the data -- not necessarily the push to open the data in the first place. We won't be delving into this debate during the course, but we will be embracing the spirit of these movements by focusing on free software for our exercises.
</p>
</div>


## Data vs. Big Data

While we're exploring what public data is and isn't, let's add another term to the mix: [big data](https://en.wikipedia.org/wiki/Big_data).

> In information technology, big data consists of datasets that grow so large that they become awkward to work with using on-hand database management tools. Difficulties include capture, storage, search, sharing, analytics, and visualizing. -- [Wikipedia page on Big Data](https://en.wikipedia.org/wiki/Big_data)

Public data is not necessarily big data, but -- to an extent -- the class of public data that falls toward the big data end of the spectrum is what we're going to focus on in this course because of the inherent challenges that one encounters when working with it, and the learning opportunities that those challenges provide.

So, what exactly is big data? Well, somewhat obviously, big data is by definition **big**. Typically, this term refers to datasets so large that it is difficult, if not impossible, to work with them using standard data-processing tools, like traditional database tools or statistics packages. In practice, this term is used for data sets that are gigabytes or more in size, or data sets that update extremely rapidly like the [Twitter fire hose](). We won't be working with this kind of big data during the course -- as the challenges it presents are a bit too unique to be broadly applicable to your day-to-day work -- but we will look at data sets that are considered large, and I'll point you to some resources for making the jump to really-big data.

For the purposes of this course, we're going to define big data (or big-ish data) as the moment when spreadsheets start to fail us. 

Until quite recently, much of the spreadsheet software available to us -- while an indespensible tool of the data cruncher! -- was limited to about 65,000 rows of data. As of the time of this writing, newer spreadsheet software like [Google Spreadsheets]() is limited to 400,000 cells (that would be roughly 20,000 rows of data if you had 20 columns in your sheet) or 20MB of data, and other tools like Google Fusion Tables are limited to roughly 100MB of data per table. At first these may not seem like limits to worry about, but -- in practice -- it is not uncommon to run up against these limits when dealing with real-world data. 

Newer versions of Microsoft Excel have increased the row limit to 1,000,000, as well as contemporary versions the popular free software spreadsheet option -- [Open Office Calc](http://en.wikipedia.org/wiki/OpenOffice.org_Calc) -- which have reportedly increased the limit to roughly 1,000,000 rows also. Nonetheless, modern-day data dumps by organizations like Wikileaks can start to push our existing tools to the limits. Take for example the [Afghan War Diary](http://www.wikileaks.org/wiki/Afghan_War_Diary,_2004-2010) at almost 400,000 rows of data, or the recently released [Stratfor data](http://www.washingtonpost.com/business/technology/wikileaks-publishes-e-mails-from-stratfor-intelligence-firm/2012/02/27/gIQA3rrndR_story.html) that is reported to be between two and five million e-mail messages.

As Tim O'Reily recently said "TK," we're swimming in data -- vast, vast amounts of data -- and that reality is only going to increase.

## What data _can_ and _cannot_ help you with

Data is rarely going to write a story or expose an problem on its own, and vice-versa there's rarely the perfect data set available to answer your research question one hundred percent. So, if the data doesn't provide the story, and if the story won't necessarily be able to rely on supporting data, the question is: **where do you start and how does data fit into the picture.**

The answer lies somewhere between investigation and exploration, between specific questions that you want to understand more clearly and a genuine curiosity about the world around you. The experienced data cruncher is both seeking to shine a light on a broad range of questions and looking broadly for questions that have not yet been asked.

> Instead of just saying "here is some data" figure out how to tell a story with it -- Amanda Cox, New York Times Graphics Editor, [@NYTGraphics](http://twitter.com/nytgraphics)

In [Amanda's lecture]() (you watched it, right?), she describes four opportunities for using data to:

* Reveal patterns
* Provide context
* Compare scales
* Describe geography

In addition to the examples in Amanda's lecture that illustrate these opportunity, I've provided three case studies below to provide you with some inspiration and a sampling of the type of data crunching that we're going to do over the next three weeks.

Specifically, we're going to try to understand how:

* Too much data can be like noise, where the signal and patterns are impossible to discern
* Data in the abstract, taking out of historical context, can be misleading. Context is important when exploring and presenting data, so try to keep the question "compared to what" in mind.
* Data can often help you understand an issue more clearly, or -- on the contrary -- can completely contradict your assumptions. Be prepared for both. 

Data crunching, at its very best, can potentially help you present a challenging, difficult, or contrary point-of-view with the support of numbers and analysis that is ostensibly objective. It can also help you to see trends that might not be visible otherwise; for example, by aggregating several local databases into one regional database. 

<div class="alert alert-info">

<p><i class="icon-info-sign">&nbsp;</i>&nbsp;&nbsp;
Infobox on sketching with data. TK.
</p>
</div>

## Case studies of public data in action

The following case studies where chosen for their exemplary demonstration of a specific type of public data crunching and presentation. In each case, the data was found in a different, the data was explored and cleaned, and -- ultimately -- it was published in a novel or new way that provided insight that wasn't visible previously. 

I hope that these example provide some inspiration for your own exploration that you'll be undertaking in the coming weeks.

### Dollars for Docs: How Industry Dollars Reach Your Doctors (document diving)

> Drug companies have long kept secret details of the payments they make to doctors and other health professionals for promoting their drugs. But 12 companies have begun publicizing the information, some because of legal settlements. ProPublica pulled their disclosures into a database so patients can search for their doctor. Accepting payments isn’t necessarily wrong, but it can raise ethical issues.

* [Dollars for Docs: How Industry Dollars Reach Your Doctors](http://projects.propublica.org/docdollars/)
* [The Coder’s Cause in “Dollars for Docs”](www.propublica.org/nerds/item/the-coders-cause-in-dollars-for-docs)

### Making Water a Matter of Race (mapping)

> To this day, Jerry Kennedy only does laundry when it rains. For the first 54 years of his life, he lived without running water, and rainstorms were the only way he could collect enough water to wash his clothes. But Kennedy isn't from some far-off rural outpost. He was born and raised in the Coal Run neighborhood of Zanesville, Ohio — a former coal-mining center of 25,000 in the eastern part of the state — just a few hundred feet from a municipal water line. Kennedy, now 58, is black. His neighbors, who did not have running water for more than 50 years, are also black. On July 10, the U.S. District Court of Ohio awarded them almost $10.9 million, ruling that they had been denied access to public water because of their race.

* [Making Water a Matter of Race](www.time.com/time/nation/article/0,8599,1822455,00.html)
* [The Revolution Will Be Mapped](http://www.miller-mccune.com/culture/the-revolution-will-be-mapped-7130/)

### Case 3 TK (network analysis)


## What to keep in mind as you start your investigation

As you start brainstorming your line of investigation (Challenge No. 2), you should keep the following tips in mind:

* Stay focused on questions that personally interest or excite you
* Avoid questions that are too complicated to explain quickly and easily (try to simplify them)
* Be nimble: generate lots of possible avenues of exploration, and be willing to back burner ideas that face significant roadblocks

## Where to start looking for publicly available data

To get started with your search, you might want to look for data that is published by government organizations or non-governmental organizations -- as calls for "open government" and transparency grow, more and more data is available from these organizations. For example, you could explore:

* Local: Does your town or city's agencies publish data? For example, you might want to look into data from departments like police, fire, corrections, or health and safety. City and town council are also an excellent source of data, for example from council meetings, expenses, or budgets. Other local public records could include land ownership, taxes, court proceedings, etc.

* State/Provincial/Regional: Some data sets are going to be under the jurisdiction of state or provincial agencies. In Canada, for instance, hospital and health data is collected at the provincial level. In the US, state-level agencies are responsible for public health, education, employment and more.

* National: National open data initiatives in Canada, the US, and the UK are good examples of efforts that some countries are putting into publishing the data they collect. These datasets can provide a good overview/aggregate look at national statistics, but often lack a level of detail to be genuinely interesting on their own. That said, national agencies like [Statistics Canada]() or the [U.S. Census Bureau]() can help to provide genuine insight into a country's "identity." National agencies are also typically responsible for [geodata](), which can be an important piece of putting your data "on the map" so to speak. 

* Global: There are also a handful of quasi-government bodies and international NGOs that publish data that is aggregated at a global level. Some examples would be the [World Bank](http://data.worldbank.org/), [United Nations](http://data.un.org), and the [World Health Organization](http://www.who.int/research/en/).

## Public and open data starting points

Here's a [growing list of starting points for public data / open data investigations](https://docs.google.com/document/d/1U-85AiKMnBIXfWj5FL43ms60U9H09r-TTdJyTV5Apww/edit). You can start here, or you can start by searching for data that's specific to your line of inquiry. If you decide to conduct your own search, please contribute back links to the sites where you find your data, or links to the datasets that you've found.

## Where to go from here

* Challenge No. 2: Propose investigations: questions that you want to answer (Est. 2 hours)
* Challenge No. 3: List data sets that might be useful to your investigation (Est. 1 hour)


