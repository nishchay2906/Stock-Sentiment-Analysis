# Stock direction from news headlines

This notebook compares classifiers that predict a binary market label from daily bundles of news headlines using TF–IDF bigrams.

## Run the notebook

From the repository root, create and activate a Python virtual environment, then install the notebook dependencies.

```sh
python -m venv .venv
. .venv/bin/activate
python -m pip install jupyterlab pandas nltk scikit-learn xgboost
python -m jupyterlab
```

Open [Stock Sentiment Analysis using News Headlines.ipynb](Stock%20Sentiment%20Analysis%20using%20News%20Headlines.ipynb) and select the virtual environment's Python kernel. Run the cells in order.

## Data

Place `Datasentiment.csv` in the repository root. The notebook expects a `Label` column and 25 headline columns in positions 3 through 27. The source CSV is absent from this repository.

Download the WordNet corpus before running the notebook with `python -m nltk.downloader wordnet`. The notebook fits TF–IDF on the training split. Its randomized holdout is a classification experiment. A time-ordered evaluation would be needed to estimate forecasting performance.
