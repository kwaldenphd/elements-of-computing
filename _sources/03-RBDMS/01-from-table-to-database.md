# From Table to Database

Let's imagine we want to know how many professional baseball players that were born in Puerto Rico played for teams located in the state of Indiana during the 2016 season.

Our first step is to break down the different components of this research question, with an eye toward what data we would need to answer this question.
- We would need to have a list of people who played professional baseball during the 2016 season.
- We would need to know country birthplace information for everyone on that list.
- We would need to know what professional teams were located in Indiana during the 2016 season.
- We would need to know which players were on specific teams 

Our next step is to possible sources or resources that might provide this data. [Baseball Reference](https://www.baseball-reference.com/), "the complete source for current and historical baseball players, teams, scores and leaders," seems like a good place to start.

We could start by looking up the records for an individual player to see what information is available. Let's take a look at the [individual player page on Baseball Reference](https://www.baseball-reference.com/players/s/samarje01.shtml) for former Notre Dame baseball and football player Jeff Samardzija.

<p align="center"><a href="https://github.com/kwaldenphd/data-models/blob/main/figures/Figure_2.png?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/data-models/blob/main/figures/Figure_2.png?raw=true" /></a></p>

<p align="center"><a href="https://github.com/kwaldenphd/data-models/blob/main/figures/Figure_3.png?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/data-models/blob/main/figures/Figure_3.png?raw=true" /></a></p>

We can get some pieces of information from this page, like player birthplace and teams played for. But not all of that information is located in a table structure. And the table structure that is present doesn't lend itself to answering our specific research question.

We could also look at the individual team page for a team located in Indiana. Let's take a look at the [2019 season team page](https://www.baseball-reference.com/register/team.cgi?id=a87c825c) for the South Bend Cubs.

<p align="center"><a href="https://github.com/kwaldenphd/data-models/blob/main/figures/Figure_4.png?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/data-models/blob/main/figures/Figure_4.png?raw=true" /></a></p>

<p align="center"><a href="https://github.com/kwaldenphd/data-models/blob/main/figures/Figure_5.png?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/data-models/blob/main/figures/Figure_5.png?raw=true" /></a></p>

We can get some pieces of information from this page, like the team location and roster. But again, not all of that information is located in a table structure. And the table structure that is present doesn't lend itself to answering our specific research questions.

Since there are only 3 affiliated professional teams in Indiana, manually downloading the spreadsheets for these teams for a single season and wrangling the data into the structure needed to answer our specific research question wouldn't be overly time intensive. But let's say we might have other research questions down the line, or we might want to make our data available to other researchers. 

Only gathering data that responds to our specific research question might save time in the short term but foreclose possibilities long-term. Imagine the types of research questions we could ask and answer with data that covered multiple seasons, for teams in multiple locations.

We could do some automated scraping and manual wrangling to end up with data structures that answer our specific research question but also would work to answer a variety of other research questions.

Let's imagine.....

A `players` table that includes information about where players were born. 

<div class="mmt-custom-content col-lg-6 col-sm-12"><table><tbody><tr><td>personID</td><td>DoB</td><td>locationID</td></tr><tr><td>1</td><td>1985</td><td>SanPedrodeMacoris_SanPedrodeMacoris_DO</td></tr><tr><td>50</td><td>1969</td><td>Santurce_PR</td></tr><tr><td>63</td><td>1989</td><td>Bani_Peravia_DO</td></tr></tbody></table></div>

A `teams` table that includes information about affiliations.

<div class="mmt-custom-content col-lg-6 col-sm-12"><table><tbody><tr><td>teamID</td><td>season</td><td>affiliateLeague</td><td>affiliate</td><td>league</td><td>teamName</td><td>class</td><td>locationID</td></tr><tr><td>1960_AmericanAssociation_Indianapolis</td><td>1960</td><td>National</td><td>PHI</td><td>American Association</td><td>Indianapolis</td><td>AAA</td><td>Indianapolis_IN_US</td></tr><tr><td>1960_Midwest_Kokomo</td><td>1960</td><td>National</td><td>LAD</td><td>Midwest</td><td>Kokomo</td><td>D</td><td>Kokomo_IN_US</td></tr><tr><td>1961_AmericanAssociation_Indianapolis</td><td>1961</td><td>National</td><td>CIN</td><td>American Association</td><td>Indianapolis</td><td>AAA</td><td>Indianapolis_IN_US</td></tr></tbody></table></div>

A `locations` table that includes additional information about locations.

<div class="mmt-custom-content col-lg-6 col-sm-12"><table><tbody><tr><td>locationID</td><td>city</td><td>state</td><td>country</td><td>region</td><td>group</td><td>lat</td><td>lon</td></tr><tr><td>Abbeville_LA_US</td><td>Abbeville</td><td>LA</td><td>US</td><td>Northern America</td><td>Northern America</td><td>31.571835</td><td>-85.250489</td></tr><tr><td>Abbeville_SC_US</td><td>Abbeville</td><td>SC</td><td>US</td><td>Northern America</td><td>Northern America</td><td>34.178172</td><td>-82.379015</td></tr><tr><td>Abbotsford_BC_CA</td><td>Abbotsford</td><td>BC</td><td>CA</td><td>Northern America</td><td>Northern America</td><td>49.05</td><td>-122.3</td></tr><tr><td>Aberdeen_MD_US</td><td>Aberdeen</td><td>MD</td><td>US</td><td>Northern America</td><td>Northern America</td><td>39.509556</td><td>-76.16412</td></tr></tbody></table></div>

A `transactions` table that includes information about which players played on specific teams in a given season.

<div class="mmt-custom-content col-lg-6 col-sm-12"><table><tbody><tr><td>personID</td><td>teamID</td></tr><tr><td>25</td><td>1999_International_Indianapolis</td></tr><tr><td>125</td><td>2013_International_Indianapolis</td></tr><tr><td>125</td><td>2014_International_Indianapolis</td></tr></tbody></table></div>

Let's take a look at at Excel workbook that includes these tables. Open the [Google Sheets project](https://docs.google.com/spreadsheets/d/1x40S3DSv5EzwPqma7ivsZIk92fre0Uj1IWhuozYO4pM/edit?usp=sharing) in a spreadsheet program (Google Sheets, Microsoft Excel, Apple Numbers).

You may need to consult the following resources as needed to understand this data:
- [ISO 3166 country code table (Wikipedia)](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2#Decoding_table)
- [United Nations geographic regions](https://unstats.un.org/unsd/methodology/m49/)
- [USPS list of state abbreviations](https://about.usps.com/who-we-are/postal-history/state-abbreviations.htm)
- [Wikipedia list of baseball team abbreviations](https://en.wikipedia.org/wiki/Wikipedia:WikiProject_Baseball/Team_abbreviations)
- [Wikipedia glossary of baseball jargon](https://en.wiktionary.org/wiki/Appendix:Glossary_of_baseball)

So now that we have some structured data, let's return to our original research question. 
- The `players` table includes information about where players were born. 
- The `teams` table includes information about teams. 
- The `locations` table includes additional location information.
- The `transactions` table tells us which players played for which teams. 

But the `transactions` table on its own doesn't include the information about player birthplace and team location we need to answer the question of how many baseball players born in Puerto Rico played for teams located in the state of Indiana. We could add that location information to the `transactions` table, but we would end up with significant redundant and duplicate information.

Behold the magic of relational databases!