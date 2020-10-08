# Data 512 A1: Data Curation

In this assignment, Wikipedia page traffic data between January 1, 2008 and August 30, 2020 is gathered from two separate [Wikimedia REST API](https://www.mediawiki.org/wiki/Wikimedia_REST_API) endpoints. The data specifically covers monthly desktop and mobile traffic across that time period.

The Wikimedia Foundation REST API terms of use can be found [here](https://www.mediawiki.org/wiki/Wikimedia_REST_API#Terms_and_conditions)

The two API endpoints are:
* The Legacy Pagecounts API ([documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts), [endpoint](https://wikimedia.org/api/rest_v1/#/Legacy%20data)): desktop-site and mobile-site traffic data from December 2007 through July 2016 can be found here.
* The Pageviews API ([documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews), [endpoint](https://wikimedia.org/api/rest_v1/#/Pageviews%20data)): desktop-site, mobile-site, and mobile-app traffic data from July 2015 through last month.

Examples for how to use these APIs can be found [here](https://public.paws.wmcloud.org/User:Jtmorgan/data512_a1_example.ipynb)

The data from the Pageviews API allows filtering of traffic from spiders and crawlers while the data from the Legacy Pagecounts API does not. Traffic from spiders and crawlers was filtered out by setting the `agent` parameter to "user" for the calls to the Pageviews API.

The code in A1.ipynb will generate five JSON files and one CSV file. The five JSON files contain JSON response data from the five API calls made in the code:
* `pagecounts_desktop-site_200801-202008.json`: desktop-site traffic from Legacy Pagecounts API
* `pagecounts_mobile-site_200801-202008.json`: mobile-site traffic from Legacy Pagecounts API
* `pageviews_desktop_200801-202008.json`: desktop-site traffic from Pageviews API
* `pageviews_mobile-site_200801-202008.json`: mobile-site traffic from Pageviews API
* `pageviews_mobile-app_200801-202008.json`: mobile-app traffic from Pageviews API

The CSV file contains processed responses from the previous five API calls. The columns are defined below:
* `year`: the year values in this row were gathered
* `month`: the month values in this row were gathered
* `pagecount_all_views`: total traffic from Legacy Pagecount API
* `pagecount_desktop_views`: desktop-site traffic from Legacy Pagecount API
* `pagecount_mobile_views`: mobile-site traffic from Legacy Pagecount API
* `pageview_all_views`: total traffic from Pageviews API
* `pageview_desktop_views`: desktop-site traffic from Pageviews API
* `pageview_mobile_views`: mobile-site and mobile-app traffic from Pageviews API

Several pandas functions were used to process the data. Documentation for pandas can be found [here](https://pandas.pydata.org/pandas-docs/stable/user_guide/index.html)

Matplotlib was used to create the visualization. Documentation can be found [here](https://matplotlib.org/api/_as_gen/matplotlib.pyplot.html#module-matplotlib.pyplot)