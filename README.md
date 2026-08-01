# AI ChatBot

A simple Python-based NLP chatbot that answers questions from a built-in knowledge base using TF-IDF and cosine similarity.

This project is designed to demonstrate the fundamentals of a retrieval-style chatbot, including:

- text normalization
- tokenization
- lemmatization
- similarity scoring
- response selection from a knowledge base

## Demo

A verified sample conversation for the project is shown below:

![AI Chatbot Sample Conversation](conversation_sample.png)

## Project Overview

The chatbot stores short domain-specific sentences in `KNOWLEDGE_BASE` and compares user input with them using a TF-IDF vectorizer.

When a user asks a question, the program:

1. cleans and normalizes the text
2. tokenizes the input
3. lemmatizes the words
4. converts the text into vector form
5. computes similarity with the knowledge base
6. returns the most relevant sentence as the answer

If the similarity score is too low, the bot returns a fallback message stating that it does not understand the question yet.

## Features

- Greeting recognition
- Farewell detection
- Simple gratitude response
- Clear-screen command support
- NLP similarity-based answer generation
- Automatic NLTK resource download when needed

## Tech Stack

- Python 3
- `nltk`
- `scikit-learn`
- `Pillow`

## Project Structure

```text
AI_ChatBot/
├── Main.py                   # Main chatbot logic
├── README.md                 # Project documentation
├── conversation_sample.png    # Verified sample conversation preview
└── .venv/                     # Virtual environment (if created locally)
```

## Requirements

Install the core dependencies before running the project:

```bash
pip install nltk scikit-learn pillow
```

If you are using a virtual environment, install them inside that environment:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy RemoteSigned
& ".venv\Scripts\Activate.ps1"
python -m pip install nltk scikit-learn pillow
```

## Windows PowerShell Setup

The project has been verified in Windows PowerShell with a virtual environment.

### 1. Activate the environment

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy RemoteSigned
& "c:\Users\DELL\OneDrive\Desktop\Ai Chat bot\.venv\Scripts\Activate.ps1"
```

### 2. Run the script

```powershell
python Main.py
```

If you prefer the full path, this also works:

```powershell
& "c:\Users\DELL\OneDrive\Desktop\Ai Chat bot\.venv\Scripts\python.exe" "c:/Users/DELL/OneDrive/Desktop/Ai Chat bot/Main.py"
```

## Verified Sample Conversation

This is the confirmed sample interaction observed from the project logic:

```text
User: hello
Bot: Hi there, how can I help you today
User: what is Python
Bot: Python is a high level general purpose programming language.
User: bye
Bot: Goodbye, take care
```

## How It Works

### 1. Knowledge Base

The chatbot uses a built-in knowledge base about:

- Python
- NLP
- machine learning
- deep learning
- chatbot design
- TF-IDF
- cosine similarity

### 2. Preprocessing

The input is normalized by:

- converting text to lowercase
- removing punctuation
- tokenizing the sentence
- applying lemmatization

### 3. Matching

The chatbot uses `TfidfVectorizer` and `cosine_similarity` to compare the input against all knowledge-base sentences and determine the closest match.

### 4. Output Behavior

The bot responds with:

- a greeting if the user says hello or similar
- a farewell message when the user exits
- a relevant knowledge answer when there is a strong match
- a fallback answer if the similarity is too weak

## Troubleshooting

### `ModuleNotFoundError: No module named 'nltk'`

This means the environment you are using does not have the required packages installed.

Use the virtual environment and install dependencies in it:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy RemoteSigned
& "c:\Users\DELL\OneDrive\Desktop\Ai Chat bot\.venv\Scripts\Activate.ps1"
python -m pip install nltk scikit-learn pillow
```

### Import security warning on newer Python versions

On newer Python versions, `nltk` may apply a safer import policy that blocks modules from the current working directory. This project has been adjusted so the script sets the required environment behavior before importing `nltk`.

## Notes

- The project is an educational chatbot example and is not a production-grade conversational AI system.
- The first run may download some NLTK resources like `punkt`, `wordnet`, or `omw-1.4` automatically.
- It is best suited for learning NLP, vector similarity, and basic chatbot design.

## License

This project is provided for educational and learning purposes.

## Author

Created as a simple NLP chatbot demonstration in Python.
