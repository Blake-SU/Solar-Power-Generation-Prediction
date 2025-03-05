# Solar-Power-Generation-Prediction


## Project Overview
This repository contains the implementation of a novel approach to predict solar power generation using microclimate data. Our model utilizes comprehensive data processing techniques including temporal embedding and adaptive normalization to analyze environmental factors and forecast solar panel power output. The project was developed for a power prediction competition where it ranked 44th out of 900+ participants.

## Features
- Processes minute-by-minute microclimate data to predict solar power generation
- Implements both forecasting and imputation methodologies
- Utilizes advanced deep learning architectures with a focus on TimesNet
- Includes comprehensive data preprocessing techniques for handling real-world temporal data
- Provides hyperparameter optimization for model tuning

## Data
The dataset includes environmental measurements from approximately 20 identical observation devices, covering January to November 2024. Data is recorded at one-minute intervals and includes:
- Wind speed (m/s)
- Atmospheric pressure (hPa)
- Temperature (°C)
- Relative humidity (%)
- Illuminance (lux)
- Power generation (W)

## Methodology
Our approach involves two main prediction strategies:

### Forecasting
- Uses past observations to predict future power generation
- Implements sliding window technique to process time series data
- Employs loss function: $\text{Loss}(\hat{x}, x) = (x - \hat{x})^2$

### Imputation
- Leverages both past and future observations to predict power during target periods
- Divides data into front, middle, and back segments
- Employs loss function: $\text{Loss}(\hat{z}, z) = (z - \hat{z})^2$

## Models
We experimented with several state-of-the-art time series models:
- TimesNet (best performer)
- LSTM (baseline)
- Crossformer
- Nonstationary Transformer
- PatchTST
- TiDE

## Results
TimesNet emerged as the superior model, particularly excelling in imputation tasks:
- Forecasting: Training Loss 0.6232, Validation Loss 0.5317
- Imputation: Training Loss 0.3773, Validation Loss 0.2281

## Documentation
- [Project Report](https://drive.google.com/file/d/1ihy47UbXaBp-zzF6DTcEV6Lhsq1JnET9/view)


