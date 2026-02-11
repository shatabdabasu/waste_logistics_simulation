ML-Based Supplier Selection for Low-Carbon Waste Logistics in Cement Plants
A Forecast-Aware Decision Strategy under Fixed Operational Constraints

The system uses a rolling, supplier-wise lag-based forecasting approach to estimate short-term waste generation. For each supplier and for each day in the simulation, historical waste data up to the previous day is used to train a baseline linear regression model. The model is formulated using a lag-1 structure, where the waste generated on the previous day serves as the input feature and the waste generated on the current day is treated as the target variable.

Training samples are constructed from consecutive day pairs (yesterday → today), allowing the model to learn short-term dependency patterns in waste generation. The trained model is then used to predict the expected waste for the current day based on the most recent observed value. This process is repeated in a rolling manner for each supplier and each day, ensuring that only past information is used for forecasting.

The predicted waste values are not used directly for emissions calculation but instead serve as a decision-support signal to prioritize suppliers during daily collection, optimizing route selection while respecting operational constraints.

Project Summary:
This project studies transport-related CO₂ emission reduction in waste co-processing logistics for cement plants. A fixed daily waste collection target must be met using suppliers located at different distances with variable waste availability. Two approaches are compared: a distance-first baseline heuristic and a forecast-aware decision strategy using lightweight machine learning. Performance is evaluated using a rolling 30-day simulation, with cumulative transport-related CO₂ emissions as the primary metric. The results show that forecast-aware supplier selection can achieve realistic and measurable emission reductions without changing fleet size, routing structure, or operational constraints.

Historical waste data
        ↓
Linear Regression (forecast)
        ↓
Waste / Distance score
        ↓
Supplier selection
        ↓
Logistics simulation
