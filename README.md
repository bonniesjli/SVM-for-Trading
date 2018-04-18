# SVM for Trading
Comparing different SVM Kernels, specifically the linear kernel, polynomial kernel, and the Radial Basis Function Kernel, in their effectiveness when applied to quantitative finance and algorithmic trading. 

## Model 1 - Based on Technical Indicators
Featuresets: various technical indicators for a company
Labels: Buy/Sell
	Buy - if price is predicted to rise 
	Sell - of price is predicted to drop

### Results (Accuracy)
Linear kernel: 53.3%
Polynomial Kernel: 57.3%
Radial Basis Function Kernel: 51.3%

### Interesting aspects for improvement:
Effects of feature standardization on SVMs
Predictability of certain technical indicators, can be studied using Hypothesis Testing
	

## Model 2 - Based on Price Correlation
This model is based on the idea that the price trend of certain groups of companies are likely to move together. Each model is generated on a per company basis, while taking into account of all other companies. 

Featuresets: Pricing change of all S&P 500 companies on a certain day
Labels: Buy/Sell/Hold
Buy - if price rise more than 2% for the next 7 days
Sell - if price drop more than 2% for the next 7 days
Else - Hold
^For this model, I followed the Programming for Finance tutorial by Sentdex (Harrison Kinsley)

### Results: 
47% mean accuracy for all S&P 500 companies in predicting buy/hold/sell
