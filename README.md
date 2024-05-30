# Remaining Useful Life (RUL) Estimator

## Overview

This repository contains a tool for estimating the Remaining Useful Life (RUL) of wind turbines. The estimator is designed to help predict the lifespan of wind turbine components based on operational data, enabling better maintenance planning and reducing downtime.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Dataset](#dataset)
- [Model Description](#model-description)

## Features

- **RUL Estimation:** Uses machine learning algorithms to estimate the RUL of wind turbine components.
- **Wind Farm Dataset:** Contains operational data from a wind farm, including time-series data on various parameters.
- **Scripts:** Includes scripts for data cleaning, preprocessing, training models and tools for visualizing data and RUL predictions.

## Installation

To install the required dependencies, you can use the provided `requirements.txt` file. It is recommended to use a virtual environment.


# Clone the repository
```bash git clone https://github.com/h777d/RUL_Estimation.git
cd rul-estimator-wind-turbine
```

# Create a virtual environment
```python -m venv env
source env/bin/activate  # On Windows use `env\Scripts\activate`
```

# Install dependencies
```pip install -r requirements.txt```

# Preparing the Data
Download the dataset: Ensure that the wind farm dataset is in the data/ directory. The dataset should be in CSV format.
Run the Python script: Use the provided script to clean and prepare the data for modeling and run the training and evaluation of the ML models.

## Dataset
The dataset is collected from a 2MW wind turbine high-speed shaft driven by a 20-tooth pinion gear [1]. A vibration signal of 6 seconds was acquired each day for 50 consecutive days (there are 2 measurements on March 17, which are treated as two days in this example). An inner race fault developed and caused the failure of the bearing across the 50-day period.
Ensure that the dataset is in the data/ directory with the appropriate format before running the script.

[1] Bechhoefer, Eric, Brandon Van Hecke, and David He. "Processing for improved spectral analysis." Annual Conference of the Prognostics and Health Management Society, New Orleans, LA, Oct. 2013.

## Model Description
The RUL estimator employs machine learning techniques to predict the remaining useful life of wind turbine components. The model takes historical operational data (vibration) as input and outputs the estimated RUL. The model is trained using supervised learning methods, where the target variable is the time to failure of the components.

Feel free to reach out if you have any questions or need further assistance!
