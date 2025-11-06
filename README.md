Part 1: Data Analysis and Insight 
1.	Data Overview
The dataset titled "Cost of Living" provides historical economic data on average monthly income and cost of living across 12 countries from 2000 to 2023, making it a valuable resource for analyzing global economic trends, affordability, purchasing power, and regional disparities over time.
 <img width="470" height="418" alt="image" src="https://github.com/user-attachments/assets/88c5123b-381b-4120-8911-a35478c2ea49" />

It includes 202 rows (including header) and 5 columns: Country, Year, Average Monthly Income, Cost of Living, Region.

•	Country: Name of the country (12 unique values: Australia, Brazil, Canada, China, France, Germany, India, Japan, Mexico, Russia, South Africa, United States).

•	Year: Year of data collection (2000–2023)

•	Average_Monthly_Income: Estimated average monthly earnings per person 

•	Cost_of_Living: Estimated average monthly expenses per person 

•	Region: Geographical classification (Asia, Europe, Africa, North America, South America, Oceania)

Although the source of the data in this file is not mentioned, it may get that from international, renowned databases like Numbeo, World Bank, etc.

This dataset provides valuable context for understanding global living standards and economic disparities. It can be used to compare how income levels relate to living costs across different parts of the world and to analyze how these relationships change over time. Researchers, policymakers, and economists may find this dataset useful for examining patterns in economic development, affordability, and regional differences in living conditions.

2.	Data Cleaning

Identify missing values and decide how to handle these missing values:
<img width="519" height="385" alt="image" src="https://github.com/user-attachments/assets/e7f0575a-fe9f-4cee-b9ee-54e0cae6d4fb" />
 
Filtering the Average_Monthly_Income column by unselecting all then choosing blanks.
<img width="940" height="99" alt="image" src="https://github.com/user-attachments/assets/2dd61dac-ca19-478e-b8fa-793afcf05bbc" />
 
After that, the missing values appear in column C (Average_Monthly_Income) at rows 162 and 178.

<img width="1367" height="474" alt="image" src="https://github.com/user-attachments/assets/f52dea58-189d-43e5-8891-5e967960e3f5" />

 
To deal with this, I chose to use deletion (omission), because this is a simple and safe way to clean data. In this method, any row with missing information is removed rather than try to guess or fill in the blanks. I chose this method because it keeps my data honest, not estimated. In Excel, I did this by selecting the two rows with missing income values, right clicking, and choosing “Delete entire row.” After doing this, the dataset went from 202 rows to 200 rows.

I used deletion because the proportion of the data missing is small just less than 1%, therefore removing those rows doesn't affect my results much. It's a simple, clear, and safe choice that helps make sure my findings are accurate and based only on complete information.
<img width="940" height="132" alt="image" src="https://github.com/user-attachments/assets/52750204-4aec-405f-b087-9e46457db5f6" />
 
Filtering the Region column by unselecting all and then choosing blanks. After that, the missing values are in column E (Region) at rows 26 and 39, both belonged to Mexico in the years 2000 and 2003.

To fix this, I used manual imputation, which means filling in the missing data by hand. Since Mexico is in North America, I replaced both missing Region values with “North America.” This method is simple, accurate, and makes sure the data matches real-world information.

•	Identify any duplicate rows and remove duplicate rows if necessary
<img width="858" height="179" alt="image" src="https://github.com/user-attachments/assets/f37bb7d8-288d-4e16-87aa-258978d05e48" />

 
After deleting the two rows with missing income data, I had 200 records left, then I then used Excel’s “Remove Duplicates” tool, which deleted two identical rows, leaving 197 unique rows. This cleaned out perfect duplicates without losing any real information.

3.	Descriptive Statistics
<img width="672" height="276" alt="image" src="https://github.com/user-attachments/assets/1f4b5fcf-ab46-49ec-aff9-b85f24755ffe" />

Descriptive statistics provide an overview of the average monthly income and cost of living of 197 observations. The data indicates an average monthly income of 4,243.97 with a cost of living expense of 3,697.51, resulting in a modest, but positive, cash balance averaging 546.46. The median values were close to the means, at 4,266.46 for income and 3,649.03 for the cost of living, indicating relatively symmetric values and no particular skewness below or above the means. Both variables reflect high variability as evidenced by their standard deviations, 2,127.41 for income and 1,990.70 for the cost of living, as well as their ranges (7,441.82 and 6,516.53), which reflects global differences in earnings and living expenses. Overall, these results reveal that the average income slightly exceeds the average cost of living, significant disparities exist across countries

Insight 1: Income and Cost of Living Variability Boxplot
<img width="748" height="446" alt="image" src="https://github.com/user-attachments/assets/04038505-8e98-44d5-96d9-a0dce16fb2b0" />
 
This boxplot illustrates that income varies far more than cost of living: income ranges from 534 to 7,976, while cost only ranges from 464 to 6,981. The middle 50% of income also spreads wider (about 2,341 to 6,093) than cost of living (1,852 to 5,413), meaning income differences across countries are much larger. The median income is higher at roughly 4,266 versus a median cost of about 3,698, showing that earnings generally exceed living costs but not evenly. No outliers appear in either dataset. Overall, the chart highlights greater inequality in income and more stability in cost of living across regions.

Insight 2: Comparison of Average Monthly Income and Cost of Living by Region
<img width="553" height="329" alt="image" src="https://github.com/user-attachments/assets/223ae204-a98c-454c-9bdc-6e800b074cc6" />

The graph shows that Europe and Asia have higher average incomes in comparison to the cost of living, which indicates stronger economies with more purchasing power. North America has a balanced relationship where high incomes are matched by similarly high costs of living. In contrast, Africa, South America, and Oceania show much smaller gaps, indicating tight financial conditions and lower overall living standards.

