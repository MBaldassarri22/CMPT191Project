# CMPT191Project

## So what is Purchasing Power Parity (PPP)?
In economics, there exists a theory that determines exchange rates called purchasing power parity (PPP), which states that the price levels between two countries should be equal. This theory states that goods in each country should cost the same once the currencies have been exchanged.

### Why Starbucks?
Our motivation for selecting Starbucks tall lattes to analyze for this project, was mainly the popularity of Starbucks as a brand itself. Starbucks is recognized worldwide with varying stores and drinks in different countries, therefore, we decided to see the variations in price that emerged from international Starbucks stores, even identifying which countries are most and least economic (within our sampled data). 

## Run-down of our coding process
This is a break-down of the procedures and steps we took throughout our analysis of data for this project. 

### Scraping the necessary data 
When scraping our data, the first thing we did was to begin by selecting and pasting the URL into our notebook. Subsequently we inspected the website to locate the table needed . Finally, we defined a function: scrape, to then run through the data and extract it into a table we could actually utilize.

### Cleaning the scraped data 
Before beginning to modify the actual numbers and quantities in the table, we removed some miscellaneous parts such as the 3rd column which was not related to the Starbucks Tall Latte, as well as the “$” symbol which would interfere with future calculations. 

### Adjust table
After getting the desired output, we selected our data size of 39 countries with varying prices, including Canada. We then got a table of worldwide currency symbols and codes from Fyorin [insert URL] to join with our existing table of latte prices, matching the countries to their respective currencies. Additionally, local tax rates were also an added part to the table. The data chosen for this task was each country’s sales tax rates [insert citation] that we collected online, then later compiled into a csv file. Since the original table with all the Starbucks prices was in USD, conversion was done to ensure our dataset at the end would be in CAD. This was achieved by applying a formula we created to the table, where prices (in USD) were multiplied by 1.40 (since 1 USD = 1.40 CAD by the time of conversion). 

### Adjust prices and currencies
With the local sales tax rates (in percentage) taken as mentioned above, we attempted to calculate the local prices for Starbucks’ tall lattes in other countries using this data and applied a defined conversion function to the table to accomplish this. We had also manually calculated the local prices for each respective countries’ lattes and after some considerations, we decided to continue further calculations with our manually calculated data instead of the ones calculated using the defined function with the CurrencyScoop API as we thought it might be outdated compared to the data we got from manual input at the time of conversion. 


### Visualizing differences in pricing 
Based on the output we got from previous steps, we subtracted the Canadian price of Starbucks tall latte from each country’s price of the drink to get a new column in our table of the pricing differences. To visualize these differences, we used the barh function to graph a bar chart, which is displayed below:
[insert graph img]

### Potential external factor for the pricing differences
After having performed the previous calculations for our data above, we looked for an external factor that could justify the findings of the price differences. The external factor we decided to examine was the population consumption of coffee for some of the countries in our data set, as countries with higher consumption could result in lower prices per coffee. 

To do this we began by finding another dataset containing fairly recent coffee consumption rates (from 2020-2021), and repeated the scraping processes above for this new dataset. A joined table was then created, connecting the price differences and the coffee consumptions, which we then created a scatter plot for in order to demonstrate a potential relationship between the two. The aforementioned scatter plot is displayed below: 
[insert scatter plot img]

To further fortify our conclusion we actually defined two other functions: one to convert the data to standard units, and the other to calculate the correlation coefficient. From our calculation, the result value was about -0.21. 

The negative direction of the data aligned with the suspected cause, where as consumption increased, the expenses decreased. A correlation of  roughly 21% isn’t the strongest however it is important to note that correlation does not prove causation. On top of that this is real life data which and there could be other factors that are affecting this outcome.  
 
### Conculsion


## Citations
