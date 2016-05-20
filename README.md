---
title: "Practical Machine Learning Assignment"
author: "Stefan Nickels"
date: "20. May 2016"
output: html_document
---

# Introduction

# Load and prepare data

```{r load}
train <- read.csv("data/pml-training.csv", 
                  na.strings = c("", "NA", "#DIV/0!"),
                  stringsAsFactors = FALSE)

test <- read.csv("data/pml-testing.csv",
                 na.strings = c("", "NA"), 
                 stringsAsFactors = FALSE)
# check

str(train)

# proportion of missings
table(round(colSums(is.na(train))/nrow(train)*100), digits=1)

# delete columns with missings >95

colSums(is.na(train))

table(train$skewness_yaw_dumbbell)
summary(train$kurtosis_roll_arm)
str(train$kurtosis_roll_arm)

kurtosis_roll_arm
sum(is.na(train$kurtosis_roll_belt))
sum(is.na(train$max_roll_belt))
table(train$max_roll_belt)
dim(train)


# train[ , colSums(is.na(train)) < 0.95 * nrow(train)]

```

```{r clean}
str(train)
summary(train)
table(train$skewness_yaw_belt)


str(test)
summary(test)

# TODO: clean all variables detected as character (assuming values mixed with error codes)
# TODO: delete useless variables in
# TODO: delete all variables with mostly missing
# TODO: delete all variables with only missings in test data set
# TODO: apply same to test data if similar problems
```



<2000 Words, <5 figures

