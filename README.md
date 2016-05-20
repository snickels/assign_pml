---
title: "Practical Machine Learning Assignment"
author: "Stefan Nickels"
date: "20. May 2016"
output: 
  html_document: 
    number_sections: yes
    toc: yes
---

# Introduction

Background Info:

Tracking device data from six young health participants, performing barbell lifts in five forms:  
* A: exactly according to the specification
* B: throwing the elbows to the front
* C: lifting the dumbbell only halfway
* D: lowering the dumbbell only halfway
* E: throwing the hips to the front (Class E)

Read more: http://groupware.les.inf.puc-rio.br/har#ixzz4962NQyaS

# Load data

```{r load}

library("caret", lib.loc="~/Library/R/3.0/library")
training <- read.csv("data/pml-training.csv", 
                  na.strings = c("", "NA", "#DIV/0!"),
                  stringsAsFactors = TRUE)

testing <- read.csv("data/pml-testing.csv",
                 na.strings = c("", "NA"), 
                 stringsAsFactors = TRUE)
                 
                 
```

# Check and prepare data

```{r clean}                
# proportion of missings
table(round(colSums(is.na(training))/nrow(training)*100))

# delete columns with missings >95
training <- training[ , colSums(is.na(training)) < 0.95]

str(training)
summary(training)


# delete specific colums
# http://stackoverflow.com/questions/36110486/unable-to-delete-columns-in-r

drops <- c('X')
training <- training[ , !(names(training) %in% drops)]


table(trainclean$user_name)

```

```{r building model}
set.seed(12345)
model <- train(classe ~., data = training, method = "glm")
# preprocessing options

# TODO: take care of tights (individuals)
# standardize values (also test set with values from )

```


```{r prediction}


```

<2000 Words, <5 figures

