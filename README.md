
# Market Basket Analysis with Apriori Algorithm

## Project Overview

This project applies the Apriori algorithm to the IMDb Top 1000 Movies and TV Shows dataset. The main goal is to find groups of actors who frequently appear together in movies.

Each movie is treated as a basket, and each actor is treated as an item. The Apriori algorithm is implemented in Python using the join, prune, and support counting steps.

## Dataset

The dataset is available on [Kaggle](https://www.kaggle.com/datasets/harshitshankhdhar/imdb-dataset-of-top-1000-movies-and-tv-shows).

It contains 1,000 movie and TV show records. For this project, only four columns are used: `Star1`, `Star2`, `Star3`, and `Star4`.

Repeated actor names within the same movie are removed when creating baskets.

## Implementation

The Apriori algorithm is implemented using three main functions:

- `frequent_singletons()`: finds frequent individual actors.
- `generate_candidates()`: creates new candidates using join and prune.
- `count_support()`: counts candidate occurrences and applies the minimum support threshold.

The `apriori()` function combines these steps to find frequent itemsets of different sizes.

## Experiments

Two experiments are included:

1. **Minimum support sensitivity:** the algorithm is tested with minimum support values of 2, 3, 4, 5, and 6.
2. **Scalability analysis:** the algorithm is tested with 100, 250, 500, 750, and 1,000 baskets.

Each experiment is repeated five times, and the median execution time is reported.

With a minimum support of 3, the algorithm finds 271 frequent single actors, 25 frequent pairs, and 3 frequent triples.

## How to Run

1. Open `market_basket.ipynb` in Google Colab.
2. Install or enable access to the Kaggle API if needed.
3. Add your Kaggle API token to Colab Secrets with the name `KAGGLE_API_TOKEN`.
4. Run the notebook cells in order.

The dataset is downloaded automatically using the Kaggle API.

The minimum support value can be changed in the notebook to test different thresholds.

## Project Files

- `market_basket.ipynb`: Python implementation and experiments.
- `Market_Basket_Analysis.pdf`: project report with methodology, results, and discussion.
- `README.md`: project description and instructions.

## Tools

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Kaggle API
