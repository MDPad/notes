---
Theme: "[[Encoding in Machine Learning]]"
---
## TF-IDF (Term Frequency-Inverse Document Frequency)

**TF-IDF** — это статистический метод, используемый для оценки важности слов в текстах в рамках обработки естественного языка (NLP). Этот метод основывается на предположении, что слова, которые часто встречаются в документе, но редко встречаются в других документах, имеют большую информативную ценность для этого документа.

Метод **TF-IDF** состоит из двух частей:

### 1. **Term Frequency (TF)** — частота термина

Это мера того, как часто слово встречается в документе.

Формула:
$$
TF(t, d) = \frac{\text{Число вхождений термина } t \text{ в документ } d}{\text{Общее количество слов в документе } d}
$$

Это простое отношение частоты появления термина в документе к общему числу слов в документе.

### 2. **Inverse Document Frequency (IDF)** — обратная частота документов

Это мера того, насколько редким является слово в корпусе документов.

Формула:
$$
IDF(t, D) = \log \left( \frac{N}{\text{Количество документов, содержащих термин } t} \right)
$$

Где:
- \( N \) — общее количество документов в корпусе.
- Количество документов, содержащих термин \( t \), — число документов, в которых встречается слово.

Важно, что если слово встречается в большинстве документов, его значение **IDF** будет низким, что свидетельствует о низкой информативности.

### 3. Итоговое значение **TF-IDF**

TF-IDF рассчитывается как произведение **TF** и **IDF** для каждого термина:
$$
TF-IDF(t, d, D) = TF(t, d) \times IDF(t, D)
$$

Это значение высокое для термина, который часто встречается в документе, но редко встречается в других документах.

---

### Пример:

Предположим, у нас есть три документа:

- **Документ 1**: "Кошки на дереве"
- **Документ 2**: "Собаки на дереве"
- **Документ 3**: "Кошки и собаки"

#### TF для слова "кошки" в документе 1:
Частота в документе 1: $\frac{1}{4}$  (так как слово "кошки" встречается один раз, а всего слов 4).

#### IDF для слова "кошки":
Количество документов, содержащих слово "кошки": 2 (документ 1 и документ 3).  
Общее количество документов: 3.

$$
IDF(\text{кошки}) = \log \left( \frac{3}{2} \right) \approx 0.176
$$

#### TF-IDF для "кошки" в документе 1:
$$
TF-IDF(\text{кошки, документ 1}) = \frac{1}{4} \times 0.176 = 0.044
$$

---

### Заключение:
Этот процесс применяется для всех терминов в корпусе текста, чтобы оценить, какие слова наиболее важны для конкретных документов. **TF-IDF** помогает выделить значимые слова, которые являются информативными для каждого документа и помогают в таких задачах, как:
- Классификация текста.
- Анализ тональности.
- Поиск информации и другие задачи обработки текста.
