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
        1. Introduction
        2. Data Description
        3. Unordered Categorical Variables - Univariate Analysis
        4. Ordered Categorical Variables - Univariate Analysis
        5. Quantitative Variables - Univariate Analysis
        6. Quantitative Variables - Summary Metrics
        7. Summary
    4. Segmented Univariate
        1. Introduction
        2. Introduction to Segmented Univariate Analysis
        3. Basis of Segmentation
        4. Quick way of Segmentation
        5. Comparison of Averages
        6. Comparison of Other Metrics
    5. Bivariate Analysis
        1. Introduction
        2. Bivariate Analysis on Continuous Variables
        3. Business Problems Involving Correlation
        4. Bivariate Analysis on Categorical variables
        5. Summary
    6. Derived Metrics
        1. Introduction
        2. What are Derived Metrics ?
        3. Types of Derived Metrics : Type Driven Metrics
        4. Types of Derived Metrics: Business Driven Metrics
        5. Types of Derived Metrics: Data Driven Metrics
        6. Summary
        
        
