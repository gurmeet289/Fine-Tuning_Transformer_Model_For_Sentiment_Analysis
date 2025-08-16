# Fine-Tuning_Transformer_Model_For_Sentiment_Analysis

This project demonstrates **full fine-tuning** of a Hugging Face Transformer model on a custom dataset using Google Colab.  
The training process updates **all model parameters** (not parameter-efficient tuning like LoRA/PEFT).

---

## Features
- Full fine-tuning of Hugging Face models (e.g., `distilbert-base-uncased`)
- Uses Hugging Face `transformers`, `datasets`, and `accelerate`
- Training & evaluation on sentiment classification dataset
- Pushes fine-tuned model to Hugging Face Hub
- Generates a model card with metadata

---

## Project Structure

    - `Fine_Tune_Model.ipynb` → Colab notebook for full fine-tuning
    - Saved fine-tuned model in Hugging Face Hub repo

---

## ⚙️ Installation
  
  ### Run this in your Colab notebook:

## 📝 Usage (Colab)
    
    1) Clone this repo or open the Colab notebook.

    2) Install dependencies : !pip install -q transformers datasets accelerate evaluate huggingface_hub

 ### Load dataset:

    Replace with your own dataset, or use Hugging Face datasets.

 ### Fine-tune the model:

    The script trains the base model (distilbert-base-uncased by default).

    All layers are updated (full model fine-tuning).

 ### Evaluate model:

    Uses evaluate to compute accuracy, F1, etc.

 ### Save and upload model to Hugging Face Hub:

    from huggingface_hub import notebook_login
    notebook_login()

 ### Then push model:

    trainer.push_to_hub()

 ## Notes

    This notebook performs full fine-tuning, which is compute & memory heavy compared to LoRA/PEFT.

    If you want lightweight training, consider adapting this to use PEFT with LoRA.

## Acknowledgements

    1) Hugging Face Transformers
    2) Datasets
    3) Accelerate

## Thank You! Keep Learning!
