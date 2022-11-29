## Exploratory Data Analysis
1. Exploratory Data Analysis
    1. Data Sourcing
        1. Introduction to EDA
           - EDA is arguably the most important and revelatory step in any kind of data analysis.
        2. Public and Private Data
           - A large amount of data collected by the government or other public agencies is made public for the purposes of research. Such data sets do not require special permission for access and are therefore called public data.
           - private data is that which is sensitive to organisations and is thus not available in the public domain. Banking, telecom, retail, and media are some of the key private sectors that rely heavily on data to make decisions.
        3. Private Data
            - While banks use data to make credit related decisions, telecoms use data to optimise plans for customers and predict customer churn. HR data analytics helps identify and predict employee behaviour.
            - While retail data analytics helps drive decisions such as pricing and stocking, the media industry uses data extensively to target viewers better. Advertisers use data to identify best avenues for targeting customers, while journalists use data visualisation to aid information.
        5. Public Data
            - [Awesome Public Datasets on GitHub](https://github.com/caesar0301/awesome-public-datasets) contains a directory of sports data from tennis, cricket, football, basketball and other sports
    2. Data Cleaning
        1. Fixing Rows and Columns
            - Checklist for Fixing Rows
                * Delete summary rows: Total, Subtotal rows
                * Delete incorrect rows: Header rows, Footer rows
                * Delete extra rows: Column number, indicators, Blank rows, Page No.
            - Checklist for Fixing Columns
                * Merge columns for creating unique identifiers if needed: E.g. Merge State, City into Full address
                * Split columns for more data: Split address to get State and City to analyse each separately
                * Add column names: Add column names if missing
                * Rename columns consistently: Abbreviations, encoded columns
                * Delete columns: Delete unnecessary columns
                * Align misaligned columns: Dataset may have shifted columns
        3. Missing Values
            - **Set values as missing values**: Identify values that indicate missing data, and yet are not recognised by the software as such, e.g treat blank strings, "NA", "XX", "999", etc. as missing.
            - **Adding is good, exaggerating is bad**: You should try to get information from reliable external sources as much as possible, but if you can’t, then it is better to keep missing values as such rather than exaggerating the existing rows/columns.
            - **Delete rows, columns**: Rows could be deleted if the number of missing values are significant in number, as this would not impact the analysis. Columns could be removed if the missing values are quite significant in number.
            - **Fill partial missing values using business judgement:** Missing time zone, century, etc. These values are easily identifiable.
        5. Standardising Values
            - **Standardise units**: Ensure all observations under a variable have a common and consistent unit, e.g. convert lbs to kgs, miles/hr to km/hr, etc.
            - **Scale values if required**:  Make sure the observations under a variable have a common scale
            - **Standardise precision** for better presentation of data, e.g. 4.5312341 kgs to 4.53 kgs.
            - **Remove outliers**: Remove high and low values that would disproportionately affect the results of your analysis.
            - **Remove extra characters** like such as common prefix/suffix, leading/trailing/multiple spaces, etc. These are irrelevant to analysis.
            - **Standardise case**: There are various cases that string variables may take, e.g. UPPERCASE, lowercase, Title Case, Sentence case, etc.
            - **Standardise format**: E.g. 23/10/16 to 2016/10/23, “Modi, Narendra" to “Narendra Modi", etc.
        7. Invalid Values
            -  **Encode unicode properly**: In case the data is being read as junk characters, try to change encoding, E.g. CP1252 instead of UTF-8.
            -  **Convert incorrect data types**: Correct the incorrect data types to the correct data types for ease of analysis. E.g. if numeric values are stored as strings, it would not be possible to calculate metrics such as mean, median, etc. Some of the common data type corrections are — string to number: "12,300" to “12300”; string to date: "2013-Aug" to “2013/08”; number to string: “PIN Code 110001” to "110001"; etc.
            -  **Correct values that go beyond range**: If some of the values are beyond logical range, e.g. temperature less than -273° C (0° K), you would need to correct them as required. A close look would help you check if there is scope for correction, or if the value needs to be removed.
            -  **Correct values not in the list**: Remove values that don’t belong to a list. E.g. In a data set containing blood groups of individuals, strings “E” or “F” are invalid values and can be removed.
            -  **Correct wrong structure**: Values that don’t follow a defined structure can be removed. E.g. In a data set containing pin codes of Indian cities, a pin code of 12 digits would be an invalid value and needs to be removed. Similarly, a phone number of 12 digits would be an invalid value.
            -  **Validate internal rules**: If there are internal rules such as a date of a product’s delivery must definitely be after the date of the order, they should be correct and consistent.
        9. Filtering Data
            - **Deduplicate data**: Remove identical rows, remove rows where some columns are identical
            - **Filter rows**: Filter by segment, filter by date period to get only the rows relevant to the analysis
            - **Filter columns**: Pick columns relevant to the analysis
            - **Aggregate data**: Group by required keys, aggregate the rest
    3. Univariate Analysis
        1. Data Description
            - types of variables:
                * Categorical variables
                    + **Unordered**: Unordered ones do not have the notion of high-low, more-less etc. Example:
                        * Type of loan taken by a person = home, personal, auto etc.
                        * Organisation of a person = Sales, marketing, HR etc.
                    + **Ordered**: Ordered ones have some kind of ordering. Some examples are
                        * Salary = High-Medium-low
                        * Month = Jan-Feb-Mar etc.
                * Quantitative / numeric variables               
        3. Unordered Categorical Variables - Univariate Analysis 
            * Plots are immensely helpful in identifying hidden patterns in the data 
            * It is possible to extract meaningful insights from unordered categorical variables using rank-frequency plots
            * Rank-frequency plots of unordered categorical variables, when plotted on a log-log scale, typically result in a power law distribution
        4. Ordered Categorical Variables - Univariate Analysis 
            - whenever you have a continuous or an ordered categorical variable, make sure you plot a histogram or a bar chart and observe any unexpected trends in it.
        5. Quantitative Variables - Univariate Analysis
            - Mean and median are single values that broadly give a representation of the entire data
            - Median is almost always a better measure of ‘representativeness’
        7. Quantitative Variables - Summary Metrics
            - Quartiles are a better measure of the spread than the standard deviation. 
            - A good way to visualise quartiles is to use a box plot. 
            - The 25th percentile is represented by the bottom horizontal line of the box, the 75th is the top line of the box, and the median is the line between them.
        9. Summary
            - **Metadata description** describes the data in a structured way. You should make it a habit of creating a metadata description for whatever data set you are working on. Not only will it serve as a reference point for you, it will also help other people understand the data better and save time.
            - **Distribution plots** reveal interesting insights about the data. You can observe various visible patterns in the plots and try to understand how they came to be.
            - **Summary metrics** are used to obtain a quantitative summary of the data. Not all metrics can be used everywhere. Thus, it is important to understand the data and then choose what metric to use to summarise the data.
    4. Segmented Univariate
        1. Basis of Segmentation
            - The entire segmentation process can be divided into four parts:
                1. Take raw data
                2. Group by dimensions
                3. Summarise using a relevant metric such as mean, median, etc.
                4. Compare the aggregated metric across groups/categories
        3. Quick way of Segmentation 
            - It looks very repetitive task to perform the same analysis on the large bunch of variables. One way of solving this problem is to make a table with the categorical variables on one axis and the numeric variables (or measures/facts) on the other
        4. Comparison of Averages
            - "Don’t blindly believe in the averages of the buckets — you need to observe the distribution of each bucket closely and ask yourself if the difference in means is significant enough to draw a conclusion. If the difference in means is small, you may not be able to draw inferences. In such cases, a technique called hypothesis testing is used to ascertain whether the difference in means is significant or due to randomness.“ Don’t worry if you do not get the concept of hypothesis correctly, It will be dealt separately in hypothesis module."
        5. Comparison of Other Metrics
            - 25th percentile, the median and the 75th percentile
    5. Bivariate Analysis
        1. Bivariate Analysis on Continuous Variables
            - correlation is a number between -1 and 1 which quantifies the extent to which two variables ‘correlate’ with each other.
                * If one increases as the other increases, the correlation is positive
                * If one decreases as the other increases, the correlation is negative
                * If one stays constant as the other varies, the correlation is zero
        3. Business Problems Involving Correlation
            - The correlated variables are grouped by similarities, and correlation can also be calculated for ‘groups of variables’. This is called ‘clustering’
        5. Bivariate Analysis on Categorical variables
            * There are two fundamental aspects of analysing categorical variables:
                1. To see the distribution of two categorical variables.
                2. To see the distribution of two categorical variables with one continuous variable
    6. Derived Metrics
        1. What are Derived Metrics ?
            * You often need to create new variables using the existing ones to get meaningful insights
            * there are three different types of derived metrics:
                1. Type-driven metrics
                2. Business-driven metrics
                3. Data-driven metrics
        2. Types of Derived Metrics: Type Driven Metrics
            - **Nominal variables**: Categorical variables, where the categories differ only by their names; there is no order among categories, e.g. colour (red, blue, green), gender (male, female), department (HR, analytics, sales)
            - **Ordinal variables**: Categories follow a certain order, but the mathematical difference between categories is not meaningful, e.g. education level (primary school, high school, college), height (high, medium, low), performance (bad, good, excellent), etc.
                - Ordinal variables are nominal as well
            - **Interval variables**: Categories follow a certain order, and the mathematical difference between categories is meaningful but division or multiplication is not, e.g. temperature in degrees celsius ( the difference between 40 and 30 degrees C is meaningful, but 30 degrees x 40 degrees is not), dates (the difference between two dates is the number of days between them, but 25th May / 5th June is meaningless), etc.
                -  Interval variables are both nominal and ordinal
            - **Ratio variables**: Apart from the mathematical difference, the ratio (division/multiplication) is possible, e.g. sales in dollars ($100 is twice $50), marks of students (50 is half of 100), etc.
                - Ratio variables are nominal, ordinal and interval type
        4. Types of Derived Metrics: Business Driven Metrics
            - Deriving metrics from the business perspective is not an easy task. It requires a decent domain experience. Without understanding the domain correctly, deriving insights becomes difficult and prone to errors. 
        5. Types of Derived Metrics: Data Driven Metrics
            - data-driven metrics can be created based on the variables present in the existing data set. For example, if you have two variables in your data set such as "weight" and "height" which shows a high correlation. So, instead of analysing "weight" and "height" variables separately, you can think of deriving a new metric "Body Mass Index (BMI)"
        
        
        
