# Where is Your Money and Why?
### Austin Barish, Raunak Advani, Jordan Rinaldi, and Victor De Lima


### NOTE: The best way to view our project is through our website by selecting ./website/index.html. 


## Executive Summary:
Our projects looks at FDIC banking data to help our audience better understand the US Banking System, particularly where and how American dollars are consolidated. The FDIC is an independent government agency tasked with insuring deposits, supervising financial institutions, and dealing with the orderly management of a bank failure. Most famously, the FDIC provides a standard insurance amount of $250,000 per depositor, per insured bank, which has accomplished for no depositor to lose a penny of insured funds due to a failure since 1934 (Federal Deposit Insurance Corporation 2020). The case of the FDIC showcased just one of the fascinating aspects of the U.S. banking system that was largely unknown to the general public. It also inspired us to carry out this project. With it, we aim to inform our audience of several distinguishing facts about the U.S. banking system.

## Data Descriptions:

You can view ./website/data.html for the full links and a more in depth description.

### Banking Data

We gathered the data from the FDIC’s API (Federal Deposit Insurance Corporation 2023). The API allows querying financial institutions’ general and structural data, historical financial information, and bank failure information. In this study, we focus on historical financial information. The FDIC API offers a comprehensive menu of fields covering all the previously mentioned topics, from financial ratios, income and balance sheet data, bank structure information, and more.

Even though the website offers a query and CSV-download user interface, we constructed our own Python API client to make the process faster (https://github.com/anly503/spring2023-project-team-4/tree/main/code/data_gathering). The client uses the Python requests library to bring in the API’s json response, where function get_all_financial_reporting_data() processes the endpoint, reporting period, fields, and result_limit as required.

We then collected the quarterly financial information for all insured banks from Q1 1992 to Q4 2022 (30 years). The data is available here. Next, we cleaned the data to combine the 30 years’ worth of data, which totaled 1,014,549 rows. Full column descriptions available on the data.html tab.

### Zip Coordinates

We collected coordinate data for developing geospatial visualizations. The data consists of zip codes and cartographic boundaries. The zip code data originates from the ZIP Code Tabulation Areas based on the 2020 Census tabulation blocks, available in US Census Bureau (2022). The cartographic boundaries consist of a shapefile describing states at the 500k resolution level, available in US Census Bureau (2021).

### quarterly_banks_by_state.csv
The data for this plot comes from the quarterly bank financial data collected using the FDIC API. Then, in the Data Cleaning tab, we grouped the data by state, by bank, and by date meaning our data now showed the total assets, deposits, etc. that each bank in a given state held in a given quarter. This helped to shrink what was previously a massive dataset. However, that was still quite large. Therefore, that data file (./data/quarterly_banks_by_state.csv) is not in our github, however, you can see the code to create this file under ./code/data_cleaning/quarterly_data_cleaning.ipynb. Running this notebook will allow you to see exactly what data we are using.

# Code Files:

## Data Gathering:

- fdic_data_api_client.ipynb: Downloads quarterly data over the last 30 years using the FDIC's API

## Data Visualization:

- quarterly_data_cleaning.ipynb: Compiles all of the quarterly data into one larger csv file for easier usage.

- plot-3.ipynb: Also known as Banking Data by State, this file uses plotly to line plot the cumulative banking data for six notable states and splits up the four largest banks from all other banks to highlight their size in their home states, as well as how some unlikely states hold larger deposits than the three states with the largest GDP.  

- geospacial_cleaning.ipynb: shows a 2x2 grid of Folium maps depicting the relative size of fourth-quarter U.S. bank assets per state every ten years since 1992 using Leaflet. Additionally, it creates a plot that shows dots representing the ZIP Code of the FDIC-insured banks’ location within the U.S., where the bubbles represent the relative size of the assets, allowing one to see the location of the largest banks.

- eqr.ipynb: examines banks that represent the top and bottom 20 in average EQR by quarter. It filters out any banks that do not appear in the data for more than 100 quarters (roughly 80% of the quarters). Using Altair it creates a linked bar and line chart allowing for user selection. Additionally, it creates a quarterly line plots. It creates a heatmap contains over 200,000 unique banks, all with average total assets owned below 500,000. Finally, it creates an animated bubble plot showing Equity Capital and Equity Capital Ratio by Year.
