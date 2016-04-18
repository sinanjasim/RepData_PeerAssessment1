# Reproducible Research: Peer Assessment 1


## Loading and preprocessing the data


```r
Activity <- read.csv ("~/Desktop/RepData_PeerAssessment1/Activity.csv")
head(Activity)
```

```
##   steps       date interval
## 1    NA 2012-10-01        0
## 2    NA 2012-10-01        5
## 3    NA 2012-10-01       10
## 4    NA 2012-10-01       15
## 5    NA 2012-10-01       20
## 6    NA 2012-10-01       25
```

```r
str(Activity)
```

```
## 'data.frame':	17568 obs. of  3 variables:
##  $ steps   : int  NA NA NA NA NA NA NA NA NA NA ...
##  $ date    : Factor w/ 61 levels "2012-10-01","2012-10-02",..: 1 1 1 1 1 1 1 1 1 1 ...
##  $ interval: int  0 5 10 15 20 25 30 35 40 45 ...
```
#### Ploting the Histogram of the steps


```r
daily <- aggregate(steps ~ date, data = Activity, sum, na.rm = TRUE)
hist(daily$steps,breaks = 15, main = "The Histogram of Daily Steps", xlab = "Number of steps", col = "red")
```

![](PA1_template_files/figure-html/unnamed-chunk-2-1.png)

## What is mean total number of steps taken per day?


## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
