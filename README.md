## LVDS2019 - NLP Sentiment Analysis

This repository contains my attempt to solve [Sentiment Analysis](https://en.wikipedia.org/wiki/Sentiment_analysis) task on [Movie reviews dataset 2004](http://www.cs.cornell.edu/people/pabo/movie-review-data/) as part of LVDS2019 Summer School NLP Course.


### How to reproduce

**Target dataset**

1. Run `data_extraction.ipynb` to download and extract dataset. `data.csv` is now in this directory.
2. Run `data_prep.ipynb`. `clean_data.csv` is now in this directory.
3. Run `train_data_only.ipynb`. Best accuracy without the extraneous data is **0.8665**.

**Data enhancement**

1. Run steps 1-2 from previous algorithm
2. Download and extract [Large Moview Review Dataset](https://ai.stanford.edu/~amaas/data/sentiment/)
3. Run `imdb_extract.ipynb`. `imdb.csv` is now in this directory.
4. Run `imdb_prep.ipynb`. `clean_imdb.csv` is created.
5. Run `train_imdb.ipynb`. Best 5-fold accuracy with data enhancement is **0.8965**.

**Data enhancement + RNN with GLoVE embedding**

1. Run steps 1-4 from previous algorithm
2. Download and extract `glove.6B.zip` from [Stanford NLP page](https://nlp.stanford.edu/projects/glove/).
3. Run `train_imdb_rnn50.ipynb` and `train_imdb_rnn200.ipynb`. Best 5-fold accuracy with data enhancement is **0.86**.

### References

* Pang B., Lee L. 2002. [Thumbs up?: sentiment classification using machine learning techniques](http://www.cs.cornell.edu/home/llee/papers/sentiment.pdf)
* Vryniotis V. 2013. [The importance of Neutral Class in Sentiment Analysis](http://blog.datumbox.com/the-importance-of-neutral-class-in-sentiment-analysis/)
