# ML_challenge

It's a machine learning programming challenge to build and train a classifier given a labeled dataset and then use it to infer the labels of a given unlabeled evaluation dataset. The goal is to achieve a higher accuracy of your model.

## Dataset

It's a dataset with 3 labels and 10 features. Train with [TrainOnMe.csv](https://github.com/jhan15/ML_challenge/blob/master/Dataset/TrainOnMe.csv), 
and test your algorithm with [EvaluateOnMe.csv](https://github.com/jhan15/ML_challenge/blob/master/Dataset/EvaluateOnMe.csv), which is unlabeled.

## Pre-processing

### Data cleaning

After data cleaning, I got a distribution as following.

| Class         | Samples       |      %|
| ------------- |:-------------:| -----:|
| Atsuto        | 295           |   29.7|
| Bob           | 516           |   51.9|
| Jörg          | 183           |   18.4|

### Transform data to Gaussian-like

![Picture1](https://user-images.githubusercontent.com/62132206/120284625-ba4a3e00-c2bc-11eb-8e59-916d5b8a5b4e.png)

### Feature engineering

![cor](https://user-images.githubusercontent.com/62132206/117428710-9c402680-af26-11eb-97b5-bd7953c1a57e.png)

## Model

I used a voting classifier based on three classifiers, which are shown in below tree.

```bash
Voting classifier
├── classifier 1: random forest
├── classifier 2: extremely randomized tree
└── classifier 3: gradient tree boosting
```

## Result

My result on [EvaluateOnMe.csv](https://github.com/jhan15/ML_challenge/blob/master/Dataset/EvaluateOnMe.csv) is listed in [106716.txt](https://github.com/jhan15/ML_challenge/blob/master/Result/106716.txt). The true labels are listed in [true_labels.csv](https://github.com/jhan15/ML_challenge/blob/master/Result/true_labels.csv). However, you shouldn't see the file before you get your results. You can refer to [TopSecret.ipynb](https://github.com/jhan15/ML_challenge/blob/master/Result/TopSecret.ipynb) for details about how the dataset is generated. According to the file, the theoretical maximum accuracy you can achieve is 93.85%. I achieved an accuracy of 85.6%.
