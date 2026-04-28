# EmoVec-Mal-Malayalam-Embeddings
Custom Malayalam word embeddings and literary novel corpus for emotion detection
# EmoVec-Mal: Malayalam Word Embeddings for Emotion Detection

Custom Word2Vec and FastText embedding models trained on a Malayalam 
literary novel corpus using IndicNLP tokenization, developed for 
emotion detection in Malayalam text.

## Files

| File | Description |
|------|-------------|
| `embeddings/malayalam_word2vec.model` | Word2Vec model trained on Malayalam novels |
| `embeddings/fasttext_model.bin` | FastText model trained on Malayalam novels |
| `corpus/malayalam_novels_corpus.txt` | Raw Malayalam novel text corpus |

## How to Load

```python
from gensim.models import Word2Vec, FastText

# Load Word2Vec
w2v_model = Word2Vec.load("malayalam_word2vec.model")
similar_words = w2v_model.wv.most_similar("സന്തോഷം")  # happiness

# Load FastText  
ft_model = FastText.load("fasttext_model.bin")
vector = ft_model.wv["സങ്കടം"]  # sadness
```

## Training Details

- **Tokenizer:** IndicNLP
- **Language:** Malayalam (Dravidian, agglutinative)
- **Source corpus:** Malayalam literary novels
- **Compared against:** Pre-trained FastText cc.ml.300.bin

## Related Dataset

MalEmo (labeled emotion detection corpus):  
👉 https://github.com/Anujk6/MalEmo-Malayalam-Emotion-Dataset

## Citation

If you use these embeddings, please cite:

Anuja K, Reghu Raj P C, Remesh Babu K R (2026).
EmoVec: Emotion detection in Malayalam using custom word embeddings.
Language Resources and Evaluation.
https://doi.org/10.1007/s10579-025-09892-7

## License
CC BY 4.0 — Free to use with attribution.
