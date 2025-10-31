# Car Review NLP Pipeline 🚗💬

This project demonstrates the use of **Large Language Models (LLMs)** for multiple Natural Language Processing (NLP) tasks on a car review dataset.  
It combines sentiment analysis, translation, extractive question answering, and summarization into one workflow.

## 📌 Project Overview
Using the **Hugging Face Transformers** library, this project performs the following:

1. **Sentiment Classification**  
   - Model: `distilbert-base-uncased-finetuned-sst-2-english`  
   - Task: Classify each car review as *Positive* or *Negative*  
   - Metrics: Accuracy & F1 Score (using the `evaluate` library)

2. **Translation**  
   - Model: `Helsinki-NLP/opus-mt-en-es`  
   - Task: Translate English car reviews into Spanish  
   - Metric: BLEU Score (evaluates translation quality)

3. **Extractive Question Answering (QA)**  
   - Model: `deepset/minilm-uncased-squad2`  
   - Task: Identify answer spans from the review text based on a question

4. **Summarization**  
   - Model: `cnicu/t5-small-booksum`  
   - Task: Summarize the key idea of a review into a concise statement

##Tech Stack
- Python  
- Transformers (Hugging Face)  
- Evaluate  
- PyTorch  
- Pandas

##Results
- Displays model predictions with confidence scores
- Computes Accuracy and F1 metrics for sentiment analysis
- Shows BLEU score for translation evaluation
- Extracts relevant answers using a QA model
- Generates summaries for long reviews
