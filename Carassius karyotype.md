### CGI Table creation
```
CGI <- list (CGI_D10_6g=data.frame(p1=p1, q1=q1, lenght=p1+q1, d1=q1-p1, r1=q1/p1, i1=100/((q1/p1)+1)), CGI_D5_9g = data.frame(p2=p2, q2=q2, lenght=p2+q2, d2=q2-p2, r2=q2/p2, i2=100/((q2/p2)+1)), CGI_X7_2_7=data.frame(p3=p3, q3=q3, lenght=p3+q3, d3=q3-p3, r3=q3/p3, i3=100/((q3/p3)+1)), CGI_D10_4g = data.frame(p4=p4, q4=q4, lenght=p4+q4, d4=q4-p4, r4=q4/p4, i4=100/((q4/p4)+1)), CGI_H15_7g = data.frame(p5=p5, q5=q5, lenght=p5+q5, d5=q5-p5, r5=q5/p5, i5=100/((q5/p5)+1)), CGI_D5_2g = data.frame(p6=p6, q6=q6, lenght=p6+q6, d6=q6-p6, r6=q6/p6, i6=100/((q6/p6)+1)), CGI_D5_8g = data.frame(p7=p7, q7=q7, lenght=p7+q7, d7=q7-p7, r7=q7/p7, i7=100/((q7/p7)+1)), CGI_X9_2_1_5 = data.frame(p8=p8, q8=q8, lenght=p8+q8, d8=q8-p8, r8=q8/p8, i8=100/((q8/p8)+1)), CGI_X9_2_1_10 = data.frame(p9=p9, q9=q9, lenght=p9+q9, d9=q9-p9, r9=q9/p9, i9=100/((q9/p9)+1)), CGI_D11_7g = data.frame(p10=p10, q10=q10, lenght=p10+q10, d10=q10-p10, r10=q10/p10, i10=100/((q10/p10)+1)))
```

### decreasing order according centromeric index
```
> CGI$CGI_D10_6g <- CGI$CGI_D10_6g [order(-CGI$CGI_D10_6g$i1),]
> CGI$CGI_D5_9g <- CGI$CGI_D5_9g [order(-CGI$CGI_D5_9g$i2),]
> CGI$CGI_X7_2_7 <- CGI$CGI_X7_2_7 [order(-CGI$CGI_X7_2_7$i3),]
> CGI$CGI_D10_4g <- CGI$CGI_D10_4g [order(-CGI$CGI_D10_4g$i4),]
> CGI$CGI_H15_7g <- CGI$CGI_H15_7g [order(-CGI$CGI_H15_7g$i5),]
> CGI$CGI_D5_2g <- CGI$CGI_D5_2g [order(-CGI$CGI_D5_2g$i6),]
> CGI$CGI_D5_8g <- CGI$CGI_D5_8g [order(-CGI$CGI_D5_8g$i7),]
> CGI$CGI_X9_2_1_5 <- CGI$CGI_X9_2_1_5 [order(-CGI$CGI_X9_2_1_5$i8),]
> CGI$CGI_X9_2_1_10 <- CGI$CGI_X9_2_1_10 [order(-CGI$CGI_X9_2_1_10$i9),]
> CGI$CGI_D11_7g <- CGI$CGI_D11_7g [order(-CGI$CGI_D11_7g$i10),]
```

### i folder into CGI list

```
CGI$lenght_i <- data.frame(lenght1=CGI$CGI_D10_6g$lenght, lenght2=CGI$CGI_D5_9g$lenght, lenght3=CGI$CGI_X7_2_7$lenght, lenght4=CGI$CGI_D10_4g$lenght, lenght5=CGI$CGI_H15_7g$lenght, lenght6=CGI$CGI_D5_2g$lenght, lenght7=CGI$CGI_D5_8g$lenght, lenght8=CGI$CGI_X9_2_1_5$lenght, lenght9=CGI$CGI_X9_2_1_10$lenght, lenght10=CGI$CGI_D11_7g$lenght, i1=CGI$CGI_D10_6g$i1, i2=CGI$CGI_D5_9g$i2, i3=CGI$CGI_X7_2_7$i3, i4=CGI$CGI_D10_4g$i4, i5=CGI$CGI_H15_7g$i5, i6=CGI$CGI_D5_2g$i6, i7=CGI$CGI_D5_8g$i7, i8=CGI$CGI_X9_2_1_5$i8, i9=CGI$CGI_X9_2_1_10$i9, i10=CGI$CGI_D11_7g$i10)
```
```
> CGI$lenght_i <- data.frame(lenght1=CGI$CGI_D10_6g$lenght, lenght2=CGI$CGI_D5_9g$lenght, lenght3=CGI$CGI_X7_2_7$lenght, lenght4=CGI$CGI_D10_4g$lenght, lenght5=CGI$CGI_H15_7g$lenght, lenght6=CGI$CGI_D5_2g$lenght, lenght7=CGI$CGI_D5_8g$lenght, lenght8=CGI$CGI_X9_2_1_5$lenght, lenght9=CGI$CGI_X9_2_1_10$lenght, lenght10=CGI$CGI_D11_7g$lenght, mean_lenght=apply (CGI$lenght_i[,1:10], 1, mean), i1=CGI$CGI_D10_6g$i1, i2=CGI$CGI_D5_9g$i2, i3=CGI$CGI_X7_2_7$i3, i4=CGI$CGI_D10_4g$i4, i5=CGI$CGI_H15_7g$i5, i6=CGI$CGI_D5_2g$i6, i7=CGI$CGI_D5_8g$i7, i8=CGI$CGI_X9_2_1_5$i8, i9=CGI$CGI_X9_2_1_10$i9, i10=CGI$CGI_D11_7g$i10)
```



### assign of category to each chromosome in the first folder (CGI_D10_6g) of CGI list
```
for(i in 1:100) {if(CGI$CGI_D10_6g$i1[i]>=35.5) {CGI$CGI_D10_6g$category[i] = "m"} else if (CGI$CGI_D10_6g$i1[i]>=25 & CGI$CGI_D10_6g$i1[i]<35.5){CGI$CGI_D10_6g$category[i] = "sm"} else if (CGI$CGI_D10_6g$i1[i]>=12.5 & CGI$CGI_D10_6g$i1[i]<25){CGI$CGI_D10_6g$category[i] = "st"} else if (CGI$CGI_D10_6g$i1[i]>0 & CGI$CGI_D10_6g$i1[i]<12.5) {CGI$CGI_D10_6g$category[i] = "a"} else {CGI$CGI_D10_6g$category[i] = "T"}}
```
```
CGI$CGI_D10_6g <- CGI$CGI_D10_6g[order(CGI$CGI_D10_6g$category, -CGI$CGI_D10_6g$lenght),]
```

### assign of category to each chromosome in the second folder (CGI_D5_9g) of CGI list
```
for(i in 1:100) {if(CGI$CGI_D5_9g$i2[i]>=35.5) {CGI$CGI_D5_9g$category[i] = "m"} else if (CGI$CGI_D5_9g$i2[i]>=25 & CGI$CGI_D5_9g$i2[i]<35.5){CGI$CGI_D5_9g$category[i] = "sm"} else if (CGI$CGI_D5_9g$i2[i]>=12.5 & CGI$CGI_D5_9g$i2[i]<25){CGI$CGI_D5_9g$category[i] = "st"} else if (CGI$CGI_D5_9g$i2[i]>0 & CGI$CGI_D5_9g$i2[i]<12.5) {CGI$CGI_D5_9g$category[i] = "a"} else {CGI$CGI_D5_9g$category[i] = "T"}}
```
```
CGI$CGI_D5_9g <- CGI$CGI_D5_9g[order(CGI$CGI_D5_9g$category, -CGI$CGI_D5_9g$lenght),]
```
```
> for(i in 1:100) {if(CGI$CGI_X7_2_7$i3[i]>=35.5) {CGI$CGI_X7_2_7$category[i] = "m"} else if (CGI$CGI_X7_2_7$i3[i]>=25 & CGI$CGI_X7_2_7$i3[i]<35.5){CGI$CGI_X7_2_7$category[i] = "sm"} else if (CGI$CGI_X7_2_7$i3[i]>=12.5 & CGI$CGI_X7_2_7$i3[i]<25){CGI$CGI_X7_2_7$category[i] = "st"} else if (CGI$CGI_X7_2_7$i3[i]>0 & CGI$CGI_X7_2_7$i3[i]<12.5) {CGI$CGI_X7_2_7$category[i] = "a"} else {CGI$CGI_X7_2_7$category[i] = "T"}}
```
```
for(i in 1:100) {if(CGI$CGI_D10_4g$i4[i]>=35.5) {CGI$CGI_D10_4g$category[i] = "m"} else if (CGI$CGI_D10_4g$i4[i]>=25 & CGI$CGI_D10_4g$i4[i]<35.5){CGI$CGI_D10_4g$category[i] = "sm"} else if (CGI$CGI_D10_4g$i4[i]>=12.5 & CGI$CGI_D10_4g$i4[i]<25){CGI$CGI_D10_4g$category[i] = "st"} else if (CGI$CGI_D10_4g$i4[i]>0 & CGI$CGI_D10_4g$i4[i]<12.5) {CGI$CGI_D10_4g$category[i] = "a"} else {CGI$CGI_D10_4g$category[i] = "T"}}
```
```
> CGI$CGI_D10_4g <- CGI$CGI_D10_4g[order(CGI$CGI_D10_4g$category, -CGI$CGI_D10_4g$lenght),]
```

### i folder into CGI list
```
CGI$i <- data.frame(i1=CGI$CGI_D10_6g$i1, i2=CGI$CGI_D5_9g$i2, i3=CGI$CGI_X7_2_7$i3, i4=CGI$CGI_D10_4g$i4, i5=CGI$CGI_H15_7g$i5, i6=CGI$CGI_D5_2g$i6, i7=CGI$CGI_D5_8g$i7, i8=CGI$CGI_X9_2_1_5$i8, i9=CGI$CGI_X9_2_1_10$i9, i10=CGI$CGI_D11_7g$i10)
```
```
CGI$lenght_i <- data.frame(lenght1=CGI$CGI_D10_6g$lenght, lenght2=CGI$CGI_D5_9g$lenght, lenght3=CGI$CGI_X7_2_7$lenght, lenght4=CGI$CGI_D10_4g$lenght, lenght5=CGI$CGI_H15_7g$lenght, lenght6=CGI$CGI_D5_2g$lenght, lenght7=CGI$CGI_D5_8g$lenght, lenght8=CGI$CGI_X9_2_1_5$lenght, lenght9=CGI$CGI_X9_2_1_10$lenght, lenght10=CGI$CGI_D11_7g$lenght, i1=CGI$CGI_D10_6g$i1, i2=CGI$CGI_D5_9g$i2, i3=CGI$CGI_X7_2_7$i3, i4=CGI$CGI_D10_4g$i4, i5=CGI$CGI_H15_7g$i5, i6=CGI$CGI_D5_2g$i6, i7=CGI$CGI_D5_8g$i7, i8=CGI$CGI_X9_2_1_5$i8, i9=CGI$CGI_X9_2_1_10$i9, i10=CGI$CGI_D11_7g$i10)
```
```
> CGI$lenght_i <- data.frame(lenght1=CGI$CGI_D10_6g$lenght, lenght2=CGI$CGI_D5_9g$lenght, lenght3=CGI$CGI_X7_2_7$lenght, lenght4=CGI$CGI_D10_4g$lenght, lenght5=CGI$CGI_H15_7g$lenght, lenght6=CGI$CGI_D5_2g$lenght, lenght7=CGI$CGI_D5_8g$lenght, lenght8=CGI$CGI_X9_2_1_5$lenght, lenght9=CGI$CGI_X9_2_1_10$lenght, lenght10=CGI$CGI_D11_7g$lenght, mean_lenght=apply (CGI$lenght_i[,1:10], 1, mean), i1=CGI$CGI_D10_6g$i1, i2=CGI$CGI_D5_9g$i2, i3=CGI$CGI_X7_2_7$i3, i4=CGI$CGI_D10_4g$i4, i5=CGI$CGI_H15_7g$i5, i6=CGI$CGI_D5_2g$i6, i7=CGI$CGI_D5_8g$i7, i8=CGI$CGI_X9_2_1_5$i8, i9=CGI$CGI_X9_2_1_10$i9, i10=CGI$CGI_D11_7g$i10)
```

```
CGI$i$var <- apply(CGI$i, 1, var)
```
```
for(i in 1:100) {if(CGI_D10_6g$i1[i]>=35.5) {CGI_D10_6g$category[i] = "m"} else if (CGI_D10_6g$i1[i]>=25 & CGI_D10_6g$i1[i]<35.5){CGI_D10_6g$category[i] = "sm"} else if (CGI_D10_6g$i1[i]>=12.5 & CGI_D10_6g$i1[i]<25){CGI_D10_6g$category[i] = "st"} else if (CGI_D10_6g$i1[i]>0 & CGI_D10_6g$i1[i]<12.5) {CGI_D10_6g$category[i] = "a"} else {CGI_D10_6g$category[i] = "T"}}
```

### CCA Table creation

```
CcVi3CZ_5_5 <- data.frame(p4=p4, q4=q4, d4=q4-p4, r4=q4/p4, i4=100/((q4/p4)+1))
```

### Order in the table according to column "r4"

```
CcVi3CZ_5_5 <- CcVi3CZ_5_5[order(CcVi3CZ_5_5$r4),]
```
```
CcVi3CZ_5_6$chromosome <- factor(c(rep(0, times=15), rep(1, times=37), rep(2, times=16), 3,3, rep(4, times=30)), labels = c("m", "sm", "st", "a", "T"))
```
```
CcVi3CZ_5_9$chromosome <- factor(c(rep(0, times=19), rep(1, times=19), rep(2, times=11), rep(4, times=51)), levels = 0:4, labels = c("m", "sm", "st", "a", "T"))
```

### Order according column "chromosome" (ascending) and then according chromosomal length (descending)
```
CcVi3CZ_5_6 <- CcVi3CZ_5_6 [order(CcVi3CZ_5_6$chromosome, -CcVi3CZ_5_6$d),]
```

### column "no" added
```
CcVi3CZ_5_6$no <- c(1:15, 1:37, 1:16, 1,2, 1:30)
```

### list added
```
CCA <- list(CcVi3CZ_5_10=CcVi3CZ_5_10, CcVi3CZ_5_9=CcVi3CZ_5_9, CcVi3CZ_5_6=CcVi3CZ_5_6)
```

### chromosome ratio "r" column extracted from each table and sorted ascendingly:
```
r <- sort(CCA$CcHe6Fi_1_2$r)
```
r2, r3 ... r10

### table "r_sorted" created for statistics of each ratio in each row:
```
r_sorted <- data.frame(r=r, r2=r2, r3=r3, r4=r4, r5=r5, r6=r6, r7=r7, r8=r8, r9=r9, r10=r10)
```

### "mean" column

```
r_sorted$mean <- rowMeans(r_sorted)
```

An issue with values "Inf" in the comumn "mean". The rest od "mean" column containing "Inf" was modified in data.frame. The mean value was counted separately without "Inf" values as follows:

row 50:
```
r_sorted[50, "mean"] <- mean (c(r_sorted[50, "r"], r_sorted[50, "r3"], r_sorted[50, "r4"], r_sorted[50, "r5"], r_sorted[50, "r6"], r_sorted[50, "r7"], r_sorted[50, "r8"], r_sorted[50, "r9"], r_sorted[50, "r10"]))
```

row 51:
```
r_sorted[51, "mean"] <- mean (c(r_sorted[51, "r"], r_sorted[51, "r3"], r_sorted[51, "r4"], r_sorted[51, "r5"], r_sorted[51, "r6"], r_sorted[51, "r7"], r_sorted[51, "r8"], r_sorted[51, "r9"]))
```

row 55:
```
r_sorted[55, "mean"] <- mean (c(r_sorted[55, "r"], r_sorted[55, "r3"], r_sorted[55, "r4"], r_sorted[55, "r6"], r_sorted[55, "r7"], r_sorted[55, "r9"]))
```

row 57:
```
r_sorted[57, "mean"] <- mean (c(r_sorted[57, "r"], r_sorted[57, "r3"], r_sorted[57, "r4"], r_sorted[57, "r6"], r_sorted[57, "r7"], r_sorted[57, "r9"]))
```
row 58 contains 5 "Inf" values and 5 real "r" values and was considered as "Inf"

### "Var" column = varriance

varriance of arm ratio of each chromosome inserted into the new column

```
r_sorted$Var <- apply(r_sorted[,-c(11)], 1, var)
```
column 11 excluded because of "mean"

An issue with values "Inf" in the comumn "Var" figured out in same way as it was in the case of mean.

