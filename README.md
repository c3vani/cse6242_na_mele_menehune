**DESCRIPTION**
This project analyzes financial complaint data obtained from the Consumer Financial Protection Bureau (CFPB). The CFPB collects complaints about consumer financial products and services, including mortgages, credit cards, bank accounts, and loans. The dataset contains information about the complaints, such as the product type, issue, and company response.

The goal of this project is to identify patterns and trends not only on the categorical and numerical data, such as counts of complaints per product category or per state per month, but also to gain insights on the narratives of the complaints themselves. Currently the CFPB can see that residents of state V complained W amount of times about product X in month Y of year Z, but now they will be able to see patterns in the contents of the complaints. We hope this will pinpoint, on a macro level, what exactly is wrong with the product, instead of just knowing that a complaint was logged in general.

The data set consists of consumer complaints reported to the CFPB. These complaints are listed in the database after the company responds or after they’ve had the complaint for 15 calendar days, whichever comes first. The data are posted in text format and require collation and cleaning. Key variables include the name of the associated financial institution, product, issue drop down, issue free text, and whether or not the company responded in a timely manner

**DATA**
For our Project we used three datasets,  
Complaint Data - CFPB Website
Census Data - US Census Bureau
Standard Zip Codes - United States Zip Codes Org

**INSTALLATION AND EXECUTION**
The installation of the code is very simple, as our project can be accessed through Github and Tableau Public. Our code is written in a mix of Python and R, so you will need to download the appropriate Python and R with Rstudio. Clone the GitHub Repository and import the files to your favorite Python or R IDE. Appropriate library and package installs are included in the code. 

To access and edit the Tableau Public work, go to our Complainalyzer page, log in to Tableau Public, and select the top right button that says “Make a copy”. Add the sheets you want and publish.

**EXECUTABLES**

Tableau : Complainalyzer.twbx
Source data for Tableau : generated from code files listed below and included in the twbx file above, 
Weekly_complaint_forecasts_top_400_companies.csv
2023_2024_product_forecasts.csv
Cfpb_data_summarized.csv
Census_data_by_zip.csv
Cfpb_data_summarized_by_zip_three.csv
cluster_data_IssueZip.csv
PopulationIssue_cluster.csv
Complaints_with_sentiments.csv

CFPB Zip Code Cleaning.rmd - generate files for Tableau with clean zip codes

Census Data Cleaning.rmd - generate combined US Census data files with clean zip codes.

EDA_Complainalyzer.ipynb - Top companies with highest Weekly Complaint count, Product level, Consumer Responses , Income and Population based Data Analysis.

Forecasting Complaint Trends:
Complaint_Time_Series_Facebook_Prophet_v1.0.ipynb - Time Series Forecast Average Weekly Complaint Trend for 2023 and 2024 for Top 400 companies with high complaint counts in each State.
Time Series Forecast Complaints by Product Type.ipynb - Time Series Forecast forecast by product, building a separate model for each of the 9 product types, as well as 3 additional models for the Credit Reporting sub-products.

Clustering:
EDA.ipynb - Explorations were done based on various attributes specifically on the demographic attributes such as looking at top 10 zip codes with highest number of complaints & correlation matrix to see the complaint count across different demographic attributes.
Complaint_clustering.ipynb - K-means clustering to group demographic attributes and complaint data(race population, issue, state, zip code, complaint type, and complaint count), 2 types of clustering was done.

Sentiment Analysis on Complaints:
Sentiment/proj_eda_2.ipynb - contains code related to LDA model building and evaluation, sentiment score analysis using VADER.The data used had customer narratives that were cleaned and tokenized for the LDA. The cleaned narratives were used for sentiment score computation.
Sentiment/Sentence Structure.Rmd - Uses the complaints data without the demographic data to look into the complaint bigrams, apply the community detecting Louvain algorithm, and visualization.

LINKS

Complainalyzer: https://public.tableau.com/app/profile/hillary.latham5228/viz/Complainalyzer/Complainalyzer
Github Repository
https://github.com/c3vani/cse6242_na_mele_menehune

