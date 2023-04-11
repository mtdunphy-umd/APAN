# APAN
Second Year Project Files

### Elections in a Post-Roe Era: An Analysis of the 2022 Midterms Elections
#### By: Michael Dunphy

[Presentation](https://docs.google.com/presentation/d/1Q5DU93FQGAexcz5tzT6y5xHMizqD4dgvBXTKYxYBYxo/edit?usp=sharing) on the topic given at the University of Maryland, College Park on April 11th, 2023 as part of the Applied Political Analytics Master's Program.

##### TL;DR
This research uses data at the candidate and district level to understand the impact of the Dobbs decision on the 2022 U.S. Midterm elections at the U.S. House and U.S. Senate level. Two measurements were modeled, controlling for relevant factors, to track individual candidate performance: individual contribution fundraising after the Dobbs decision and candidate win probability. Two measurements were modeled, controlling for relevant factors, to track electoral performance at the district level: vote margin shift from the 2020 Presidential election and the probability of a Democrat winning based on district characteristics. It was found that states with higher salience of abortion, measured by Google Trends search data, increased Democratic candidate fundraising at both office levels. States that implemented abortion bans or were hostile towards abortion saw an increased shift in Democratic vote share from the 2020 Presidential election at both office levels. It is recommended that Democrats focus on the abortion issue in campaign and party messaging in the upcoming 2024 elections to increase candidate fundraising performance and raise awareness of bans and hostile policies toward abortion to mobilize pro-choice voters, increasing Democratic vote share. Recommended competitive House districts to implement this strategy include: AZ-1, AZ-6, IA-3, MI-10, MT-1, NE-2, and WI-3. Recommended competitive Senate races to implement this strategy include: AZ, WI, and PA.

##### Introduction
On June 24th, 2022, the United States Supreme court decided in Dobbs v. Jackson Women’s Health Organization that the U.S. constitution does not provide the right to abortion, overruling Roe v. Wade and Planned Parenthood v. Casey. This gave individual states the power to regulate any aspect of abortion not protected by federal law. Debate over the abortion issue increased with many states implementing trigger bans and several other states proposing policies hostile towards abortion. This made abortion a highly salient issue during the 2022 Midterm election cycle with many candidates discussing the Dobbs decision in campaign messaging. 

Political science research has shown that abortion can be considered an “easy issue” due to its persistence, salience, and ability to be easily understood election cycle to election cycle. The abortion issue has gradually transformed the political parties with elites polarizing on the issue with Democrats adopting the “pro-choice” policy position and Republicans adopting the “pro-life” policy position. This led to mass level polarization with voters sorting themselves along party lines on this issue. Previous research has shown that past Supreme Court decisions on abortion have had electoral impacts including influences on U.S. President, Senate, House, gubernatorial, and state legislature elections.

Given the surprising midterm election results with Democrats overperforming fundamentals and the high salience of abortion this election cycle, this research looks to address the question: what impact did the Dobbs decision have on the results of the 2022 U.S. House and U.S. Senate midterm elections?

##### Research Design
Four hypotheses were formed to test the electoral impact of the Dobbs decision:
- Increased salience of abortion will improve the performance for Democrats as pro-choice voters will be mobilized due to the loss of the constitutional right to an abortion
- Increased performance for Democrats in states that have banned or are hostile towards abortion
- Gender of candidates will be significant with women Democratic candidates overperforming since voters assume Democrats and women candidates to be more pro-choice
- Increased share of college educated voters and religious adherence of Evangelical protestants at the district level will increase and decrease Democratic performance respectively as these are major predictors of an individual’s position on abortion

Data used in this analysis was collected from multiple sources including: 
- FiveThirtyEight: 2022 U.S. House and U.S. Senate candidate data
- Federal Election Commission (FEC): Individual contribution fundraising data
- Dave’s Redistricting App (DRA): 2020 Presidential vote share by district
- The New York Times: 2022 Midterm election results
- Ballotpedia/Cook Political Report/USA Today: 2022 Midterm vote share margin shift from 2020 Presidential election at the district level
- Census Bureau: 2021 American Community Survey demographic data at the district level
- Google Trends: Number of searches including “abortion” at the state level in the last week of the election cycle relative to the 2022 peak for that state
- Center for Reproductive Rights: Abortion law status tracking states that have implemented abortion bans or have hostile policies towards abortion at the state level 
- Association of Religion Data Archives: Religious adherence rate per 1,000 for Evangelical Protestants at the state level

Four multivariate regression models were created to measure electoral performance, controlling for relevant variables, among House, Senate, and competitive House candidates/districts with competitive House districts being determined by the 2020 Presidential vote share being within a margin of 10 ppt. The four measurements of electoral performance include: individual contribution fundraising proportion after the Dobbs decision (Democrat fundraising amount / Democrat and Republican fundraising amount in race), candidate win probability, vote margin shift from the 2020 Presidential election, and the probability of a Democrat winning based on district characteristics. Data was collected and processed in R with data visuals created in Tableau. The R Markdown file and Tableau workbook can be viewed on github upon request along with data files for replication purposes. Districts without a Democratic or Republican opponent or had two Republicans/Democrats running against each other were removed resulting in 848 candidates (786 House candidates, 62 Senate candidates) and 424 districts (393 House districts, 31 Senate districts) included in analysis.

##### Results
The results of the first model measuring the fundraising proportion of individual contributions given to candidates after the Dobbs decision found that salience of abortion was statistically significant, increasing the post-Dobbs fundraising proportion for Democrats among House, Senate, and Competitive House candidates. Abortion law status (whether the state banned or had hostile policies towards abortion) significantly increased the fundraising proportion for Democrats at the Senate level with religious adherence slightly increasing the fundraising proportion for Democrats among all House candidates. The results of the second model measuring the probability of a candidate winning the general election found that gender was the only variable of interest to be statistically significant, increasing the probability of a candidate win when the candidate was a woman by 8%.

The results of the third model measuring the Democratic vote margin shift from the 2020 Presidential election to the 2022 Midterm election found that salience of abortion significantly decreased the margin shift among all House districts while abortion law status significantly increased the vote margin shift among all House and Competitive House districts. Religious adherence for Evangelical Protestants significantly decreased the margin shift among all House districts. The results of the final model measuring the probability of a Democratic candidate winning based on district characteristics found that none of the variables of interest were statistically significant predictors.

It was found through this analysis that election denialism of the 2020 Presidential election hurt Republican candidates, decreasing the post-Dobbs fundraising proportion for these candidates by 16 ppt at the Senate level and increasing the shift in Democratic vote margin from 2020 by 1.3 ppt among all House districts. However, this helped House GOP candidates in the post-Dobbs fundraising proportion by 5 ppt.

##### Recommendations
Looking at the 2024 elections, it is recommended the Democratic party:
Focus on the abortion issue in campaign and party messaging as increased salience on this issue increased Democratic candidate fundraising
Raise awareness of bans and hostile abortion policies from GOP state legislatures as pro-choice voters become mobilized, increasing Democratic vote share
Tie the Dobbs decision and election denialism to the GOP as these are unpopular issues that Democrats can use to hurt GOP candidate electoral performance

Pick-up House districts that were within a margin of 5 ppt in 2022 to target in 2024 with this strategy include: AZ-1, AZ-6, IA-3, MI-10, MT-1, NE-2, and WI-3. Competitive Senate districts to target in 2024 with this strategy include AZ, WI, and PA. These districts all have low Evangelical religious adherence rates at the state level and could improve candidate fundraising and voter mobilization efforts with a strategy focusing on the abortion issue.


#### Data

Data collected for this analysis came from multiple sources. To start, data was collected from 538’s “2022 Primary Project” [GitHub repository](https://github.com/fivethirtyeight/data/tree/master/primary-project-2022) which tracked the 2022 midterm primary candidates at the federal level. This data was processed to extract general election candidates by filtering candidates based on whether or not they won their primary election (or if there was one, their runoff election). 900 candidates were pulled with information on endorsements, incumbency status, race, and gender of the candidates. 

Contributions to candidates were provided by the [FEC](https://www.fec.gov/) which tracks federal level campaign finance information. This data included 'Candidate master', ‘Candidate-committee linkages’, and ‘Contributions by individuals’ on the [bulk data webpage](https://www.fec.gov/data/browse-data/?tab=bulk-data). Candidates not matched by the FEC fundraising data were manually  [confirmed](https://docs.google.com/spreadsheets/d/1C_W9G6RHF3NjHTEAeIrTNIa8rMdiZBfzfMp6cHl1C_w/edit?usp=sharing) on the FEC website to not having contribution records for this election cycle.

Google trends data was provided by Google, using the [gtrendsR R package](https://cran.r-project.org/web/packages/gtrendsR/gtrendsR.pdf) to identify the salience of the abortion issue this election cycle for each state.

District level data was provided by [Dave’s Redistricting App](https://davesredistricting.org/maps#home) (DRA) for each state. This data was manually collected for each state and inputted into this [google sheet](https://docs.google.com/spreadsheets/d/1bEdkobH-AgaGFZ0zHO3r_dnA5DVJPjFnWhNm8g-P5N0/edit?usp=sharing). The sources of data and processing done to calculate these values for districts can be viewed on [DRA’s website](https://davesredistricting.org/maps#aboutdata). Data that was used was the 2020 presidential vote share for each party.

Election result data was manually collected for the [New York Times Midterm Tracker](https://www.nytimes.com/interactive/2022/11/08/us/elections/results-senate.html?action=click&pgtype=Article&state=default&module=election-results&context=election_recirc&region=NavBar) for house and senate candidates and inputted into this [google sheet](https://docs.google.com/spreadsheets/d/1PFxFBpbsdMT8_b8weiqAeTIx1Q11vgNIWIlYYAjOU0M/edit?usp=sharing).

Vote margin shift from 2020 Presidential election to 2022 Midterm election was collected in this [google sheet](https://docs.google.com/spreadsheets/d/1PBX0qkvmVmMcLcrWWGPydQzvHQ696JCubXYyqLDFZfY/edit?usp=sharing). House level shift is provided by [Ballotpedia](https://ballotpedia.org/Election_results,_2022:_Comparison_of_2020_presidential_and_2022_U.S._House_midterm_results) and Senate level shift was calculated using data provided by [Cook Political Report](https://www.cookpolitical.com/2020-national-popular-vote-tracker) and [USA Today](https://www.usatoday.com/elections/results/2022-11-08/senate/).

Urbanization index of districts was provided by 538 and collected in this [google sheet](https://docs.google.com/spreadsheets/d/1vLdj5PHHtZdqk1EY0mWStBifLVRz9vT1H6zZrVIB7aY/edit?usp=sharing). House level data source can be found [here](https://github.com/fivethirtyeight/data/blob/master/district-urbanization-index-2022/urbanization-index-2022.csv) and Senate level data source can be found [here](https://fivethirtyeight.com/features/how-urban-or-rural-is-your-state-and-what-does-that-mean-for-the-2020-election/).

State region was provided by the Census Bureau and collected in this [google sheet](https://docs.google.com/spreadsheets/d/1PGKTLvrdfa6cAFQgrgJHiZb1_RUw0AezEnoSoh5BCLQ/edit?usp=sharing). The data source can be found [here](https://www2.census.gov/geo/pdfs/maps-data/maps/reference/us_regdiv.pdf).

Religious adherence rates by state was provided by the Association of Religion Data Archives and collected in this [google sheet](https://docs.google.com/spreadsheets/d/1NQCAYqo4MO9HZOA5GcpdsXuBoKEypaFBuFmB7XUwn94/edit?usp=sharing). The data source can be found [here](https://thearda.com/us-religion/maps/us-state-maps?color=orange&m1=2_2_9999_2020&m2=2_2_1_2020).

State abortion law status was provided by the Center for Reproductive Rights and was collected in this [google sheet](https://docs.google.com/spreadsheets/d/1BDRWHJN-D0XnyXBWZFY6fRpqv4bmJxDNdWPrjDECv_s/edit?usp=sharing). The data source can be found [here](https://reproductiverights.org/maps/abortion-laws-by-state/).


#### Actions
- Candidates loaded from 538 and processed to only include general election candidates
- FEC data (individual donations, candidates, candidate-committee link) was collected for the 2022 cycle and joined together. Fundraising amount total past Dobbs decision date (6/24/2022) aggregated by candidate.
- FEC data and 538 candidates joined on LAST NAME, STATE, OFFICE, DISTRICT
- Candidates not matched were checked with FEC website to make sure there were no records of transactions for these candidates
- Districts with no Democratic or Republican opponent, had either two Republicans or two Democrats running were filtered out. 846 candidates (784 House candidates, 62 Senate candidates, 423 districts (392 House districts, 31 Senate districts)
- District level data was aggregated and district level variables were calculated
- DRA data (2020 pres Dem margin) was added to the district level data set
- NYT election results (winner) was added to the candidate level data set
- Shift from Pres 2020 was added to the district level data set
- State abortions status was added to the district level data set with three numeric dummy variables representing: illegal status, hostile status, and other status
- Google Trends data with number of hits for “abortion” last week of election cycle relative to 2022 peak was added to the district level data set
- Census data (education, income, age, gender, and share white) processed and added to district level data
- State region was processed and added to district level data
- Urbanization index was processed and added to district level data
- Religious adherence rate per 1000 by state was processed and added to district level data
- Created three types for candidate and district data sets: house candidates/districts, senate candidates/districts, competitive house candidates/districts (competitive determined by 2020 margin within 10%)
- Created the linear and logistic models with formatted output
