# DATA 551 - Dashboard Proposal

### Mitch, Thomson, Eric
February 27, 2021


### Section 1: Motivation and Purpose

Our Role: Data Scientist public advisory group

Target audience: Canadian and American public

The status and progress of the COVID-19 vaccination rollout is of great public interest. Thus far, Canada's progress has lagged behind that of the United States on a per-capita basis. This has led the current administration to come under increasing scrutiny, as the public grows eager for a return to normalcy after enduring almost a full year of the pamdemic. This creates a need for easy access to hard data on vaccination progress.

We felt that creating a comprehensive dashboard outlining the state and provincial-level vaccination rollout across both Canada and the US would give the public a way to keep themselves informed on this important issue without having to sift through traditional news media coverage. By including data for both Canada and the US in one place, users will be able to not only compare how their state/province is doing relative to the national average, but also how their nation as a whole is doing in comparison to their neigbhor. Given that Canada is often compared against the United States, we feel that our dashboard will add value in comparison to what currently exists by including detailed data for both nations in one place.

Beyond this, such a dashboard could eventually be used to reflect on the impact of anti-vaccination sentiment on vaccine administration. While the main constraint is currently supply, as COVID vaccines become more widely available in the coming months, questions surrounding the public's willingness to take a vaccination will become relevant. Given that a more complete return to normalcy is predicated on achieving herd immunity through widespread vaccination, it will be useful to offer individuals an easy way to compare administration rates across different localities.


### Section 2: Description of the Data

We will be creating our dashboard using data sources that are updated approximately every day. We have written a script which checks these sources every hour and automatically includes any new data in our dashboard. We currently have daily time-series data on the total number of vaccinations administered as well as distributed for each state/province (contained in the `total_vaccinations_raw` and `total_distributed_raw` columns) spanning from 1/12/21 onward (putting the current size of our dataset at about 2000 rows). We are computing population-adjusted figures by dividing the `total_vaccinations_raw` column by the `pop_est` column, which contains the population estimates for each state/province. We have also computed the 7-day rolling mean of the daily change in vaccinations for each locality (contained in the `daily_vaccinations_rolling` column), allowing us to examine trends in the pace of vaccinations across different geographic areas. Each row of our dataset represents a particular state/province at a particular date.


### Section 3: Research questions and usage scenarios

*The purpose of this section is to get you to think about how your target audience might use the app you’re to designing and to account for those needs in the proposal.*

High-level Research Questions:
1) What percentage of people have been vaccinated in my or my family members' state, province, territory, region, or country?
2) How does Canada compare to the United States in terms of their vaccine rollout on a per capita basis?
3) How does vaccine distribution and administration over time differ between specific states, provinces, territories, regions, and countries?

Joan is a Canadian citizen in her early sixties with a history of smoking and very basic computer skills that allow her to use search engines and GUIs. She knows she's in a high-risk group for severe COVID-19, but is not yet near the top of the vaccination piority list for her region. She also worries about her grown children living far away from home, who will be very low on the priority list. She likes to \[research\] the current vaccine rollout, and \[check progress\] daily. She wants a single, easily digestible source for up-to-date information on the localities where her friends and family live across Canada and the US. She also wants to \[compare\] national and regional differences in vaccination rollout progress to judge her political leaders. Joan also wants to \[review]\ the history of the rollout in different regions to get a sense of how quickly progress was made and whether it is accelerating in the areas where her loved ones live. When she opens the dashboard in her web browser, she will see a map of Canada and the US with colors representing the total population-adjusted vaccination rate for each state and province as well as summary stats and charts. When she clicks into a locality of interest, the dashboard map will zoom in and then show a time-series of the local rollout process, more locally-focussed stats, and some model predictions of vaccination completion timelines based on current progress.


### Section 4: Description of you app and sketch

Our dashboard will contain a landing page that shows a choropleth map of the United States and Canada containing the current population-adjusted cumulative vaccination administration for each state/province (as defined by the total number of vaccinations administered divided by population), as well as a slider allowing users to examine the map at a particular point in time. We also plan to include interactive line plots showing both the cumulative population-adjusted vaccination rates as well as the 7-day rolling mean of the daily chance in vaccinations for any given state/province, along with a comparison to the national average. We plan to allow users to select particular localities using either a drop-down menu or by clicking a particular region on the map. In addition to this, we plan to include high-level summary statistics for the overall vaccination progress of both the US and Canada to the right of our map. We also plan to include a section where users can make more detailed comparisons of specific metrics across specific localities, e.g. "Daily population-adjusted rolling mean of vaccination distribution for California vs. New York".