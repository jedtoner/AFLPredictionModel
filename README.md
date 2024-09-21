# AFL Game Prediction Model

## Overview

The AFL Game Prediction Model leverages advanced machine learning techniques to forecast the outcomes of Australian Football League (AFL) games. By utilizing a hierarchical Bayesian framework, the model analyzes team statistics and latent parameters to predict match results, providing insights into team performance and dynamics throughout the season.

## Key Features

- **Hierarchical Bayesian Modeling:** Implements a structured Bayesian approach to capture team-specific effects and uncertainties in predictions.
- **Principal Component Analysis (PCA):** Utilizes PCA for dimensionality reduction, effectively handling multicollinearity among team statistics.
- **Dimensionality Reduction:** Reduces complex team performance metrics into principal components, enhancing model efficiency and interpretability.
- **Model Diagnostics with ArviZ:** Employs ArviZ for comprehensive model diagnostics, ensuring robustness and convergence of the Bayesian model.
- **In-Sample and Out-of-Sample Validation:** Validates model performance both within the training data and on unseen data, demonstrating reliability in predictions.
- **Automated Predictions:** Provides functions to predict game outcomes and winners with ease, integrating seamlessly with data inputs.
- **Scalable Data Management:** Organizes and preprocesses large datasets efficiently, facilitating easy updates and extensions.
- **Visualization:** Generates insightful plots for posterior distributions and model parameters, aiding in the interpretation of results.

## Installation

Follow these steps to set up the project on your local machine:

1. **Clone the Git Repository:**
   ```bash
   git clone https://github.com/yourusername/afl-game-prediction.git
   cd afl-game-prediction
   ```

2. **Create a Virtual Environment:**
   ```bash
   python -m venv venv
   ```

3. **Activate the Virtual Environment:**
   - On Windows:
     ```bash
     venv\\Scripts\\activate
     ```
   - On macOS/Linux:
     ```bash
     source venv/bin/activate
     ```

4. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

## Data Sources

The project utilizes data from the following sources:

- **AFL Games Statistics:** [Kaggle AFL Stats Dataset](https://www.kaggle.com/datasets/stoney71/aflstats/data?select=stats.csv)
  
  This dataset includes comprehensive statistics for AFL games, which are preprocessed and used to train the Bayesian model.

## Usage Instructions

To run the AFL Game Prediction Model, follow these steps:

1. **Prepare the Data:**
   Ensure that the dataset is placed in the `data/` directory as specified in the notebook.

2. **Run the Notebook:**
   Open the Jupyter notebook `afl_prediction_model.ipynb` and execute the cells sequentially to train the model and perform predictions.

3. **Predict Game Outcomes:**
   Utilize the provided functions to predict the outcomes of specific games. For example:
   ```python
   home_team = "Richmond"
   away_team = "Adelaide"
   predict_game(home_team, away_team, trace, variance=False)
   predict_winner(home_team, away_team, trace)
   ```

4. **Evaluate Model Performance:**
   Assess the in-sample and out-of-sample accuracy using the provided evaluation metrics and plots.
