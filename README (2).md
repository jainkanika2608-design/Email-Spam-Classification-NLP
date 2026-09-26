# Email Spam Classification Using Natural Language Processing and Machine Learning

A beginner-friendly, end-to-end machine learning project that classifies email/SMS messages as **SPAM** or **NOT SPAM (Ham)** using **TF-IDF** feature extraction and a **Multinomial Naive Bayes** classifier — implemented as a single, self-contained Google Colab notebook.

## Overview

This project was built as an individual minor internship project for the first semester of a B.Tech CSE (AI) programme. It demonstrates a complete classical NLP + ML pipeline: data acquisition, cleaning, text preprocessing, TF-IDF feature extraction, model training, evaluation, and an interactive prediction demo.

## Features

- Automatic dataset download with a built-in offline fallback (no manual upload needed)
- Clean, well-commented text preprocessing pipeline
- TF-IDF feature extraction (`TfidfVectorizer`)
- Multinomial Naive Bayes classifier (`MultinomialNB`)
- Full evaluation suite: Accuracy, Precision, Recall, F1-score, Confusion Matrix, Classification Report
- Visualizations: class distribution, message length distribution, confusion matrix heatmap
- Interactive cell to classify any custom message, with safe handling of empty/invalid input
- Runs top-to-bottom in Google Colab with **no API keys, no paid services, and no manual file uploads**

## Tech Stack

| Category | Tool |
|---|---|
| Language | Python 3 |
| Environment | Google Colab |
| Data | pandas, numpy |
| NLP / Features | scikit-learn `TfidfVectorizer` |
| Model | scikit-learn `MultinomialNB` |
| Visualization | matplotlib, seaborn |

## How to Run

1. Open `Email_Spam_Classification_NLP_ML.ipynb` in [Google Colab](https://colab.research.google.com/).
2. Run all cells in order (**Runtime → Run all**), or run them one by one from top to bottom.
3. When you reach the interactive section, type any email/SMS-style message when prompted to see a live SPAM / NOT SPAM prediction.

No installation, API key, or dataset upload is required — everything is handled inside the notebook.

## Dataset

The project uses the public **SMS Spam Collection** dataset (5,574 labelled English SMS messages), downloaded automatically from a stable public source at runtime. If the download is ever unavailable, the notebook automatically falls back to a small, self-contained example dataset embedded directly in the code, so the notebook always runs successfully end-to-end.

## Project Structure

```
├── Email_Spam_Classification_NLP_ML.ipynb   # Main Colab notebook (run this)
├── Project_Report.docx                      # Full academic project report
└── README.md                                # This file
```

## Evaluation Metrics

The model is evaluated on a held-out 20% test split using:

- **Accuracy** – overall correctness
- **Precision** – reliability of spam predictions
- **Recall** – how many actual spam messages were caught
- **F1-score** – balance of precision and recall
- **Confusion Matrix** – full breakdown of correct/incorrect predictions

Exact numbers depend on the specific train/test split and dataset used at run time; see the notebook output for current results.

## Limitations

This is an educational project trained on a limited dataset and should not be treated as a production-grade or general-purpose spam filter. See the "Limitations" section in the notebook and project report for details.

## License

This project is intended for academic/educational use.
