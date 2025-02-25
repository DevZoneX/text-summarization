### **README for Fine-Tuning a Small Language Model (SLM) for Summarization**  

---

## **Project Overview**  
This project focuses on fine-tuning a **Small Language Model (SLM)** (e.g., **mT5-Base, Qwen2.5-0.5B, Atlas-Chat-2B**) for **summarization** of **non-English text**.  
We implement **LoRA (Low-Rank Adaptation)** and **custom quantization** for efficient training on **Google Colab’s free-tier GPU**.  
Evaluation includes **ROUGE, BERTScore, and LLM-as-a-Judge**.  

---

## **Project Structure**  

📂 **Fine-Tuned-SLM/** *(Root Directory)*  
 ├── `requirements.txt` – Dependencies  
 ├── `data.ipynb` – Jupyter Notebook for preparing dataset
 └── `finetune.ipynb` – Jupyter Notebook for training, inference, and evaluation
 │  
 ├── 📂 **data/** *(Contains dataset - preprocessed files)*  
 │   ├── `train.json` – Training dataset  
 │   ├── `test.json` – Test dataset  
 │   └── `val.json` – Validation dataset  
 │  
 ├── 📂 **results/** *(Contains model checkpoints and evaluation results)*  
 │   ├── `fine_tuned_model/` – Saved model and tokenizer  
 │   ├── `evaluation_metrics.json` – ROUGE & BERTScore results  
 │   └── `sample_summaries.txt` – Example generated summaries  
 │  
 ├── `README.md` *(This file)*  
 ├── `report.pdf` *(Project report)*
 ├── `run.sh` *(Bash script to automate training & inference)*

---

## **Installation & Setup**  
### **1️⃣ Install Dependencies**  
Run the following command to install required libraries:  
```bash
pip install -r requirements.txt
```
Or install manually:  
```bash
pip install transformers datasets accelerate bitsandbytes peft rouge-score sacrebleu torch
```

## **Collaborators**
- [**Abboud Zakaria**]
- [**Brahim Touayouch**]