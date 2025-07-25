# ConverSQL-Text-to-SQL-Converter

# ConverSQL: Comparative Analysis of Transformer-Based Models for Natural Language to SQL Mapping

This repository contains the implementation and evaluation of various transformer-based models for converting natural language queries into structured SQL commands — a task commonly known as **Text-to-SQL**.

## 🧠 Abstract

This project investigates the effectiveness of Transformer-based models in translating natural language questions into structured SQL queries. We fine-tuned and evaluated multiple encoder-decoder architectures — including **T5**, **BART**, **FLAN-T5**, and **BART-Large** — using a synthetic dataset of question-SQL pairs.

Uniform preprocessing steps like tokenization, padding, and truncation were applied to ensure consistent input formatting across all models. A custom evaluation pipeline was developed to measure both the **syntactic** and **semantic** accuracy of the generated SQL queries.

**Key Results:**
- **FLAN-T5** achieved the highest accuracy: **99.5%**
- **BART-Large** demonstrated strong generalization
- FLAN-T5 showed consistent training behavior across epochs

## 🛠️ Features

- ✅ Support for multiple transformer models (T5, BART, FLAN-T5, BART-Large)
- ✅ Custom dataset handling for question-SQL pairs
- ✅ Training and fine-tuning pipeline with HuggingFace Transformers
- ✅ Evaluation metrics for syntactic and semantic correctness
- ✅ Easy model switching via config

## 📊 Results Summary

| Model       | Accuracy | Generalization | Notes                        |
|-------------|----------|----------------|------------------------------|
| FLAN-T5     | 99.5%    | High           | Most consistent performance |
| BART-Large  | 92.1%    | High           | Strong generalization       |
| T5          | 86.3%    | Medium         | Stable but less precise     |
| BART        | 92.7%    | Medium         | Decent baseline             |

## 🖥️ Gradio Interface

To make the Text-to-SQL model more accessible and interactive, we integrated a Gradio interface. This simple web UI allows users to enter a natural language question (e.g., “Show all customers from New York”) and receive the corresponding SQL query generated by the fine-tuned transformer model in real-time. The interface is lightweight, runs locally in a browser, and eliminates the need for manual code execution — making the system usable by non-technical users as well. This helps demonstrate the model’s capabilities in a user-friendly way and is a step toward real-world deployment.

## ✅ Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/sanikautkr03/ConverSQL.git
cd ConverSQL
