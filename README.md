# Site Analysis

This README file is less so much for a python library but rather a versatile data analysis repository. This part covers the further predictive analysis as bonus from the original descriptive analysis notebook and report.

## Tutorial

In this tutorial, we will demonstrate the use of `website_analysis` and the various files within the repository that delve into the mock data sheet named `site_data.csv`.

## The different files.

### Spreadsheet Data

Here is the fulcram of the entire repository. A mock datasheet named as `site_data.csv` meant to simulate customer movements throughout a website on a two month period. The link is found in the bibliography. The columns assign each customer with a unique id, also giving their movements an event id, linked to what event it is, when it occurs and from where the customer found the site. If the event is a purchase, it also assigns a purchase amount.

### Jupyter Data Exploration

The main file within the repository named `website_analysis.ipynb` that applies descriptive analysis to work out what has occured within the website using the datasheet. It begins however by cleaning the data, which doesn't amount to much as initial tests return 'False', meaning there are no duplicate or empty rows. This is followed by understanding the scale of data we are working with, trends over time, cross examining traffic performance, finding funnel ratios between events and finally product analysis. Further detail on the workflow can be found in the report. 

### Descriptive Report

A brief report on the analysis named `website_analysis_report.pdf`, written in LaTeX using overleaf to give a professional outlook. It uses a tau-class, technically a template for research articles and academic documentation, but it appeared to be well suited for the current report. The report covers all developments within the python exploration, also grazing on diagnostic analysis to work out the reason for certain findings, and prescriptive analysis for the measures that could be put in place to improve what should be website goals. 

### Dashboard

A post-analysis production labelled as `website_analysis_dashboard.pdf`, links analysis to presentation, giving a soft launch of data on easier to see slide. It is made using cognos analytics, which I found to be fairly comprehensive and easy to use. The pdf is a solid image of the true dashboard which is interactive and gives further details when highlighted. The main feature is the cross analysis of event type by traffic source, which is delved into deeper beneath by the cross analysis of traffic purchases by product. Of course it also gives general details for a wider point of view in the side profile with a more business focus.

### Site Prediction

Further post-analysis work, with the final type of data analysis, predictive. Here in another jupyter notebook named `website_prediction.ipynb`, we use the prescriptive outcome from the report and build a tool to predict how certain measures would change the revenue. Of course it is only speculative and due to limited data is likely to be deviated from true results. 

For use of the python tools when being used on other data of a similar format, begin:
```python
import pandas as pd
import numpy as np
```
That brings in the necessary python of which they rely on.
```python
reallocate(counts, from_ch, to_ch, pct)
projected_revenue(counts)
```
These were the original tools used, to reallocate the traffic from one source to another and then project the revenue based on the counts, either being the original amounts, or the new after reallocation. 
- `counts` is the weighting given to each traffic source.
- `from_ch` is the first source we are taking from.
- `to_ch` is the second source we are moving them to.
- `pct` is the percentage (as a decimal) of the first we are moving.

```python
potential_revenue(counts, from_ch, to_ch, pct)
```
A comprehensive version of the previous tools for user convenience.
This is then further improved later on with...
```python
potential_revenue_2(from_ch, to_ch, pct)
```
... which gives the same result but with neater code for those who seek a better understanding.

### ReadMe File

This current file to accompany the rest of the repository, despite it being an analysis with little tools rather than a full python library. 

## Explanation

### Reason for website data analysis

The reason for this repository is to develop personal skills surrounding data analysis, and gain better experience in this field I have been learning about for better understanding.

Data analysis itself is a useful skill that helps to organise, interpret, and understand data to identify patterns, make informed decisions, solve problems, and improve outcomes, which can be used on a large scale.

### Types of analysis

There are four main different types of data analysis which we cover, if not, mention within the analysis.
- Descriptive, this is the first step within any workflow with finding out essentially what has happened.
- Diagnostic, accompanying we have why the events of descriptive analysis occured.
- Prescriptive, using the information we have found to suggest measures to be put in place to fix or improve the situation.
- Predictive, using past data to model what future data could look like.

### Limitations

Due to it being a mock, the limitations lie in that we are stuck to using the limited data available to us. Data on a larger timeline, or further details on events could lead to more comprehensive data or further points of analysis.

## Reference

### List of functions

The following functions are written in `website_prediction.ipynb`:

- `reallocate`
- `projected_revenue`
- `potential_revenue`
- `potential_revenue_2`

### Bibliography

Relevant research links:
https://careerfoundry.com/en/blog/data-analytics/different-types-of-data-analysis/
https://www.investopedia.com/terms/d/descriptive-analytics.asp
https://amplitude.com/explore/analytics/what-diagnostic-analytics
https://cloud.google.com/learn/what-is-predictive-analytics
https://www.investopedia.com/terms/p/prescriptive-analytics.asp
https://www.tableau.com/en-gb/learn/articles/data-visualization

Mock data source:
https://www.youtube.com/redirect?event=video_description&redir_token=QUM4Zm9rUjJfU3VCWjJka3dvWUhzamluS3VIcHxBR3JiS2FuVk5jcUc5WTZqelFmbkx1ZHdlbEJsXzlTaEduUzFqdFFEMVpWV0x1bTd5c3lzRjEyc0R3YTNKY0ItVXU0djBDbEtKMHVwZWg4RWdWTDZ6VGMtUVBqdFN2cEhQZF9K&q=https%3A%2F%2Fdrive.google.com%2Fdrive%2Ffolders%2F1fBrE4euyfsTJLAQ5CmIVUGQWALlFQfWO%3Fusp%3Dsharing&v=U-JlXWDqvco


