# Contributing to HSK Vocabulary 3.0 — Spanish 🇪🇸

First off, thank you for considering contributing! It's people like you who make this a great resource for the Spanish-speaking community.

## 🛠️ How Can I Contribute?

### Reporting Errors
If you find a mistake in a translation, Pinyin, or a Hanzi character, please [open an Issue](https://github.com/nar-ran/hsk-vocab-es/issues).

### Improving Data
You can suggest better example sentences or more precise notes via Pull Requests.

### Adding New Levels
Before starting work on HSK 2 or higher, please open an Issue to coordinate with the maintainers.

## 📏 Contribution Guidelines

To keep the dataset clean and functional, please follow these rules:

1.  **Validate against Schema:** All JSON changes **must** pass the `hsk-schema.json` validation.
2.  **Character Encoding:** Always save files in **UTF-8**.
3.  **Consistency:** 
    * Use neutral Spanish.
    * Examples must follow the format: `Hanzi (Pinyin) - Translation.`
4.  **Unique IDs:** Do not reuse or change existing IDs (e.g., `hsk1-word-0001`) as it might break third-party apps.

## 🚀 Development Workflow

1.  **Fork** the repository.
2.  **Create a branch** (`git checkout -b feature/amazing-feature`).
3.  **Commit your changes** (`git commit -m 'fix: correct pinyin for word X'`).
4.  **Push to the branch** (`git push origin feature/amazing-feature`).
5.  **Open a Pull Request**.

---
*By contributing, you agree that your contributions will be licensed under the project's MIT License.*