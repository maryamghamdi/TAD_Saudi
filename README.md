# TAD-Saudi: An Explainable AI Framework for Trustworthy Financial App Detection
This is the source code for the paper: TAD-Saudi: An Explainable AI Framework for Trustworthy Financial App Detection by Dr.Raed Alharbi and Maryam Alghamdi.

# Files
- `Data_processing.ipynb` Contains functions for collecting and preprocessing data.
- `Models.ipynb` Contains all the models in the paper.
- `Analysis.ipynb` Contains codes for analyzing the results.


# Requirements
The code requires Python 3.x and the following Python libraries installed:
- requests
- pytorch_tabnet
- transformers
- category_encoders
- pandas
- matplotlib.pyplot
- numpy
- sklearn
- xgboost
- catboost
- pytorch_tabnet
- category_encoders
- imblearn
- torch
- joblib
- json
- os
- shap

You can install the required packages using:
```bash
pip install -r requirements.txt
```

# Dataset
The data used in the code is uploaded in the file `TAD_Saudi_Finance_Apps.csv`.  
This dataset contains metadata, user reviews, and permissions for **246 financial apps** available in the **Saudi Android store**.  
The dataset was collected by the authors using web scraping techniques and APIs, and **manually labeled**.

### Columns Description
: 
`rating_1 to rating_20`: Numerical rating (1 to 5 stars) corresponding to each review.
`permission_1 to permission_14`: List of permissions requested by the app, written in Arabic (e.g., camera access, storage, microphone, etc.). Missing values in these columns indicate that the app does not request the corresponding permission.
`Label`: Classification of the app as Real (trustworthy) or Fake (untrustworthy).

| Column Name        | Description |
|--------------------|-------------|
| `app_id`           | Unique identifier of the app, typically its package name. |
| `app_name`         | Name of the financial app. |
| `description`      | Arabic-language description of the app from the store. |
| `rating`           | Average user rating of the app (on a 1–5 scale). |
| `total_ratings`    | Total number of user ratings received. |
| `review_1` to `review_20` | User-written reviews in Arabic for each app. |
| `rating_1` to `rating_20` | Star rating (1 to 5) provided by the user for each corresponding review. |
| `permission_1` to `permission_14` | Permissions requested by the app (e.g., storage, camera, microphone), written in Arabic. |
| _Note:_ Missing values in these columns indicate that the app **does not request** the corresponding permission. |
| `Label`     | Classification of the app as `Real` (**trustworthy**) or `Fake` (**untrustworthy**). |
