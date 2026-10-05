# Semantic Search Practice

Сравнительное исследование двух моделей эмбеддингов для семантического поиска по исходному коду.

## Описание

В работе сравниваются две предобученные модели эмбеддингов:
- `paraphrase-multilingual-MiniLM-L12-v2`
- `paraphrase-multilingual-mpnet-base-v2`

Цель — определить, какая модель лучше находит релевантные фрагменты кода по текстовому запросу.

## Данные

- `code_corpus.json` — 200 фрагментов Python-кода с описаниями и категориями
- `eval_questions.json` — 25 тестовых вопросов с правильными ответами
- `categories.json` — список тематических категорий

## Что внутри

| Файл | Описание |
|------|----------|
| `semantic_search.ipynb` | Jupyter Notebook с кодом |
| `final_conclusion.txt` | Финальный вывод |
| `precision_results.csv` | Таблица Precision@3 |
| `tsne_minilm.png` | График t-SNE |

## Результаты

| Модель | Precision@3 |
|--------|-------------|
| MiniLM | 80% |
| mpnet | 80% |

Обе модели показали одинаковое качество. Рекомендуется **MiniLM** — она работает в 2 раза быстрее.

## Как запустить

```bash
pip install sentence-transformers numpy pandas matplotlib scikit-learn
jupyter notebook semantic_search.ipynb
```

## Автор

Комарова Виктория Валерьевна  
Группа БВТ2502  
МТУСИ, 2026
