### **README for Fine-Tuning a Small Language Model (SLM) for Summarization**  

---

## **Project Overview**  
This project focuses on fine-tuning a **Small Language Model (SLM)** (**Qwen2.5-0.5B**) for **summarizing French text** using data distilled from a larger LLM (**Qwen2.5-7B**).  
We implement **LoRA (Low-Rank Adaptation)** and **custom quantization** to enable efficient training on **Google Colab’s free-tier GPU**.  
Evaluation metrics include **ROUGE** and **BERTScore**.  

---

## **Project Structure**  

📂 *(Root Directory)*  
```
 ├── requirements.txt                # Dependencies  
 ├── create_documents.ipynb          # Fetches documents from Wikipedia  
 ├── create_summaries.ipynb          # Generates summaries for the fetched documents  
 ├── finetune_with_SFT.ipynb         # Fine-tuning using SFT, inference, and evaluation  
 ├── finetune_with_DPO.ipynb         # Fine-tuning using DPO, inference, and evaluation  
 ├── scores.ipynb                     # Computes BERT and ROUGE scores  
 │  
 ├── 📂 data_2k_tokens/               # Preprocessed dataset (max 2k tokens per document)  
 │   ├── train.json                   # Training dataset  
 │   ├── test.json                     # Test dataset  
 │  
 ├── 📂 data_8k_tokens/               # Preprocessed dataset (max 8k tokens per document)  
 │   ├── train.json                   # Training dataset  
 │   ├── test.json                     # Test dataset  
 │  
 ├── 📂 bert_scores/                  # BERT scores for SFT and DPO fine-tuned models  
 ├── 📂 rouge_scores/                 # ROUGE scores for SFT and DPO fine-tuned models  s
 │
 ├── 📂 articles/                     # Fetched articles from Wikipedia
 ├── 📂 summaries/                    # Summarized articles with the different models
 │  
 ├── README.md                        # This file  
 ├── report.pdf                        # Project report  
```

---

## **Installation & Setup**  
### **1️⃣ Install Dependencies**  
Run the following command to install required libraries:  
```bash
pip install -r requirements.txt
```
Or install manually:  
```bash
pip install transformers datasets accelerate bitsandbytes peft rouge-score sacrebleu torch sentencepiece blobfile tiktoken bert-score tqdm pandas wikipedia
```

---

## **Collaborators**  
- **Brahim Touayouch**  
- **Zakaria Abboud**   