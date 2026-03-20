# Object-Oriented Stock Prediction System
**Tools:** Python, Pandas, NumPy, Scikit-Learn, yfinance, 
Plotly, Matplotlib

## Overview
A modular, class-based stock analysis and machine learning system 
built entirely with object-oriented programming principles. The system 
automates the full pipeline from data fetching through strategy 
backtesting and ML model evaluation for any user-specified ticker.

Four core classes handle the full workflow:
- **StockDataHandler** — fetches and cleans data from yfinance
- **StockAnalyzer** — computes returns, volatility, and trading signals
- **FeatureEngine** — engineers 15+ predictive features
- **MLModel** — trains, evaluates, and compares ML models

## Key Results
- MACD strategy delivered **48.43% total return** vs. 39.84% 
  buy-and-hold benchmark (2022–2025) on AAPL
- Linear Regression achieved **R² ≈ 0.90, RMSE = 3.63**
- Identified and explained why tree-based models fail on financial 
  time series extrapolation (Random Forest R²: −11.27)

## Models Compared
| Model | RMSE | R² Score |
|---|---|---|
| **Linear Regression** | **3.63** | **0.8982** |
| Ridge Regression | 3.64 | 0.8979 |
| Lasso Regression | 3.97 | 0.8785 |
| Random Forest | 39.89 | −11.27 |
| SVM | 64.04 | −30.63 |

## Trading Strategies Backtested
| Strategy | Total Return | Annual Return |
|---|---|---|
| Buy & Hold | 39.84% | — |
| SMA Crossover | 46.64% | 13.69% |
| **MACD** | **48.43%** | **14.15%** |
| Bollinger Bands | 4.42% | 1.46% |

## Repository Structure
- `notebooks/` — full OOP implementation and ML evaluation
- `report/` — final project report with results and charts
