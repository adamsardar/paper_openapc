# Log: Review of publication fees being spent by FWF, Wellcome Trust and JISC

## Data Sources

All data files were downloaded on 2 June 2016.

### FWF

- Katharina Rieck, Doris Haslinger, Sasa Meischke-Ilic, Ünzüle Kirindi-Hentschel, & Falk Reckling. (2016). Austrian Science Fund (FWF) Publication Cost Data 2015. Figshare. http://doi.org/10.6084/m9.figshare.3180166

- Falk Reckling, & Katharina Rieck. (2015). Austrian Science Fund (FWF) Publication Cost Data 2014. Figshare. http://doi.org/10.6084/m9.figshare.1378610

### JISC

- Stuart Lawson. (2015). APC data for 25 UK higher education institutions - 2014. Figshare. http://doi.org/10.6084/m9.figshare.1305596.v5

- Stuart Lawson. (2016). APC data for 27 UK higher education institutions in 2015. Figshare. http://doi.org/10.6084/m9.figshare.1507481.v4

### Wellcome Trust

- Robert Kiley. (2016). Wellcome Tust/COAF spend on open access publishing (article processing charges) - 2014-15. Figshare. http://doi.org/10.6084/m9.figshare.3118936.v1

- Robert Kiley. (2015). Wellcome Trust open access (OA) spend and compliance monitoring: 2013-14. Figshare. http://doi.org/10.6084/m9.figshare.1321361.v5

## Pre-processing

Before loading cost data into the R console, we removed windows encoding from the Jisc data files. We also removed currency symbols from the Wellcome Trust spreadsheets and converted them to csv files with LibreOffice.

Pre-processed files were stored in this folder.

## Converting currencies

To summarize  Wellcome Trust's and Jisc's spending, we converted the prices from GBP to Euro in accordance with the average Euro foreign exchange reference rates provided by the European Central Bank. Our comparison between the open data initiatives focussed on the last two years 2014 and 2015. Because Wellcome Trust's spending was reported for the periods 2013 - 2014 and 2014 - 2015, we referred to the average exchange rates of the full two-year period as we could not determine the actual invoicing dates from the data.

## Cost aggregation

Note, we used the accompanying data report to determine FWF publication fee spending

### JISC 2014


```r
jisc_14 <- read.csv("jisc_2014.csv", header = TRUE, sep =",")
jisc_14$APC <- as.numeric(as.character(jisc_14$APC.paid....including.VAT.if.charged))
```

```
## Warning: NAs durch Umwandlung erzeugt
```

```r
# convert to average euro exchange rate
jisc_14$APC <- jisc_14$APC * 1.2411

apc_sum <- aggregate(jisc_14$APC, list(jisc_14$Type.of.publication), sum, na.rm = TRUE)
apc_n <- as.data.frame(table(jisc_14$Type.of.publication))

tt <- data.frame(apc_n, apc_sum[,c("x")])

colnames(tt) <- c("Type", "Freq", "Fees paid in Euro")

tt$`Mean Fee` <- tt$`Fees paid in Euro` / tt$Freq

tt
```

```
##                                       Type Freq Fees paid in Euro
## 1                                          2812       4861771.996
## 2                                     Book    1          7822.939
## 3                             Book chapter   10         21746.368
## 4     Conference Paper/Proceeding/Abstract   21         16630.430
## 5 journal Article/Review (Full OA journal)    2          4042.660
## 6 Journal Article/Review (Full OA journal) 1159       1893819.672
## 7  Journal Article/Review (Hybrid journal) 2938       5409623.345
##    Mean Fee
## 1 1728.9374
## 2 7822.9388
## 3 2174.6368
## 4  791.9252
## 5 2021.3299
## 6 1634.0118
## 7 1841.2605
```

```r
sum(tt$`Fees paid in Euro`)
```

```
## [1] 12215457
```

```r
write.csv(tt, "aggregated_jisc_2014.csv")
```

### JISC 2015


```r
jisc_15 <- read.csv("jisc_2015.csv", header = TRUE, sep =",")

jisc_15$APC <- as.numeric(as.character(jisc_15$APC.paid....including.VAT.if.charged))
```

```
## Warning: NAs durch Umwandlung erzeugt
```

```r
# convert to average euro exchange rate
jisc_15$APC <- jisc_15$APC * 1.3785

apc_sum <- aggregate(jisc_15$APC, list(jisc_15$Type.of.publication), sum, na.rm = TRUE)

apc_n <- as.data.frame(table(jisc_15$Type.of.publication))

tt <- data.frame(apc_n, apc_sum[,c("x")])

colnames(tt) <- c("Type", "Freq", "Fees paid in Euro")

tt$`Mean Fee` <- tt$`Fees paid in Euro` / tt$Freq

tt
```

```
##                                       Type Freq Fees paid in Euro
## 1                                           178         345215.70
## 2                                     Book    1          15714.90
## 3                         Conference paper    4           4257.47
## 4                   Journal Article/Review   62         156555.51
## 5 Journal Article/Review (Full OA journal) 1168        2211958.18
## 6  Journal Article/Review (Hybrid journal) 2944        6977753.23
##    Mean Fee
## 1  1939.414
## 2 15714.900
## 3  1064.367
## 4  2525.089
## 5  1893.800
## 6  2370.161
```

```r
sum(tt$`Fees paid in Euro`)
```

```
## [1] 9711455
```

```r
write.csv(tt, "aggregated_jisc_2015.csv")
```

### wellcome 2013-14


```r
wellcome_13_14 <- read.csv("wellcome_13_14.csv", header = T, sep =",")
wellcome_13_14$APC <- wellcome_13_14$Cost......inc.VAT.when.charged.

# convert to average euro exchange rate
wellcome_13_14$APC <- wellcome_13_14$APC * 1.2094

apc_n <- data.frame(table(wellcome_13_14$Journal.Type))
apc_sum <- aggregate(wellcome_13_14$APC, list(wellcome_13_14$Journal.Type), sum, na.rm = TRUE)
apc_mean <- aggregate(wellcome_13_14$APC, list(wellcome_13_14$Journal.Type), mean, na.rm = TRUE)

tt <- data.frame(apc_n, apc_sum[,c("x")], apc_mean[,c("x")])

colnames(tt) <- c("Type", "Freq", "Fees paid in Euro", "Mean Fee paid in Euro")

tt
```

```
##     Type Freq Fees paid in Euro Mean Fee paid in Euro
## 1          55          117261.3              2132.023
## 2 hybrid 1894         4648878.5              2454.529
## 3     oa  607          911301.9              1501.321
```

```r
sum(tt$`Fees paid in Euro`)
```

```
## [1] 5677442
```

```r
write.csv(tt, "aggregated_wellcome_13_14.csv")
```

### wellcome 2014 - 2015


```r
wellcome_14_15 <- read.csv("wellcome_14_15.csv", header = T, sep =",")
wellcome_14_15$APC <- wellcome_14_15$Cost......inc.VAT.when.charged.

# convert to average euro exchange rate
wellcome_14_15$APC <- wellcome_14_15$APC * 1.3099


apc_n <- data.frame(table(wellcome_14_15$Journal.Type))
apc_sum <- aggregate(wellcome_14_15$APC, list(wellcome_14_15$Journal.Type), sum, na.rm = TRUE)
apc_mean <- aggregate(wellcome_14_15$APC, list(wellcome_14_15$Journal.Type), mean, na.rm = TRUE)

tt <- data.frame(apc_n, apc_sum[,c("x")], apc_mean[,c("x")])

colnames(tt) <- c("Type", "Freq", "Fees paid in Euro", "Mean Fee paid in Euro")

tt
```

```
##     Type Freq Fees paid in Euro Mean Fee paid in Euro
## 1         102          266422.4              2611.985
## 2 hybrid 2065         5690177.6              2755.534
## 3     oa  775         1418097.2              1829.803
```

```r
sum(tt$`Fees paid in Euro`)
```

```
## [1] 7374697
```

```r
write.csv(tt, "aggregated_wellcome_14_14.csv")
```
