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
- [Contributing](#contributing)
- [License](#license)

## Features

- **RUL Estimation:** Uses machine learning algorithms to estimate the RUL of wind turbine components.
- **Wind Farm Dataset:** Contains operational data from a wind farm, including time-series data on various parameters.
- **Preprocessing Scripts:** Includes scripts for data cleaning and preprocessing.
- **Visualization Tools:** Tools for visualizing data and RUL predictions.

## Installation

To install the required dependencies, you can use the provided `requirements.txt` file. It is recommended to use a virtual environment.

```bash
# Clone the repository
git clone https://github.com/your-username/rul-estimator-wind-turbine.git
cd rul-estimator-wind-turbine

# Create a virtual environment
python -m venv env
source env/bin/activate  # On Windows use `env\Scripts\activate`

# Install dependencies
pip install -r requirements.txt
Usage
Preparing the Data
Download the dataset: Ensure that the wind farm dataset is in the data/ directory. The dataset should be in CSV format.

Preprocess the data: Use the provided preprocessing script to clean and prepare the data for modeling.

bash
Copy code
python scripts/preprocess_data.py --input data/wind_farm_data.csv --output data/processed_data.csv
Training the Model
Train the RUL estimation model using the preprocessed data.

bash
Copy code
python scripts/train_model.py --input data/processed_data.csv --output models/rul_model.pkl
Making Predictions
Use the trained model to make RUL predictions.

bash
Copy code
python scripts/predict_rul.py --model models/rul_model.pkl --input data/new_data.csv --output results/predictions.csv
Dataset
The wind farm dataset includes the following columns:

timestamp: The time of the data record.
turbine_id: Identifier for the wind turbine.
feature_1, feature_2, ..., feature_n: Various operational parameters recorded from the turbine sensors.
component_status: Status of the turbine component (healthy, degraded, failed).
Ensure that the dataset is in the data/ directory with the appropriate format before running the scripts.

Model Description
The RUL estimator employs machine learning techniques to predict the remaining useful life of wind turbine components. The model takes historical operational data as input and outputs the estimated RUL. The model is trained using supervised learning methods, where the target variable is the time to failure of the components.

Contributing
We welcome contributions to improve the RUL estimator. If you have suggestions or bug reports, please open an issue on GitHub. To contribute code, fork the repository and submit a pull request with your changes.

License
This project is licensed under the MIT License. See the LICENSE file for more details.

Feel free to reach out if you have any questions or need further assistance!

Happy predicting!

Maintainers: