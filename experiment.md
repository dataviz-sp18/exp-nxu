MACS 40700: Assignment 2 - Experiment
================
Alice Mee Seon Chung, Ningyin Xu
5/1/2018

Overview
--------

In this work, we try to utilize experiment to test the application of the hierarchy of elementary perceptual, put together by William S. Cleveland and Rober McGill, on the visualization of time-series data. In the hierarchy, graphs with position along common scales enable the most accurate estimates. We extend this idea arguing that for temporal data, which often includes multiple simulateneous time series, the context of the position matters in terms of how accurate and fast readers can extract the information on local comparisons.

Question and Hypothesis
-----------------------

We want to examine and test the principles of visualization and run task regarding a graphical perception experiment. In this experiment, we aim to answer the question: When temporal data is structured to have multiple groups, is separated line graph (small multiple lines) more efficient in conveying accurate information on within group differences than simple line plot? Our basic assumption is that the number of time series lines in a graph has strong effect on the perception performance. We develop the following hypotheses:

> *H*<sub>1</sub>: A separated line graph enables more accurate estimate for within group differences than a simple line graph.

> *H*<sub>2</sub>: A separated line graph by categories will take readers less time to make decision in this occasion.

Experiment Design
-----------------

To test these two hypotheses, we designed an experiment consisting of one task: estimating the ratio of 2 data points from a plot. The participants have to read the values of 2 data points (for 1 year) from data, and estimate the percentage of the lower one is to the higher one. To compare the effect of 2 types of line graphs, the experiment randomly presents data using one type of line plots.

We first offer a screening question to subjects to avoid unreliable answers. Each subject needs to answer, "which group has the highest income value across the years?", to the graph below. The answer should be "Black, Man". If the subject fails this test, the survey will end.

![screening](image/4linegraph.png)

Once the participant passed the screening test, they entered into our random experiment. They will be required to ask the same question for one of the following 2 graphs: In 2014, what percentage does the black women's income take out of black men's income? We asked the subjects to roughly estimate the percentage, and provide the formula to do it in case our question is vague in some ways.

![plot1](image/4linegraph.png)

![plot2](image/separatedline.png)

Data and Descriptive Analysis
-----------------------------

In total, we received 248 responses from Amazon Turk in about 72 hours. Among these responses, 20 responses are not finished before we close the survey, and 37 responses failed our screening test. Here we will do our descriptive analyses on our finished responses that passed our screening test, which include 191 observations. Among these observations, 88 are randomly assigned to answer the question for lines graph, and 103 are assigned to small multiple lines group.

We reported the survey answers from these two groups in "Fig: Density of Survey Answers". One can tell that in both groups, most people have an answer value close to the true value. However, the "small multiple lines" group seems to have higher chance to reach the true value according to this preliminary result, which could mean our 1st hypothesis(*H*<sub>1</sub>) is right.

![](experiment_files/figure-markdown_github/descriptive%20analysis%201-1.png)

Then let's take a look at the answering speed of participants. It seems that "line graph" has advantage in this scenario, which has more subjects completing the question in less time than average. And in "small multiple lines", there are more subjects taking more than 250 seconds to finish the survey. This preliminary result shows that our 2nd hypothesis(*H*<sub>2</sub>) might be wrong. In the next section, we will use methods that are more reliable to test these two hypotheses.

![](experiment_files/figure-markdown_github/descriptive%20analysis%202-1.png)

Analysis and Results
--------------------

### Accuracy

Following the methodology from Cleveland and McGill(1984), we decided to measure how the respondent estimates incorrectly using log error accuracy.

The measure that we used is defined as:

![plot3](image/formula.png)

and large log error accuracy means the estimate is far from true value.

<table style="width:90%;">
<colgroup>
<col width="41%" />
<col width="18%" />
<col width="30%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">line graph</th>
<th align="center">small multiple lines</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>Mean Log error Accuracy</strong></td>
<td align="center">3.482</td>
<td align="center">3.417</td>
</tr>
</tbody>
</table>

The mean of log error accuracy of two questions are shown in the above table. From the table we can observe that the mean of log error accuracy with "small multiple lines"" is higher than that with "line graph" and the difference is **0.0249**. From this result, we can conclude that in "small multiple lines", people tend to estimate more accurate than "line graph".

![](experiment_files/figure-markdown_github/analysis%202-1.png)

Now take a look at the density plot of log error accuracy by two graph types. The vertical line in the left side is the case that an estimate is identical to the true value, i.e. $log\_{2}\\frac{1}{8} = -3$. Since the log error accuracy takes the absolute value in the formula, all the results fell into the right side of accurate estimate on the plot. When we compared these two graphs, shapes are similar to each other. But a peak point of "line graph" located on the right side when comparing to the graph of "small multiple lines". This indicates that the resondents who assigned to "small multiple lines" tend to have more accurate estimates. This result is consistent with our hypothesis *H*<sub>1</sub>.

### Speed

<table style="width:83%;">
<colgroup>
<col width="34%" />
<col width="18%" />
<col width="30%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">line graph</th>
<th align="center">small multiple lines</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>Mean Duration</strong></td>
<td align="center">76.34</td>
<td align="center">101.699</td>
</tr>
<tr class="even">
<td align="center"><strong>Mean Duration within estimate [47.5,67.5]</strong></td>
<td align="center">80.2</td>
<td align="center">84.512</td>
</tr>
</tbody>
</table>

To test our hypotesis *H*<sub>2</sub>, we now focus on the duration time to answer within each graph. From the 1st row of above table, mean of duration time with "small multiple lines" is a lot larger than the mean of duration time with "line graph" and the difference is about 25 seconds. This indicates that overall, "line graph" renders information faster than "small multiple graph". However, as we observed in the descriptive analysis, there are outliers in duration time, we need to consider outliers to remedy. We decided to focus only on an interval around true estimate value 57.456. We arbitrary selected the interval as \[-10, 10\] from the true estmate value, \[47.5, 67.5\]. Then we calculated the mean of duration time of each graph type and the result is shown in the 2nd row in the table. These duration times also indicate that the time duration with "small multiple lines" is larger and the difference is about 4 seoncds. This result contradicts with our hypothesis *H*<sub>2</sub>.

### Accuracy & Speed

<table style="width:94%;">
<colgroup>
<col width="45%" />
<col width="18%" />
<col width="30%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">line graph</th>
<th align="center">small multiple lines</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>Mean Log error Accuracy</strong></td>
<td align="center">3.482</td>
<td align="center">3.417</td>
</tr>
<tr class="even">
<td align="center"><strong>Mean Log error Accuracy within estimate [47.5, 67.5]</strong></td>
<td align="center">2.109</td>
<td align="center">1.798</td>
</tr>
<tr class="odd">
<td align="center"><strong>Mean Log error Accuracy with duration under 25 sec</strong></td>
<td align="center">3.863</td>
<td align="center">3.353</td>
</tr>
</tbody>
</table>

Additionally, we further conducted analyses which consider accuracy and speed at the same time. We made the same criteria as we applied in previous section "Speed" in the second row and calucalted the log error accuracy whithin the interval. The log error accuracy with "line graph" is larger than the log error accuracy with "small muliple lines" within the interval estimate \[47.5, 67.5\]. This indicates that even within the groups that made a close estimate to the true value, the mean of log error accuracy with "small multiple lines" is smaller than that with "line graph". Thus, "small multiple lines" are more powerful in terms of accuracy.

We also made another criteria: we compared accuracy for the reponsdents who made their decision relatively fast, under 25 seconds. The result is in the 3rd row in the above table, and this also shows that the mean log error accuracy with "small multiple lines" is smaller. Thus we can conclude that the respondents, who assigned with "small multiple lines" and decided their decision under 25 seconds, were able to make more accurate estimate than the respondents who assigned with "line graph" and decided their decision under 25 seconds.

Conclusion
----------

For this experiment, we hypothesized that with multiple time series, all series in one simple line plot would increase the difficulty for subjects to extract the information regarding local comparison, more specifically, within group differences for the data structured with groups. By difficulty, we mainly focused on: (1) the difficulty to extract accurate information; and (2) difficulty to extract information in a short time. Hence our experiment aims to look at the accuracy and answering speed for two randomized groups, exposing to "line graph" and "small multiple lines". The analysis and results seem to be consistent wtih our first hypothesis *H*<sub>1</sub>, a separated line graph enables more accurate estimate for within group differences than a simple line graph. However, the analysis and results seem to contradict with our second hypothesis *H*<sub>2</sub>, a separated line graph by categories will take readers less time to make decision in this occasion.

Overall the distribution of estimate by each graph type showed that the result of two graphs are similar to each other. To analyze closely, we applied the log error accuracy to measure how the respondent estimate the value incorrectly. The large log error accuracy indicates the estimate is far from the true value. The density plot of the log error accuracy and the table with the mean of log error accuracy with each graph type, "line graph" and "small multiple lines", showed that overall the log error accuracy of "small multiple lines" is smaller than that of "line graph". This means that the respondents perform better with "small multiple lines" and thus, "small multiple lines" is less difficult to extract accurate information than "line graph".

Secondly, we focus on "speed" and difficulty to extract information in a short time. The density plot of duration time and the table with the mean of duration with each graph type clearly showed that "small multiple lines" took more times to make estimate than "line graph". The respondents with "small multiple lines" tended to spend more time to extract information and this may indicate that the "small multiple lines" have difficulty to extract information compared to "line graph".

Reference & Appendix
--------------------

\[1\] Cleveland, William S., and Robert McGill. "Graphical perception: Theory, experimentation, and application to the development of graphical methods." Journal of the American statistical association 79.387 (1984): 531-554.

\[2\] Cairo, Alberto. The truthful art: Data, charts, and maps for communication. New Riders, 2016.

\[3\] Heer, Jeffrey, and Michael Bostock. "Crowdsourcing graphical perception: using mechanical turk to assess visualization design." Proceedings of the SIGCHI conference on human factors in computing systems. ACM, 2010.

\[4\] Javed, Waqas, Bryan McDonnel, and Niklas Elmqvist. "Graphical perception of multiple time series." IEEE transactions on visualization and computer graphics 16.6 (2010): 927-934.

\[5\] Heer, Jeffrey, Nicholas Kong, and Maneesh Agrawala. "Sizing the horizon: the effects of chart size and layering on the graphical perception of time series visualizations." Proceedings of the SIGCHI Conference on Human Factors in Computing Systems. ACM, 2009.

``` r
# This is our data operations for constructing the survey.
# We got our source data from IPUMS.
data = fread("/Users/apple/Dropbox/18spring/dataviz/usa_00002.csv", 
             na.strings=c("0000000", "0000001", "9999999"))
dat = data[, .(avginc = mean(INCTOT, na.rm=TRUE)), by=.(YEAR, SEX, RACE)]

rm(data)

dat = dat[, gender := ifelse(SEX==1, "Man", "Woman")]
dat = dat[, race := ifelse(RACE==1, "black", "not black")]
dat = dat[YEAR!=1970, .(inc = mean(avginc, na.rm=TRUE)), by=.(YEAR, gender, race)]

ggplot(data=as.data.frame(dat), aes(x=YEAR, y=inc)) +
  geom_point() + 
  geom_line(aes(color = race, linetype=gender)) +
  scale_x_continuous(breaks = seq(2007, 2016, 1)) +
  scale_y_continuous(limits = c(0,60000), breaks = seq(0, 60000, 10000)) +
  theme_minimal() +
  labs(title = "Income Growth by gender and race",
       x = "Year",
       y = "Income",
       caption = "Source: IPUMS") +
  theme(panel.grid.minor = element_blank(), text = element_text(size=18))

ggplot(data=as.data.frame(dat), aes(x=YEAR, y=inc)) +
  geom_point() + 
  geom_line(aes(color = race, linetype=gender)) +
  facet_wrap(~ race) +
  scale_x_continuous(breaks = seq(2007, 2016, 1)) +
  scale_y_continuous(limits = c(0,60000), breaks = seq(0, 60000, 10000)) +
  theme_minimal() +
  labs(title = "Income Growth by gender and race",
       x = "Year",
       y = "Income",
       caption = "Source: IPUMS") +
  theme(panel.grid.minor = element_blank(), text = element_text(size=15), panel.spacing = unit(2, "lines"))

# Answer to our main survey question:
percentage = 100 * dat[YEAR==2014 & gender == "Woman" & race == "black", inc] / dat[YEAR==2014 & gender == "Man" & race == "black", inc]
```
