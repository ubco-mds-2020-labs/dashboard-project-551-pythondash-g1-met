# DATA 551 - Dashboard Proposal

### Mitch, Thomson, Eric
February 27, 2021

### Section 1: Motivation and Purpose

Our Role: Data Scientist public advisory group

Target audience: Canadian and United States public

The public in the United States and Canada want to understand the status of Coronavirus vaccination programs. In Canada, as of February 27th 2021, vaccine administration has lagged behind the United States on a per capita basis. As a result, the Canadian government has come under increasing scrutiny. Coronavirus has widespread impact on peoples mental health, job status, and daily lives. Those eager to resume normal acitvities, or those fearful of the current vaccination trajectory find themselves relying on traditional forms of media to try and extract the 'big picture'of vaccination status. Having vulnerable family members ourselves, we've seen the impact the 'daily check' of Coronavirus media can have on people. We felt this was an oppertunity to create a dashboard that displays relevant Coronavirus numbers, without sensationalism. Our mission is to enable people to stay informed on a frequency of their choosing, but also to allow them to unplug from traditional media, which can be mentally taxing in an already stressful time.

A secondary purpose of our dashboard is to leverage data to reflect on the impact anti-vaccination sentiment has on the vaccination process. At the time of writing, local governments aren't struggling to find willing parties to be vaccinated. However, due to longstanding media coverage of so called 'anti-vaxxers', there is reason to believe that eventually, different local governments will vaccinate everyone willing to be vaccinated. As a return to our previous way of life is contingent on widespread vaccination and the development of herd immunity, it will be valuable for people to identify areas with lower per capita vaccination, so they can be more informed for voting, traveling, or where they may want to live.

Historically, Canadians tend to compare ourselves with the United States. However, all the existing mainstream tools and dashboards tend to focus on regional or national status updates. Our hope is to build out a dashboard that shows a comparison between Canada and the United States that enables people to stay informed.



### Section 2: Description of the Data

We will be visualizing a dataset that is updated approximately every day. As of February 27th 2021, the dataset features 2995 rows of Coronavirus vaccination data. Each row represents one State, Province or Territory (location) reporting vaccination numbers to the public for a given day. Each reporting instance (row) features 14 variables. We sourced some recent population estimates from government sources to allow for per-capita comparisons between regions with vastly different populations. This column is derived from dividing the sum of the total vaccinations ('total_vaccinations_int') and dividing by the sum of ('pop_est').




### Section 3: Research questions and usage scenarios

*The purpose of this section is to get you to think about how your target audience might use the app you’re to designing and to account for those needs in the proposal.*

High-level Research Questions:
1) What percentage of people have been vaccinated in my or my family members' state, province, territory, region, or country?
2) How does Canada compare to the United States in terms of their vaccine rollout on a per capita basis?
3) How does vaccine distribution and administration over time compare between specific states, provinces, territories, regions, and countries?

Joan is a Canadian citizen in her early sixties with a history of smoking and very basic computer skills that allow her to use search engines and GUIs. She knows she's in a high-risk group for severe COVID-19, but is not yet near the top of the vaccination piority list for her region. She also worries about her grown children living far away from home, who will be very low on the priority list. She likes to \[research\] the current vaccine rollout, and \[check progress\] daily. She wants a single, easily digestible source for up-to-date information on the localities where her friends and family live across Canada and the US. She also wants to \[compare\] national and regional differences in vaccination rollout progress to judge her political leaders. Joan also wants to \[review]\ the history of the rollout in different regions to get a sense of how quickly progress was made and whether it is accelerating in the areas where her loved ones live. When she opens the dashboard in her web browser, she will see a map of Canada and the US with colors representing the total population-adjusted vaccination rate for each state and province as well as summary stats and charts. When she clicks into a locality of interest, the dashboard map will zoom in and then show a time-series of the local rollout process, more locally-focussed stats, and some model predictions of vaccination completion timelines based on current progress.

### Section 4: Description of you app and sketch

The dashboard contains a landing page that shows a choropleth map of the current US and Canada surrounded by key numbers and x-y plots of our key variables. The map has colour encoding the current population-adjusted cumulative vaccination rate. There is an interactive a line-plot showing the percent vaccination rate for a single geographical locality, such as a state, province, or region. From a drop-down list, users can filter for localities of interest, and there is a slider to select date ranges to display. Similarly, the choropleth map has a date range slider and drop-down menus to select variables of interest to encode in color. There is an area displaying key numerical indicators for each nation. These include the total and per-capita number of vaccine doses distributed and injected, as well as the percent of total popolation remaining, and the rate of vaccine dose delivery and injection. This will also be customized by the locality-selection drop-down menu. There will also be time-series plots to compare vaccination rates between the different regions and localities, as well as between the two nations. The choropleth map will also be interactive, with each state/province being clickable. Once selected, the map will zoom into that locality. Then the surrounding plots and numbers will adjust to reflect similar vizualizations of more locality-specific data, as well as comparisons to the two national averages.