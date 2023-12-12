# News-sentiment-data-engineering

## Summary

- Extracts news sentiment data for Tesla Inc between 25-02-2023 and 25-08-2023 using GaiaLens’ news API, saves it as 'Tesla_newssent_extaction.csv' and then aggregates it.
- Before aggregating, a 5% decay for each month that has passed from the current date is applied to the sentiment score.
- Then the downweighted scores are averaged per required metric column specified in 'sentiment_columns.csv' and saved as a CSV called 'telsa_newssent_aggregation.csv'.
- The final output is therefore a dataframe with companyname and all the sentiment columns where each of the sentiment column is a mean over down-weighted values across all the dates.

### filename map
1. **'Dates_tesla.csv'** The pre-specified date range to collect news sentiment from.
2. **'Sentiment_columns'** The pre-specified sentiment topics to extract data for.
3. **'Tesla_newssent_aggregation'** The final csv from the aggregation
4. **'Tesla_newssent_extraction'** The final csv from the aggregation
