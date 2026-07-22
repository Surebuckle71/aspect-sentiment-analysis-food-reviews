# Transformer-Based Aspect Sentiment Analysis for Food Reviews

M.Sc. Data Science project (University of Europe for Applied Sciences) comparing BERT, RoBERTa, and XLM-RoBERTa for aspect-based sentiment analysis (ABSA) on restaurant reviews.

## Summary

Reviews often cover several aspects (food, service, ambiance, price) with mixed sentiment in a single review. This project compares transformer models against classical baselines (LSTM, SVM) on over 1.3 million Zomato Bangalore aspect-sentiment instances across four aspects: **Food, Service, Ambiance, Price**.

RoBERTa-base performed best overall (83.6% accuracy, 82.9% macro F1), narrowly ahead of BERT and XLM-RoBERTa, and all transformer models substantially outperformed LSTM (71.2%) and SVM (68.5%). Food sentiment was easiest to classify (F1 85.3%); Price was hardest (F1 79.8%). Neutral sentiment remained the most difficult class across all models (41-49% accuracy).

The `.ipynb` files are clean/unexecuted source. To see the actual results (plots, metrics, predictions), view the rendered exports:
- [Part 1: Data Preprocessing](https://htmlpreview.github.io/?https://github.com/Surebuckle71/aspect-sentiment-analysis-food-reviews/blob/main/reports/Part1_Zomato_Final.html)
- [Part 2: Model Training](https://htmlpreview.github.io/?https://github.com/Surebuckle71/aspect-sentiment-analysis-food-reviews/blob/main/reports/Part2_ZomatoTrain_Models.html)
- [Part 3: Predictions](https://htmlpreview.github.io/?https://github.com/Surebuckle71/aspect-sentiment-analysis-food-reviews/blob/main/reports/Part3_ZomatoPredictions.html)

## Dataset

[Zomato Bangalore Restaurants](https://www.kaggle.com/datasets/himanshupoddar/zomato-bangalore-restaurants) dataset (Kaggle), restaurant reviews used to derive aspect-level sentiment labels for Food, Service, Ambiance, and Price.

Raw and preprocessed data (1.3M+ review instances, several GB) are not included in this repo due to size. Download from the link above to reproduce the pipeline.

## Contents

- `Part1_Zomato_Final.ipynb`: data loading and preprocessing
- `Part2_ZomatoTrain_Models.ipynb`: model training (BERT, RoBERTa, XLM-RoBERTa, LSTM, SVM baselines)
- `Part3_ZomatoPredictions.ipynb`: evaluation and predictions
- `docs/dataset_statistics.png`: dataset statistics
- `docs/bibliography.bib`: references
- `reports/`: pre-rendered HTML exports of each notebook with full outputs (see links above)

## Usage

```bash
pip install -r requirements.txt
jupyter notebook Part1_Zomato_Final.ipynb
```
