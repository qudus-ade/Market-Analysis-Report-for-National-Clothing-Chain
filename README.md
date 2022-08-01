# Market-Analysis-Report-for-National-Clothing-Chain
An analysis to know the products to advertise to each customer

## Introduction
This project is the final of three projects in the Udacity Data Analysis and Visualization with Microsoft Power BI Nanodegree Program. An online national clothing chain needs help in creating a targeted marketing campaign. Sales have been flat and they want to lure lost customers back. They want to advertise specific products to specific customers in specific locations, but they don’t know who to target.

## Data
The data listed below were loaded into Power BI using _Get Data_ in Power Query
* US Census Bureau: Average income, location, population, industry
* Business Data: Product inventory, product prices, customer rating, product return rate
* Customer Data: Customer ID, names, location, date of birth, purchase history
* Additional Data: Weather, Demographics

## Research Questions
1. What is the correlation (R2 value) between sales and income?
2. What is the correlation (R2 value) between customer ratings and product return rate?
3. What are the linear regression formulas to predict customer income from customer sales?
4. Which customer do you predict has the highest income?
5. Which product will be advertised the most?

Check [here](https://github.com/qudus-ade/Market-Analysis-Report-for-National-Clothing-Chain/blob/main/Market%20Analysis%20Report%20for%20National%20Clothing%20Chain.pbix) for the full report.

## Data Preparation
The following transformation processes were done in Power Query:
* **Product Inventory**
The columns were divided using Text to Columns button on Microsoft Excel before the data was loaded into Power BI using Power Query. Then other transformations were done inside Power Query.
* **Purchase List**
The Purchase Value of all dates were unpivoted into the long format.
* **Date Table**
A date table was created for the date reference in the model.

## Analysis/Visualization
#### Data Categories
Categories are created in calculated column using DAX so we can target customers with products in their categories
* Income Categories: This report divided incomes into three categories
  * Low:    < $90,000
  * Medium: $90,000 - $105,000
  * High:   >= $105,000
* Weather Categories: Products were categorized into Neutral, Summer/Spring, and Winter according to their use in different weather conditions.
* Price Categories: Products were categorized into Low and Medium according to their prices
  * Low:		< $300
  * Medium:	$300 - $700
  * High: 	>= $700

