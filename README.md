# MLB Pitch Classification System

## Overview

This project is a machine learning system designed to classify pitches thrown in Major League Baseball (MLB) games. The system uses advanced tracking data to predict the type of pitch based on characteristics such as speed and spin. The model is designed to be used in real-time, providing predictions that can be displayed during broadcasts or in-stadium.

## Features

- **Data Processing**: Gathers and processes pitch data from MLB games.
- **Model Training**: Trains a machine learning model for each pitcher to classify their pitches.
- **Prediction API**: Provides a web API to make real-time pitch type predictions.
- **Metrics Calculation**: Evaluates the performance of the trained models.
- **Customizable**: Designed to be extended to additional pitchers or different types of models.

## Getting Started

### Prerequisites

Ensure you have Python installed. Install the required dependencies with:

```bash
pip install -r requirements.txt
```

### Directory Structure

Your project should follow this directory structure:

```kotlin
./pitch-classification/
│
├── data/
│   ├── pitcher_name.parquet
│   └── ...
│
├── models/
│   ├── pitcher_name.joblib
│   └── ...
│
├── .gitignore
├── README.md
├── client.py
├── make-data.py
├── make-metrics.py
├── make-models.py
├── requirements.txt
├── run.py
├── server.py
└── utils.py
```

- **data/**: Contains the processed pitch data in `.parquet` format.
- **models/**: Stores the trained models in `.joblib` format.
- **client.py**: Client script to interact with the API.
- **make-data.py**: Script to generate and process pitch data.
- **make-metrics.py**: Script to calculate and evaluate model metrics.
- **make-models.py**: Script to train models for each pitcher.
- **run.py**: Script to start the server.
- **server.py**: Web server that hosts the prediction API.
- **utils.py**: Utility functions used throughout the project.

## Usage

### Data Processing

Generate and preprocess the data for each pitcher:

```bash
python make-data.py
```

### Model Training

Train the models for each pitcher:

```bash
python make-models.py
```

### Running the Server

Start the server to host the prediction API:

```bash
python run.py
```

### Making Predictions

Use the `client.py` script to make predictions via the API:

```bash
python client.py
```

### Metrics Calculation

Calculate metrics to evaluate model performance:

```bash
python make-metrics.py
```

## Data Sources

- **MLB Statcast**: Used for gathering pitch data.
- **Baseball Savant**: Additional data source for pitch characteristics.

## Technology Stack

- **Machine Learning**: scikit-learn, PyTorch
- **Web API**: FastAPI
- **Data Processing**: pandas, pybaseball
- **Model Serialization**: joblib
- **Data Storage**: Parquet

## License

This project is open-source and available under the MIT License.
