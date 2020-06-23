# compare-nlp-models
Comparing how different Language Models and context free embeddings perform on very small amount of labeled training data.



<b>Models to compare:</b><br/>
Baseline:Majority class (always predict majority class)\

FLAIR:
- Glove
- en-twitter (static word embedding)
- Fasttext: en crawl
- Fasttext: news wiki
- ELMO- Flair-embedding
- Bert base-uncased
- BPE - Byte Pair Embedding
- GPT-1

<b>Data sets:</b><br/> 
Hatespeech Detection in Tweets

Automated Hate Speech Detection and the Problem of Offensive Language<br/>
Paper: https://aaai.org/ocs/index.php/ICWSM/ICWSM17/paper/view/15665 <br/>
Data: https://github.com/t-davidson/hate-speech-and-offensive-language/

Sentiment analysis of Business news<br/>
Benchmarks and models for entity-oriented polarity detection, by Pivovarova L. et al. <br/>
http://www.aclweb.org/anthology/N18-3016 <br/>
Dataset: http://puls.cs.helsinki.fi/polarity


Train data sizes:\
0, 100, 200, 500, 1000, 3000, 7000,  18783 (business news articles)\
0, 100, 200, 500, 1000, 3000, 7000,  13718 (hatespeech Tweets)


<b>Results</b>


![alt text](https://github.com/jannenev/compare-nlp-models/blob/master/images/figure_f1_trainsize_hatespeech_marker.png) <br/>
 F1 per train samples: Hatespeech / Tweets


![alt text](https://github.com/jannenev/compare-nlp-models/blob/master/images/figure_f1_trainsize_news_marker.png) <br/>
F1 per train samples: Business new

