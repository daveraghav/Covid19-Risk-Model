# Covid19 Risk Model
 
This repo contains the model preparation and prediction files for Covid19 UK's regional risk model. The current state of dataset is almost ready / prepared for machine learning with lot of feature engineering carried out and additional regional datasets combined. Here are the details included in the initial master dataset for the risk model:

+ Covid19 cases history on regional / upper tier local authority level
+ Population density, age distribution for each of those levels
+ Area (sq km) of each region
+ Estimate R0 and K values for each datapoint
+ Rolling means of estimated R0 
+ Rolling Means of cases
+ Mean changes in cases for past 7 days for each datapoint (3 gradient points)
+ Important measures implemented by UK Government on date-by-date bases (school closure, etc..)
    + Timedelta from of each of these measures from start and end dates of implementation
    + Binary indication (1 or 0) of each measure being Active/Inactive for each datapoint
+ A basic xgboost regressor model has been created to predict the daily new cases in each region of UK

## Next Steps

+ Improve the basic model, create more features, try different target variables for prediction
+ Geographic visualisation (contour/scatter maps) of the newly created features, cases, risks and predictions to follow
+ More features will shortly be added to account for imformation like number of superstores, food production facilities to caculate actual localised food security risk based on covid19 situation
+ Rerun the model on optimised datasets

