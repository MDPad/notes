---
Theme: "[[ML]]"
---
Encoding is the transformation of one type of data into another. It is necessary to prepare data for training a model. In particular, we transform **categorical, non-numeric data**, such as text and categories, into **numerical representations**. This step is essential for compatibility with machine learning algorithms.

## Steps of Encoding

1. **Prepare the Text**
   - Remove stop words
   - Eliminate low-value words (such as prepositions)
   - Apply normalization (e.g., use a unified format for the entire text, such as converting all words to lowercase)
2. **Tokenization**
   - Divide the text into tokens, which can represent full words or meaningful parts of words, such as lemmas (a process known as **lemmatization**).
3. **Transform Text Data into Numeric Values**
   - Use methods such as **One-Hot Encoding**, **Label Encoding**, or other appropriate techniques.

## Types of Encoding

1. [[One-Hot Encoding]]
2. [[Label Encoding]]
3. Ordinal Encoding
4. Count Encoding
5. Target Encoding
6. Leave-One-Out Encoding
7. CatBoost Encoding
8. [[TF-IDF]]
