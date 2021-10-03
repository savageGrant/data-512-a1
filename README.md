# data-512-a1

### Author: Grant Savage

# Goal of project
To aquire, process and analyze a dataset of monthly traffic on English Wikipedia from January 1 2008 through September 2021.

# Data Sources

The project pulls data from Wikimedia's API. We leverage two endpoints:
1.  Legacy Pagecounts API ([documentation]( https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts), [endpoint](https://wikimedia.org/api/rest_v1/#/Pagecounts_data_(legacy)/get_metrics_legacy_pagecounts_aggregate_project_access_site_granularity_start_end) )

2. PageView API ([documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews), [endpoint](https://wikimedia.org/api/rest_v1/#/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end))


## [Wikimedia Foundation REST API terms of use](https://www.mediawiki.org/wiki/Wikimedia_REST_API#Terms_and_conditions)


# Final Data Fields for .csv 
### .csv file can be found in the data_clean folder.

|Column                  | Value     |
|------------------------|-------    |
|year 	                 | YYYY      |
|month 	                 | MM        |
|pagecount_all_views     | num_views |
|pagecount_desktop_views | num_views |
|pagecount_mobile_views  | num_views |
|pageview_all_views      | num_views |
|pageview_desktop_views  | num_views |
|pageview_mobile_views 	 | num_views |

# Known Issues and Special Considerations

The Pageview API excludes spiders/crawlers data, it only takes user agent data, the data from Pagecounts API do not.
All mobile data is unavailable until October 2014. Previous data includes only desktop and main site views.