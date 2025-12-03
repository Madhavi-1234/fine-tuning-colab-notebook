📘 Fine-Tuning BERT on IMDB Movie Reviews

A hands-on Generative AI practical using Hugging Face Transformers

This project demonstrates how to fine-tune a BERT (bert-base-cased) model for sentiment classification on the IMDB movie reviews dataset.
The full experiment was done on Google Colab with GPU support.


🚀 Project Overview

This notebook covers:

Loading the IMDB dataset

Tokenizing text using AutoTokenizer

Initializing BERT for Sequence Classification

Setting TrainingArguments

Using Trainer API for training

Tracking logs using Weights & Biases (W&B)

Evaluating the fine-tuned model

This project is part of my Generative AI course, focusing on understanding how pre-trained models learn during fine-tuning.


📂 Dataset

The dataset used is the IMDB Movie Reviews dataset from the datasets library:

from datasets import load_dataset
dataset = load_dataset("imdb")


The dataset contains:

50,000 labelled reviews

Binary sentiment: 0 = negative, 1 = positive

🛠 Libraries Used
pip install transformers
pip install datasets
pip install wandb


🧠 Model Used

BERT-base-cased
Fine-tuned for binary sentiment classification.


⚙️ Training Details

Epochs: 5

Batch Size: 16

Learning Rate: 2e-5

Optimizer: AdamW

Evaluation: Per epoch

Logging: W&B

Training script uses:

from transformers import Trainer, TrainingArguments


📊 Evaluation

After training, performance is evaluated using:

trainer.evaluate()


Outputs include:

Accuracy

Loss

Other evaluation metrics (depending on setup)


🔧 Tools & Platforms


Google Colab (T4 GPU)

Hugging Face Transformers

W&B for experiment tracking

GitHub for version control


🙏 Acknowledgements

Special thanks to Abhinay Yadav Sir for teaching Generative AI concepts and guiding us through hands-on practicals.
