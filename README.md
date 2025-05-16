# Perceptron Mobile Phone Like/Dislike Classification

This repository contains a machine learning project that uses the Perceptron algorithm to predict whether a mobile phone will be "Liked" or "Not Liked" by the user, given its specifications.

I made this project as a part of a Deep Learning course I did.

## Project Overview

The goal of this project is to predict whether a user would like a mobile phone or not based on its specifications. The classification is done using a Perceptron model, which is one of the simplest forms of artificial neural networks.

The project uses a dataset from 91mobiles to achieve this.

### Assumption

- If the average rating of a mobile phone is greater than or equal to 4, then it's considered that the user likes it; otherwise, not.
- This can be edited by modifying the THRESHOLD in the python notebook

## Dataset

The dataset consists of mobile phone specifications and their ratings:

- `train.csv`: Training data with mobile phone specifications and ratings
- `test.csv`: Test data with mobile phone specifications (ratings not included)
- `sample_submission.csv`: Sample format for submission

The dataset contains numerous features related to mobile phones, including:

- Physical attributes (Height, Width, Weight, Screen Size, etc.)
- Hardware specifications (RAM, Internal Memory, Processor, etc.)
- Battery capacity
- Camera specifications
- Connectivity options
- And many more

## Data Preprocessing

Several preprocessing steps are performed:

1. Removal of features with many missing values
2. Removal of features with very low variance
3. Removal of multivalued and unimportant features
4. Filling missing values with appropriate strategies
5. Feature engineering to extract valuable information from complex features
6. Scaling numerical features to a range of 0-1

## Model: Perceptron

The Perceptron algorithm is implemented from scratch with the following features:

- Weight initialization with all 1's
- Learning rate and epochs as hyperparameters
- Checkpoint saving for best accuracy during training
- Custom fit method for training the model
- Ability to handle binary classification tasks

### Training

The model is trained with:

- 1500 epochs
- Learning rate of 0.01
- Binary classification (1 for liked, 0 for not liked)
- This is again modifiable by editing the values in the function call

## Usage

1. Run the Jupyter notebook `perceptron.ipynb` to train the model and generate predictions
2. The model will create a `submission.csv` file with predictions for the test data

## Files in the Repository

- `perceptron.ipynb`: Jupyter notebook containing all the code
- `data/train.csv`: Training dataset
- `data/test.csv`: Test dataset
- `data/sample_submission.csv`: Example submission format
- `submission.csv`: Generated predictions for test data

## Dependencies

- Python 3.x
- NumPy
- Pandas
- Matplotlib
- Scikit-learn (for evaluation metrics only)

## Approach

1. Feature selection and engineering to identify the most relevant phone specifications
2. Data cleaning and preprocessing to handle missing values and standardize features
3. Implementation of a custom Perceptron model
4. Training the model on the processed data
5. Generating predictions for the test dataset
