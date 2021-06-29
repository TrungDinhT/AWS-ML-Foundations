# Machine Learning steps

## Introduction
- Define the problem -> Build dataset -> Train model -> Evaluate model -> Use model

## Define the problem
- Define the problem in a way that ML algorithms can be applied
  - Unsupervised learning
    - clustering
    - ...
  - Supervised learning
    - Regression
    - Classification
    - ...
  - Reinforcement learning

## Build a dataset
1. Collect data: [Q] does the data match the ML task?
2. Inspect data: [Q] does it have outliers/missing values / right format? How to handle/preprocess?
3. Summary statistics: [Q] does data has a trait/trend? How is data structured/distributed (are the assumptions for model correct)? Min/max/mean/median?
4. Visualize data: [Q] how to visualize to raise data understanding / tell story?

## Model training
- Split dataset -> train + test + validation set
- Model parameters (or weights in DL) -> define how the model behave
- Loss function -> codify how close the model behaves as expected
- Many models have to be tested, selected and "mixed" to find the best solution