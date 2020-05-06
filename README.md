# 251-firstlab
This lab allowed us to construct a confidence interval of a data set.

# Lab Week 8 
# CI for one mean 

myfile <- file.choose()
mms.bags <- read.csv(myfile, header =T)

summary(mms.bags)
head(mms.bags)

# sample mean
x.bar <- mean(mms.bags$weight)
x.bar

# Sample Standard Deviation
bags.sd <- sd(mms.bags$weight)
bags.sd

# Sample Size First is row number, second is column number 
dim(mms.bags)
n <- dim(mms.bags)[1]
n

# Standard Error 
se <- bags.sd/sqrt(n)
se

# t*
df <- n -1
df
# 95% CI = .95 + 2.5 
t_95 <- qt(p=.975, df = df)
t_95

# ME 
ME_95 <- t_95*se
ME_95

CI_95 <- c(x.bar-ME_95, x.bar+ME_95)
CI_95
