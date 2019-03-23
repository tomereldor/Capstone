# Quantifying Your Customer’s Lifetime Value by Markovian Engagement States
## Markov Modeling Customers by Engagement States for Quantifying Lifetime Value and Further Insights.
-----------------------------------
**Tomer Eldor  
Majors: Computational Sciences: Data Science, Social Sciences: Economics  
Capstone Project  
Minerva Schools  
2019**  

Abstract
This capstone project lays out a framework with a user-friendly toolkit for modeling users engagement states as a markov chain, using it for prediction of future engagement states and calculating the Lifetime Value for each engagement group. It consists of:
Case study in practice: example of analysis and insights at Via Transportation, Inc.
R Coding Tutorial for replicating this analysis, implemented by transferring such analysis onto a dataset of donations for democratic elections campaigns, specifically donations to Bernie Sanders’ donations from 2015-2016, through ActBlue donations platform.
The goal of this capstone is manifold:
1. Promote an underutilized academic methodology (inspired by Pfeifer & Carraway, 2000) of using markov models to predict user states and lifetime value into practical usage in private settings - where customer lifetime value is utilized and needed most.
2. Do the above through teaching R code (with best practices), to help new learners and professionals utilize this methodology while advancing their technical skills, yet most importantly - critically thinking and altering this analysis to fit their needs; since no one environment is alike. There needs to be a high level of touch, such that this R tutorial forces a user with sufficient skills and time to critically think and alter needed elements of this analysis. 
3. Apply this analysis to Via transportation Inc, gather conclusions and impact relevant decisions in the company.
4. Transfer this analysis further into a political sphere and donations data rather then for-profit data, show that it is useful there, and provide the insights derived from this analysis that could be useful for future democratic political campaigns specifically or donation campaigns in general. 

Check out these links below:

### Project Code, Tutorial Notebook and Analysis Report
1. View the [Analysis Report Webpage](http://htmlpreview.github.io/?https://github.com/tomereldor/Capstone/blob/master/ACTBLUE%20Analysis/ACTBLUEAnalysis.html) presenting the ActBlue case study and findings.  
2. See the step-by-step R Coding Tutorial on [RPubs](http://rpubs.com/tomereldor/actblue) for how I applied framework on the ActBlue donations data and how you might do it for your data
3. To replicate, download the [R Notebook](https://github.com/tomereldor/Capstone/blob/master/Actblue_Markov_Tutorial_3_for_publishing.Rmd) presented in the RPubs above.

### Data

__ActBlue campaign finance filings.__  ActBlue, a political action committee, processes the vast majority of contributions to Bernie Sanders's 2016 presidential campaign. The analyses use ActBlue's `PRE-RUNOFF`, `POST-SPECIAL`, `PRE-PRIMARY`, `POST-RUN-OFF`, `MID-YEAR`, `YEAR-END`, `FEB MONTHLY`, and `MARCH MONTHLY` filings sent to the Federal Election Commission. These filings cover the entirety of the Sanders presidential campaign, which began on April 30, 2015. The data include all "receipts" for this time period, and were downloaded from ProPublica's [FEC Itemizer](https://projects.propublica.org/itemizer/committee/C00401224/2016). Some rows in the files contained unmatched quotation marks (e.g., `"NOT EMPLOYED,`) in the `employer` field. BuzzFeed News fixed those rows by hand; you can download these cleaned-up files [here](https://archive.org/details/actblue-fec-filings-april-2015-to-feb-2016).
- Download the [data](https://drive.google.com/open?id=19FZoWqePhnudd7lentiQue8hje8RbGzZ). The original data 
https://archive.org/details/actblue-fec-filings-april-2015-to-feb-2016
The Dataset was too big to upload here, but you can get my already processed files from my drive (request permission if needed and I will grant it) [here](https://drive.google.com/open?id=19FZoWqePhnudd7lentiQue8hje8RbGzZ). 
