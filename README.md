# BISTRO: A General-Purpose Oracle for Macroeconomic Forecasting

**BISTRO** (BIS Time-series Regression Oracle) is a general-purpose time series model for macroeconomic forecasting. It is based on the transformer architecture used in Large Language Models (LLMs) and is fine-tuned on thousands of macroeconomic time series from the BIS data portal.

This repository contains the code and example notebooks for using BISTRO.

## Security Vulnerability

**Important:** This project contains a dependency with a known critical security vulnerability. Please read our [**Vulnerability Disclosure**](VULNERABILITY_DISCLOSURE.md) for details on the associated risks and mitigation steps before using this code.

## Overview

Many traditional forecasting approaches require a different model for each variable. BISTRO provides a **low-cost and flexible tool** for baseline forecasts and conditional scenarios.

## Intro video

[![Watch the BISTRO intro video](./bistro_intro.jpg)](./bistro_intro.mp4)

### Key Capabilities
- **Unconditional forecasting**: Produces baseline forecasts for key aggregates (e.g., inflation).
- **Conditional scenarios**: Lets you fix future paths of variables (e.g., oil prices, exchange rates) to explore alternative scenarios.
- **Nonlinear patterns**: Captures nonlinear relationships that standard linear models may miss.
- **Fine-tuned**: Trained on 4,925 time series across 63 economies.

## Try it now (no installation required)

You can run everything directly in your browser using **Google Colab**. It is free and requires no setup.

| Notebook | Description | Link |
| :--- | :--- | :--- |
| **Forecast Single Series** | Simple forecast for one variable (e.g., inflation) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/bis-med-it/bistro/blob/main/script/forecast_single_timeseries.ipynb) |
| **Forecast Unconditional** | Forecast with extra variables (covariates) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/bis-med-it/bistro/blob/main/script/forecast_unconditional_scenario.ipynb) |

### How to use Google Colab
1. **Click a link above** to open the notebook.
2. If asked, sign in with your Google account.
3. In the top menu, click **Runtime → Run all**.
4. Scroll down to see the results.

### Python version (recommended)
- **Recommended option:** Use **Google Colab**, which comes with a pre-configured Python environment.  
- **If you run locally (optional):** Use **Python 3.11** (or a close equivalent). This is typically the most compatible choice for current ML libraries.  
  (Exact package versions are listed in `requirements.txt`.)

## Using your own data
To forecast your own data:
1. Create a **CSV file** like the examples (usually a Date column and a Value column).
2. In Colab, click the **folder icon** on the left.
3. Drag and drop your CSV file.
4. Update the **filename** in the notebook (e.g., change `'bis_cpi_us_yoy_m.csv'` to `'my_data.csv'`).

## Running locally (optional)

Most users do not need this. Use this only if you want to run the notebooks on your own computer.

### Model weights and Git LFS (optional but recommended)
Some large files (e.g., model weights) may be stored using **Git LFS**. If Git LFS is not installed, `git clone` may not download these files correctly.

**Install Git LFS first (recommended):**
1. Install Git LFS: https://git-lfs.com/
2. Then run:
   ```bash
   git lfs install
   git clone https://github.com/bis-med-it/bistro.git
   ```

## Project structure
- `data/`: Sample CSV data (e.g., US CPI, policy rates).
- `script/`: Notebooks and scripts for running the model.

## Citation
If you use this model or code, please reference the paper:

**BISTRO: A General-Purpose Time Series Model for Macroeconomic Forecasting**  
*Batuhan Koyuncu, Byeungchun Kwon, Marco Lombardi, Hyun Song Shin, Fernando Perez-Cruz*  
BIS Quarterly Review, March 2026
