---
title: "Practical Machine Learning Assignment"
author: "Stefan Nickels"
date: "20. July 2015"
output: html_document
---

# Introduction

# Load and prepare data

<<<<<<< HEAD
```{r load}
train <- read.csv("data/pml-training.csv", 
                  na.strings = "",
                  stringsAsFactors = FALSE)

test <- read.csv("data/pml-testing.csv",
                 na.strings = "",
                 stringsAsFactors = FALSE)
# check

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
=======
hallo rstudio


ok, hallo github
>>>>>>> c5eff8849792f96f0fa2c5d672ab795ad63a4f35
