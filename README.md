# Introduction

This repository is for **'You Can't See Their Bias: Exploring Implicit Media Bias in Non-Political News Articles'** paper. We publicly release 1) Implicit Media Bias Dataset (IMBD) and 2) source code of four classifiers for reproducibility.


## 1. IMBD
News articles in the section of information technology and science, which were published in two most-biased Korean news outlets.

- human_evaluated_news_articles_200.csv ( KB)
  - 200 labeled news articles (100 conservative and 100 progressive)
  - columns: `id, date, topic, title, text, news_outlet_label, human_label, objectiveness, fairness, unbiasedness`\
      id - integer (1 to 200) identifier for news articles (same as the annotated label in *K*-means clustering; refer to the paper)\
      news_outlet_label - integer {0: 'consevative', 1: 'progressive'}\
      human_label - integer {0: 'consevative', 1: 'progressive', 2: 'neutral'}\
      objectiveness, fairness, unbiasedness - float (-3.00 to 3.00)

- trained_news_articles_24376.csv ( KB)
  - 24,376 labeled news articles (18,094 conservative and 6,282 progressive)
  - columns: `date, topic, title, text, news_outlet_label`\
      news_outlet_label - integer {0: 'consevative', 1: 'progressive'}


## 2. Source Code of Four Classifiers
Classifiers which are trained/examined with large-scale non-political articles (trained_news_articles_24376.csv), to identify each article's political orientations (news_outlet_label of human_evaluated_news_articles_200.csv).

- requirements.txt

- models/naive_bayes.py

- models/cnn.py

- models/bilstm.py

- models/bert.py


For more details of news outlets and experiment settings, please refer to our paper.
