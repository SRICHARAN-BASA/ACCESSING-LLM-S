# 🚀 Accessing Groq LLMs using API Key

This project demonstrates how to access **Groq LLMs** using Python and an API key, and generate responses using a simple prompt.

---

## 📌 Features

* Connect to Groq API
* Use environment variables for security
* Generate responses from LLM (Llama 3 model)
* Simple and beginner-friendly setup

---

## 🛠️ Tech Stack

* Python
* Groq API
* dotenv (for environment variables)

---

## 📂 Project Structure

```
ACCESSING_LLM/
│── venv/                # Virtual environment (ignored)
│── .env                 # API key (ignored)
│── .gitignore
│── Accessing_LLM_API.ipynb
```

---

## 🔐 Setup Instructions

### 1️⃣ Clone the repository

```
git clone https://github.com/your-username/your-repo.git
cd ACCESSING_LLM
```

---

### 2️⃣ Create virtual environment

```
python -m venv venv
```

Activate it:

* Windows:

```
venv\Scripts\activate
```

---

### 3️⃣ Install dependencies

```
pip install groq python-dotenv
```

---

### 4️⃣ Create `.env` file

Create a file named `.env` in root:

```
GROQ_API_KEY=your_api_key_here
```

⚠️ Never share this key publicly

---

### 5️⃣ Run the code

Open the notebook:

```
Accessing_LLM_API.ipynb
```

Run all cells to get output from Groq LLM.

---

## 🧠 Sample Code

```python
import os
from groq import Groq
from dotenv import load_dotenv

load_dotenv()

api_key = os.getenv("GROQ_API_KEY")

client = Groq(api_key=api_key)

completion = client.chat.completions.create(
    model="llama-3.3-70b-versatile",
    messages=[
        {"role": "user", "content": "What is Python?"}
    ]
)

print(completion.choices[0].message.content)
```

---

## 🚨 Important Notes

* Add `.env` and `venv/` to `.gitignore`
* Never push API keys to GitHub
* Regenerate key if exposed

---

## 📌 Output Example

The model will return a natural language response explaining the prompt.

---

