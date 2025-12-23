# SUB-TASK - NATURAL LANGUAGE PROCESSING ASSIGNMENT
## Topic: English-Vietnamese Medical Machine Translation

This project constructs a bidirectional medical machine translation system (**English ↔ Vietnamese**) based on the **NLLB-200** foundation model by Meta AI, utilizing the **LoRA** (Low-Rank Adaptation) fine-tuning technique to optimize performance on medical domain data.

## 📂 File Descriptions

Below is a brief description of the files and directories within the project:

### 1. Code Notebooks
* **`Eng_To_Vie.ipynb`**:
    * Notebook used to **train** the translation model for the **English → Vietnamese** direction.
    * Run this file to generate the forward translation Adapter.
* **`Vie_To_Eng.ipynb`**:
    * Notebook used to **train** the translation model for the **Vietnamese → English** direction.
    * Run this file to generate the reverse translation Adapter (using swapped input data).
* **`Score.ipynb`**:
    * Notebook used for **inference** and **evaluation** of translation quality (calculating BLEU scores) using the trained models.

### 2. Model Folders
* **`export_model_eng_to_vie/`**:
    * Contains the trained LoRA Adapter for the **English → Vietnamese** direction.
* **`export_model_vie_to_eng/`**:
    * Contains the trained LoRA Adapter for the **Vietnamese → English** direction.

### 3. Analysis Results
* **`Analysis_En_Vi.csv`**:
    * CSV file containing sentences translated from English to Vietnamese (for comparison with ground truth).
* **`Analysis_Vi_En.csv`**:
    * CSV file containing sentences translated from Vietnamese to English.

## 🚀 Quick Start Guide

### 1. Installation
Install the required libraries:
```bash
pip install transformers datasets peft accelerate sacrebleu
```

### 2. Usage
* **To retrain the models:** Run `Eng_To_Vie.ipynb` or `Vie_To_Eng.ipynb`.
* **To evaluate/translate:** Open `Score.ipynb`, point the path to the `export_model...` directory, and run the translation cells.

---
**Additional Information:**
* **Dataset:** VLSP (Medical Domain).
* **Technology:** NLLB-200, LoRA, Hugging Face Transformers.
