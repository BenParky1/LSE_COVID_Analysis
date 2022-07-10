# LSE_COVID_Analysis
Repo for Assignement 2 of the LSE Data Analytics Course

Assignment 2: Data Analytics using Python

Assignment Report

When importing the data, it has been assigned a default index, both dataframes are ordered by State/Province first then by date. This should help when joining the dataframes together. There are also columns which are of no value to the purpose of this analysis such as Latitude and Longitude. There is also an ‘Others’ State/Province. I am presuming this is possibly the UK mainland and Northern Ireland, but this is not clear so will be left as Others for this analysis.
The data is ordered by date and province. The vaccinated and second dose columns seem to be showing the same data, ie. if a person has had 2 doses they are classified as vaccinated. As I don’t have population data for the provinces, it is unclear if the data figures are high or low. The variables in the numeric columns seem to be cumulative numbers and not numbers specific to that date. There may be errors in the data though, as when scanning through the Gibraltar data frame, the recovered values drop back to 0 on 05/08/2021. This seems unusual as I would expect the values to stay the same as the previous day if 0 people recovered on a certain day. This may be due to a change in the way the data was being recorded. I have subtracted the variables in the first dose column from the second dose column to calculate the number of people who have only had one dose. This does return negative figures for some dates as the first dose value is higher than the second dose value. This will be explored further using visualisations and grouping

When grouping the data by Province and returning the maximum values, it appears that the data may be incorrect or there may be outliers. The maximum number to receive a first dose in some of the provinces seems to be high. I would like to explore how the data looks when plotted on a graph over time and as a scatter graph or box plot to see if there are any outliers and if there are any trends to the data. It should be a lot easier to see if my initial thoughts that the data is cumulative or not from a plot over the timeframe.
I have also grouped the data and used the sum function to see if the data provided for each date is the data for that day, but this makes the values extremely large which does not seem correct.

When plotting data of dose administration rates by time in line graphs it is clear to see that the data for doses is not cumulative and is the number of doses administered per day. When these figures are aggregated, they result is unrealistically high numbers which I can not trust. For this assignment, I am going to use the data provided to create visualisations and to find insights to solve the business problem, but this may not be possible. 

The scatter plot of Vaccinated vs First dose shows a direct correlation between them. As these are numbers for the number of doses and not the percentage of the population, this plot may be showing which province has the bigger populations.

The recovered data is also strange, the recoveries are cumulative until a point where it seems like the data isn’t recorded any longer, causing the recovered value to drop to 0. Due to this I am not going to concentrate on recoveries.

The values for the province ‘Others’ are very large and will skew any data, so others has been removed from the analysis.

From plotting first dose vs second dose and using a hue of province on a scatter plot it is evident that there is a correlation between them. The line graphs showing first and second doses show a high uptake of the vaccines, the first doses administered peaking prior to the fully vaccinated doses. The line graph for deaths shows the waves of deaths as the virus spread and steep rises can be attributed to the different virus variances such as Omicron.

When plotting the number of total deaths on a bar chart, the provinces with higher death totals correlates with the number vaccinated, pointing towards these provinces having higher populations. As the province populations are unknown it is not possible to analyse these deaths as a death per capita.

Twitter hashtag analysis

The csv file of Twitter trends was analysed by searching for text including the #, creating a data frame and then plotting the most common hashtags in a bar chart. Analysis of the results show that various references to COVID-19 were very popular at the time of this data collation. Hashtags relating to COVID-19 include people tweeting about places of high infection, variances on the spelling and formatting of COVID-19 and people were clearly discussing vaccinations at the time. I would be interesting to see how these trends change over time, and if the decline in tweets about COVID and in particular the vaccinations correlate with the reduction in daily vaccinations in the data provided for this assignment.

Conclusion

It is very difficult to gain any real insights into the data as the data seems to be either incorrect or the way data has been captured during the timeframe has been changed. In a real world situation, I would ask for a second opinion from a colleague on the values I have found after merging the data frames and grouping the data, to sense check my work. As the data does not include any province populations, it is very difficult to ascertain whether the vaccine roll out, recoveries and death rates are high or low ie. is 54 deaths on the Isle of Man 0.1% of the population or 1%?
 


![image](https://user-images.githubusercontent.com/102144782/178143201-d2fca3bc-32fd-46eb-9e86-c3af1e4e4c94.png)
