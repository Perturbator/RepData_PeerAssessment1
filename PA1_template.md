# Reproducible Research: Peer Assessment 1
John Bobo  


## Loading and preprocessing the data
First we load the data:

```r
amd = read.csv("/Users/johnbobo/data_science/datasciencecoursera/reproducible_research/RepData_PeerAssessment1/activity.csv")
```

***

## What is mean total number of steps taken per day?
We use dplyr to group by date and then find the average steps per day

```r
library(dplyr)
```

```
## 
## Attaching package: 'dplyr'
## 
## The following object is masked from 'package:stats':
## 
##     filter
## 
## The following objects are masked from 'package:base':
## 
##     intersect, setdiff, setequal, union
```

```r
amd_by_day <-amd %>%
            group_by(date) %>%
                mutate(stepsPerDay = sum(steps))
mean(amd_by_day$stepsPerDay, na.rm = TRUE)
```

```
## [1] 10766.19
```
**Mean steps taken per day**: 10766

***

## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
