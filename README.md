# Pokémon GO Catch Difficulty Classification

This project analyzes Pokémon GO data and builds machine learning models to predict whether a Pokémon is relatively easy or hard to catch.

The target variable was created using `Capture_rate` and `Escape_rate`, which were combined into a simplified probability of catching a Pokémon before it escapes.

## Dataset

The data comes from the Kaggle dataset:

https://www.kaggle.com/datasets/netzuel/pokmon-go-dataset-15-generations/data

The dataset contains base information about Pokémon in Pokémon GO, including stats such as `Attack`, `Defense`, `Stamina`, `MaxCP`, types, `Capture_rate`, and `Escape_rate`.

## Methods

The project includes:

- exploratory data analysis,
- target variable creation,
- data preprocessing,
- comparison of five classification models:
  - Perceptron,
  - Logistic Regression,
  - k-Nearest Neighbors,
  - Support Vector Machine,
  - Decision Tree,
- cross-validation,
- learning curve,
- validation curve,
- hyperparameter tuning with Grid Search,
- interpretation of the final Decision Tree model.

## Results

The best general performance among the basic models was achieved by SVM, but the Decision Tree model was selected for further analysis because it achieved similar results, handled the `hard` class well, and was easier to interpret.

The final Decision Tree model achieved approximately:

- Accuracy: 0.69
- F1-score macro: 0.69

The most important feature in the final model was `MaxCP`, suggesting that the overall combat strength of a Pokémon was strongly related to catch difficulty in this simplified setting.

## Limitations

The project uses species-level base data. It does not include encounter-level information, such as the actual CP of a specific Pokémon, Poké Ball type, berries, throw quality, curveball, medals, or player bonuses.

A natural extension of this project would be to collect data from individual catch encounters and analyze how catch difficulty varies within the same Pokémon species.
