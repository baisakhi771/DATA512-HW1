# Project Title: Rare Diseases Wikipedia Pageviews Analysis

## Project Overview
The goal of this project is to analyze monthly Wikipedia pageviews for articles related to rare diseases, from July 1, 2015, to September 30, 2024. The dataset consists of pageview counts across desktop and mobile access types, allowing us to perform a time-series analysis to explore traffic trends over the past nine years. The project also aims to provide insights into how these articles gained popularity or fluctuated in viewership over time.

## Data Sources
The data used in this project was retrieved from the Wikipedia Pageviews API (https://doc.wikimedia.org/generated-data-platform/aqs/analytics-api/reference/page-views.html), which provides public access to Wikipedia article traffic statistics. The API allows users to specify article titles, access types (desktop or mobile), and time granularity (monthly in this case) to get the pageviews for any Wikipedia article. 

### License of Source Data

The data used in this project is sourced from the Wikipedia Pageviews API, which is provided by the Wikimedia Foundation. The data is publicly available under the terms of the [Creative Commons Attribution-ShareAlike 3.0 Unported License (CC BY-SA 3.0)](https://creativecommons.org/licenses/by-sa/3.0/).

### Wikimedia Foundation Terms of Use

The use of data from Wikipedia is governed by the [Wikimedia Foundation Terms of Use](https://foundation.wikimedia.org/wiki/Terms_of_Use). According to these terms, any redistribution or modification of the data must comply with the CC BY-SA 3.0 license, meaning that appropriate attribution is required, and any derivative works must be distributed under the same license.

### Applicability to Dataset

This project utilizes publicly available data from Wikipedia, which is used in compliance with the terms of the Wikimedia Foundation. The dataset created for this analysis does not modify the original data but is aggregated and analyzed in accordance with these guidelines. Appropriate credit is given to the Wikimedia Foundation for the data provided.


### API Documentation
The pageview data was retrieved via the Wikipedia Pageviews API, which provides access to historical page traffic for Wikipedia articles.
We have used a sample code(https://drive.google.com/file/d/1fYTIX79t9jk-Jske8IwysV-rbRkD4_dc/view?usp=drive_link) for the API call. This sample code is licensed CC-BY(https://creativecommons.org/licenses/by/4.0/).


## Files and Outputs
### Data Files
rare_diseases_cleaned.AUG.2024.csv: This file contains the raw data retrieved from the Wikipedia Pageviews API for all specified rare diseases articles, including desktop and mobile traffic from July 1, 2015, through September 30, 2024.

### Output Files
rare-disease_monthly_mobile_start201507-end202409.json - This file conntains pageview data for access types mobile-app and mobile-web together for each disease and every month from 01 July 2015 to 30 September 2024.
rare-disease_monthly_desktop_start201507-end202409.json - This file conntains pageview data for access type desktop for each disease and every month from 01 July 2015 to 30 September 2024.
rare-disease_monthly_cumulative_start201507-end202409.json - This file conntains pageview data for access types desktop, mobile-app and mobile-web together for each disease and every month from 01 July 2015 to 30 September 2024.


### Graph Images:

Maximum_and_Minimum_average_views.png: Visualizes the articles with the highest and lowest average monthly pageviews for both desktop and mobile access types.
Top_10_peak_page_views.png: Shows time series for the top 10 articles by peak pageviews for desktop and mobile access.
Fewest_months_of_data_combined.png: Displays the articles with the fewest months of available pageview data, highlighting relatively short time series.


## How to Use This Project

Data Retrieval: The data is fetched from the Wikipedia Pageviews API using Python scripts, which can be run to get the most up-to-date data.

Preprocessing: The raw data is cleaned by checking for null and NaN values and combining mobile-web and mobile-app traffic into one "mobile" access type.

Analysis: Several time-series analyses are conducted, including identifying the articles with the highest and lowest average pageviews, the top 10 articles by peak pageviews, and those with the fewest months of available data.

Visualization: The results of the analysis are visualized using line graphs to display trends and patterns over time.

Known Issues or Special Considerations:

Access Types: Mobile-web and mobile-app data are merged into a single "mobile" access type to simplify analysis. This might obscure trends specific to one of the access types.

Data Freshness: The data was last retrieved on October 5, 2024, and includes pageviews up until September 30, 2024.

## License
This project is licensed under the MIT License. See the LICENSE file for details.
