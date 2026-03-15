# HSK Vocabulary 3.0 — Spanish 🇪🇸 ![Status](https://img.shields.io/badge/Status-In_Progress-orange)

![JSON](https://img.shields.io/badge/JSON-000000?style=for-the-badge&logo=json&logoColor=white)
![HSK 1](https://img.shields.io/badge/HSK_1-brightgreen?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

Open source JSON library of the official HSK 3.0 vocabulary translated into Spanish.

This project provides a structured, developer-friendly dataset of HSK vocabulary, designed for apps, websites, research, and educational tools.

---

## 📑 Table of Contents

* [Features](#-features)
* [Structure](#-structure)
* [Examples](#-examples)  
  * [Characters](#-characters)
  * [Words](#-words)
* [Repository Structure](#-repository-structure)
* [Purpose](#-purpose)
* [Usage](#-example-usage)
* [Contributing](#-contributing)
* [License](#-license)
* [Status](#-status)
* [Sources](#-sources)

---

## ✨ Features

* Based on official HSK 3.0 vocabulary lists.
* **Multi-word support:** Translations stored as arrays for better precision.
* **Structured Examples:** Hanzi, Pinyin, and Spanish separated into objects.
* Stable unique IDs for every entry.
* Characters and words separated.
* JSON Schema included for data validation.
* Open source (MIT license).
* Easy integration into any programming language

---

## 📦 Structure

Each level file follows this structure:

```json
{
  "schema": "hsk-vocab-1.0",
  "version": "3.0",
  "level": 1,
  "language": "es",
  "source": "HSK 3.0 Official Vocabulary List",
  "generated_at": "2026",

  "counts": {
    "words": 500,
    "characters": 300
  },

  "characters": [],
  "words": []
}
```

---
## 🧪 Examples

### 🔤 Characters

Example:

```json
{
  "id": "hsk1-char-0001",
  "hanzi": "爱",
  "pinyin": "ài",
  "translation": ["amar", "querer"],
  "type": "carácter",
  "example": {
    "hanzi": "我爱我的家",
    "pinyin": "Wǒ ài wǒ de jiā",
    "translation": "Amo mi hogar."
  },
  "notes": "Puede funcionar como verbo o sustantivo."
}
```

---

### 🧩 Words

Example:

```json
{
  "id": "hsk1-word-0001",
  "hanzi": "爱好",
  "pinyin": "àihào",
  "translation": ["hobby", "afición", "interés"],
  "type": "palabra",
  "characters": ["爱", "好"],
  "example": {
    "hanzi": "我的爱好 es 音乐",
    "pinyin": "Wǒ de àihào shì yīnyuè",
    "translation": "Mi hobby es la música."
  },
  "notes": "Se usa para hablar de intereses personales."
}
```

---

## 📁 Repository Structure

```
data/
  hsk1.json

schema.json

README.md
CONTRIBUTING.md
LICENSE
```

Future versions will include additional levels:

```
data/
  hsk1.json
  hsk2.json
  hsk3.json
```

---

## 🎯 Purpose

This project exists to provide a high-quality, open, and structured HSK vocabulary dataset in Spanish.

It is especially useful for:

* App developers
* Students
* Teachers
* Researchers
* Language learning tools

---

## 🔗 Example usage

JavaScript:

```javascript
import vocab from "./data/hsk1.json";

// Accessing translations (Array)
console.log(vocab.words[0].translation.join(", ")); 

// Accessing structured examples
const example = vocab.words[0].example;
console.log(`${example.hanzi} - ${example.translation}`);
```

Python:

```python
import json

with open("data/hsk1.json", encoding="utf-8") as f:
    data = json.load(f)

# Get the first translation of a word
print(data["words"][0]["translation"][0])

# Get example pinyin
print(data["words"][0]["example"]["pinyin"])
```

---

## 🤝 Contributing

Contributions are welcome! Whether it's fixing a translation or improving an example, your help is appreciated.

Please read our [Contributing Guidelines](./CONTRIBUTING.md) before submitting a Pull Request to ensure data integrity and schema compliance.

---

## 📜 License

MIT License

You are free to use this project for personal, educational, or commercial purposes.

---

## ❤️ Motivation

There is currently no complete HSK 3.0 vocabulary dataset in Spanish.

This project aims to solve that by providing a structured dataset designed for modern software development.

---

## 🚀 Status

HSK 1: Completed structure & Data.
HSK 2-9: In progress.

Future updates will include all HSK 3.0 levels.

---

## 📚 Sources

This project is supported by the following open data sources:

* **[vocabulary_band1.pdf](https://www.chinaeducenter.com/cecdl/vocabulary_band1.pdf)**: Official CLEC standard.
* **[elkmovie/hsk30](https://github.com/elkmovie/hsk30)**: Technical base for the character and word lists (MIT License).
