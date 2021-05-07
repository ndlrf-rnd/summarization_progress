# summarization_progress
Abstractive and extractive summarization models for Russian language.
For baseline we take models and datasets from "summarus" repository made by Gusev Ilya
Ultimate goal: make abstractive summarization without hallucinations (more like extractive)
### useful links:
* https://towardsdatascience.com/understanding-automatic-text-summarization-1-extractive-methods-8eb512b21ecc
* https://towardsdatascience.com/understanding-automatic-text-summarization-2-abstractive-methods-7099fa8656fe

# Abstractive summarization

## Baseline taken from https://github.com/IlyaGusev/summarus
## our models:
* gazeta_mT5_large: model ready, code in progress

## our datasets:
* handcrafted_proza: preprocess in progress

### Russian summarization datasets:
* RIA train/val/test: https://www.dropbox.com/s/rermx1r8lx9u7nl/ria.tar.gz
* Lenta train/val/test: https://www.dropbox.com/s/v9i2nh12a4deuqj/lenta.tar.gz
* Gazeta train/val/test: https://www.dropbox.com/s/cmpfvzxdknkeal4/gazeta_jsonl.tar.gz

## Links to BASELINE models and prediction scripts can be found on https://github.com/IlyaGusev/summarus/blob/master/README.md#summarization---gazeta-russian-news-dataset

### Results on gazeta test:

| Model                     | R-1-f | R-2-f | R-L-f | METEOR | BLEU |
|:--------------------------|:------|:------|:------|:-------|:-----|
| gazeta_pgn_7kk            | 29.4  | 12.7  | 24.6  | 21.2   | 38.8 |
| gazeta_pgn_7kk_cov        | 29.8  | 12.8  | 25.4  | 22.1   | 40.8 |
| gazeta_pgn_25kk           | 29.6  | 12.8  | 24.6  | 21.5   | 39   |
| gazeta_pgn_words_13kk     | 29.4  | 12.6  | 24.4  | 20.9   | 35.9 |
| gazeta_summarunner_3kk    | 31.6  | 13.7  | 27.1  | 26.0   | 46.3 |
| gazeta_mbart              | 32.6  | 14.6  | 28.2  | 25.7   | 49.8 |
| gazeta_mbart_lower        | 32.7  | 14.7  | 28.3  | 25.8   | 48.7 |
| gazeta_mt5                | -     | -     | -     | -      | -    |
---------------------------------------------------------------------
# Extractive summarization

## Approach: https://arxiv.org/pdf/1906.04165.pdf
## Library: https://pypi.org/project/bert-extractive-summarizer/

## Target literature: 
* "economic" - https://rusneb.ru/catalog/000199_000009_004090560/ 
* "kolobok" - https://nukadeti.ru/skazki/kolobok
### Full text results:
#### "economic" target book
* https://drive.google.com/file/d/119vyOYTdgRgxe5vtp4BHx6qVV6PL8eyr/view?usp=sharing - LABSE
* https://drive.google.com/file/d/1cNuVTOpwtvVNCE1nyHAmDwVc2SeKE5Mu/view?usp=sharing - MBART
* https://drive.google.com/file/d/1JZUQd5AAWxUZywXpRBAcsS5DpmI4FSTF/view?usp=sharing - ROBERTA
* https://drive.google.com/file/d/1w2_3Yet_mp8ZVPoUcn9cuwrCSYzE-4Sd/view?usp=sharing - RUBERT

#### "kolobok" target book
* https://drive.google.com/file/d/1rkNn-3DDeQdWDhdLPsaR8qEWBgbss3Yj/view?usp=sharing - LABSE
* https://drive.google.com/file/d/1ToKoaUlhfb2rQzWmikQLJeqNBieguSe2/view?usp=sharing - MBART
* https://drive.google.com/file/d/1_FZSi21bjFYslM5wRVFk72m_YreRO1Cm/view?usp=sharing - ROBERTA
* https://drive.google.com/file/d/1GELgHVS_4OmGzKperSfLpZZG75Y_Otqd/view?usp=sharing - RUBERT

### in my opinion, LABSE is the best
