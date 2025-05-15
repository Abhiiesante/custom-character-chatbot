# 🤖 Custom Character Chatbot

A custom chatbot built using OpenAI's language model and a dataset of character descriptions from film, television, and theater. This project showcases how embedding-based similarity search and custom prompts can dramatically improve chatbot performance in niche domains.

This project was built **without high-level frameworks** (like LangChain) to demonstrate the inner workings of chatbot logic using just `pandas`, `sentence-transformers`, and `OpenAI API`.

---

## 📁 Dataset: `character_descriptions.csv`

Each row includes:
- `Name`: Character name
- `Description`: Personality traits and background
- `Medium`: Film, TV, Theater, etc.
- `Setting`: Where the story takes place

Example snippet:
```

Name: Alex Ryder
Description: A brave teenage spy with a strong sense of justice.
Medium: Television
Setting: Modern London

````

---

## ⚙️ Features

- ✅ Embedding-based similarity search using `sentence-transformers`
- ✅ Semantic match between user query and character profiles
- ✅ Custom prompts to guide the language model
- ✅ Comparison with basic (no-context) prompt
- ✅ Interactive querying
- ✅ Demonstration of how prompt customization improves performance

---

## 💻 Installation

### Step 1: Clone the Repository

```bash
git clone https://github.com/your-username/custom-character-chatbot.git
cd custom-character-chatbot
````

### Step 2: Install Requirements

Ensure you're in a Python 3.9+ environment:

```bash
pip install -r requirements.txt
```

### `requirements.txt` includes:

```
openai
pandas
numpy
scikit-learn
sentence-transformers
```

---

## 🚀 How It Works

### 🔍 Embedding + Similarity Search

* Generate embeddings for all characters using `SentenceTransformer`.
* Generate an embedding for the user question.
* Use cosine similarity to find the top `k` most relevant character entries.
* Send the selected context along with the user query to the OpenAI model.

### 🧠 Prompt Structure

```
You are a helpful assistant. Use the context below to answer the user question.

Context:
<Character Description 1>
<Character Description 2>
...

Question:
<SOME USER QUESTION>
```

---

## 📊 Performance Demonstration

We ask **2 questions** with both **basic prompts** and **custom prompts**:

#### ❓ Question 1: *Suggest a brave character from a fantasy world*

* **Basic Answer:**
  “Brave characters are common in fantasy. Look for warriors or heroes.”

* **Custom Answer:**
  “Based on the context, *Kael the Dragonslayer* is a brave knight from a mythical kingdom who defends villages from magical threats.”

#### ❓ Question 2: *Find a detective character from a modern city setting*

* **Basic Answer:**
  “Detective stories are often set in cities with crime investigations.”

* **Custom Answer:**
  “According to the dataset, *Detective Marla Gray* works in modern-day Chicago solving cybercrime cases with advanced tech skills.”

✅ **Conclusion:** Custom prompts powered by dataset context deliver more precise and helpful answers.

---

## 🧪 Run the Notebook

Open and run `character_bot.ipynb` step-by-step to:

* Load and embed data
* Ask interactive questions
* Compare custom vs basic responses

---

## 📝 Future Improvements

* 🔍 Add user interface (Gradio or Streamlit)
* 📚 Expand dataset with more diverse characters
* 🧠 Fine-tune on custom data for better performance

---

## 📜 License

This project is open-source under the MIT License.

---

## 🤝 Credits

Built as part of a **Custom Chatbot Challenge** to demonstrate prompt engineering, vector similarity search, and OpenAI API usage from scratch.

---

## 🙌 Support

If you found this helpful, feel free to ⭐ star the repo and share your feedback!

```

Let me know if you’d like a `requirements.txt` snippet or a badge for the top of the README.
```
