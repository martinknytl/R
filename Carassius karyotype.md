# CAU 

#### list creation with each metaphase as a table

Vectors were written manually from measuring of each chromosome
```
CAU <- list (CaXX1IL_1_1=data.frame(p1=p1, q1=q1, lenght1=p1+q1, d1=q1-p1, r1=q1/p1, i1=100/((q1/p1)+1)), CaXX1IL_1_2 = data.frame(p2=p2, q2=q2, lenght2=p2+q2, d2=q2-p2, r2=q2/p2, i2=100/((q2/p2)+1)), CaXX1IL_1_3=data.frame(p3=p3, q3=q3, lenght3=p3+q3, d3=q3-p3, r3=q3/p3, i3=100/((q3/p3)+1)), CaXX1IL_1_4 = data.frame(p4=p4, q4=q4, lenght4=p4+q4, d4=q4-p4, r4=q4/p4, i4=100/((q4/p4)+1)), CaXX1IL_1_7 = data.frame(p5=p5, q5=q5, lenght5=p5+q5, d5=q5-p5, r5=q5/p5, i5=100/((q5/p5)+1)), CaXX1IL_1_8 = data.frame(p6=p6, q6=q6, lenght6=p6+q6, d6=q6-p6, r6=q6/p6, i6=100/((q6/p6)+1)), CaXX1IL_1_6 = data.frame(p7=p7, q7=q7, lenght7=p7+q7, d7=q7-p7, r7=q7/p7, i7=100/((q7/p7)+1)), CaXX1IL_2_1 = data.frame(p8=p8, q8=q8, lenght8=p8+q8, d8=q8-p8, r8=q8/p8, i8=100/((q8/p8)+1)), CaXX1IL_2_2 = data.frame(p9=p9, q9=q9, lenght9=p9+q9, d9=q9-p9, r9=q9/p9, i9=100/((q9/p9)+1)), CaXX1IL_2_3 = data.frame(p10=p10, q10=q10, lenght10=p10+q10, d10=q10-p10, r10=q10/p10, i10=100/((q10/p10)+1)))
```

#### decreasing order according centromeric index
```
CAU$CaXX1IL_1_1 <- CAU$CaXX1IL_1_1 [order(-CAU$CaXX1IL_1_1$i1),]
CAU$CaXX1IL_1_2 <- CAU$CaXX1IL_1_2 [order(-CAU$CaXX1IL_1_2$i2),]
CAU$CaXX1IL_1_3 <- CAU$CaXX1IL_1_3 [order(-CAU$CaXX1IL_1_3$i3),]
CAU$CaXX1IL_1_4 <- CAU$CaXX1IL_1_4 [order(-CAU$CaXX1IL_1_4$i4),]
CAU$CaXX1IL_1_7 <- CAU$CaXX1IL_1_7 [order(-CAU$CaXX1IL_1_7$i5),]
CAU$CaXX1IL_1_8 <- CAU$CaXX1IL_1_8 [order(-CAU$CaXX1IL_1_8$i6),]
CAU$CaXX1IL_1_6 <- CAU$CaXX1IL_1_6 [order(-CAU$CaXX1IL_1_6$i7),]
CAU$CaXX1IL_2_1 <- CAU$CaXX1IL_2_1 [order(-CAU$CaXX1IL_2_1$i8),]
CAU$CaXX1IL_2_2 <- CAU$CaXX1IL_2_2 [order(-CAU$CaXX1IL_2_2$i9),]
CAU$CaXX1IL_2_3 <- CAU$CaXX1IL_2_3 [order(-CAU$CaXX1IL_2_3$i10),]
```

#### "lenght_i" folder into CAU list
```
CAU$lenght_i <- data.frame(lenght1=CAU$CaXX1IL_1_1$lenght1, lenght2=CAU$CaXX1IL_1_2$lenght2, lenght3=CAU$CaXX1IL_1_3$lenght3, lenght4=CAU$CaXX1IL_1_4$lenght4, lenght5=CAU$CaXX1IL_1_7$lenght5, lenght6=CAU$CaXX1IL_1_8$lenght6, lenght7=CAU$CaXX1IL_1_6$lenght7, lenght8=CAU$CaXX1IL_2_1$lenght8, lenght9=CAU$CaXX1IL_2_2$lenght9, lenght10=CAU$CaXX1IL_2_3$lenght10, i1=CAU$CaXX1IL_1_1$i1, i2=CAU$CaXX1IL_1_2$i2, i3=CAU$CaXX1IL_1_3$i3, i4=CAU$CaXX1IL_1_4$i4, i5=CAU$CaXX1IL_1_7$i5, i6=CAU$CaXX1IL_1_8$i6, i7=CAU$CaXX1IL_1_6$i7, i8= CAU$CaXX1IL_2_1$i8, i9= CAU$CaXX1IL_2_2$i9, i10= CAU$CaXX1IL_2_3$i10)
```

#### "mean_lenght", "var_lenght", "mean_i" and "var_i" columns added into "lenght_i" folder of CAU list. It is not possible to create whole data frame using command with mean and variance. R language has to know other collumns first. Also, separately is created "mean_lenght/variance_lenght" and "mean_i/variance_i"

```
CAU$lenght_i <- data.frame(lenght1=CAU$CaXX1IL_1_1$lenght1, lenght2=CAU$CaXX1IL_1_2$lenght2, lenght3=CAU$CaXX1IL_1_3$lenght3, lenght4=CAU$CaXX1IL_1_4$lenght4, lenght5=CAU$CaXX1IL_1_7$lenght5, lenght6=CAU$CaXX1IL_1_8$lenght6, lenght7=CAU$CaXX1IL_1_6$lenght7, lenght8=CAU$CaXX1IL_2_1$lenght8, lenght9=CAU$CaXX1IL_2_2$lenght9, lenght10=CAU$CaXX1IL_2_3$lenght10, mean_lenght=apply (CAU$lenght_i[,1:10], 1, mean), variance_lenght=apply(CAU$lenght_i[,1:10], 1, var), i1=CAU$CaXX1IL_1_1$i1, i2=CAU$CaXX1IL_1_2$i2, i3=CAU$CaXX1IL_1_3$i3, i4=CAU$CaXX1IL_1_4$i4, i5=CAU$CaXX1IL_1_7$i5, i6=CAU$CaXX1IL_1_8$i6, i7=CAU$CaXX1IL_1_6$i7, i8= CAU$CaXX1IL_2_1$i8, i9= CAU$CaXX1IL_2_2$i9, i10= CAU$CaXX1IL_2_3$i10)
CAU$lenght_i <- data.frame(lenght1=CAU$CaXX1IL_1_1$lenght1, lenght2=CAU$CaXX1IL_1_2$lenght2, lenght3=CAU$CaXX1IL_1_3$lenght3, lenght4=CAU$CaXX1IL_1_4$lenght4, lenght5=CAU$CaXX1IL_1_7$lenght5, lenght6=CAU$CaXX1IL_1_8$lenght6, lenght7=CAU$CaXX1IL_1_6$lenght7, lenght8=CAU$CaXX1IL_2_1$lenght8, lenght9=CAU$CaXX1IL_2_2$lenght9, lenght10=CAU$CaXX1IL_2_3$lenght10, mean_lenght=apply (CAU$lenght_i[,1:10], 1, mean), variance_lenght=apply(CAU$lenght_i[,1:10], 1, var), i1=CAU$CaXX1IL_1_1$i1, i2=CAU$CaXX1IL_1_2$i2, i3=CAU$CaXX1IL_1_3$i3, i4=CAU$CaXX1IL_1_4$i4, i5=CAU$CaXX1IL_1_7$i5, i6=CAU$CaXX1IL_1_8$i6, i7=CAU$CaXX1IL_1_6$i7, i8= CAU$CaXX1IL_2_1$i8, i9= CAU$CaXX1IL_2_2$i9, i10= CAU$CaXX1IL_2_3$i10, mean_i=apply (CAU$lenght_i[,13:22], 1, mean), variance_i=apply(CAU$lenght_i[,13:22], 1, var))
```

#### additional column for "mean_i_corrected"

each value where the number is zero more then 5 times is considered to be zero in mean.
```
CAU$lenght_i$mean_i_corrected <- apply (CAU$lenght_i[,13:22], 1, mean)


CAU$lenght_i[66:81, "mean_i_corrected"] <- 0
```

#### a new column "category" of each chromosome
```
for(i in 1:100) {if(CAU$lenght_i$mean_i_corrected[i]>=35.5) {CAU$lenght_i$category[i] = "m"} else if (CAU$lenght_i$mean_i_corrected[i]>=25 & CAU$lenght_i$mean_i_corrected[i]<35.5){CAU$lenght_i$category[i] = "sm"} else if (CAU$lenght_i$mean_i_corrected[i]>=12.5 & CAU$lenght_i$mean_i_corrected[i]<25){CAU$lenght_i$category[i] = "st"} else if (CAU$lenght_i$mean_i_corrected[i]>0 & CAU$lenght_i$mean_i_corrected[i]<12.5) {CAU$lenght_i$category[i] = "a"} else {CAU$lenght_i$category[i] = "T"}}
```

#### CAU dotplot creation
```
plot(CAU$lenght_i$mean_i, CAU$lenght_i$mean_lenght, pch=16, col="blue", ylim = c(15, 45), xlab = "centromeric index", ylab = "chromosomal length", ann=TRUE, las=1, abline(v=c(0, 12.5, 25, 35.5), col="gray", lty=2))
```
```
CAU_dotplot <- recordPlot()
```

#### CAU boxplot creation

##### function for creation of 50 vectors = 50 homologous chromosomal pairs. The first vector from all first two lines of "i" (centromeric index) of each folder (data frame) = chromosome with the highest centromeric index (chromosome1)

```
Select_chrome <- function(i,j) {chromosome <- c(CAU$CaXX1IL_1_1$i1[i:j], CAU$CaXX1IL_1_2$i2[i:j], CAU$CaXX1IL_1_3$i3[i:j], CAU$CaXX1IL_1_4$i4[i:j], CAU$CaXX1IL_1_7$i5[i:j], CAU$CaXX1IL_1_8$i6[i:j], CAU$CaXX1IL_1_6$i7[i:j], CAU$CaXX1IL_2_1$i8[i:j], CAU$CaXX1IL_2_2$i9[i:j], CAU$CaXX1IL_2_3$i10[i:j])}
```

```
chromosome1 <- Select_chrome(1,2)
chromosome2 <- Select_chrome(3,4)
chromosome3 <- Select_chrome(5,6)
chromosome4 <- Select_chrome(7,8)
chromosome5 <- Select_chrome(9,10)
chromosome6 <- Select_chrome(11,12)
chromosome7 <- Select_chrome(13,14)
chromosome8 <- Select_chrome(15,16)
chromosome9 <- Select_chrome(17,18)
chromosome10 <- Select_chrome(19,20)
chromosome11 <- Select_chrome(21,22)
chromosome12 <- Select_chrome(23,24)
chromosome13 <- Select_chrome(25,26)
chromosome14 <- Select_chrome(27,28)
chromosome15 <- Select_chrome(29,30)
chromosome16 <- Select_chrome(31,32)
chromosome17 <- Select_chrome(33,34)
chromosome18 <- Select_chrome(35,36)
chromosome19 <- Select_chrome(37,38)
chromosome20 <- Select_chrome(39,40)
chromosome21 <- Select_chrome(41,42)
chromosome22 <- Select_chrome(43,44)
chromosome23 <- Select_chrome(45,46)
chromosome24 <- Select_chrome(47,48)
chromosome25 <- Select_chrome(49,50)
chromosome26 <- Select_chrome(51,52)
chromosome27 <- Select_chrome(53,54)
chromosome28 <- Select_chrome(55,56)
chromosome29 <- Select_chrome(57,58)
chromosome30 <- Select_chrome(59,60)
chromosome31 <- Select_chrome(61,62)
chromosome32 <- Select_chrome(63,64)
chromosome33 <- Select_chrome(65,66)
chromosome34 <- Select_chrome(67,68)
chromosome35 <- Select_chrome(69,70)
chromosome36 <- Select_chrome(71,72)
chromosome37 <- Select_chrome(73,74)
chromosome38 <- Select_chrome(75,76)
chromosome39 <- Select_chrome(77,78)
chromosome40 <- Select_chrome(79,80)
chromosome41 <- Select_chrome(81,82)
chromosome42 <- Select_chrome(83,84)
chromosome43 <- Select_chrome(85,86)
chromosome44 <- Select_chrome(87,88)
chromosome45 <- Select_chrome(89,90)
chromosome46 <- Select_chrome(91,92)
chromosome47 <- Select_chrome(93,94)
chromosome48 <- Select_chrome(95,96)
chromosome49 <- Select_chrome(97,98)
chromosome50 <- Select_chrome(99,100)
```

```
boxplot(chromosome1, chromosome2, chromosome3, chromosome4, chromosome5, chromosome6, chromosome7, chromosome8, chromosome9, chromosome10, chromosome11, chromosome12, chromosome13, chromosome14, chromosome15, chromosome16, chromosome17, chromosome18, chromosome19, chromosome20, chromosome21, chromosome22, chromosome23, chromosome24, chromosome25, chromosome26, chromosome27, chromosome28, chromosome29, chromosome30, chromosome31, chromosome32, chromosome33, chromosome34, chromosome35, chromosome36, chromosome37, chromosome38, chromosome39, chromosome40, chromosome41, chromosome42, chromosome43, chromosome44, chromosome45, chromosome46, chromosome47, chromosome48, chromosome49, chromosome50, ylim=c(-1, 50), xlim=c(1, 50), horizontal = FALSE, ylab = "centromeric index", xlab = "chromosome", las = 1, pch = 20, whisklty = 3, boxcol = "blue", boxfill = gray(0.95), boxlwd = 2, boxwex = 0.7, names = 1:50)
```

CAU boxplot put as an object
```
CAU_boxplot <- recordPlot()
```






# CCA 

#### list creation with each metaphase as a table

Vectors were written manually from measuring of each chromosome
```
CCA <- list (CcVi3CZ_5_10=data.frame(p1=p1, q1=q1, lenght1=p1+q1, d1=q1-p1, r1=q1/p1, i1=100/((q1/p1)+1)), CcVi3CZ_5_9 = data.frame(p2=p2, q2=q2, lenght2=p2+q2, d2=q2-p2, r2=q2/p2, i2=100/((q2/p2)+1)), CcVi3CZ_5_6=data.frame(p3=p3, q3=q3, lenght3=p3+q3, d3=q3-p3, r3=q3/p3, i3=100/((q3/p3)+1)), CcVi3CZ_5_5 = data.frame(p4=p4, q4=q4, lenght4=p4+q4, d4=q4-p4, r4=q4/p4, i4=100/((q4/p4)+1)), CcVi3CZ_2_3 = data.frame(p5=p5, q5=q5, lenght5=p5+q5, d5=q5-p5, r5=q5/p5, i5=100/((q5/p5)+1)), CcVi3CZ_3_5 = data.frame(p6=p6, q6=q6, lenght6=p6+q6, d6=q6-p6, r6=q6/p6, i6=100/((q6/p6)+1)), CcVi3CZ_3_4 = data.frame(p7=p7, q7=q7, lenght7=p7+q7, d7=q7-p7, r7=q7/p7, i7=100/((q7/p7)+1)), CcHe5Fi_1_1 = data.frame(p8=p8, q8=q8, lenght8=p8+q8, d8=q8-p8, r8=q8/p8, i8=100/((q8/p8)+1)), CcHe5Fi_2_1 = data.frame(p9=p9, q9=q9, lenght9=p9+q9, d9=q9-p9, r9=q9/p9, i9=100/((q9/p9)+1)), CcHe6Fi_1_2 = data.frame(p10=p10, q10=q10, lenght10=p10+q10, d10=q10-p10, r10=q10/p10, i10=100/((q10/p10)+1)))
```

#### decreasing order according centromeric index

```
CCA$CcHe5Fi_1_1 <- CCA$CcHe5Fi_1_1 [order(-CCA$CcHe5Fi_1_1$i8),]
CCA$CcHe5Fi_2_1 <- CCA$CcHe5Fi_2_1 [order(-CCA$CcHe5Fi_2_1$i9),]
CCA$CcHe6Fi_1_2 <- CCA$CcHe6Fi_1_2 [order(-CCA$CcHe6Fi_1_2$i10),]
CCA$CcVi3CZ_5_10 <- CCA$CcVi3CZ_5_10 [order(-CCA$CcVi3CZ_5_10$i1),]
CCA$CcVi3CZ_5_9 <- CCA$CcVi3CZ_5_9 [order(-CCA$CcVi3CZ_5_9$i2),]
CCA$CcVi3CZ_5_6 <- CCA$CcVi3CZ_5_6 [order(-CCA$CcVi3CZ_5_6$i3),]
CCA$CcVi3CZ_5_5 <- CCA$CcVi3CZ_5_5 [order(-CCA$CcVi3CZ_5_5$i4),]
CCA$CcVi3CZ_2_3 <- CCA$CcVi3CZ_2_3 [order(-CCA$CcVi3CZ_2_3$i5),]
CCA$CcVi3CZ_3_5 <- CCA$CcVi3CZ_3_5 [order(-CCA$CcVi3CZ_3_5$i6),]
CCA$CcVi3CZ_3_4 <- CCA$CcVi3CZ_3_4 [order(-CCA$CcVi3CZ_3_4$i7),]
CCA$CcHe5Fi_1_1 <- CCA$CcHe5Fi_1_1 [order(-CCA$CcHe5Fi_1_1$i8),]
CCA$CcHe5Fi_2_1 <- CCA$CcHe5Fi_2_1 [order(-CCA$CcHe5Fi_2_1$i9),]
CCA$CcHe6Fi_1_2 <- CCA$CcHe6Fi_1_2 [order(-CCA$CcHe6Fi_1_2$i10),]
```

#### "lenght_i" folder into CCA list
```
CCA$lenght_i <- data.frame(lenght1=CCA$CcVi3CZ_5_10$lenght1, lenght2=CCA$CcVi3CZ_5_9$lenght2, lenght3=CCA$CcVi3CZ_5_6$lenght3, lenght4=CCA$CcVi3CZ_5_5$lenght4, lenght5=CCA$CcVi3CZ_2_3$lenght5, lenght6=CCA$CcVi3CZ_3_5$lenght6, lenght7=CCA$CcVi3CZ_3_4$lenght7, lenght8=CCA$CcHe5Fi_1_1$lenght8, lenght9=CCA$CcHe5Fi_2_1$lenght9, lenght10=CCA$CcHe6Fi_1_2$lenght10, i1=CCA$CcVi3CZ_5_10$i1, i2=CCA$CcVi3CZ_5_9$i2, i3=CCA$CcVi3CZ_5_6$i3, i4=CCA$CcVi3CZ_5_5$i4, i5=CCA$CcVi3CZ_2_3$i5, i6=CCA$CcVi3CZ_3_5$i6, i7=CCA$CcVi3CZ_3_4$i7, i8= CCA$CcHe5Fi_1_1$i8, i9=CCA$CcHe5Fi_2_1$i9, i10=CCA$CcHe6Fi_1_2$i10)
```

#### "mean_lenght", "var_lenght", "mean_i" and "var_i" columns added into "lenght_i" folder of CCA list. It is not possible to create whole data frame using command with mean and variance. R language has to know other collumns first. Also, separately is created "mean_lenght/variance_lenght" and "mean_i/variance_i"
```
CCA$lenght_i <- data.frame(lenght1=CCA$CcVi3CZ_5_10$lenght1, lenght2=CCA$CcVi3CZ_5_9$lenght2, lenght3=CCA$CcVi3CZ_5_6$lenght3, lenght4=CCA$CcVi3CZ_5_5$lenght4, lenght5=CCA$CcVi3CZ_2_3$lenght5, lenght6=CCA$CcVi3CZ_3_5$lenght6, lenght7=CCA$CcVi3CZ_3_4$lenght7, lenght8=CCA$CcHe5Fi_1_1$lenght8, lenght9=CCA$CcHe5Fi_2_1$lenght9, lenght10=CCA$CcHe6Fi_1_2$lenght10, mean_lenght=apply (CCA$lenght_i[,1:10], 1, mean), variance_lenght=apply(CCA$lenght_i[,1:10], 1, var), i1=CCA$CcVi3CZ_5_10$i1, i2=CCA$CcVi3CZ_5_9$i2, i3=CCA$CcVi3CZ_5_6$i3, i4=CCA$CcVi3CZ_5_5$i4, i5=CCA$CcVi3CZ_2_3$i5, i6=CCA$CcVi3CZ_3_5$i6, i7=CCA$CcVi3CZ_3_4$i7, i8= CCA$CcHe5Fi_1_1$i8, i9=CCA$CcHe5Fi_2_1$i9, i10=CCA$CcHe6Fi_1_2$i10)
CCA$lenght_i <- data.frame(lenght1=CCA$CcVi3CZ_5_10$lenght1, lenght2=CCA$CcVi3CZ_5_9$lenght2, lenght3=CCA$CcVi3CZ_5_6$lenght3, lenght4=CCA$CcVi3CZ_5_5$lenght4, lenght5=CCA$CcVi3CZ_2_3$lenght5, lenght6=CCA$CcVi3CZ_3_5$lenght6, lenght7=CCA$CcVi3CZ_3_4$lenght7, lenght8=CCA$CcHe5Fi_1_1$lenght8, lenght9=CCA$CcHe5Fi_2_1$lenght9, lenght10=CCA$CcHe6Fi_1_2$lenght10, mean_lenght=apply (CCA$lenght_i[,1:10], 1, mean), variance_lenght=apply(CCA$lenght_i[,1:10], 1, var), i1=CCA$CcVi3CZ_5_10$i1, i2=CCA$CcVi3CZ_5_9$i2, i3=CCA$CcVi3CZ_5_6$i3, i4=CCA$CcVi3CZ_5_5$i4, i5=CCA$CcVi3CZ_2_3$i5, i6=CCA$CcVi3CZ_3_5$i6, i7=CCA$CcVi3CZ_3_4$i7, i8= CCA$CcHe5Fi_1_1$i8, i9=CCA$CcHe5Fi_2_1$i9, i10=CCA$CcHe6Fi_1_2$i10, mean_i=apply (CCA$lenght_i[,13:22], 1, mean), variance_i=apply(CCA$lenght_i[,13:22], 1, var))
```

#### additional column for "mean_i_corrected"

each value where the number is zero more then 5 times is considered to be zero in mean.
```
CCA$lenght_i$mean_i_corrected <- apply (CCA$lenght_i[,13:22], 1, mean)
CCA$lenght_i[59:74, "mean_i_corrected"] <- 0
```

#### a new column "category" of each chromosome
```
for(i in 1:100) {if(CCA$lenght_i$mean_i_corrected[i]>=35.5) {CCA$lenght_i$category[i] = "m"} else if (CCA$lenght_i$mean_i_corrected[i]>=25 & CCA$lenght_i$mean_i_corrected[i]<35.5){CCA$lenght_i$category[i] = "sm"} else if (CCA$lenght_i$mean_i_corrected[i]>=12.5 & CCA$lenght_i$mean_i_corrected[i]<25){CCA$lenght_i$category[i] = "st"} else if (CCA$lenght_i$mean_i_corrected[i]>0 & CCA$lenght_i$mean_i_corrected[i]<12.5) {CCA$lenght_i$category[i] = "a"} else {CCA$lenght_i$category[i] = "T"}}
``` 

#### CCA dotplot creation
```
plot(CCA$lenght_i$mean_i, CCA$lenght_i$mean_lenght, pch=16, col="red", ylim = c(15, 45), xlab = "centromeric index", ylab = "chromosomal length", ann=TRUE, las=1, abline(v=c(0, 12.5, 25, 35.5), col="gray", lty=2))
```
```
CCA_dotplot <- recordPlot()
```

#### CCA boxplot creation

##### function for creation of 50 vectors = 50 homologous chromosomal pairs. The first vector from all first two lines of "i" (centromeric index) of each folder (data frame) = chromosome with the highest centromeric index (chromosome1)

```
Select_chrome <- function(i,j){
     chromosome <- c(CCA$CcVi3CZ_5_10$i1[i:j],
                     CCA$CcVi3CZ_5_9$i2[i:j], CCA$CcVi3CZ_5_6$i3[i:j], CCA$CcVi3CZ_5_5$i4[i:j],
                     CCA$CcVi3CZ_2_3$i5[i:j], CCA$CcVi3CZ_3_5$i6[i:j], CCA$CcVi3CZ_3_4$i7[i:j],
                     CCA$CcHe5Fi_1_1$i8[i:j], CCA$CcHe5Fi_2_1$i9[i:j], CCA$CcHe6Fi_1_2$i10[i:j])
 }
```
```
chromosome1 <- Select_chrome(1,2)
chromosome2 <- Select_chrome(3,4)
chromosome3 <- Select_chrome(5,6)
chromosome4 <- Select_chrome(7,8)
chromosome5 <- Select_chrome(9,10)
chromosome6 <- Select_chrome(11,12)
chromosome7 <- Select_chrome(13,14)
chromosome8 <- Select_chrome(15,16)
chromosome9 <- Select_chrome(17,18)
chromosome10 <- Select_chrome(19,20)
chromosome11 <- Select_chrome(21,22)
chromosome12 <- Select_chrome(23,24)
chromosome13 <- Select_chrome(25,26)
chromosome14 <- Select_chrome(27,28)
chromosome15 <- Select_chrome(29,30)
chromosome16 <- Select_chrome(31,32)
chromosome17 <- Select_chrome(33,34)
chromosome18 <- Select_chrome(35,36)
chromosome19 <- Select_chrome(37,38)
chromosome20 <- Select_chrome(39,40)
chromosome21 <- Select_chrome(41,42)
chromosome22 <- Select_chrome(43,44)
chromosome23 <- Select_chrome(45,46)
chromosome24 <- Select_chrome(47,48)
chromosome25 <- Select_chrome(49,50)
chromosome26 <- Select_chrome(51,52)
chromosome27 <- Select_chrome(53,54)
chromosome28 <- Select_chrome(55,56)
chromosome29 <- Select_chrome(57,58)
chromosome30 <- Select_chrome(59,60)
chromosome31 <- Select_chrome(61,62)
chromosome32 <- Select_chrome(63,64)
chromosome33 <- Select_chrome(65,66)
chromosome34 <- Select_chrome(67,68)
chromosome35 <- Select_chrome(69,70)
chromosome36 <- Select_chrome(71,72)
chromosome37 <- Select_chrome(73,74)
chromosome38 <- Select_chrome(75,76)
chromosome39 <- Select_chrome(77,78)
chromosome40 <- Select_chrome(79,80)
chromosome41 <- Select_chrome(81,82)
chromosome42 <- Select_chrome(83,84)
chromosome43 <- Select_chrome(85,86)
chromosome44 <- Select_chrome(87,88)
chromosome45 <- Select_chrome(89,90)
chromosome46 <- Select_chrome(91,92)
chromosome47 <- Select_chrome(93,94)
chromosome48 <- Select_chrome(95,96)
chromosome49 <- Select_chrome(97,98)
chromosome50 <- Select_chrome(99,100)
```

```
boxplot(chromosome1, chromosome2, chromosome3, chromosome4, chromosome5, chromosome6, chromosome7, chromosome8, chromosome9, chromosome10, chromosome11, chromosome12, chromosome13, chromosome14, chromosome15, chromosome16, chromosome17, chromosome18, chromosome19, chromosome20, chromosome21, chromosome22, chromosome23, chromosome24, chromosome25, chromosome26, chromosome27, chromosome28, chromosome29, chromosome30, chromosome31, chromosome32, chromosome33, chromosome34, chromosome35, chromosome36, chromosome37, chromosome38, chromosome39, chromosome40, chromosome41, chromosome42, chromosome43, chromosome44, chromosome45, chromosome46, chromosome47, chromosome48, chromosome49, chromosome50, ylim=c(-1, 50), xlim=c(1, 50), horizontal = FALSE, ylab = "centromeric index", xlab = "chromosome", las = 1, pch = 20, whisklty = 3, boxcol = "red", boxfill = gray(0.95), boxlwd = 2, boxwex = 0.7, names = 1:50)
```

CCA boxplot put as an object
```
CCA_boxplot <- recordPlot()
```










# CGI 

#### list creation with each metaphase as a table

Vectors were written manually from measuring of each chromosome
```
CGI <- list (CGI_D10_6g=data.frame(p1=p1, q1=q1, lenght=p1+q1, d1=q1-p1, r1=q1/p1, i1=100/((q1/p1)+1)), CGI_D5_9g = data.frame(p2=p2, q2=q2, lenght=p2+q2, d2=q2-p2, r2=q2/p2, i2=100/((q2/p2)+1)), CGI_X7_2_7=data.frame(p3=p3, q3=q3, lenght=p3+q3, d3=q3-p3, r3=q3/p3, i3=100/((q3/p3)+1)), CGI_D10_4g = data.frame(p4=p4, q4=q4, lenght=p4+q4, d4=q4-p4, r4=q4/p4, i4=100/((q4/p4)+1)), CGI_H15_7g = data.frame(p5=p5, q5=q5, lenght=p5+q5, d5=q5-p5, r5=q5/p5, i5=100/((q5/p5)+1)), CGI_D5_2g = data.frame(p6=p6, q6=q6, lenght=p6+q6, d6=q6-p6, r6=q6/p6, i6=100/((q6/p6)+1)), CGI_D5_8g = data.frame(p7=p7, q7=q7, lenght=p7+q7, d7=q7-p7, r7=q7/p7, i7=100/((q7/p7)+1)), CGI_X9_2_1_5 = data.frame(p8=p8, q8=q8, lenght=p8+q8, d8=q8-p8, r8=q8/p8, i8=100/((q8/p8)+1)), CGI_X9_2_1_10 = data.frame(p9=p9, q9=q9, lenght=p9+q9, d9=q9-p9, r9=q9/p9, i9=100/((q9/p9)+1)), CGI_D11_7g = data.frame(p10=p10, q10=q10, lenght=p10+q10, d10=q10-p10, r10=q10/p10, i10=100/((q10/p10)+1)))
```

#### decreasing order according centromeric index
```
CGI$CGI_D10_6g <- CGI$CGI_D10_6g [order(-CGI$CGI_D10_6g$i1),]
CGI$CGI_D5_9g <- CGI$CGI_D5_9g [order(-CGI$CGI_D5_9g$i2),]
CGI$CGI_X7_2_7 <- CGI$CGI_X7_2_7 [order(-CGI$CGI_X7_2_7$i3),]
CGI$CGI_D10_4g <- CGI$CGI_D10_4g [order(-CGI$CGI_D10_4g$i4),]
CGI$CGI_H15_7g <- CGI$CGI_H15_7g [order(-CGI$CGI_H15_7g$i5),]
CGI$CGI_D5_2g <- CGI$CGI_D5_2g [order(-CGI$CGI_D5_2g$i6),]
CGI$CGI_D5_8g <- CGI$CGI_D5_8g [order(-CGI$CGI_D5_8g$i7),]
CGI$CGI_X9_2_1_5 <- CGI$CGI_X9_2_1_5 [order(-CGI$CGI_X9_2_1_5$i8),]
CGI$CGI_X9_2_1_10 <- CGI$CGI_X9_2_1_10 [order(-CGI$CGI_X9_2_1_10$i9),]
CGI$CGI_D11_7g <- CGI$CGI_D11_7g [order(-CGI$CGI_D11_7g$i10),]
```

#### "lenght_i" folder into CGI list
```
CGI$length_i <- data.frame(length1=CGI$CGI_D10_6g$lenght, lenght2=CGI$CGI_D5_9g$lenght, lenght3=CGI$CGI_X7_2_7$lenght, lenght4=CGI$CGI_D10_4g$lenght, lenght5=CGI$CGI_H15_7g$lenght, lenght6=CGI$CGI_D5_2g$lenght, lenght7=CGI$CGI_D5_8g$lenght, lenght8=CGI$CGI_X9_2_1_5$lenght, lenght9=CGI$CGI_X9_2_1_10$lenght, lenght10=CGI$CGI_D11_7g$lenght, i1=CGI$CGI_D10_6g$i1, i2=CGI$CGI_D5_9g$i2, i3=CGI$CGI_X7_2_7$i3, i4=CGI$CGI_D10_4g$i4, i5=CGI$CGI_H15_7g$i5, i6=CGI$CGI_D5_2g$i6, i7=CGI$CGI_D5_8g$i7, i8=CGI$CGI_X9_2_1_5$i8, i9=CGI$CGI_X9_2_1_10$i9, i10=CGI$CGI_D11_7g$i10)
```

#### "mean_lenght", "var_lenght", "mean_i" and "var_i" columns added into "lenght_i" folder of CGI list. It is not possible to create whole data frame using command with mean and variance. R language has to know other collumns first. Also, separately is created "mean_lenght/variance_lenght" and "mean_i/variance_i"
```
CGI$lenght_i <- data.frame(lenght1=CGI$CGI_D10_6g$lenght, lenght2=CGI$CGI_D5_9g$lenght, lenght3=CGI$CGI_X7_2_7$lenght, lenght4=CGI$CGI_D10_4g$lenght, lenght5=CGI$CGI_H15_7g$lenght, lenght6=CGI$CGI_D5_2g$lenght, lenght7=CGI$CGI_D5_8g$lenght, lenght8=CGI$CGI_X9_2_1_5$lenght, lenght9=CGI$CGI_X9_2_1_10$lenght, lenght10=CGI$CGI_D11_7g$lenght, mean_lenght=apply (CGI$lenght_i[,1:10], 1, mean), variance_lenght=apply(CGI$lenght_i[,1:10], 1, var), i1=CGI$CGI_D10_6g$i1, i2=CGI$CGI_D5_9g$i2, i3=CGI$CGI_X7_2_7$i3, i4=CGI$CGI_D10_4g$i4, i5=CGI$CGI_H15_7g$i5, i6=CGI$CGI_D5_2g$i6, i7=CGI$CGI_D5_8g$i7, i8=CGI$CGI_X9_2_1_5$i8, i9=CGI$CGI_X9_2_1_10$i9, i10=CGI$CGI_D11_7g$i10)
CGI$lenght_i <- data.frame(lenght1=CGI$CGI_D10_6g$lenght, lenght2=CGI$CGI_D5_9g$lenght, lenght3=CGI$CGI_X7_2_7$lenght, lenght4=CGI$CGI_D10_4g$lenght, lenght5=CGI$CGI_H15_7g$lenght, lenght6=CGI$CGI_D5_2g$lenght, lenght7=CGI$CGI_D5_8g$lenght, lenght8=CGI$CGI_X9_2_1_5$lenght, lenght9=CGI$CGI_X9_2_1_10$lenght, lenght10=CGI$CGI_D11_7g$lenght, mean_lenght=apply (CGI$lenght_i[,1:10], 1, mean), variance_lenght=apply(CGI$lenght_i[,1:10], 1, var), i1=CGI$CGI_D10_6g$i1, i2=CGI$CGI_D5_9g$i2, i3=CGI$CGI_X7_2_7$i3, i4=CGI$CGI_D10_4g$i4, i5=CGI$CGI_H15_7g$i5, i6=CGI$CGI_D5_2g$i6, i7=CGI$CGI_D5_8g$i7, i8=CGI$CGI_X9_2_1_5$i8, i9=CGI$CGI_X9_2_1_10$i9, i10=CGI$CGI_D11_7g$i10, mean_i=apply (CGI$lenght_i[,13:22], 1, mean), variance_i=apply(CGI$lenght_i[,13:22], 1, var))
```

#### additional column for "mean_i_corrected" 

each value where the number is zero more then 5 times is considered to be zero in mean.
```
CGI$lenght_i$mean_i_corrected <- apply (CGI$lenght_i[,13:22], 1, mean)
CGI$lenght_i[51:75, "mean_i_corrected"] <- 0
```

#### a new column "category" of each chromosome
```
for(i in 1:100) {if(CGI$lenght_i$mean_i_corrected[i]>=35.5) {CGI$lenght_i$category[i] = "m"} else if (CGI$lenght_i$mean_i_corrected[i]>=25 & CGI$lenght_i$mean_i_corrected[i]<35.5){CGI$lenght_i$category[i] = "sm"} else if (CGI$lenght_i$mean_i_corrected[i]>=12.5 & CGI$lenght_i$mean_i_corrected[i]<25){CGI$lenght_i$category[i] = "st"} else if (CGI$lenght_i$mean_i_corrected[i]>0 & CGI$lenght_i$mean_i_corrected[i]<12.5) {CGI$lenght_i$category[i] = "a"} else {CGI$lenght_i$category[i] = "T"}}
```

#### CGI dotplot creation
```
plot(CGI$lenght_i$mean_i, CGI$lenght_i$mean_lenght, pch=16, col="yellow3", ylim = c(15, 45), xlab = "centromeric index", ylab = "chromosomal length", ann=TRUE, las=1, abline(v=c(0, 12.5, 25, 35.5), col="gray", lty=2))
```
```
CGI_dotplot <- recordPlot()
```

#### CGI boxplot creation

##### function for creation of 50 vectors = 50 homologous chromosomal pairs. The first vector from all first two lines of "i" (centromeric index) of each folder (data frame) = chromosome with the highest centromeric index (chromosome1)

```
> Select_chrome <- function(i,j) {chromosome <- c(CGI$CGI_D10_6g$i1[i:j], CGI$CGI_D5_9g$i2[i:j], CGI$CGI_X7_2_7$i3[i:j], CGI$CGI_D10_4g$i4[i:j], CGI$CGI_H15_7g$i5[i:j], CGI$CGI_D5_2g$i6[i:j], CGI$CGI_D5_8g$i7[i:j], CGI$CGI_X9_2_1_5$i8[i:j], CGI$CGI_X9_2_1_10$i9[i:j], CGI$CGI_D11_7g$i10[i:j])}
```

```
  <- Select_chrome(99,100)
```

```
boxplot(chromosome1, chromosome2, chromosome3, chromosome4, chromosome5, chromosome6, chromosome7, chromosome8, chromosome9, chromosome10, chromosome11, chromosome12, chromosome13, chromosome14, chromosome15, chromosome16, chromosome17, chromosome18, chromosome19, chromosome20, chromosome21, chromosome22, chromosome23, chromosome24, chromosome25, chromosome26, chromosome27, chromosome28, chromosome29, chromosome30, chromosome31, chromosome32, chromosome33, chromosome34, chromosome35, chromosome36, chromosome37, chromosome38, chromosome39, chromosome40, chromosome41, chromosome42, chromosome43, chromosome44, chromosome45, chromosome46, chromosome47, chromosome48, chromosome49, chromosome50, ylim=c(-1, 50), xlim=c(1, 50), horizontal = FALSE, ylab = "centromeric index", xlab = "chromosome", las = 1, pch = 20, whisklty = 3, boxcol = "yellow3", boxfill = gray(0.95), boxlwd = 2, boxwex = 0.7, names = 1:50)
```

CGI boxplot put as an object:
```
CGI_boxplot <- recordPlot()
```









#### assign of category to each chromosome in the "mean_i_corrected" folder

for(i in 1:100) {if(CGI$lenght_i$mean_i_corrected[i]>=35.5) {CGI$lenght_i$category[i] = "m"} else if (CGI$lenght_i$mean_i_corrected[i]>=25 & CGI$lenght_i$mean_i_corrected[i]<35.5){CGI$lenght_i$category[i] = "sm"} else if (CGI$lenght_i$mean_i_corrected[i]>=12.5 & CGI$lenght_i$mean_i_corrected[i]<25){CGI$lenght_i$category[i] = "st"} else if (CGI$lenght_i$mean_i_corrected[i]>0 & CGI$lenght_i$mean_i_corrected[i]<12.5) {CGI$lenght_i$category[i] = "a"} else {CGI$lenght_i$category[i] = "T"}}

#### assign of category to each chromosome in the first folder (CGI_D10_6g) of CGI list
```
for(i in 1:100) {if(CGI$CGI_D10_6g$i1[i]>=35.5) {CGI$CGI_D10_6g$category[i] = "m"} else if (CGI$CGI_D10_6g$i1[i]>=25 & CGI$CGI_D10_6g$i1[i]<35.5){CGI$CGI_D10_6g$category[i] = "sm"} else if (CGI$CGI_D10_6g$i1[i]>=12.5 & CGI$CGI_D10_6g$i1[i]<25){CGI$CGI_D10_6g$category[i] = "st"} else if (CGI$CGI_D10_6g$i1[i]>0 & CGI$CGI_D10_6g$i1[i]<12.5) {CGI$CGI_D10_6g$category[i] = "a"} else {CGI$CGI_D10_6g$category[i] = "T"}}
```
```
CGI$CGI_D10_6g <- CGI$CGI_D10_6g[order(CGI$CGI_D10_6g$category, -CGI$CGI_D10_6g$lenght),]
```

#### assign of category to each chromosome in the second folder (CGI_D5_9g) of CGI list
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












# All lists (CAU, CCA, CGI) put together in one environment

all three scripts (CAU, CCA, CGI) uploaded (CAU as the last one) = CAU chromosome1-50 remained on the environment

#### Put all dotplots on one pic and put all boxplots together as a single plot

```
(par_dotplot <- par(mfcol=c(3,1), mai=c(0.53,0.55,0.17,0.1), font=3))
```
```
plot(CAU$lenght_i$mean_i, CAU$lenght_i$mean_lenght, pch=16, col="blue", ylim = c(15, 45), xlab = "centromeric index", ylab = "chromosomal length", ann=TRUE, las=1, abline(v=c(0, 12.5, 25, 35.5), col="gray", lty=2))
```
```
legend("bottomright", legend = "Carassius auratus", pch = 16, col = "blue")
```
```
plot(CCA$lenght_i$mean_i, CCA$lenght_i$mean_lenght, pch=16, col="red", ylim = c(15, 45), xlab = "centromeric index", ylab = "chromosomal length", ann=TRUE, las=1, abline(v=c(0, 12.5, 25, 35.5), col="gray", lty=2))
```
```
legend("bottomright", legend = "Carassius carassius", pch = 16, col = "red")
```
```
plot(CGI$lenght_i$mean_i, CGI$lenght_i$mean_lenght, pch=16, col="yellow3", ylim = c(15, 45), xlab = "centromeric index", ylab = "chromosomal length", ann=TRUE, las=1, abline(v=c(0, 12.5, 25, 35.5), col="gray", lty=2))
```
```
legend("topright", legend = "Carassius gibelio", pch = 16, col = "yellow3")
```
```
CAU_CCA_CGI_dotplot <- recordPlot
```
```
paste0("chromosome", 1:50, "=chromosome", 1:50, collapse = ",")
```
[1] "chromosome1=chromosome1,chromosome2=chromosome2,chromosome3=chromosome3,chromosome4=chromosome4,chromosome5=chromosome5,chromosome6=chromosome6,chromosome7=chromosome7,chromosome8=chromosome8,chromosome9=chromosome9,chromosome10=chromosome10,chromosome11=chromosome11,chromosome12=chromosome12,chromosome13=chromosome13,chromosome14=chromosome14,chromosome15=chromosome15,chromosome16=chromosome16,chromosome17=chromosome17,chromosome18=chromosome18,chromosome19=chromosome19,chromosome20=chromosome20,chromosome21=chromosome21,chromosome22=chromosome22,chromosome23=chromosome23,chromosome24=chromosome24,chromosome25=chromosome25,chromosome26=chromosome26,chromosome27=chromosome27,chromosome28=chromosome28,chromosome29=chromosome29,chromosome30=chromosome30,chromosome31=chromosome31,chromosome32=chromosome32,chromosome33=chromosome33,chromosome34=chromosome34,chromosome35=chromosome35,chromosome36=chromosome36,chromosome37=chromosome37,chromosome38=chromosome38,chromosome39=chromosome39,chromosome40=chromosome40,chromosome41=chromosome41,chromosome42=chromosome42,chromosome43=chromosome43,chromosome44=chromosome44,chromosome45=chromosome45,chromosome46=chromosome46,chromosome47=chromosome47,chromosome48=chromosome48,chromosome49=chromosome49,chromosome50=chromosome50"

The result of the command "paste()" put into the keyboard and paste as a new command behind the "list()"
```
list(chromosome1=chromosome1,chromosome2=chromosome2,chromosome3=chromosome3,chromosome4=chromosome4,chromosome5=chromosome5,chromosome6=chromosome6,chromosome7=chromosome7,chromosome8=chromosome8,chromosome9=chromosome9,chromosome10=chromosome10,chromosome11=chromosome11,chromosome12=chromosome12,chromosome13=chromosome13,chromosome14=chromosome14,chromosome15=chromosome15,chromosome16=chromosome16,chromosome17=chromosome17,chromosome18=chromosome18,chromosome19=chromosome19,chromosome20=chromosome20,chromosome21=chromosome21,chromosome22=chromosome22,chromosome23=chromosome23,chromosome24=chromosome24,chromosome25=chromosome25,chromosome26=chromosome26,chromosome27=chromosome27,chromosome28=chromosome28,chromosome29=chromosome29,chromosome30=chromosome30,chromosome31=chromosome31,chromosome32=chromosome32,chromosome33=chromosome33,chromosome34=chromosome34,chromosome35=chromosome35,chromosome36=chromosome36,chromosome37=chromosome37,chromosome38=chromosome38,chromosome39=chromosome39,chromosome40=chromosome40,chromosome41=chromosome41,chromosome42=chromosome42,chromosome43=chromosome43,chromosome44=chromosome44,chromosome45=chromosome45,chromosome46=chromosome46,chromosome47=chromosome47,chromosome48=chromosome48,chromosome49=chromosome49,chromosome50=chromosome50)
```

#### remove chromosome1-50 and p/q vectors from CAU and put chromosomes from another (CCA) species
```
paste0("chromosome", 1:50, collapse = ",")
```
[1] "chromosome1,chromosome2,chromosome3,chromosome4,chromosome5,chromosome6,chromosome7,chromosome8,chromosome9,chromosome10,chromosome11,chromosome12,chromosome13,chromosome14,chromosome15,chromosome16,chromosome17,chromosome18,chromosome19,chromosome20,chromosome21,chromosome22,chromosome23,chromosome24,chromosome25,chromosome26,chromosome27,chromosome28,chromosome29,chromosome30,chromosome31,chromosome32,chromosome33,chromosome34,chromosome35,chromosome36,chromosome37,chromosome38,chromosome39,chromosome40,chromosome41,chromosome42,chromosome43,chromosome44,chromosome45,chromosome46,chromosome47,chromosome48,chromosome49,chromosome50"

```
CAU_chrome1_50 <- list(chromosome1=chromosome1,chromosome2=chromosome2,chromosome3=chromosome3,chromosome4=chromosome4,chromosome5=chromosome5,chromosome6=chromosome6,chromosome7=chromosome7,chromosome8=chromosome8,chromosome9=chromosome9,chromosome10=chromosome10,chromosome11=chromosome11,chromosome12=chromosome12,chromosome13=chromosome13,chromosome14=chromosome14,chromosome15=chromosome15,chromosome16=chromosome16,chromosome17=chromosome17,chromosome18=chromosome18,chromosome19=chromosome19,chromosome20=chromosome20,chromosome21=chromosome21,chromosome22=chromosome22,chromosome23=chromosome23,chromosome24=chromosome24,chromosome25=chromosome25,chromosome26=chromosome26,chromosome27=chromosome27,chromosome28=chromosome28,chromosome29=chromosome29,chromosome30=chromosome30,chromosome31=chromosome31,chromosome32=chromosome32,chromosome33=chromosome33,chromosome34=chromosome34,chromosome35=chromosome35,chromosome36=chromosome36,chromosome37=chromosome37,chromosome38=chromosome38,chromosome39=chromosome39,chromosome40=chromosome40,chromosome41=chromosome41,chromosome42=chromosome42,chromosome43=chromosome43,chromosome44=chromosome44,chromosome45=chromosome45,chromosome46=chromosome46,chromosome47=chromosome47,chromosome48=chromosome48,chromosome49=chromosome49,chromosome50=chromosome50)
```
```
rm(chromosome1,chromosome2,chromosome3,chromosome4,chromosome5,chromosome6,chromosome7,chromosome8,chromosome9,chromosome10,chromosome11,chromosome12,chromosome13,chromosome14,chromosome15,chromosome16,chromosome17,chromosome18,chromosome19,chromosome20,chromosome21,chromosome22,chromosome23,chromosome24,chromosome25,chromosome26,chromosome27,chromosome28,chromosome29,chromosome30,chromosome31,chromosome32,chromosome33,chromosome34,chromosome35,chromosome36,chromosome37,chromosome38,chromosome39,chromosome40,chromosome41,chromosome42,chromosome43,chromosome44,chromosome45,chromosome46,chromosome47,chromosome48,chromosome49,chromosome50)
```
#### CCA environment uploaded

```
CCA_chrome1_50 <- list(chromosome1=chromosome1,chromosome2=chromosome2,chromosome3=chromosome3,chromosome4=chromosome4,chromosome5=chromosome5,chromosome6=chromosome6,chromosome7=chromosome7,chromosome8=chromosome8,chromosome9=chromosome9,chromosome10=chromosome10,chromosome11=chromosome11,chromosome12=chromosome12,chromosome13=chromosome13,chromosome14=chromosome14,chromosome15=chromosome15,chromosome16=chromosome16,chromosome17=chromosome17,chromosome18=chromosome18,chromosome19=chromosome19,chromosome20=chromosome20,chromosome21=chromosome21,chromosome22=chromosome22,chromosome23=chromosome23,chromosome24=chromosome24,chromosome25=chromosome25,chromosome26=chromosome26,chromosome27=chromosome27,chromosome28=chromosome28,chromosome29=chromosome29,chromosome30=chromosome30,chromosome31=chromosome31,chromosome32=chromosome32,chromosome33=chromosome33,chromosome34=chromosome34,chromosome35=chromosome35,chromosome36=chromosome36,chromosome37=chromosome37,chromosome38=chromosome38,chromosome39=chromosome39,chromosome40=chromosome40,chromosome41=chromosome41,chromosome42=chromosome42,chromosome43=chromosome43,chromosome44=chromosome44,chromosome45=chromosome45,chromosome46=chromosome46,chromosome47=chromosome47,chromosome48=chromosome48,chromosome49=chromosome49,chromosome50=chromosome50)
```
```
rm(chromosome1,chromosome2,chromosome3,chromosome4,chromosome5,chromosome6,chromosome7,chromosome8,chromosome9,chromosome10,chromosome11,chromosome12,chromosome13,chromosome14,chromosome15,chromosome16,chromosome17,chromosome18,chromosome19,chromosome20,chromosome21,chromosome22,chromosome23,chromosome24,chromosome25,chromosome26,chromosome27,chromosome28,chromosome29,chromosome30,chromosome31,chromosome32,chromosome33,chromosome34,chromosome35,chromosome36,chromosome37,chromosome38,chromosome39,chromosome40,chromosome41,chromosome42,chromosome43,chromosome44,chromosome45,chromosome46,chromosome47,chromosome48,chromosome49,chromosome50)
```




```
(par_boxplot <- par(mfcol=c(3,1), mai=c(0.53,0.55,0.1,0.1), font = 4))
```
```
boxplot(CAU_chrome1_50, ylim=c(-1, 50), xlim=c(1, 50), horizontal = FALSE, ylab = "centromeric index", xlab = "chromosome", las = 1, whisklty = 3, boxcol = "blue", boxfill = gray(0.95), boxlwd = 2, boxwex = 0.7, names = 1:50)
```
```
text(51, 40, "Carassius auratus", col = "blue", adj = 1)
```
```
boxplot(CCA_chrome1_50, ylim=c(-1, 50), xlim=c(1, 50), horizontal = FALSE, ylab = "centromeric index", xlab = "chromosome", las = 1, whisklty = 3, boxcol = "red", boxfill = gray(0.95), boxlwd = 2, boxwex = 0.7, names = 1:50)
```
```
text(51, 40, "Carassius carassius", col = "red", adj = 1)
```
```
boxplot(CGI_chrome1_50, ylim=c(-1, 50), xlim=c(1, 50), horizontal = FALSE, ylab = "centromeric index", xlab = "chromosome", las = 1, whisklty = 3, boxcol = "yellow3", boxfill = gray(0.95), boxlwd = 2, boxwex = 0.7, names = 1:50)
```
```
text(51, 40, "Carassius gibelio", col = "yellow3", adj = 1)
```
```
CAU_CCA_CGI_boxplot <- recordPlot
```


#### boxplot for each chromosome separately for comparison in each species

```
par_boxplot_supplement <- par(mfcol=c(25,2), mar=c(0.1,2,0.1,0.1), cex.axis = 0.7, ann = F, font = 2, las = 1, yaxp = c(0, 50, 10), xaxt = "n")
```
```
par(par_boxplot_supplement)
```
```
for (i in 1:50) {cat(paste0("boxplot(CAU_chrome1_50$chromosome", i, ", CCA_chrome1_50$chromosome", i, ", CGI_chrome1_50$chromosome", i), ", ylim = c(1, 50), ylab = 'centromeric index', xlab =", paste0("'chromosome", i,"',"), " whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5)", "\n", paste0('text(3.6, 30, "chr',i,'", adj = 1)'), "\n")}
```

copied and pastee entire concateneted text and added grid(col = "lightgray") into boxplots of chr8, 11-31. Boxplots were evaluated usinf function "stats" and CAU with CGI vary in values of the second and third quartile.
```
boxplot(CAU_chrome1_50$chromosome1, CCA_chrome1_50$chromosome1, CGI_chrome1_50$chromosome1 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome1',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr1", adj = 1) 
boxplot(CAU_chrome1_50$chromosome2, CCA_chrome1_50$chromosome2, CGI_chrome1_50$chromosome2 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome2',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr2", adj = 1) 
boxplot(CAU_chrome1_50$chromosome3, CCA_chrome1_50$chromosome3, CGI_chrome1_50$chromosome3 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome3',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr3", adj = 1) 
boxplot(CAU_chrome1_50$chromosome4, CCA_chrome1_50$chromosome4, CGI_chrome1_50$chromosome4 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome4',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr4", adj = 1) 
boxplot(CAU_chrome1_50$chromosome5, CCA_chrome1_50$chromosome5, CGI_chrome1_50$chromosome5 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome5',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr5", adj = 1) 
boxplot(CAU_chrome1_50$chromosome6, CCA_chrome1_50$chromosome6, CGI_chrome1_50$chromosome6 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome6',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr6", adj = 1) 
boxplot(CAU_chrome1_50$chromosome7, CCA_chrome1_50$chromosome7, CGI_chrome1_50$chromosome7 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome7',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr7", adj = 1) 
boxplot(CAU_chrome1_50$chromosome8, CCA_chrome1_50$chromosome8, CGI_chrome1_50$chromosome8 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome8',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr8", adj = 1, grid(col = "lightgray")) 
boxplot(CAU_chrome1_50$chromosome9, CCA_chrome1_50$chromosome9, CGI_chrome1_50$chromosome9 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome9',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr9", adj = 1) 
boxplot(CAU_chrome1_50$chromosome10, CCA_chrome1_50$chromosome10, CGI_chrome1_50$chromosome10 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome10',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr10", adj = 1) 
boxplot(CAU_chrome1_50$chromosome11, CCA_chrome1_50$chromosome11, CGI_chrome1_50$chromosome11 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome11',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr11", adj = 1, grid(col = "lightgray")) 
boxplot(CAU_chrome1_50$chromosome12, CCA_chrome1_50$chromosome12, CGI_chrome1_50$chromosome12 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome12',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr12", adj = 1, grid(col = "lightgray")) 
boxplot(CAU_chrome1_50$chromosome13, CCA_chrome1_50$chromosome13, CGI_chrome1_50$chromosome13 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome13',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr13", adj = 1, grid(col = "lightgray")) 
boxplot(CAU_chrome1_50$chromosome14, CCA_chrome1_50$chromosome14, CGI_chrome1_50$chromosome14 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome14',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr14", adj = 1, grid(col = "lightgray")) 
boxplot(CAU_chrome1_50$chromosome15, CCA_chrome1_50$chromosome15, CGI_chrome1_50$chromosome15 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome15',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr15", adj = 1, grid(col = "lightgray")) 
boxplot(CAU_chrome1_50$chromosome16, CCA_chrome1_50$chromosome16, CGI_chrome1_50$chromosome16 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome16',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr16", adj = 1, grid(col = "lightgray")) 
boxplot(CAU_chrome1_50$chromosome17, CCA_chrome1_50$chromosome17, CGI_chrome1_50$chromosome17 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome17',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr17", adj = 1, grid(col = "lightgray")) 
boxplot(CAU_chrome1_50$chromosome18, CCA_chrome1_50$chromosome18, CGI_chrome1_50$chromosome18 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome18',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr18", adj = 1, grid(col = "lightgray")) 
boxplot(CAU_chrome1_50$chromosome19, CCA_chrome1_50$chromosome19, CGI_chrome1_50$chromosome19 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome19',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr19", adj = 1, grid(col = "lightgray")) 
boxplot(CAU_chrome1_50$chromosome20, CCA_chrome1_50$chromosome20, CGI_chrome1_50$chromosome20 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome20',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr20", adj = 1, grid(col = "lightgray")) 
boxplot(CAU_chrome1_50$chromosome21, CCA_chrome1_50$chromosome21, CGI_chrome1_50$chromosome21 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome21',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr21", adj = 1, grid(col = "lightgray")) 
boxplot(CAU_chrome1_50$chromosome22, CCA_chrome1_50$chromosome22, CGI_chrome1_50$chromosome22 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome22',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr22", adj = 1, grid(col = "lightgray")) 
boxplot(CAU_chrome1_50$chromosome23, CCA_chrome1_50$chromosome23, CGI_chrome1_50$chromosome23 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome23',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr23", adj = 1, grid(col = "lightgray")) 
boxplot(CAU_chrome1_50$chromosome24, CCA_chrome1_50$chromosome24, CGI_chrome1_50$chromosome24 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome24',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr24", adj = 1, grid(col = "lightgray")) 
boxplot(CAU_chrome1_50$chromosome25, CCA_chrome1_50$chromosome25, CGI_chrome1_50$chromosome25 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome25',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr25", adj = 1, grid(col = "lightgray")) 
boxplot(CAU_chrome1_50$chromosome26, CCA_chrome1_50$chromosome26, CGI_chrome1_50$chromosome26 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome26',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr26", adj = 1, grid(col = "lightgray")) 
boxplot(CAU_chrome1_50$chromosome27, CCA_chrome1_50$chromosome27, CGI_chrome1_50$chromosome27 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome27',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr27", adj = 1, grid(col = "lightgray")) 
boxplot(CAU_chrome1_50$chromosome28, CCA_chrome1_50$chromosome28, CGI_chrome1_50$chromosome28 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome28',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr28", adj = 1, grid(col = "lightgray")) 
boxplot(CAU_chrome1_50$chromosome29, CCA_chrome1_50$chromosome29, CGI_chrome1_50$chromosome29 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome29',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr29", adj = 1, grid(col = "lightgray")) 
boxplot(CAU_chrome1_50$chromosome30, CCA_chrome1_50$chromosome30, CGI_chrome1_50$chromosome30 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome30',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr30", adj = 1, grid(col = "lightgray")) 
boxplot(CAU_chrome1_50$chromosome31, CCA_chrome1_50$chromosome31, CGI_chrome1_50$chromosome31 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome31',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr31", adj = 1, grid(col = "lightgray")) 
boxplot(CAU_chrome1_50$chromosome32, CCA_chrome1_50$chromosome32, CGI_chrome1_50$chromosome32 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome32',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr32", adj = 1) 
boxplot(CAU_chrome1_50$chromosome33, CCA_chrome1_50$chromosome33, CGI_chrome1_50$chromosome33 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome33',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr33", adj = 1) 
boxplot(CAU_chrome1_50$chromosome34, CCA_chrome1_50$chromosome34, CGI_chrome1_50$chromosome34 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome34',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr34", adj = 1) 
boxplot(CAU_chrome1_50$chromosome35, CCA_chrome1_50$chromosome35, CGI_chrome1_50$chromosome35 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome35',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr35", adj = 1) 
boxplot(CAU_chrome1_50$chromosome36, CCA_chrome1_50$chromosome36, CGI_chrome1_50$chromosome36 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome36',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr36", adj = 1) 
boxplot(CAU_chrome1_50$chromosome37, CCA_chrome1_50$chromosome37, CGI_chrome1_50$chromosome37 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome37',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr37", adj = 1) 
boxplot(CAU_chrome1_50$chromosome38, CCA_chrome1_50$chromosome38, CGI_chrome1_50$chromosome38 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome38',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr38", adj = 1) 
boxplot(CAU_chrome1_50$chromosome39, CCA_chrome1_50$chromosome39, CGI_chrome1_50$chromosome39 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome39',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr39", adj = 1) 
boxplot(CAU_chrome1_50$chromosome40, CCA_chrome1_50$chromosome40, CGI_chrome1_50$chromosome40 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome40',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr40", adj = 1) 
boxplot(CAU_chrome1_50$chromosome41, CCA_chrome1_50$chromosome41, CGI_chrome1_50$chromosome41 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome41',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr41", adj = 1) 
boxplot(CAU_chrome1_50$chromosome42, CCA_chrome1_50$chromosome42, CGI_chrome1_50$chromosome42 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome42',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr42", adj = 1) 
boxplot(CAU_chrome1_50$chromosome43, CCA_chrome1_50$chromosome43, CGI_chrome1_50$chromosome43 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome43',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr43", adj = 1) 
boxplot(CAU_chrome1_50$chromosome44, CCA_chrome1_50$chromosome44, CGI_chrome1_50$chromosome44 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome44',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr44", adj = 1) 
boxplot(CAU_chrome1_50$chromosome45, CCA_chrome1_50$chromosome45, CGI_chrome1_50$chromosome45 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome45',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr45", adj = 1) 
boxplot(CAU_chrome1_50$chromosome46, CCA_chrome1_50$chromosome46, CGI_chrome1_50$chromosome46 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome46',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr46", adj = 1) 
boxplot(CAU_chrome1_50$chromosome47, CCA_chrome1_50$chromosome47, CGI_chrome1_50$chromosome47 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome47',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr47", adj = 1) 
boxplot(CAU_chrome1_50$chromosome48, CCA_chrome1_50$chromosome48, CGI_chrome1_50$chromosome48 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome48',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr48", adj = 1) 
boxplot(CAU_chrome1_50$chromosome49, CCA_chrome1_50$chromosome49, CGI_chrome1_50$chromosome49 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome49',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr49", adj = 1) 
boxplot(CAU_chrome1_50$chromosome50, CCA_chrome1_50$chromosome50, CGI_chrome1_50$chromosome50 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome50',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5) 
text(3.6, 30, "chr50", adj = 1)
```

Output value ($\$stats$) compared between each species. The $i$ values within the the first quartile (Q1), median (Q2) and the third quartile (Q3) were detaily investigated, especially if some some $i$ values of each individual chromosome are shared in each Carassius species.

e.g.:

```
(boxplot(CAU_chrome1_50$chromosome8, CCA_chrome1_50$chromosome8, CGI_chrome1_50$chromosome8 , ylim = c(1, 50), ylab = 'centromeric index', xlab = 'chromosome8',  whisklty = 3, boxcol = c(4, 2, 'yellow3'), boxfill = gray(0.95), boxlwd = 3, boxwex = 0.5))
```

$stats
         [,1]     [,2]     [,3]
[1,] 38.57225 35.57611 36.14993
[2,] 39.34915 36.76658 37.37413
[3,] 40.84316 37.89800 38.41969
[4,] 42.04733 39.80127 39.01074
[5,] 44.08874 41.62508 41.42052

$n
[1] 20 20 20

$conf
         [,1]     [,2]     [,3]
[1,] 39.88989 36.82584 37.84148
[2,] 41.79642 38.97015 38.99790

$out
numeric(0)

$group
numeric(0)

$names
[1] "" "" ""

#### Additional editations

````
> cat(names(CAU$lenght_i), fill=1, sep = "'")
````
manually  added the first ' and comma

'lenght1',
'lenght2',
'lenght3',
'lenght4',
'lenght5',
'lenght6',
'lenght7',
'lenght8',
'lenght9',
'lenght10',
'mean_lenght',
'variance_lenght',
'i1',
'i2',
'i3',
'i4',
'i5',
'i6',
'i7',
'i8',
'i9',
'i10',
'mean_i',
'variance_i',
'mean_i_corrected',
'category


```
cat(names(CAU), fill = 1, paste0(" <- c('p", 1:10, "', 'q", 1:10, "', 'length", 1:10, "', 'd", 1:10, "', 'r", 1:10, "', 'i", 1:10,"')"))
```
```
names(CAU$CaXX1IL_1_1) <- c('p1', 'q1', 'length1', 'd1', 'r1', 'i1') 
 
names(CAU$CaXX1IL_1_2) <- c('p2', 'q2', 'length2', 'd2', 'r2', 'i2') 
 
names(CAU$CaXX1IL_1_3)  <- c('p3', 'q3', 'length3', 'd3', 'r3', 'i3') 
 
names(CAU$CaXX1IL_1_4)  <- c('p4', 'q4', 'length4', 'd4', 'r4', 'i4') 
 
names(CAU$CaXX1IL_1_7)  <- c('p5', 'q5', 'length5', 'd5', 'r5', 'i5') 
 
names(CAU$CaXX1IL_1_8)  <- c('p6', 'q6', 'length6', 'd6', 'r6', 'i6') 
 
names(CAU$CaXX1IL_1_6)  <- c('p7', 'q7', 'length7', 'd7', 'r7', 'i7') 
 
names(CAU$CaXX1IL_2_1)  <- c('p8', 'q8', 'length8', 'd8', 'r8', 'i8') 

names(CAU$CaXX1IL_2_2)  <- c('p9', 'q9', 'length9', 'd9', 'r9', 'i9') 
 
names(CAU$CaXX1IL_2_3)  <- c('p10', 'q10', 'length10', 'd10', 'r10', 'i10')
                              
names(CAU$lenght_i) <- c('length1', 'length2', 'length3', 'length4', 'length5', 'length6', 'length7', 'length8', 'length9', 'length10', 'mean_length', 'variance_length', 'i1', 'i2', 'i3', 'i4', 'i5', 'i6', 'i7', 'i8', 'i9', 'i10', 'mean_i', 'variance_i', 'mean_i_corrected', 'category')
```
````
> cat(names(CAU), fill = 1)
CaXX1IL_1_1 
CaXX1IL_1_2 
CaXX1IL_1_3 
CaXX1IL_1_4 
CaXX1IL_1_7 
CaXX1IL_1_8 
CaXX1IL_1_6 
CaXX1IL_2_1 
CaXX1IL_2_2 
CaXX1IL_2_3 
lenght_i
````
````
names(CAU) <- c("CaXX1IL_1_1", "CaXX1IL_1_2", "CaXX1IL_1_3", "CaXX1IL_1_4", "CaXX1IL_1_7", "CaXX1IL_1_8", "CaXX1IL_1_6", "CaXX1IL_2_1", "CaXX1IL_2_2", "CaXX1IL_2_3", "length_i")
````
````
> paste0("CCA$", names(CCA) )
 ````
```` 
names(CCA$CcVi3CZ_5_10) <- c('p1', 'q1', 'length1', 'd1', 'r1', 'i1') 
 
names(CCA$CcVi3CZ_5_9) <- c('p2', 'q2', 'length2', 'd2', 'r2', 'i2') 
 
names(CCA$CcVi3CZ_5_6)  <- c('p3', 'q3', 'length3', 'd3', 'r3', 'i3') 
 
names(CCA$CcVi3CZ_5_5)  <- c('p4', 'q4', 'length4', 'd4', 'r4', 'i4') 
 
names(CCA$CcVi3CZ_2_3)  <- c('p5', 'q5', 'length5', 'd5', 'r5', 'i5') 
 
names(CCA$CcVi3CZ_3_5)  <- c('p6', 'q6', 'length6', 'd6', 'r6', 'i6') 
 
names(CCA$CcVi3CZ_3_4)  <- c('p7', 'q7', 'length7', 'd7', 'r7', 'i7') 
 
names(CCA$CcHe5Fi_1_1)  <- c('p8', 'q8', 'length8', 'd8', 'r8', 'i8') 

names(CCA$CcHe5Fi_2_1)  <- c('p9', 'q9', 'length9', 'd9', 'r9', 'i9') 
 
names(CCA$CcHe6Fi_1_2)  <- c('p10', 'q10', 'length10', 'd10', 'r10', 'i10')
                              
names(CCA$lenght_i) <- c('length1', 'length2', 'length3', 'length4', 'length5', 'length6', 'length7', 'length8', 'length9', 'length10', 'mean_length', 'variance_length', 'i1', 'i2', 'i3', 'i4', 'i5', 'i6', 'i7', 'i8', 'i9', 'i10', 'mean_i', 'variance_i', 'mean_i_corrected', 'category')
````
````
> names(CCA)
 [1] "CcVi3CZ_5_10" "CcVi3CZ_5_9"  "CcVi3CZ_5_6"  "CcVi3CZ_5_5" 
 [5] "CcVi3CZ_2_3"  "CcVi3CZ_3_5"  "CcVi3CZ_3_4"  "CcHe5Fi_1_1" 
 [9] "CcHe5Fi_2_1"  "CcHe6Fi_1_2"  "lenght_i"   
````
````
names(CCA) <- c("CcVi3CZ_5_10", "CcVi3CZ_5_9", "CcVi3CZ_5_6", "CcVi3CZ_5_5", "CcVi3CZ_2_3", "CcVi3CZ_3_5", "CcVi3CZ_3_4", "CcHe5Fi_1_1", "CcHe5Fi_2_1", "CcHe6Fi_1_2",  "length_i")
````
````
> paste0("CGI$", names(CGI) )
 
````
````
names(CGI$CGI_D10_6g) <- c('p1', 'q1', 'length1', 'd1', 'r1', 'i1') 
 
names(CGI$CGI_D5_9g) <- c('p2', 'q2', 'length2', 'd2', 'r2', 'i2') 
 
names(CGI$CGI_X7_2_7)  <- c('p3', 'q3', 'length3', 'd3', 'r3', 'i3') 
 
names(CGI$CGI_D10_4g)  <- c('p4', 'q4', 'length4', 'd4', 'r4', 'i4') 
 
names(CGI$CGI_H15_7g)  <- c('p5', 'q5', 'length5', 'd5', 'r5', 'i5') 
 
names(CGI$CGI_D5_2g)  <- c('p6', 'q6', 'length6', 'd6', 'r6', 'i6') 
 
names(CGI$CGI_D5_8g)  <- c('p7', 'q7', 'length7', 'd7', 'r7', 'i7') 
 
names(CGI$CGI_X9_2_1_5)  <- c('p8', 'q8', 'length8', 'd8', 'r8', 'i8') 

names(CGI$CGI_X9_2_1_10)  <- c('p9', 'q9', 'length9', 'd9', 'r9', 'i9') 
 
names(CGI$CGI_D11_7g)  <- c('p10', 'q10', 'length10', 'd10', 'r10', 'i10')
                              
names(CGI$lenght_i) <- c('length1', 'length2', 'length3', 'length4', 'length5', 'length6', 'length7', 'length8', 'length9', 'length10', 'mean_length', 'variance_length', 'i1', 'i2', 'i3', 'i4', 'i5', 'i6', 'i7', 'i8', 'i9', 'i10', 'mean_i', 'variance_i', 'mean_i_corrected', 'category')
````
````
names(CGI) <- c("CGI_D10_6g", "CGI_D5_9g", "CGI_X7_2_7", "CGI_D10_4g", "CGI_H15_7g", "CGI_D5_2g", "CGI_D5_8g", "CGI_X9_2_1_5", "CGI_X9_2_1_10", "CGI_D11_7g", "length_i")
````
