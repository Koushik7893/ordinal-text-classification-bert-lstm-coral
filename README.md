# 📊 Ordinal Text Classification with Traditional, Deep, and Transformer Models

Ordinal text classification deals with **ordered labels** — like star ratings or sentiment levels — where the class labels follow a natural order (e.g., 1 < 2 < 3 < 4 < 5). Unlike multiclass classification, ordinal classification penalizes wrong predictions more heavily when the order is violated.

---

## 📌 Tasks Covered

This project explores ordinal classification using:

### 🔹 Traditional Machine Learning
| Model                     | Dataset           | Notes                         |
|--------------------------|-------------------|-------------------------------|
| `mord.LogisticAT()`      | Amazon Polarity   | Ordinal Logistic Regression   |

### 🔹 Deep Learning
| Model                     | Dataset           | Notes                         |
|--------------------------|-------------------|-------------------------------|
| LSTM + Ordinal Regression| IMDb              | Softmax replaced with ordinal logic |

### 🔹 Transformers (BERT-based)
| Model                     | Dataset           | Notes                         |
|--------------------------|-------------------|-------------------------------|
| BERT + CORAL Head        | Amazon Polarity   | Ordinal loss (CORAL)          |
| DistilBERT + Softmax     | Yelp Review Full  | Baseline ordinal setup        |
| BERT + XGBoost (features)| IMDb              | Embedding-level classification|

---

## 📂 Folder Structure

```

ordinal-text-classification-nlp/
│
├── notebooks/
│   ├── ordinal\_logreg\_mord\_amazon.ipynb
│   ├── lstm\_ordinal\_imdb.ipynb
│   ├── distilbert\_softmax\_yelp.ipynb
│   ├── bert\_coral\_amazon.ipynb
│   └── bert\_embeddings\_xgb\_imdb.ipynb
│
├── requirements.txt
├── README.md


---

## 🧪 Datasets Used

| Dataset             | Description                                 |
|---------------------|---------------------------------------------|
| Amazon Polarity     | Binary/5-level review scores                |
| IMDb                | Movie reviews with sentiment ratings        |
| Yelp Review Full    | Star-based review scores (1–5)              |

All datasets are available from `datasets` library (`HuggingFace Datasets`).

---

## 📊 Evaluation Metrics

- MAE (Mean Absolute Error)
- Quadratic Weighted Kappa
- Accuracy
- Confusion Matrix
- Ordinal-specific penalties

---

## 🔧 Installation

```bash
git clone https://github.com/Koushik7893/ordinal-text-classification-bert-lstm-coral.git
cd ordinal-text-classification-bert-lstm-coral
pip install -r requirements.txt
````

---

## 🔍 Key Learnings

* Traditional models like `mord` work well for interpretable ordinal tasks.
* LSTMs with ordinal-specific heads can outperform softmax-based classifiers.
* **CORAL loss** helps encode the order in multi-class transformer outputs.

---

## ✍️ Author

**Koushik Reddy**
🔗 [Hugging Face](https://huggingface.co/Koushim) 

---

## 📌 License

This project is open source and available under the [Apache License](LICENSE).

````
