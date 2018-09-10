## GloVe: Global Vectors for Word Representation (Arabic Model)

|البعد جتا |أقاربها |  الكلمة| 
|----------|--------|--------|
|          |        |  التقوى| 
|0.571273  | الاخلاص  |        |
|0.556925  | الايمان |        |
|0.536685  |الطاعة  |        |
|0.524090  |الورع   |        |
|0.523659  |الاستقامة|        |
|0.512803  |الخشية  |        |
|          |        |  كلب   | 
|0.568289  | حيوان  |        |
|0.547309  | حمار   |        |
|0.519542  |اسد     |        |
|0.498536  |صيد     |        |
|0.482568  | الذئب  |        |


|كبير -> اكبر |  رجل -> رجال | علاقة كلمتين |
| ----------- | -------------|-------------|
| جميل->؟ اجمل |  امراة ->؟ نساء |         | 
| عالي->؟ اعلى |  قول ->؟ اقوال |         | 
| رائع->؟ اروع |                 |         | 


We provide an implementation of the GloVe model for learning word representations, and describe how to download web-dataset vectors or train your own. See the [paper](http://nlp.stanford.edu/pubs/glove.pdf) for more information on glove vectors.

## Download pre-trained word vectors
The links below contain word vectors obtained from the respective corpora. If you want word vectors trained on other data sets, feel free to edit <a href="https://github.com/tarekeldeeb/GloVe-Arabic/blob/master/arabic_corpus/make_corpus.sh"> this script</a>. Pre-trained word vectors are made available under the <a href="https://github.com/ojuba-org/waqf/tree/master/2.0">Waqf v2.0 Public License</a>. 
<div class="entry">
<ul style="padding-left:0px; margin-top:0px; margin-bottom:0px">
  <li> Arabic Corpus (1.75B tokens, 1.5M vocab, 256d vectors): <a href="https://archive.org/details/arabic_corpus">Download Archive</a> </li>
</ul>
</div>

## Train word vectors on a new corpus

<img src="https://travis-ci.org/stanfordnlp/GloVe.svg?branch=master"></img>

If the web datasets above don't match the semantics of your end use case, you can train word vectors on your own corpus.

    $ git clone https://github.com/tarekeldeeb/GloVe-Arabic
    $ cd GloVe-Arabic && make
    $ ./demo.sh

The demo.sh script downloads a small corpus, consisting of the first 100M characters of Wikipedia. It collects unigram counts, constructs and shuffles cooccurrence data, and trains a simple version of the GloVe model. It also runs a word analogy evaluation script in python to verify word vector quality. More details about training on your own corpus can be found by reading [demo.sh](https://github.com/tarekeldeeb/GloVe-Arabic/blob/master/demo.sh) or the [src/README.md](https://github.com/tarekeldeeb/GloVe-Arabic/tree/master/src)

### License
All work contained in this package is licensed under the Apache License, Version 2.0. See the include LICENSE file.
