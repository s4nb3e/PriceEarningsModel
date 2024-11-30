# Model Card

Note that in this project I trained three models: A linear regression, a random forest model and a neural network. The random forest model performed best so I use it in the model card.

## Model Description

**Input:**
The input to the model is a selection of fundamental stock data. The specific input variables are:
1. Consensus analyst estimates for next three year revenue growth for the company.
2. Consensus analyst estimates for next three year operating profit growth (EBIT) for the company.
3. Previous year's Return On Capital Employed for the company.
4. Previous year's gross profit margin for the company.
5. Previous year's operating profit margin (EBIT) for the company.
6. Net debt/EBITDA for the company.
7. The liquidity of the company's shares (measured by daily traded volume as a percentage of shares outstanding)

**Output:**
The output of the model is a prediction for the company's price to earnings (PER) ratio. This ratio is a measure of the valuation of a company. It takes the company's share price and divides it by the analyst consensus of the expected profits per share over the next twelve months.

**Model Architecture:**
The model is a random forest model with the following hyperparameters.
n_estimators = 70
max_depth = 20

## Performance

To evaluate the results of the model I calculated the root mean square error on the test data and compared it to: (i) A naïve guess using the train dataset sample average P/E; (ii) A simple linear regression; (iii) The best trained neural network I developed. The average P/E in the dataset (excluding outliers) is 19x. The random forest model performs slightly better than a naïve guess using the average of the training data, but not that much better.

![rmse table](rmse_table.png)

## Limitations

Note that this model has only been trained on stocks that are within the consumer staples and consumer discretionary sector. As a result it would not be appropriate for stocks in other sectors.

Another limitation of this model is that it appears to be very poor at modelling higher valuation stocks (with a P/E above 40x).

## Trade-offs

My goal was to build a simple model that could help to estimate P/E ratios. However, the trade-off is somewhat poor performance. In order to improve the performance I would want to improve and increase the number of features in the input dataset. In particular I would want to: (i) Use average historic data for returns on capital and margins, not just the prior year number; (ii) Get data on volatility of returns on capital and margins; (iii) Incorporate some form of sentiment data, for example sentiment from earnings calls.
