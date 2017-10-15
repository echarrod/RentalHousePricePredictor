# UK House Rental Price Predictor

Predicting the rental price the following property features of UK houses:
- longitutude
- latitude
- bedrooms
- size (metres squared)
- dwelling type
- has garden

Using this date, this notebook looks at comparing basic price estimators, and calculating the importance of each of the above features with regards to price.
# Future Work
- Obviously currently it's creating longitude and latitude as independent variables, when to get a more accurate regressor we should consider them together. I've started to look at extracting the first part of the post code from these with PyGeoCoder, which would give us a suitable feature to replace long & lat.
- We could train a model which would predict the time_on_market field, based on the rental price, in a similar way we've done here. So that you can adjust the rent to see how it would effect the esimated time on the market.
- Instead of looking at rental price, we could look at the difference with the national average for that time, e.g. £400/month in 2008 when the data first starts is a lot different to £400/month for the most recent listing this year. This could further be extended to compare it with the average price in the area using the coordinates.
Data from 2011 for the UK in general (including and excluding London as two separate figures) - https://www.ons.gov.uk/economy/inflationandpriceindices/bulletins/indexofprivatehousingrentalprices/july2017
Regional-specific data can be found here, but it wouldn't be as easy to integrate, as it doesn't look like they offer it in a Pandas-friendly format, we would need a web crawler - https://homelet.co.uk/homelet-rental-index
