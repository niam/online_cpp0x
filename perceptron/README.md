##perceptron_binary.cpp
impelements a 2-class margin perceptron in one file. 
mknews20.cpp shuffles data from the news20.binary dataset and creates news20.train and news20.test.

###Build
Requires c++0x features with "Range-based for", which gcc 4.6.0 or higher supports. Tested on gcc 4.6.0. 

```
% g++ -std=c++0x -O2 perceptron_binary.cpp -o perceptron_binary
% g++ -O2 mknews20.cpp -o mknews20
```

###Usage

    ./perceptron_binary trainingfile testfile [iteration] [margin] [bias]
Defaults are: iteration=1, margin=0.0, bias=0.0

###Example
```
% wget http://www.csie.ntu.edu.tw/~cjlin/libsvmtools/datasets/binary/news20.binary.bz2
% bzip2 -dc news20.binary.bz2|./mknews20
% ./perceptron_binary news20.train news20.test 10 0.6
Accuracy: 4819/4996=0.964572
Zerofication rate: 334121/1355194=0.246548
```
"Accuracy" = # of correct answers / # of data.
"Zerofication rate" = # of zero features / # of all the features.

##References
 - LIBSVM Data: Classification (Binary Class) http://www.csie.ntu.edu.tw/~cjlin/libsvmtools/datasets/binary.html
 - oll http://code.google.com/p/oll/

