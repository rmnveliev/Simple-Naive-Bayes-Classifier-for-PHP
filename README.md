# Simple NaiveBayesClassifier for PHP

This project is somewhat a fork of a Ruby implementation of Naive Bayes Classifier <https://github.com/alexandru/stuff-classifier>. There is a blog posts <http://bionicspirit.com/blog/2012/02/09/howto-build-naive-bayes-classifier.html> finely written and simple in its algorithm which I'm sure just about anyone can implement in any programming language.

The project is implemented in PHP in its simplest form. Fork it and play with the codes.
Forked from https://github.com/tistaharahap/Simple-Naive-Bayes-Classifier-for-PHP

Major redesign with the codes to only use Redis as store. Very impressive benchmarks.
- Redis using php-redis extension <https://github.com/nicolasff/phpredis>


## Changelist

[28 November 2018]
Added redis storage interface, more specific logic for topface....

[18 October 2012]
Added offset/row to classify method and also deTrain method to tackle data updates if applicable.

[14 October 2012]
Optimization - Classify method and Redis store are updated to do calculations after all the data is acquired first to speed up results.


## How To Use/Test

Run the index.php file on command line, any arguments passed after the index.php file will be treated as keywords.

```bash
$ php index.php technology apple mobile
```

## Performance

Very high performance by implementing the store with Redis. Using hashmaps and namespacing to minimize classifying time.

Hardware:
- Macbook Air Late 2011
- Intel Core i5 1.7 GHz
- 4 GB DDR3 Memory
- 128 GB SSD

Datasets:
- 1,212 Sets
- 319,384 KeywordSets

Classifier:
- 1 word: pizza => 0.01428 seconds
- 2 words: pizza pasta => 0.02171 seconds
- 3 words: pizza pasta meatball => 0.04062 seconds


## Contributors

- glenscott - https://github.com/glenscott
- ZaKull - https://github.com/ZaKull


The MIT License (MIT)

Copyright (c) 2012 Batista Harahap

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.


[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/tistaharahap/simple-naive-bayes-classifier-for-php/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

