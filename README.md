# Assignments

This repository contains a collection of data science, machine learning, and NLP assignments completed as part of the program. Each notebook focuses on a different task, from text preprocessing and classification to semantic search and emotion analysis.

## Repository overview

The projects in this repository include:

- Custom Chatbot: a semantic FAQ-based chatbot using sentence embeddings
- Emotion Detection: text-based emotion classification using NLP techniques
- Keyword Extraction: extracting important words and phrases from text
- Model Evaluation for Text (TF-IDF Vectorizer): comparing model performance using TF-IDF features
- Spam Classifier (CountVectorizer + Naive Bayes): building a spam detection model
- Restaurant Sales: exploratory data analysis and sales insights
- Text Extraction using Regex: extracting structured information from text using regular expressions

## Project structure

```text
.
├── Custom_Chatbot.ipynb
├── Emotion_Detection (1).ipynb
├── Keyword_Extraction.ipynb
├── Model_eval_for_text_(tfidfvectorizer).ipynb
├── Restraunt_Sales.ipynb
├── Spam_Classifier_(CountVectorizer_and_NaiveBias).ipynb
├── Text_Extraction_using_Regex.ipynb
├── README.md
└── .gitignore
```

## Tech stack

The assignments use a range of Python libraries commonly used in NLP and data science, including:

- Python
- Jupyter Notebook
- pandas
- NumPy
- scikit-learn
- NLTK
- Matplotlib
- Seaborn
- sentence-transformers
- PyTorch

## Requirements

- Python 3.8+
- Jupyter Notebook or VS Code with Jupyter support
- Internet access (for downloading models/packages when needed)

Install the core dependencies with:

```bash
python -m venv .venv
source .venv/bin/activate   # On macOS/Linux
# .venv\Scripts\Activate.ps1  # On Windows PowerShell

pip install --upgrade pip
pip install jupyter pandas numpy scikit-learn nltk matplotlib seaborn sentence-transformers torch
```

## Getting started

1. Clone the repository:

```bash
git clone https://github.com/ManYaAr/Capeg-assignments.git
cd Capeg-assignments
```

2. Create and activate a virtual environment.

3. Install the dependencies.

4. Open the project notebooks in Jupyter:

```bash
jupyter notebook
```

5. Run the notebook you want to explore.

## Notes

- Each notebook is a standalone assignment and can be run independently.
- Some notebooks may require additional dataset downloads or model initialization on first run.
- The repository is intended for learning and experimentation in NLP and machine learning.

## Author

Created by [Manya Arora](https://github.com/ManYaAr).
