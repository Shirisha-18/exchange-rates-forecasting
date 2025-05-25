## Forecasting currency exchange rates using recurrent neural networks

### A Data-Driven Forecasting Model for Currency Volatility

Accurate forecasting of currency exchange rates is vital for a wide range of stakeholders, including investors, multinational corporations, policymakers, and economists. Exchange rates are inherently volatile and influenced by numerous factors that interact in complex, often nonlinear ways. Traditional statistical models often struggle to capture these complexities, leading to suboptimal predictions.

This project leverages the power of recurrent neural networks (RNNs) and their advanced variants such as LSTM and bidirectional RNNs to model and predict exchange rate movements. By analyzing historical exchange rate data and incorporating relevant economic indicators, the proposed machine learning models aim to improve forecasting accuracy. The ultimate goal is to provide reliable predictions that can assist in financial decision-making, risk management, and policy formulation.


## Background

The foreign exchange market is the largest and most liquid financial market globally, with exchange rates fluctuating continuously based on various macroeconomic variables, geopolitical events, and market sentiment. Predicting these fluctuations is a complex problem due to the nonlinear and time-dependent nature of the data.

Traditional forecasting approaches like ARIMA and other linear time series models have limitations in handling the intricate temporal dependencies and sudden shocks characteristic of FX markets. Recurrent Neural Networks (RNNs), particularly Long Short-Term Memory (LSTM) and Bidirectional RNNs, offer advanced capabilities to capture long-term dependencies and bidirectional context in sequential data, making them well-suited for time series forecasting.

This project explores these deep learning architectures to build robust models that can learn patterns from historical exchange rate data and produce accurate forecasts, ultimately aiding in better understanding and managing currency volatility.

## Research Objectives

1. **Analyze Historical Patterns and Volatility Trends**
Identify trends and volatility regimes in historical exchange rate data to understand market dynamics.

2. **Predict Exchange Rate Movements Using ML Models**
Build predictive models using both traditional and modern machine learning algorithms.

3. **Evaluate Model Robustness Across Multiple Currencies**
Apply the modeling framework to major currencies such as USD, EUR, JPY, and GBP to validate generalizability.


## Data Sources
- Historical exchange rate data from central banks and public financial datasets.

- Economic indicators (GDP, inflation rates, interest rates, oil prices).

- Global events data and financial market indices 

## Project Organization

```

├── data
│   ├── raw            <- Original exchange rate, economic, and global event data
│   ├── processed      <- Cleaned and feature-engineered datasets
│
├── notebooks          <- Jupyter notebooks for EDA, modeling, and evaluation
│
├── models             <- Trained models and prediction outputs
│
├── reports
│   └── figures        <- Visualizations and evaluation plots
│
├── references         <- Economic papers and data documentation
│
├── requirements.txt   <- Environment dependencies
│
└── README.md          <- Project overview and usage instructions

```

## Results and Evaluation

The performance of various recurrent neural network models was evaluated using Root Mean Squared Error (RMSE) and Mean Absolute Percentage Error (MAPE) as metrics. The results are summarized below:


| Model               | RMSE   | MAPE (%)  |
|---------------------|--------|-----------|
| Single Layer RNN    | 0.1311 | 4.82      |
| Multi Layer RNN     | 0.1770 | 6.15      |
| Bidirectional RNN   | 0.1495 | 5.30      |
| LSTM (Single Layer) | 0.1258 | 4.47      |


- The LSTM (Single Layer) model achieved the lowest RMSE and MAPE, indicating the best predictive accuracy among the tested models.

- The Single Layer RNN also performed reasonably well but lagged behind the LSTM, likely due to its limited ability to capture longer-term dependencies.

- The Bidirectional RNN improved over the Multi Layer RNN by processing data in both forward and backward directions, which helped in capturing additional context.

- The Multi Layer RNN showed the weakest performance, possibly due to overfitting or training difficulties with deeper architectures on this dataset.

These results highlight the effectiveness of LSTM networks for modeling the complex, nonlinear patterns in currency exchange rate time series, as well as the importance of model architecture selection for accurate forecasting.

## Conclusion

This project successfully developed and compared multiple recurrent neural network architectures to forecast currency exchange rates. The single-layer LSTM model consistently outperformed other RNN variants, demonstrating its capability to handle the dynamic and non-linear nature of financial time series data.

Accurate currency exchange rate predictions are vital for risk management, investment decisions, and policy formulation. The findings suggest that deep learning models, especially LSTMs, can provide valuable forecasting tools in the foreign exchange market.

Future enhancements could include incorporating additional economic indicators, experimenting with more complex architectures like GRUs or hybrid models, and expanding the dataset to include multiple currencies and external factors for broader applicability.


## Limitations

1. **Limited Real-Time Economic Shocks**

    The model doesn't yet incorporate real-time news or breaking geopolitical events that significantly impact short-term currency movements.

2. **Sparse Data for Emerging Market Currencies**

   Data availability and quality for less-traded currencies limit model effectiveness outside major FX pairs.

3. **Exchange Rate Manipulation or Pegging**

   Currencies with government-controlled exchange regimes may behave differently and reduce predictive validity.


## Future Work

1. **Incorporate Sentiment Analysis**
Add textual analysis of financial news, central bank statements, and social media sentiment to capture qualitative drivers of FX volatility.

2. **Forecast Confidence Intervals**
Integrate probabilistic forecasting to provide uncertainty ranges and risk scenarios.

3. **Real-Time Dashboard**
Build an interactive dashboard for currency trend monitoring and live forecast visualization.

4. **Cross-Currency Arbitrage Modeling**
Model currency triangle arbitrage opportunities using multi-pair relationships.


## References

- Ince, Onur. "Forecasting Exchange Rates Out-of-Sample with Panel Methods and Real-Time Data." *University of Houston*.

- Das, A., & Pramod, D. (2023). Exchange Rate Prediction with Machine Learning, Deep Learning, and Time Series Methods Using Alternative Data. In *2023 International Conference on Advancement in Computation & Computer Technologies (InCACCT)*, Gharuan, India, pp. 698-703.  
DOI: [10.1109/InCACCT57535.2023.10141844](https://doi.org/10.1109/InCACCT57535.2023.10141844)

- Zhao, Lu, and Wei Qi Yan. "Prediction of Currency Exchange Rate Based on Transformers." *Journal of Risk and Financial Management*, 2024, 17(8), 332.  
DOI: [10.3390/jrfm17080332](https://doi.org/10.3390/jrfm17080332)  

