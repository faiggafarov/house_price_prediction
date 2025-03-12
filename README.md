# Feature Importance Visualization

This project provides a Python script to train a LightGBM model and visualize the feature importance of the dataset.

## Installation

Ensure you have the required libraries installed. You can install them using:

```bash
pip install numpy pandas lightgbm matplotlib seaborn scikit-learn
```

## Usage

1. Prepare your dataset and define `X` (features) and `y` (target variable).
2. Run the script to train the LightGBM model and visualize the feature importance.

### Example Code

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
from lightgbm import LGBMRegressor

# Function to plot feature importance
def plot_importance(model, features, num=20, save=False):
    feature_imp = pd.DataFrame({"Value": model.feature_importances_, "Feature": features.columns})
    plt.figure(figsize=(12, 14))
    sns.set(font_scale=1.2)
    sns.barplot(x="Value", y="Feature", data=feature_imp.sort_values(by="Value", ascending=False)[0:num])
    plt.title("Feature Importance", fontsize=14)
    plt.xlabel("Importance", fontsize=12)
    plt.ylabel("Features", fontsize=12)
    plt.xticks(rotation=45)
    plt.gca().invert_yaxis()
    plt.tight_layout()
    plt.show()
    if save:
        plt.savefig("importances.png")

# Train model and plot feature importance
model = LGBMRegressor()
model.fit(X, y)
plot_importance(model, X, num=20)
```

## Saving the Plot

To save the feature importance plot as an image, pass `save=True` when calling `plot_importance`:

```python
plot_importance(model, X, num=20, save=True)
```

This will save the image as `importances.png` in the working directory.
