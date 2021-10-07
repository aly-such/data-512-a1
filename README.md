# A.1. Data Curation

## Goal:
#### The broad goal of this project is to get an understanding of accounting for openness and replicability when collecting, cleaning, and analyzing data so that the future audience can recreate, refine, and critique the work. This will lead to more effective and accurate data solutions and findings.
#### More specifically, we will be working through the basic steps of data curation mentioned above for a dataset of monthly traffic to English Wikipedia from January 2008 to September 2021. This will involve aggregating monthly data from the Legacy Page Counts API as well as The Page Views API. We will want to look at desktop, mobile, and overall visits to English Wikipedia during this timeframe.

## Data Sources:
#### 1.	License: https://github.com/aly-such/data-512-a1/blob/e97221a8eb4f5c63c45a4905eb13dceea68c012f/LICENSE
#### 2.	Terms of Use: https://www.mediawiki.org/wiki/REST_API#Terms_and_conditions
#### 3.	Legacy Pagecount API – monthly: https://wikimedia.org/api/rest_v1/#!/Pagecounts_data_(legacy)/get_metrics_legacy_pagecounts_aggregate_project_access_site_granularity_start_end
#### 4.	Pageview API – monthly: https://wikimedia.org/api/rest_v1/#!/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end

## Data Description for en-wikipedia_traffic_200712-202108.csv:
#### 1.	Year = year of data point taken from timestamp, datetime
#### 2.	Month = month of data point taken from timestamp, datetime
#### 3.	Pageview_mobile_views = Number of mobile visits, a combination of app + web, int
#### 4.	Pageview_desktop_views = Number of desktop visits, int
#### 5.	Pageview_all_views = Total number of visits, mobile + desktop, int
#### 6.	Pagecount_mobile_views = Number of mobile visits, Legacy API, int
#### 7.	Pagecount_desktop_views = Number of desktop visits, Legacy API, int
#### 8.	Pagecount_all_views = Total number of visits, Mobile + desktop, Legacy API, int

## Notes:
#### When gathering data from the Pageview API, filter agent to user so that we can work with organic traffic. We want to avoid web scrawlers and spiders because they are bots. The Legacy Pagecount API does not have this option to filter, so there will be minor differences. 

## Visualization:
![image](https://user-images.githubusercontent.com/77369888/136437468-2d4fc1c7-39e2-435b-8a05-acc6f86543b5.png)
