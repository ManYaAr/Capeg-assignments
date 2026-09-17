# Semantic Chatbot

A lightweight semantic question-answering chatbot built with Python and Sentence Transformers. Instead of matching user input by exact keywords, it compares the meaning of a question with a collection of FAQ questions and returns the answer associated with the closest match.

## Features

- Semantic rather than exact-text question matching
- Uses cosine similarity through `sentence-transformers`
- Multilingual sentence-embedding model: `distiluse-base-multilingual-cased-v1`
- Simple FAQ-style question and answer dataset
- Interactive command-line chat loop
- Type `exit` or `quit` to end the conversation

## How it works

1. FAQ questions are stored together with their answers.
2. The chatbot encodes the FAQ questions into vector embeddings.
3. A user's query is encoded using the same model.
4. Semantic search finds the most similar FAQ question.
5. The chatbot returns the answer associated with that question.

This approach allows related questions such as `How can I stay focused?` and `How to improve focus?` to be treated as similar even when their wording is different.

## Project structure

```text
.
├── Custom_Chatbot.ipynb  # Notebook containing the chatbot implementation
└── README.md             # Project documentation
```

## Requirements

- Python 3.8 or later
- Jupyter Notebook or Google Colab
- pandas
- sentence-transformers
- PyTorch (installed as a dependency of `sentence-transformers` in most environments)

## Getting started

### Option 1: Run in Google Colab

1. Open [`Custom_Chatbot.ipynb`](./Custom_Chatbot.ipynb).
2. Open the notebook in Google Colab.
3. Run the cells from top to bottom.
4. When prompted, enter a question in the chatbot.

### Option 2: Run locally

Clone the repository and install the dependencies:

```bash
git clone https://github.com/ManYaAr/Semantic-Chatbot.git
cd Semantic-Chatbot
python -m venv .venv
```

Activate the virtual environment:

```bash
# macOS/Linux
source .venv/bin/activate

# Windows PowerShell
.venv\Scripts\Activate.ps1
```

Install the required packages:

```bash
python -m pip install --upgrade pip
pip install pandas sentence-transformers jupyter
```

Start Jupyter and open the notebook:

```bash
jupyter notebook Custom_Chatbot.ipynb
```

Run all cells in order and start the chatbot when the final cell is reached.

## Example

```text
Chatbot: Hello! Ask a question or type exit to quit.
You : tell me about machine learning
Chatbot : Machine learning is a field of AI that uses statistical techniques to give computers the ability to learn without being explicitly programmed.
You : how to stay focused
Chatbot : Improve focus with mindful practices and setting clear goals.
You : exit
Chatbot: Goodbye!
```

## Customizing the chatbot

To use the chatbot with your own knowledge base, edit the FAQ data in `Custom_Chatbot.ipynb`. Keep the questions and answers aligned by index, then rerun the cells that create the DataFrame and embeddings.

For larger datasets, consider storing the questions and answers in CSV or JSON files and adding a similarity threshold so the chatbot can respond gracefully when no FAQ entry is relevant.

## Limitations

- The chatbot returns the answer for the single closest FAQ question; it does not generate new answers.
- Responses are limited to the questions and answers included in the dataset.
- The embedding model is downloaded the first time it is loaded and may require an internet connection.
- The current implementation does not include a confidence threshold or conversation history.

## Author

Created by [Manya Arora](https://github.com/ManYaAr).

## License

No license has been specified for this repository yet. Add a license if you intend to allow others to use, modify, or redistribute the project.
