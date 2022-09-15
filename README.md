## Objective:
The goal of this project is to analyze housing data in King County Washington to figure out what features have what sort of impact on the sale price, create a model that can predict price by inputing these features, and then use this data to solve some real world problem. Along the way we will need to clean our data, do some feature engineering, explain and display our work/findings via models and graphs.

## The Buisiness Problem: 
Substantial Rentals LLC is a company that purchases real estate for the purposes of renting out units with airbnb.  Substantial Rentals wants to ensure the real estate that it is interested in acquiring is not overvalued and would like a method of fairly pricing prospective properties.


# Data Cleaning:
Before we can use features in our model to predict price, we need to make sure that these features can be interpreted accurately or interpreted at all.

### Null Values
Waterfront, view, and yr renovated all had null values that we filled with zeroes in their place, which in the context of the data is logical to do.  For example in the feature waterfront only 146 out of the 19221 values were waterfront properties. So not only is the ratio extremely low as it is, but intuitively if a property was a waterfront property that information would be mentioned rather than ommitted as it is something to brag about. 

### Categorical and Ordinal to Nominal
Waterfront, view, zipcode, condition, grade, and date are categorical data, of which view, condition and grade are ordinal. As mentioned above we converted the data to integer values so they are interpretable.

### Dropping and Feature Engineering
We ended up dropping the variables 'yr_built', 'date', 'lat', 'long', 'floors', and 'id'.
The yr_built, lat, long and floors we engineered into more useful variables and date and id we simply dropped.
For example we used the latitude and longitude to calculate the properties distance from Seattle city center.

### Normalizing


# Models:
As we are trying to predict the price, logically price is going to be our target variable (y value). This predicted 
### Baseline Model:
As sqft_living was our feature most correlated with price it was the one baseline model used. Obviously, this simple baseline model did not perform well as the R2 (Coefficient of Determination) could only account for *insert amount* of the variation.  This makes intuitive sense as more than one factor influences the price of a house.
*post graph here*


## Summary