# compare-nlp-models
Comparing how different Language Models and context free embeddings perform on very small amount of labeled training data.



<b>Models to compare:</b><br/>
Baseline:Majority class (always predict majority class)\

FLAIR:
- Glove
- en-twitter (static word embedding)
- Fasttext: en crawl
- Fasttext: news wiki
- ELMO
- Flair-embedding
- Bert base-cased
- BPE - Byte Pair Embedding
- GPT-1

<b>Data sets:</b><br/> 
Hatespeech Detection in Tweets
Automated Hate Speech Detection and the Problem of Offensive Language<br/>
Paper: https://aaai.org/ocs/index.php/ICWSM/ICWSM17/paper/view/15665 <br/>
Data: https://github.com/t-davidson/hate-speech-and-offensive-language/

Sentiment analysis of Business news<br/>
Benchmarks and models for entity-oriented polarity detection <br/>
Paper: http://www.aclweb.org/anthology/N18-3016 <br/>
Dataset: http://puls.cs.helsinki.fi/polarity


Train data sizes:\
0, 100, 200, 500, 1000, 3000, 7000,  18783 (business news articles)\
0, 100, 200, 500, 1000, 3000, 7000,  13718 (hatespeech Tweets)


<b>Baseline</b><br />
I will use predicting always majority class as a baseline, which models should improveover.

For Hatespeech data set, the majority class (1 - offensive language) represents 76 %of samples in test data (0.7596). Predicting always majority gives also f1-score of 0.76, which we will use as a lower bound.

For Business news data set, the majority class is 3 "positive" with 31.7 % of data.This gives f1 baseline of 0.317. Having total of 5 classes in news data, compared to 3 of hatespeech, the news dataset gives harder problem to score numerically high.

<b>Results</b>


![alt text](https://github.com/jannenev/compare-nlp-models/blob/master/images/figure_f1_trainsize_hatespeech_marker.png) <br/>
 F1 per train samples: Hatespeech / Tweets


![alt text](https://github.com/jannenev/compare-nlp-models/blob/master/images/figure_f1_trainsize_news_marker.png) <br/>
F1 per train samples: Business new

