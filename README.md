# Market-Analysis-Report-for-National-Clothing-Chain
An analysis to know the products to advertise to each customer

## Introduction
This project is the final project in the Udacity Data Analysis and Visualization with Microsoft Power BI Nanodegree Program. An online national clothing chain needs help in creating a targeted marketing campaign. Sales have been flat and they want to lure lost customers back. They want to advertise specific products to specific customers in specific locations, but they don’t know whom to target.

## Data
The data listed below were loaded into Power BI using _Get Data_ in Power Query
* US Census Bureau:
  * Average income
  * Location
  * Population
  * Industry
* Business Data:
  * Product inventory
  * Product prices
  * Customer rating
  * Product return rate
* Customer Data:
  * Customer ID
  * Names
  * Location
  * Date of birth
  * Purchase history
* Additional Data:
  * Weather
  * Demographics

## Research Questions
1. What is the correlation (R2 value) between sales and income?
2. What is the correlation (R2 value) between customer ratings and product return rate?
3. What are the linear regression formulas to predict customer income from customer sales?
4. Which customer do you predict has the highest income?
5. Which product will be advertised the most?

Check [here](https://github.com/qudus-ade/Market-Analysis-Report-for-National-Clothing-Chain/blob/main/Market%20Analysis%20Report%20for%20National%20Clothing%20Chain.pbix) for the full report.

## Data Preparation
The following transformation processes were done in Power Query:
* **Product Inventory**: The columns were divided using Text to Columns button on Microsoft Excel before the data was loaded into Power BI using Power Query. Then other transformations were done inside Power Query.
* **Purchase List**: The Purchase Value of all dates were unpivoted into the long format.
* **Date Table**: A date table was created for the date reference in the model.

## Analysis/Visualization
### Data Categories
Categories are created in calculated column using DAX so we can target customers with products in their categories
* Income Categories: This report divided incomes into three categories
  * Low:    < $90,000
  * Medium: $90,000 - $105,000
  * High:   >= $105,000
* Weather Categories: Products were categorized into Neutral, Summer/Spring, and Winter according to their use in different weather conditions.
* Price Categories: Products were categorized into Low, Medium and High according to their prices
  * Low:		< $300
  * Medium:	$300 - $700
  * High: 	>= $700

### Results
**Regression Formula to predict Income from Sales**\
A scatterplot was used to analyze the relationship between average income and sales of each states. Linear regression was used to model the relationship.

![image](https://user-images.githubusercontent.com/67699946/182250267-ada2c608-7665-4d1c-bf70-ff9c9921c194.png)

* There is a strong positive relationship shown by the upward trend of the scatter plot.
* The R squared value is 0.78 which means the fitted model can explain 78% of the variations in the average income.
* The fitted model is ***Average Income = 72.43 Sales + 72638.21***

**The Distribution of Predicted Household Incomes**
Bins were created using DAX to plot the Histogram Chart

![image](https://user-images.githubusercontent.com/67699946/182250963-370d0eb6-ee5f-4d72-933d-3ef563ce73ae.png)

**Heat Map showing the Distribution of Average Income by States in the US**

![6](https://user-images.githubusercontent.com/67699946/182706802-48622eae-09e0-4d44-9fb2-b51e191fd28e.PNG)

The map shows that Washington DC has the highest average income in the US while Mississippi has the least.

**Product Category and Price**

![image](https://user-images.githubusercontent.com/67699946/182707812-a7a0b597-0ec8-4376-9be3-5cece26eb0ae.png)

The products have been placed into categories according to their prices as mentioned earlier. The medium categories have more potential customers as we have categorised most the US population as medium income earners.

**Return Rates vs Customer Ratings**

![11](https://user-images.githubusercontent.com/67699946/182708466-0770c251-00e7-4f90-a224-825afae74076.PNG)

There is a negative relationship between return rates and customer ratings i.e. customers who have to return products will not give the product high ratings.

**Customer with the Highest Income**

![12](https://user-images.githubusercontent.com/67699946/182708893-f538fb76-d47f-4521-9ce5-b76b05244650.PNG)

Jon Little earns the highest annual income; $452,895.71.

**State Categorization by Weather Condition**

![image](https://user-images.githubusercontent.com/67699946/182709709-d53d2fbb-16c5-40d1-867a-c27ca3e2c716.png)

![image](https://user-images.githubusercontent.com/67699946/182709750-e6c49460-0c7e-4830-b276-35dfccf17b50.png)

The products are classified into Summer/Spring to be targeted to Warm areas, Winter for Cold areas, and Neutral that are not related to any weather condition. The map shows that winter products should be targeted to the northern part of the country while the Summer/Spring should be targeted to the southern parts of the country.

**Sales between Sep 2020 and March 2021**

![image](https://user-images.githubusercontent.com/67699946/182710122-0fb059d8-c94a-495f-8b1b-9ffe988fe00d.png)

The sales pattern between September 2020 and March 2021 shows that sales was very low between January to March 2021 compared to sales in December 2020.

**Industries by Population**

37 million people are into Educational services, health care, and social assistance which is the most populated industry in the United States.

![image](https://user-images.githubusercontent.com/67699946/182711159-f3a0dc4b-1e30-4d96-913e-c7f7716fa84c.png)

A breakdown of the population in industry by state is below

![image](https://user-images.githubusercontent.com/67699946/182711506-9de67114-721b-4976-acfe-b1c0fd84dcef.png)

## Recommendations
1.	Medium-priced and winter products should be the most advertised as they have the largest market.
2.	Company should strive to reduce the return rates of products to boost customer satisfaction and ratings.

Check [here](https://github.com/qudus-ade/Market-Analysis-Report-for-National-Clothing-Chain/blob/main/Market%20Analysis%20Report%20for%20National%20Clothing%20Chain.pbix) for the full report.

![image](https://user-images.githubusercontent.com/67699946/182713575-7ef0b9b8-ad8c-4453-b869-8af0453f4540.png)
