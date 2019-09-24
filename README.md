# Application - Tree stream mining algorithm with Chernoff-bound 

## Guide

This application is the implementation of Tree stream mining algorithm with Chernoff-bound  which is published in Tree stream mining algorithm with Chernoff-bound and standard deviation approach for big data stream, Journal of Big Data, volume 6, Article number: 58 (2019), ISSN: 2196-1115.

### Base Framework
MOA (Massive Online Analysis) it the base framework that we used for ch.
* [Massive Online Analysis - Home Page](https://moa.cms.waikato.ac.nz/) - Massive Online Analysis - Home Page.
* [Massive Online Analysis - Github Page](https://github.com/Waikato/moa) - Massive Online Analysis - Github Page

### Datasets
MOA (Massive Online Analysis) it the base framework that we used for ch.
* [Airline Dataset](https://drive.google.com/drive/folders/0B6arI8oRbapXZDVVbmE3WUc1SWs?usp=sharing) - Airline Dataset (9 GB).
* [Traffic Dataset](https://drive.google.com/open?id=0B6arI8oRbapXZl82bDNfazNNOUE) - Traffic Dataset (25 GB)

### Application
Please download this application
* [moa-ch.jar](https://drive.google.com/file/d/1IrMA1-yy1QJVlXHa7x66h4jUqFW-6INj/view?usp=sharing) - Application jar file (25 MB).

### Script to run LearnModel FIMT-DD-ch
```
java -cp moa-ch.jar moa.DoTask "LearnModelRegression -l trees.FIMTDD -s (ArffFileStream -f (traffic.arff)) -O (ch-traffic-demand.moa) -m 100000000"
```
### Script to test EvaluateModel FIMT-DD-ch
```
java -cp moa-ch.jar moa.DoTask "EvaluateModelRegression -m file:ch-traffic-demand.moa -s (ArffFileStream -f (traffic.arff)) -i 100000"
```

### Parameters in LearnModelRegression
```
-m : max instance
-s : stream file to learn by the model ( you can change this file as data training forthe model)
-O : save the model
```

### Parameters in EvaluateModelRegression
```
-m : load model file
-s : stream file to learn by the model ( you can change this file to test the model)
-i : amount of instances to be tested
```
