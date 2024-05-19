# Covid Vaccination Data Analysis

## Table of Contents

- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Tools](#tools)
- [Data Preparation](#data-preparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Findings](#findings)
- [Conclusion](#conclusion)

### Project Overview

This Exploratory Data Analysis aims to provide insights into the administration of Covid vaccines from September 2021 until May 2022 in the UK. By examining the daily doses administered over that time period, we seek to identify trends in the data to see how and where things changed as well as to suggest possible causes. This will grant a deeper understanding of how the vaccination campaign went before running a regression model to predict the number of doses administered on a given day.

### Data Source

Covid Vaccination Data: The dataset used for this analysis is compiled from the UK government’s Coronavirus Vaccinations page in the 'UK_VaccinationsData.xlsx' file. It contains information on the Country, Year, Month, Quarter, day, whether it was a working day and the number of first, second and third doses administered.

### Tools

- Excel - Dataset
- RStudio - Data Cleaning & Analysis

### Data Preparation

In preparing the data for analysis, I performed the following tasks:
1. Loaded the data into R
2. Looked at the structure and descriptive statistics of the data
3. Checked for missing values
4. Handled the missing values
5. Formatted categorical variables as factors
6. Re-checked descriptive statistics

### Exploratory Data Analysis

This EDA involved asking the following questions:

- What is the distribution of daily doses?
- Which country had the most efficient vaccination campaign?
- What is the relationship between different doses?
- What was the trend of daily doses administered over time?
- Was there a difference in doses administered in Q4 of 2021 compared to Q1 of 2022 in England?

### Findings

1. The descriptive statistics, histograms, and boxplots reveal that the distribution of daily doses administered for the first, second, and third doses are positively skewed, with significant outliers present, particularly for the first and third doses. These outliers represent instances where a notably higher number of people were vaccinated in a single day than usual. Despite these outliers, all three doses exhibit a similar distribution pattern, with the vast majority of observations clustered in the lower values. This suggests a consistent trend in the administration of COVID-19 vaccines, with most days witnessing a relatively low number of doses administered, while occasional spikes occur, likely due to factors such as mass vaccination events or changes in vaccination strategies.

2. The bar chart illustrates a clear distribution of COVID-19 vaccinations across the four countries within the UK, with England accounting for the majority of vaccinations, followed by Scotland, Wales, and Northern Ireland. However, to fully contextualize these figures, it's essential to consider each country's population size. Upon comparing the percentage split of vaccines administered to the population split for each country, a notable finding emerges: each country is receiving vaccinations at rates proportional to its population. This observation suggests that no individual country within the UK has been significantly faster or more effective than another in vaccinating its population. Instead, the distribution of vaccinations appears to align closely with the demographic makeup of each country. Such equitable distribution underscores the coordinated efforts and equitable allocation of resources across the UK to ensure widespread vaccine coverage and mitigate disparities in vaccination rates among different regions.

3. The line graph depicting the relationship between the first and second doses reveals a surprising finding: a strong positive relationship exists between them. Contrary to the initial expectation that as more people receive the second dose, fewer would remain on the first dose, the analysis shows that as the number of individuals receiving the first dose increases, so does the number of individuals receiving the second dose. This unexpected result is further corroborated by the Pearson correlation coefficient, which has a value of 0.835, indicating a robust positive correlation between the two variables. Such a correlation suggests that temporal factors, such as increased vaccine availability and phased vaccination campaigns, may have influenced the observed trend. Specifically, the phased approach to vaccine distribution, coupled with efforts to prioritize high-risk populations, likely contributed to the consistent progression of individuals from the first to the second dose, ultimately leading to a positive correlation between the doses administered.

4. The line graph depicting the monthly and cumulative total of vaccines administered over the time period offers valuable insights into the progression of the vaccination campaign and its impact on the course of the pandemic. The monthly total shows a clear peak in December, suggesting a surge in vaccinations during the holiday season. This spike likely reflects a concerted effort by authorities and individuals alike to get vaccinated before Christmas and New Year's, aiming to ensure safer gatherings with friends and family during the festive period. Subsequently, there is a significant drop-off in January, which could be attributed to several factors. It may indicate a decrease in public concern about the pandemic and a corresponding decline in vaccination uptake. Alternatively, it could signify the successful culmination of a vaccination campaign, with a substantial proportion of the population now vaccinated, resulting in a natural decrease in vaccination rates. The cumulative line further highlights how the rate of vaccinations began to plateau from February onwards, suggesting a stabilization in the vaccination campaign, where the initial rapid increase in vaccinations gradually slows as the campaign progresses.

5. Upon further examination of the data, comparing Q4 of 2021 with Q1 of 2022 reveals a substantial disparity in the number of vaccines administered in England for the first and third doses. Utilizing an independent two-sample t-test, we evaluated whether the difference between the average number of second dose vaccines administered in Q4 and Q1 was statistically significant. The results of the test confirmed a significant difference, indicating that the average number of each dose administered in Q4 was notably higher than in Q1. This means that the average number of each dose administered in Q4 was significantly greater than in Q1. This finding strengthens the argument that the pivotal shift in the course of the pandemic occurred during Q4, as evidenced by the heightened vaccination efforts during this period followed by the significant decrease in Q1.

### Conclusion

This exploratory analysis has revealed a significant pivot in the pandemic trajectory following Q4 of 2021, particularly highlighted in December, a period marked by widespread administration of the third and final vaccine doses. Subsequently, there was a notable decline in vaccine administration during the early months of 2022. This decline can be attributed to the culmination of the vaccination campaign, with a substantial portion of the population now fully vaccinated. Additionally, factors such as decreased public concern about COVID-19 and a reduced sense of urgency to get vaccinated may have contributed to the decline in vaccination rates during this period. However, it's essential to acknowledge that this interpretation warrants further investigation to comprehensively understand the multifaceted dynamics influencing vaccination trends and public health behaviors.
