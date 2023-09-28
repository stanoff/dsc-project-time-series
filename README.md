**TIME SERIES ANALYSIS FOR REAL ESTATE INVETSMENT**

**INTRODUCTION**

Real estate refers to physical property consisting of land, buildings, and any natural resources found on or beneath the land's surface. It is a tangible asset that encompasses a wide range of properties, including residential homes, commercial buildings, industrial facilities, vacant land, and more. Real estate is a fundamental component of the economy and plays a significant role in various aspects of society, including housing, commerce, and investment.Real estate is a valuable asset class that can appreciate in value over time, generate rental income, and provide a hedge against inflation. It is also a common investment choice for individuals and institutions looking to diversify their portfolios. The real estate market can be influenced by factors such as supply and demand, economic conditions, interest rates, and government policies.

**STATEMENT OF PROBLEM**

Real estate constitutes a substantial portion of wealth for many individuals, particularly homeowners in the United States. The dynamics of the real estate market are influenced by a multitude of factors, including government policies, demographic trends among potential buyers, affordability considerations, disparities in housing access, geographic location, cash flow prospects, liquidity conditions, and the prevailing economic environment. The interplay of these numerous variables often complicates the decision-making process for prospective buyers. To address this complexity, Apex Consultants aims to develop a predictive time series model capable of identifying the top five zip codes for strategic real estate investments.

**Main Objectives**

1. To develop a time series model that would predict the top five zipcodes to invest in


**Specific Objectives**

1. To serve as a consulting partner for Apex Consultant  Firm, offering well-informed recommendations on the top five zip codes for investment opportunities.

2. To analyze and track historical trends in house price returns to understand how they have evolved over time.

**Data Understanding**

The dataset used in this study was obtained from Zillow Research Website and has 14,723 rows and 272 columns. The representation of each and every column present in our dataset is discussed below:

RegionID - shows the unique ID of each region and it is an integer(int64) data type.

RegionName - shows the name of the region by zipcode and it is an integer(int64) data type.

City - shows the city where the region is located which is of string data type.

State - shows the state where the region is located and it is of string(object) data type.

Metro - shows the metropolitan area where the region is located (if applicable).

CountyName - shows the name of the county where the region is located.It is a string (object) data type.

SizeRank - shows the relative size of the region compared to other regions in the datase and it is an integer (int64) data type.

1996 upto 2018 - 	depicts the median home price for the region in months and years. It is a float (float64) data type.


**Feature Engineering**

We will create two new columns called ROI and %ROI which is the known return on investment.The return on investment allows one to measure the profitability of an investment.It is calculated by dividing the net profit( or loss) from an investment by its cost.A positive return on investment indicates that the investment has been profitable whereas a negative return on investment indicates that the investment has not been profitable


ROI is a useful metric for evaluating different investment opportunities. It can help you to identify investments that are likely to be profitable and to avoid investments that are likely to be unprofitable. ROI can also be used to compare the performance of different investments over time.

Generally, ROI is a valuable metric that can be used to measure the profitability of an investment and to make better investment decisions.

**Data Cleaning and Preparation**

To facilitate a comprehensive exploration of our dataset, we have defined several custom functions:

transform_to_long_format(df): converts our dataframe from a wide to long format

data_shape(df): This function reveals the shape of the DataFrame, providing the number of rows and columns in the dataset.

data_info(df): Offering valuable insights, this function presents information about the data, such as column names, data types, and the count of non-null values in each column.

data_missing(df): With a focus on data completeness, this function detects the presence of missing values by examining each column for null entries. If no missing values are found, a message indicating their absence is displayed.

identify_duplicates(df): This function pinpoints and provides details about duplicate rows in the dataset. It computes the count and percentage of duplicated rows present. In case no duplicates exist, it conveys a message confirming their non existence.

**DATA PREPROCESSING**

When working with time series models, we typically assume that the data is stationary, meaning that the statistical properties such as mean, variance, and autocorrelation do not change over time for each lag. This assumption of stationarity is essential for efficient model development.

To ensure the data's stationarity before modeling, two common approaches are employed. First, the Dickey-Fuller test is conducted to formally assess stationarity. Second, the rolling mean is examined visually to detect any trends or patterns that might indicate non-stationarity.

In cases where the data is found to be non-stationary, differencing is applied as a common technique to transform it into a stationary form, thus meeting the requisite conditions for time series modeling.

**Conclusion and Recommendation**

Based on the graph above, the zipcode 94804 has the highest ROI forecast. Therefore, it would be advantageous for the investor to consider investing in this zipcode.

All the Zipcodes show promising predicted prices, with positive returns, except for the 85035 zipcode.

Given the information presented in the graph above, we can provide our top five recommendations along with their expected ROI after three years.

Investors can make informed decisions by considering any of the suggested zipcodes, except for 85035, which does not yield a positive return on investment.