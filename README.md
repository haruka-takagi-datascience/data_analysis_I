# Housing Sale Price Analysis with Multi-Linear Regression

The data that this report will be exploring was obtained from the Toronto Real Estate Board (TREB) on detached houses in two separate neighborhoods (a neighborhood in Toronto: neighborhood T) & (a neighborhood in Mississauga: neighborhood M). 

This data set contains the information of the following variables.
ID: property identification
sale: the actual sale price of the property in Canadian dollars
list: the last list price of the property in Canadian dollars
bedroom: the total number of bedrooms
bathroom: the number of bathrooms
parking: the total number of parking spots
maxsqfoot: the maximum square footage of the property
taxes: previous year’s property tax
lotwidth: the frontage in feet
lotlength: the length in feet of one side of the property
location: M (for Mississauga), T (for Toronto)

We will use this data to establish a mulitple linear regression model (MLR) which home buyers can use to predict the sale price of single-family, detached homes in the two neighborhoods in the Greater Toronto Area.

Our main objectives for this data analysis report is…
1. Execute data manipulation, such as but not limited to, removing NA values, adding variables, removing variables and removing highly influential points from the dataset.
2. Execute exploratory data analysis, such as but not limited to, examine the correlations of quantitative variables and check constant variance assumption fulfillment.
3. Execute model creation, such as but not limited to, creation of full model and applications of backwards AIC & BIC.
4. Discuss model validity and limitations, such as but not limited to, examination of diagnostic plots and next steps.

### Data Preprocessing
Before we start working with our data, we will do some standard procedures for data pre-processing.
1. Set seed to 2020
2. Randomly select a sample of 150 cases from the original data.
3. Create a new variable lotsize by multiplying lotwidth and lotlength. Lotsize will replace lotwidth and lotlength in the dataset.
4. Remove unnecessary variables from the dataset.
5. Remove NA values.
6. Remove bad leverage points from the dataset.

INSERT IMAGE

7. Run an initial multi-linear regression to identify leverage and influential points.

INSERT IMAGE

The first line in the output above shows leverage values of the data points to their corresponding ID’s. The second line shows Cook’s distance. As we can see observation 109 has both the highest leverage value and Cook’s distance. Thus, we will remove this point from the dataset, as it may be a bad leverage point.



