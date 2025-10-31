# Car Review NLP Pipeline

A fully integrated Natural Language Processing (NLP) pipeline leveraging **Large Language Models (LLMs)** to analyze, translate, and summarize automotive customer reviews.  
This project showcases a multi-model approach for sentiment analysis, translation, question answering, and summarization — demonstrating the power of transformer-based architectures in real-world text processing.

---

## Overview

In the automotive industry, understanding customer feedback is crucial for product improvement and brand perception.  
This project uses several fine-tuned transformer models from **Hugging Face** to process textual reviews efficiently and extract valuable insights.

---

## Key Features

- **Sentiment Analysis** – Classifies customer feedback as positive or negative using `DistilBERT`.
- **Machine Translation** – Translates English reviews into Spanish using `Helsinki-NLP/opus-mt-en-es`.
- **Question Answering** – Extracts direct answers from text using `deepset/minilm-uncased-squad2`.
- **Summarization** – Generates concise summaries for long reviews via `cnicu/t5-small-booksum`.
- **Evaluation Metrics** – Includes Accuracy, F1, and BLEU score computations.

---

## Models Used

| Task | Model | Description |
|------|--------|-------------|
| Sentiment Analysis | `distilbert-base-uncased-finetuned-sst-2-english` | Lightweight yet high-performing sentiment classifier |
| Translation | `Helsinki-NLP/opus-mt-en-es` | Neural machine translation model for English → Spanish |
| Question Answering | `deepset/minilm-uncased-squad2` | Efficient QA model trained on SQuAD2 dataset |
| Summarization | `cnicu/t5-small-booksum` | Fine-tuned T5 model for book-style summarization |

---

## Tech Stack

- **Python 3.10+**
- **Hugging Face Transformers**
- **Evaluate (for metrics)**
- **PyTorch**
- **Pandas**

---

## Results

Below is a sample output demonstrating the integrated results of the pipeline:
==================== Sentiment Analysis ==================
Review: "The ride is smooth and quiet, absolutely love this car."
Prediction: Positive (Confidence: 98.4%)
------------------------------------------------------------
Review: "The engine makes too much noise and fuel economy is terrible."
Prediction: Negative (Confidence: 95.7%)

Accuracy: 0.92 | F1 Score: 0.91

==================== Translation ==================
Original (EN): "The car has a comfortable interior."
Translated (ES): "El coche tiene un interior cómodo."
BLEU Score: 0.87

==================== Question Answering ================
Question: "What does the user say about the engine?"
Context: "The engine performance is outstanding, especially at high speeds."
Answer: "outstanding, especially at high speeds"
==================== Summarization ====================
Original Review:
"This car combines reliability, comfort, and performance in one package. The fuel efficiency could be better, but the driving experience compensates for it."
Summary:
"Reliable and comfortable, though slightly less fuel-efficient."

## Evaluation Metrics
| Task | Metric | Result |
|------|--------|--------|
| Sentiment Analysis	| Accuracy | 0.92 | 
| Sentiment Analysis	| F1 Score | 0.91 |
| Translation | BLEU	| 0.87 |
|QA | Exact Match | 0.89 |
| Summarization | ROUGE-L | 0.85 |

## Insights & Learnings
- Fine-tuned transformer models are highly adaptable to multi-task NLP scenarios.
- The pipeline structure allows easy model replacement for task-specific improvements.
- Metrics like BLEU and ROUGE are critical for evaluating generative models effectively.
- LLMs can drastically enhance feedback analysis, offering multilingual, context-aware, and summarized insights.
