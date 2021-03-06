<a href="http://www.europeana-newspapers.eu/"><img src=http://www.europeana-newspapers.eu/wp-content/uploads/2013/09/europeana_newspapers_forwebsite1.jpg></a> 

### ner-corpora
Named Entity Recognition corpora for Dutch, French, German from [Europeana Newspapers](http://www.europeana-newspapers.eu/named-entity-recognition-for-digitised-newspapers/).

### Introduction

The corpora comprise files divided by language, encoded in the BIO format ([Ramshaw & Marcus, 1995](http://www.aclweb.org/anthology/W/W95/W95-0107.pdf)). The BIO format is a simple, text-based format that divides texts into single tokens per line, and, separated by a whitespace, tags to indicate which ones are named entities. The most commonly used tags are *PER* (person), *LOC* (location) and *ORG* (organization). To indicate named entities that span multiple tokens, the tags have a prefix of either *B-* (begining of named entity) or *I-* (continuation of named entity). *O* tags are used to indicate that the token is not a named entity.

Example:
```
The O
NBA B-ORG
player O
Michael B-PER
Jordan I-PER
is O
from O
the O
United B-LOC
States I-LOC
of I-LOC
America I-LOC
. O
```

### Background

The BIO files in this repository are based on OCRed and manually annotated texts from the following libraries:

* [enp_DE.onb.bio](https://github.com/EuropeanaNewspapers/ner-corpora/tree/master/enp_DE.onb.bio) - newspapers from the [Austrian National Library](http://www.theeuropeanlibrary.org/tel4/newspapers/gallery?provider-id=P01252)
* [enp_DE.lft.bio](https://github.com/EuropeanaNewspapers/ner-corpora/tree/master/enp_DE.lft.bio) - newspapers from the [Dr Friedrich Teßmann Library](http://www.theeuropeanlibrary.org/tel4/newspapers/gallery?provider-id=P02013)
* [enp_DE.sbb.bio](https://github.com/EuropeanaNewspapers/ner-corpora/tree/master/enp_DE.sbb.bio) - newspapers from the [Berlin State Library](http://www.theeuropeanlibrary.org/tel4/newspapers/gallery?provider-id=P01606)
* [enp_FR.bnf.bio](https://github.com/EuropeanaNewspapers/ner-corpora/tree/master/enp_FR.bnf.bio) - newspapers from the [National Library of France](http://www.theeuropeanlibrary.org/tel4/newspapers/gallery?provider-id=P01190)
* [enp_NL.kb.bio](https://github.com/EuropeanaNewspapers/ner-corpora/tree/master/enp_NL.kb.bio) - newspapers from the [National Library of the Netherlands](http://www.theeuropeanlibrary.org/tel4/newspapers/gallery?provider-id=P01350)

For the full data set including the [ALTO](http://www.loc.gov/standards/alto/) OCR files and the binary classifiers derived, please go [here](http://lab.kbresearch.nl/static/html/eunews.html).

### License 

[CC0](https://creativecommons.org/publicdomain/zero/1.0/)

You are free to use this data without restrictions. We're thankful if you give attribution to:  

*Europeana Newspapers NER corpora*   
*https://github.com/EuropeanaNewspapers/ner-corpora/.*  
*Europeana Newspapers Project, 2012-2015.*    
*http://www.europeana-newspapers.eu/.*

### References

* [An Open Corpus for Named Entity Recognition in Historic Newspapers](http://www.lrec-conf.org/proceedings/lrec2016/pdf/110_Paper.pdf)  
Proceedings of the 10th edition of the Language Resources and Evaluation Conference, 23-28 May 2016, Portorož, Slovenia.

### Known issues

The way the above corpora were produced, additional work is required to leverage the full potential of the annotated data for tasks such as evaluation, where gold standard quality is required. Currently, the data still contains many OCR errors, and, due to post-processing, parts of sentences containing a lot of noise have been filtered (i.e. cut). This also makes it difficult to map the annotated texts to the original newspaper articles, and may have negative effects on sentence position as a feature. 

Instructions how to help clean up the data can be found [here](https://github.com/EuropeanaNewspapers/ner-corpora/wiki/Corpus-cleanup).
