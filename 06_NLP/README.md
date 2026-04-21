# Natural Language Processing

NLP enables machines to understand, process, and generate human language. It underpins search engines, chatbots, document AI, summarization, sentiment analysis, and the LLM systems covered in section 09.

---

## Learning Steps

### 1. Text Preprocessing
- Tokenization, stopword removal, stemming, lemmatization
- Regular expressions for text cleaning
- Text normalization and encoding

### 2. Classical NLP
- Bag of Words (BoW), TF-IDF
- N-grams, feature extraction
- Named Entity Recognition (NER)
- Part-of-Speech (POS) tagging, dependency parsing

### 3. Word Embeddings
- Word2Vec, GloVe, FastText
- Understanding semantic similarity and vector space

### 4. Sequence Models
- RNNs, LSTMs, GRUs for text (see section 05)
- Encoder-Decoder architecture, seq2seq, attention mechanism

### 5. Transformers & BERT
- Transformer architecture (self-attention, multi-head attention)
- BERT, RoBERTa, DistilBERT — fine-tuning for classification/NER
- Hugging Face `transformers` library

### 6. Large Language Models (LLMs)
- GPT family, instruction tuning, RLHF
- Prompt engineering, few-shot, zero-shot
- Connects directly to section 09 (ICT Automation / AI Engineering)

### 7. Applied NLP Tasks
- Text classification, sentiment analysis
- Question answering, summarization
- Information extraction, document understanding
- Semantic search with vector databases

---

## Libraries & Tools

| Tool | Use Case |
|------|----------|
| spaCy | Industrial-strength NLP pipeline |
| NLTK | Classic NLP, tokenization, corpora |
| Hugging Face Transformers | Pre-trained models, fine-tuning |
| Hugging Face Datasets | NLP benchmark datasets |
| Gensim | Word embeddings, topic modeling (LDA) |
| TextBlob | Lightweight sentiment and parsing |
| LangChain / LlamaIndex | LLM orchestration (see section 09) |

---

## PDF Resources

* [spaCy Cheat Sheet](./spaCy_Cheat_Sheet_final.pdf)

---

## Learning Resources

- [Hugging Face NLP Course](https://huggingface.co/learn/nlp-course/chapter1/1) — best free NLP course
- [fast.ai NLP](https://www.fast.ai/)
- [Stanford CS224N: NLP with Deep Learning](https://web.stanford.edu/class/cs224n/)
- [Kaggle: Natural Language Processing](https://www.kaggle.com/learn/natural-language-processing)
