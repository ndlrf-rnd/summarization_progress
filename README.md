# summarization_progress
Abstractive and extractive summarization models for Russian language.
For baseline we take models and datasets from "summarus" repository made by Gusev Ilya


# Baseline taken from https://github.com/IlyaGusev/summarus

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
