
<p style="color: red; font-weight: bold">>>>>>  gd2md-html alert:  ERRORs: 0; WARNINGs: 1; ALERTS: 10.</p>
<ul style="color: red; font-weight: bold"><li>See top comment block for details on ERRORs and WARNINGs. <li>In the converted Markdown or HTML, search for inline alerts that start with >>>>>  gd2md-html alert:  for specific instances that need correction.</ul>

<p style="color: red; font-weight: bold">Links to alert messages:</p><a href="#gdcalert1">alert1</a>
<a href="#gdcalert2">alert2</a>
<a href="#gdcalert3">alert3</a>
<a href="#gdcalert4">alert4</a>
<a href="#gdcalert5">alert5</a>
<a href="#gdcalert6">alert6</a>
<a href="#gdcalert7">alert7</a>
<a href="#gdcalert8">alert8</a>
<a href="#gdcalert9">alert9</a>
<a href="#gdcalert10">alert10</a>

<p style="color: red; font-weight: bold">>>>>> PLEASE check and correct alert issues and delete this message and the inline alerts.<hr></p>


<h2>Coding Tutorial of This Framework in R: a Case Study of Actblue Campaign Donations</h2>


<p>Application 2 of this technique with open source code and data

**External Product #3: Please review the tutorial at [rpubs.com/tomereldor/markov](http://rpubs.com/tomereldor/markov).**

After explaining the framework in general and demonstrating a deep application of it in practice in a business setting, I have created a coding tutorial teaching how to apply this framework to one's one data in R, by applying this framework to an open-source dataset of [ActBlue donations](https://secure.actblue.com/) to political campaigns. 

I leveraged this tutorial to apply this framework to a vastly different setting: the  political and non-profit realm, analyzing the patterns of donations for democratic elections campaigns through<span style="text-decoration:underline;"> [ActBlue](https://secure.actblue.com/)</span> (an online donations platform), based on data of donations to Bernie Sanders' campaign during April 2015 - February 2016.

The data was retrieved from [ActBlue archives](https://archive.org/details/actblue-fec-filings-april-2015-to-feb-2016). Initial data retrieval and preprocessing before importing into this notebook were done in this [separate notebook on GitHub](https://github.com/tomereldor/actblue-donors/blob/master/notebooks/Tomers-actblue-preprocessing.ipynb).

<h3>The Tutorial as an Educational Tool & Knowledge Transfer</h3>


<h4>Tutorial Description</h4>


Do you have reoccuring users, customers or benefactors? Have you ever needed to invest in them without knowing exactly how much you should? Have you ever wanted to gain a deeper understanding of your users lifetime journey and their states of engagement? Lastly, have you wanted to get better at R coding and learn the extremely efficient data processing method 'data.table'? 

In this tutorial you will learn how to segment your users to states of engagement and analyze them to predict their (_discounted) customer lifetime value_, by modeling them using a Markov Model. You will learn about the data preprocessing procedures, building a transition matrix, creating the markov model, finding the steady state, and most importantly using the formula for (_discounted) customer lifetime value _to quantify and predict it using Markov models. You will produce interactive and complex plots demonstrating these values, model prediction accuracy, and the historical progressions of all metrics of interest. You will learn how we derive insights and conclusions from these plots and dat. 

You will learn to use the data.table library for efficient and intuitive data processing, ggplot for plotting professionaly and ggplotly for producing interactive visualizations. You will also learn using plyr and dplyr, a more commonly used data processing method in R, running custom functions and loops. 

<h4>Tutorial Objectives and Learning Outcomes</h4>


**#ss-customervalue **– define and evaluate the value of your customers.

**#cs-markovmodels **– Identify, understand, and apply Markov models to approximate Markovian system behaviors.

**#cs-resultsreport **– Demonstrate results of a data-science analysis project and communicate them comprehensively and effectively considering your audience. 

**#r-coding** – learn or improve coding skills in R programming language. Learn advanced useful libraries and techniques such as plyr, dplyr, and data.table

<h4>Prerequisites and Working Knowledge</h4>


Learners starting this tutorial should have prior knowledge or experience working in R. If any of the specific techniques (like working with RMarkdown, dplyr or ggplot) are unfamiliar to you, you should look up basic usage of these packages and resources like their [cheat-sheets](https://www.rstudio.com/resources/cheatsheets/) and [quick-reference guides](http://r-statistics.co/ggplot2-cheatsheet.html).

<h3>Methods and Choices</h3>


<h4>Choice of Data </h4>


I chose to transfer this analysis to the vastly different political donations realm for multiple reasons. First, it was useful to show the wide applicability of this framework for vastly different areas. This area is inherently different since it is _not _a business, for profit, or private sector, but it is all the opposites. Additionally, users are voluntarily choosing to donate using this platform; but they do it still on a recurring basis which makes our framework relevant. Moreover, as the nonprofit and public sector, it is almost unprecedented to analyze the "lifetime value" of your customers and use predictive algorithmic modeling for that. 

Additionally, this is an especially useful era (2019) to analyse and derive insights about optimizing donations to political campaigns. I have sent this information to employees at political campaign organizations (of Bernie Sanders as well as my personal support, Andrew Yang) and setting up discussions about utilizing such frameworks to optimize their donations.

<h4>Choice of Coding Language and Format of the Coding Tutorial </h4>


Analysts in the public sector, statisticians, economists and econometricians, tend to work more in R and statistical programs than in Python (my two working knowledge languages). Additionally, ggplot is a professional plotting library, with a convenient [layered grammar of graphics](http://vita.had.co.nz/papers/layered-grammar.html), than Python equivalents like "matplotlib". Hence, I chose to write this guide in R for greater usability for the audience of this political domain, and encouraging more professionals in the public or nonprofit sector to use this framework which bases on concepts taken from the for-profit sector.

The written format is taken from the top examples for "online coding tutorials" for python and R common today as an ongoing tool to learn new specific libraries, techniques and skills in a languages that the programmer is already familiar with – which is what I aim for in this case. Similar examples include most popular data science websites such as [Analytics Vidhya](https://www.analyticsvidhya.com/learning-paths-data-science-business-analytics-business-intelligence-big-data/learning-path-r-data-science/) and [Towards Data Science](https://towardsdatascience.com/tagged/r-programming) the highest ranked tutorials on [hackr.io](https://hackr.io/tutorials/learn-r): [R Markdown, The Definitive Guide](https://bookdown.org/yihui/rmarkdown/notebook.html), [Introduction to R Programming](https://cecilialee.github.io/blog/2017/12/05/intro-to-r-programming.html), [15 page tutorial for R](http://www.studytrails.com/r/15-page-tutorial-for-r/) and many data science courses like this course from [CUNY](https://rpubs.com/destination4debabrata).

This format is basically an HTML version of a R Markdown notebook, which users can download and run on their own machine, to make reproducibility of this analysis the as easy and accessible as possible.

<h4>Choice of Programming Methodologies </h4>


I chose to use particularly useful libraries that are common practice and important skills for R data scientists, analysts and econometricians, like dplyr, tideverse and ggplot. I extended this by highlighting the significantly more efficient and intuitive library of _data.table_. In the body of the tutorial I included a comparison of one data wrangling task which took 3 full minutes with normal methods (dplyr) and less than 1 second with _data.table_. 

I wrapped all my important coding procedures in functions to showcase working standard coding style and habits, while demonstrating the use of which by running them multiple times on different data subsets or needs.

I chose ggplot for visualization and set the theme to be "minimal" for most plots (white background, simple black text, and human vision appropriate size configurations) to help the users' eye focus on the data. For most of the plots I used the interactive plotting library _plotly_ (via the wrapper "ggplotly") to enable interaction, increased engagement and exploration by the user. That way, users are more drawn to the plot, will spend more time on them, and can explore _what they really want to know_ - so we can reach an unprecedented level of personalization for the user with one plot. For example, one manager might want to know the full picture and zoom out, while their analyst responsible for new donors might want to highlight, zoom in and track the particular quantities of new donors alone. More information about the usefulness and relevance of plotly could be found on [their website](https://plot.ly/), and an example advocating for the benefits of using interactive plotly visualizations could be found [here](http://grunberger.com/2017-08-18-use_Plotly/). 

<h3>Results and Discussion</h3>


Below I provide a brief summary with some of the results and plots generated by the analysis.

<h4>Engagement States</h4>


Informed by both qualitative insights related to the given tiers of donations and quantitative insights based on data distributions explorations and the output from a clustering algorithm, I divided the users to states of donations based on their number of donations per month and average amount of donations in each month. 



1. **Frequency**: 
    1. **Monthly**: 1-4 Donations a Month 
    2. **Weekly**: 5-10 donations per month  
    3. **Daily**: 11 or more donations per month  
2. **Amount**:   
    4. "**1**": Average Donation Between $0.01-10  
    5. "**10**": Average Donation Between $10.01-25  
    6. "**25**": Average Donation Between $25.01-50 
    7. "**50**": Average Donation Above $50.  
3. "**Non**" - means the user did not make any donation that month.  

Figure 31 below displays the distribution of users at each state on the dimensions of number of times and average amount of donations.



<p id="gdcalert1" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/ACTBLUE-Analysis0.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert2">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/ACTBLUE-Analysis0.png "image_tooltip")



        Figure 31 – plot of the key two dimensions of activity: frequency (number of donations this month on the axis) and contribution amount of activity (average donation amount). 

From figure 31 above we can see that almost all the donations above $250 were at most at a monthly frequency. Throughout this analysis, the states are defined on a monthly basis. So if a user has donated one or a couple of times in a single month, they would be "Monthly" for that month; but it doesn't mean that they necessarily would be also monthly at the next month. This plot also demonstrated why segmenting according to these two dimensions of frequency and amount of donations is important rather then confusing between them. For example, if we would have instead sum up all donations per month, we would have confused people who donated a lot once per month with people who donated a bit every day – the two tail ends of the distributions. This would be a shame since we want to know what types of donors brought more value, to be able to interpret and take action against it, such as encouraging people to donate at that pattern that we saw gave more overall value (for example, "donate $30 monthly" or "donate $1 every day" are different asks to make from a user). 

<h4>Transition Matrix</h4>


Tabulating the transitions from the entire dataset creates the following transition matrix:


<table>
  <tr>
   <td>From↓ \ To→
   </td>
   <td><strong>New</strong>
   </td>
   <td><strong>Non</strong>
   </td>
   <td><strong>monthly1</strong>
   </td>
   <td><strong>monthly10</strong>
   </td>
   <td><strong>monthly25</strong>
   </td>
   <td><strong>monthly50+</strong>
   </td>
   <td><strong>weekly1</strong>
   </td>
   <td><strong>weekly10</strong>
   </td>
   <td><strong>weekly25+</strong>
   </td>
   <td><strong>weekly 50+</strong>
   </td>
   <td><strong>daily1</strong>
   </td>
   <td><strong>daily10</strong>
   </td>
   <td><strong>daily25</strong>
   </td>
   <td><strong>daily50+</strong>
   </td>
  </tr>
  <tr>
   <td><strong>New</strong>
   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
<strong>0.85</strong></p>

   </td>
   <td><p style="text-align: right">
0.07</p>

   </td>
   <td><p style="text-align: right">
0.02</p>

   </td>
   <td><p style="text-align: right">
0.04</p>

   </td>
   <td><p style="text-align: right">
0.02</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
  </tr>
  <tr>
   <td><strong>Non</strong>
   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
<strong>0.74</strong></p>

   </td>
   <td><p style="text-align: right">
0.12</p>

   </td>
   <td><p style="text-align: right">
0.06</p>

   </td>
   <td><p style="text-align: right">
0.06</p>

   </td>
   <td><p style="text-align: right">
0.02</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
  </tr>
  <tr>
   <td><strong>monthly1</strong>
   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
<strong>0.31</strong></p>

   </td>
   <td><p style="text-align: right">
<strong>0.58</strong></p>

   </td>
   <td><p style="text-align: right">
0.07</p>

   </td>
   <td><p style="text-align: right">
0.02</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
  </tr>
  <tr>
   <td><strong>monthly10</strong>
   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
<strong>0.36</strong></p>

   </td>
   <td><p style="text-align: right">
0.12</p>

   </td>
   <td><p style="text-align: right">
<strong>0.38</strong></p>

   </td>
   <td><p style="text-align: right">
0.1</p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0.02</p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
  </tr>
  <tr>
   <td><strong>monthly25</strong>
   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
<strong>0.45</strong></p>

   </td>
   <td><p style="text-align: right">
0.06</p>

   </td>
   <td><p style="text-align: right">
0.09</p>

   </td>
   <td><p style="text-align: right">
<strong>0.36</strong></p>

   </td>
   <td><p style="text-align: right">
0.03</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
  </tr>
  <tr>
   <td><strong>monthly50</strong>
   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
<strong>0.51</strong></p>

   </td>
   <td><p style="text-align: right">
0.03</p>

   </td>
   <td><p style="text-align: right">
0.04</p>

   </td>
   <td><p style="text-align: right">
0.09</p>

   </td>
   <td><p style="text-align: right">
<strong>0.32</strong></p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
  </tr>
  <tr>
   <td><strong>weekly1</strong>
   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0.04</p>

   </td>
   <td><p style="text-align: right">
<strong>0.33</strong></p>

   </td>
   <td><p style="text-align: right">
0.11</p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
<strong>0.25</strong></p>

   </td>
   <td><p style="text-align: right">
0.13</p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0.06</p>

   </td>
   <td><p style="text-align: right">
0.03</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
  </tr>
  <tr>
   <td><strong>weekly10</strong>
   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0.04</p>

   </td>
   <td><p style="text-align: right">
0.11</p>

   </td>
   <td><p style="text-align: right">
<strong>0.23</strong></p>

   </td>
   <td><p style="text-align: right">
0.08</p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
0.05</p>

   </td>
   <td><p style="text-align: right">
<strong>0.27</strong></p>

   </td>
   <td><p style="text-align: right">
0.08</p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
0.07</p>

   </td>
   <td><p style="text-align: right">
0.02</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
  </tr>
  <tr>
   <td><strong>weekly25+</strong>
   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0.04</p>

   </td>
   <td><p style="text-align: right">
0.04</p>

   </td>
   <td><p style="text-align: right">
0.1</p>

   </td>
   <td><p style="text-align: right">
<strong>0.22</strong></p>

   </td>
   <td><p style="text-align: right">
0.08</p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
0.1</p>

   </td>
   <td><p style="text-align: right">
<strong>0.23</strong></p>

   </td>
   <td><p style="text-align: right">
0.08</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0.04</p>

   </td>
   <td><p style="text-align: right">
0.05</p>

   </td>
   <td><p style="text-align: right">
0.02</p>

   </td>
  </tr>
  <tr>
   <td><strong>weekly50</strong>
   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0.07</p>

   </td>
   <td><p style="text-align: right">
0.03</p>

   </td>
   <td><p style="text-align: right">
0.04</p>

   </td>
   <td><p style="text-align: right">
0.09</p>

   </td>
   <td><p style="text-align: right">
<strong>0.29</strong></p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
0.02</p>

   </td>
   <td><p style="text-align: right">
0.08</p>

   </td>
   <td><p style="text-align: right">
<strong>0.26</strong></p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
0.02</p>

   </td>
   <td><p style="text-align: right">
0.06</p>

   </td>
  </tr>
  <tr>
   <td><strong>daily1</strong>
   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
0.09</p>

   </td>
   <td><p style="text-align: right">
0.02</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
<strong>0.19</strong></p>

   </td>
   <td><p style="text-align: right">
0.09</p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
<strong>0.43</strong></p>

   </td>
   <td><p style="text-align: right">
0.15</p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
  </tr>
  <tr>
   <td><strong>daily10</strong>
   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
0.04</p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
0.04</p>

   </td>
   <td><p style="text-align: right">
<strong>0.2</strong></p>

   </td>
   <td><p style="text-align: right">
0.09</p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
0.06</p>

   </td>
   <td><p style="text-align: right">
<strong>0.4</strong></p>

   </td>
   <td><p style="text-align: right">
0.09</p>

   </td>
   <td><p style="text-align: right">
0.03</p>

   </td>
  </tr>
  <tr>
   <td><strong>daily25</strong>
   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0.02</p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
0.02</p>

   </td>
   <td><p style="text-align: right">
0.03</p>

   </td>
   <td><p style="text-align: right">
0.02</p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0.07</p>

   </td>
   <td><p style="text-align: right">
<strong>0.17</strong></p>

   </td>
   <td><p style="text-align: right">
0.08</p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
<strong>0.15</strong></p>

   </td>
   <td><p style="text-align: right">
<strong>0.31</strong></p>

   </td>
   <td><p style="text-align: right">
<strong>0.13</strong></p>

   </td>
  </tr>
  <tr>
   <td><strong>daily50+</strong>
   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0.06</p>

   </td>
   <td><p style="text-align: right">
0.03</p>

   </td>
   <td><p style="text-align: right">
0.03</p>

   </td>
   <td><p style="text-align: right">
0.04</p>

   </td>
   <td><p style="text-align: right">
0.07</p>

   </td>
   <td><p style="text-align: right">
0.01</p>

   </td>
   <td><p style="text-align: right">
0.04</p>

   </td>
   <td><p style="text-align: right">
0.08</p>

   </td>
   <td><p style="text-align: right">
<strong>0.22</strong></p>

   </td>
   <td><p style="text-align: right">
0</p>

   </td>
   <td><p style="text-align: right">
0.04</p>

   </td>
   <td><p style="text-align: right">
<strong>0.15</strong></p>

   </td>
   <td><p style="text-align: right">
<strong>0.21</strong></p>

   </td>
  </tr>
</table>



        Figure 32 – Transition Matrix for the ActBlue donor states. States are colored by their activity level: the base color is based on the frequency, and saturation/darkness (hue) is based on the contribution amount within that activity level. The cells are colored conditionally similarly to a heatmap, were darker green represents higher probabilities of transitions. Notice the two diagonal patterns, and the transitions from monthly to "Non" at the "Non" column. 

The above transition matrix (figure 32) already conveys some insights. I have bolded the highest values in each row/column. 

As expected, the first column is all zeros, since no one transitions to be "new". However, people also never (or almost never) transition from being new or being monthly directly to a daily donation pattern (notice all the zeros approaching the right corner). 

More interestingly, the tables shows the following insights:



1. **These states are quite stable - donors mostly stick to their monthly donation patterns**. The diagonals are in most cases the highest probabilities – meaning that these states are relatively stable; people tend to keep their engagement states from one month to another. However, the _monthly_ state is extremely prone to stop donating the following month, as you can see at the probabilities of transitioning to the "Non" column. 
2. **Monthly users are likeliest to stop donating, and much more likely so the larger the donation value was.** That is detectable by looking at the "Non" column and seeing that all of its significant transitions coming from active states are coming from the Monthly States.
3. **Weekly and Daily donors are very likely to reduce their donation frequency, but keep the same amount range per donation. **That is detectable by the lower diagonal pattern. Specifically:
    1. **Weekly** donors and **daily high value donors ($50+)** are similarly likely to "downgrade" to a monthly donation at the same level range as they are to stay at the same state.
    2. **Daily donors below $25** are roughly **half as likely to reduce their frequency** keeping the same average amount as they are to stay at their own state.

<h4>Steady States</h4>


The analysis of steady state shows us the following distribution of donors under each state (see figure 33 below).



<p id="gdcalert2" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/ACTBLUE-Analysis1.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert3">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/ACTBLUE-Analysis1.png "image_tooltip")



        Figure 33 – Number of donors at each state in reality (in red) and steady state (in blue)

By looking at the disparities between reality (in red) and the eventual steady state equilibria (in blue) at figure 33 above we can see that, if transition patterns persist, more donors will return to donating (biased by the time period of donations that is _approaching _elections period). Also, **more donors will end up at the monthly donations, and more of them at lower donation amount. **That is detectable by the differences between reality and the steady state distributions for the monthly states. 

<h4>Discounted Lifetime Values</h4>


Let's observe the actual predicted discounted lifetime value for donors at each state below.



<p id="gdcalert3" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/ACTBLUE-Analysis2.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert4">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/ACTBLUE-Analysis2.png "image_tooltip")



        Figure 34 – Donation Amounts (in green) and DLV predictions (in light green with a 0.6 discount factor and in yellow with a 0.8 discount factor. Notice that the states with higher donation amounts and lower frequency exhibit greater average monthly donation amounts _and _predicted DLVs. However, the Monthly state might be confounding because it could be just a single donation that put the donor at a "monthly" state for that month alone. This is expressed by the high transitions to "Non" from monthly states. 

The stacked barplot of DLVs above shows us some interesting results:



1. **The highest monthly donations come from _monthly (or single-time) donors, and they are predicted to donate disproportionately even more in the future _**(notice the length and proportion of their predicted DLV relative to the others). \
_This is in **contrast to the common argument that ActBlue tries to capitalize on small donations** ([Levine, Subak-Skees; 2018](https://fivethirtyeight.com/features/how-actblue-is-trying-to-turn-small-donations-into-a-blue-wave/)_[^1]_); candidates would get more donations overall from monthly or single time donors than they would from small frequent donations._


2. **The second highest DLV is weekly50+, and third highest DLV is from daily50+ **(both at the highest amount tier)**. **This might be counterintuitive to how we'd expect this to work – if you donate at a similar range, you should donate more overall if you donate more frequently; but it's not so. The more frequently donors donate, the donate less; and so much less that the aggregate is actually less than donors donating fewer times. 
3. **The monthly total is higher the fewer contributions you make. **This is true at each amount tier (if you compare daily1 and weekly1 against monthly1, and so on). This is true both for the actual current donations and expected future donations.
4. **Predicted Future DLV value is higher the fewer donations you make, at any given tier. **If you examine any given amount tier (all the '1's, all the '10's and so on) you discover that the prediction proportion of future DLV is much higher for the lower frequency donors than the more frequent donors. 

<h4>Potential Explanation: Temporal / Exponential Discounting</h4>


These insights might teach us something about the psychology or behavioral economics aspect of these donor's donation patterns. While ActBlue campaigns might try to get people to donate a smaller amount on a daily basis assuming that people will see that as a small commitment and discount the future donated money, we see that: 

(1) this seems to be false, and **people seem to donate more if they donated at once**, and (2) **people are likelier to quit donating if their donation pattern frequent**, even if they donated more on a less frequent basis.

The first part of this finding might be explained if people actually have an **_aversion _or _anxiety_ from the commitment **of donating very frequently; or that they are **dreading that the amounts will compound to be much higher** than they really are because of the weight of the daily burdon. 

This might be also explained from a classical behavioral economics point of view by the  the exponential or the quasi-hyperbolic discounting bias (which is the same if 

<p id="gdcalert4" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: equation: use MathJax/LaTeX if your publishing platform supports it. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert5">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

_,_ your unique sensitivity discount factor, is neutral and equals to one) . 

The exponential discounting bias formula says that your utility evaluation for many different portions of amounts over time is represented as follows:

The exponential discounting formula goes like this:



<p id="gdcalert5" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/ACTBLUE-Analysis3.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert6">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/ACTBLUE-Analysis3.png "image_tooltip")
[^2]

Where U is your overall utility, _u_ is your utility function, C is the amount you get at each timestep, and 

<p id="gdcalert6" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: equation: use MathJax/LaTeX if your publishing platform supports it. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert7">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

_ _is the discount factor. 

Imagine that you are choosing between donating either (A) $30 per month of 30 days, or (B) $1 per day, and that your time periods are daily time periods. From a standing point in time perspective, looking at the options as if you are now at the first of the month, if option A is taken away from your account at the end of the month, you actually discount it by 30 days:



<p id="gdcalert7" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: equation: use MathJax/LaTeX if your publishing platform supports it. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert8">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>



Such that the perceived amount will be small if it is at the end of the month.

On the other hand, if you pay each day, it looks like this:



<p id="gdcalert8" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: equation: use MathJax/LaTeX if your publishing platform supports it. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert9">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>



For example, at a reasonable discount value of 0.8, the daily donation was discounted to seem like $6, while the donation at the end of the month was discounted to seem like $0.001 (calculations below[^3]). 

This will still be a similar case if we recalculate this anew at _each day_ of the month as we approach the donation day – the expected amount will be still lower for almost all days other than the donation day itself in the monthly donation case rather than the daily donation case. 

Additionally, the donor will probably _not remember _the fact of the donation at any non-donating day and thus not include that in their calculations, nor will it take a mental burden upon them, as opposed to the daily donation which they would notice every single day. If there was a threshold of number of times that you feel good about donating before feeling that you have fulfilled your duty and wanting to stop, this also might explain this behavior. 

Finally, another perspective could be broad-framing: the mental comparison a donor makes of the donation to other expenses occurring at the same time period. On a daily basis, a donor probably deals with very small expenses, mostly on food, which might be at a similar range to the daily donation. However on a monthly basis, the person is used to think about their rent or mortgage and other monthly much greater expenses, next to which the monthly donation seems smaller than ratio between the daily donation to daily expenses. 

All of these are potential behavioral explanations to the phenomena of monthly donations being higher and more persistent. 

<h4>Model Prediction Accuracy</h4>


After recalibrating the discount factor, the model predictions (in red) versus the true DLV distributions can be seen at the plot below - same as in Via's case:



<p id="gdcalert9" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/ACTBLUE-Analysis4.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert10">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/ACTBLUE-Analysis4.png "image_tooltip")



        Figure 35 – Distribution of _true_ discounted lifetime values, their means in yellow, and predicted DLVs per each one of the donor states. This plot shows that for most states the prediction wasn't very far from reality, but mostly overestimated, with some exceptions (like for weekly 50+ where it was underestimated). It also shows the non-normal distributions of the true values which make this problem harder to model.

You can see that the predicted value (the red line) is usually pretty close to the true mean, and mostly overestimates it but not always (such as in the Weekly50+ case where it was underestimating it).

<h4>Group Discounted Lifetime Values Throughout History</h4>


Below I attach a plot of the estimated DLVs contributed in total from each group (state), including the amounts and the number of donors at each group at each month, at figure 36. Notice that the highest four lines are all the monthly states – showing how, by far, the groups of donors in all the monthly states were responsible for the majority of contributions. 



<p id="gdcalert10" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/ACTBLUE-Analysis5.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert11">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/ACTBLUE-Analysis5.png "image_tooltip")



        Figure 36 – DLV contributions in aggregate per group. See that monthly states are responsible by far for the highest DLVs from all; and that they have been mostly increasing through time (with a local peak around September 2015). The rest of the more frequent states are responsible for only a fraction of the expected group total DLVs and only increase right towards the end of the period (2016). This could very well be by the sheer size of the Monthly group relative to the other groups. 

Figure 36 above shows the over and above the higher donation values for the monthly states, it is also the sheer amount of monthly donors (or single-time donors) that makes them bring _almost all of the value_ to the Bernie Sanders campaign during 2015-2016. 

<h3>Conclusions, Limitations and Future Work</h3>


To summarize this case study, here are some of the high-level insights that would matter more for decision makers from such an analysis:



1. While some of the states are a bit more stable, most states tended to drop down a tier of frequency but stay at a similar amount of donation the following month.
2. There were more and more Monthly donors, and more and more of Low donation amounts. Intuitively, it was easy to get people to join or stay in the lower commitment donation patterns.
3. The groups with the highest average DLV came from the highest average donation, not from frequency. Meaning, even if people donated every day, it still didn't sum up to the same amounts in a whole month as the monthly donors.
4. Within the high amount donors of various frequencies, there was an INVERSE relationship with the frequency; monthly donors typically donated more than weekly and they donated more than daily donors of the same average amount tier.
5. In aggregate discounted lifetime donation values (times the number of drivers), most of the lifetime value comes from the monthly donors, even if they donate a small amount, because they were a much larger group. Therefore, for the Sanders' campaigners - or democratic campaigners - you might be better off convincing more people to donate a monthly donation of whatever magnitude they can afford, than trying to get a higher frequency of donations that will later be stopped, or than trying to push hard for a higher amount.

First, I should point out that this study was mainly done as an example for demonstrating the technique and has a number of limitations. 

First, the states weren't iterated and refined until finding optimal states. In future work, I would recommend refining the states until they are 70% or more stable, and that they define the lifetime journey of a donor more accurately. This set of states lacked churned and dormant states as separate from the "Non" state which has confounded the data and numbers around the "Non" state. Additionally, a major limitation is that the states were monthly and on a 1-month basis, so they actually didn't separate a single time donor from a monthly donor per month. To be exact, I have separated the data to include only donors who donated more than once over that period. So all the monthly donors donated any frequency between twice per year to twice per month. That is a very wide range. 

Lastly, it might also be a selection bias or just imbalance of donation groups: monthly donors just might be wealthier donors. I have no income or sufficiently informative demographic information about the donors that would allow me to check that assumption. 

For future work, I would want to meet with domain experts – political campaign analysts, workers or managers, and discuss this topic with them, to find what are their own perceptions of limitations of this project and what would be the most useful for them to analyze and how. Then I would reiterate the project accordingly. There are many ways to improve this project technically - including better state definitions, retiretring states, applying hidden markov models, improving prediction accuracy and more – we first should learn what the decision makers of this data analysis project would actually need or want before heading off directions that will not be useful to them. 


<!-- Footnotes themselves at the bottom. -->
## Notes

[^1]:

     This is a Fivethirtyeight article that was one of the inspirations for this analysis: [Levine, C., & Zubak-Skees, C. (2018)](https://fivethirtyeight.com/features/how-ActBlue-is-trying-to-turn-small-donations-into-a-blue-wave/). 

[^2]:
     See [Rasmusen, Eric (2008)](http://www.rasmusen.org/special/hyperbolic-rasmusen.pdf)

[^3]:
     Ran a quick Python function:   [x+=(0.8**i) for i in range(30) ], resulting in x = 5.99, while 08<sup>30</sup> = 0.00123


<!-- Docs to Markdown version 1.0β16 -->
