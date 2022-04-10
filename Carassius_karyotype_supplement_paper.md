````
> CAU <- list (CaXX1IL_1_1=data.frame(p1=p1, q1=q1, length1=p1+q1, d1=q1-p1, r1=q1/p1, i1=100/((q1/p1)+1)), CaXX1IL_1_2 = data.frame(p2=p2, q2=q2, length2=p2+q2, d2=q2-p2, r2=q2/p2, i2=100/((q2/p2)+1)), CaXX1IL_1_3=data.frame(p3=p3, q3=q3, length3=p3+q3, d3=q3-p3, r3=q3/p3, i3=100/((q3/p3)+1)), CaXX1IL_1_4 = data.frame(p4=p4, q4=q4, length4=p4+q4, d4=q4-p4, r4=q4/p4, i4=100/((q4/p4)+1)), CaXX1IL_1_7 = data.frame(p5=p5, q5=q5, length5=p5+q5, d5=q5-p5, r5=q5/p5, i5=100/((q5/p5)+1)), CaXX1IL_1_8 = data.frame(p6=p6, q6=q6, length6=p6+q6, d6=q6-p6, r6=q6/p6, i6=100/((q6/p6)+1)), CaXX1IL_1_6 = data.frame(p7=p7, q7=q7, length7=p7+q7, d7=q7-p7, r7=q7/p7, i7=100/((q7/p7)+1)), CaXX1IL_2_1 = data.frame(p8=p8, q8=q8, length8=p8+q8, d8=q8-p8, r8=q8/p8, i8=100/((q8/p8)+1)), CaXX1IL_2_2 = data.frame(p9=p9, q9=q9, length9=p9+q9, d9=q9-p9, r9=q9/p9, i9=100/((q9/p9)+1)), CaXX1IL_2_3 = data.frame(p10=p10, q10=q10, length10=p10+q10, d10=q10-p10, r10=q10/p10, i10=100/((q10/p10)+1)))

> CAU$CaXX1IL_1_1 <- CAU$CaXX1IL_1_1 [order(-CAU$CaXX1IL_1_1$i1),]
> CAU$CaXX1IL_1_2 <- CAU$CaXX1IL_1_2 [order(-CAU$CaXX1IL_1_2$i2),]
> CAU$CaXX1IL_1_3 <- CAU$CaXX1IL_1_3 [order(-CAU$CaXX1IL_1_3$i3),]
> CAU$CaXX1IL_1_4 <- CAU$CaXX1IL_1_4 [order(-CAU$CaXX1IL_1_4$i4),]
> CAU$CaXX1IL_1_7 <- CAU$CaXX1IL_1_7 [order(-CAU$CaXX1IL_1_7$i5),]
> CAU$CaXX1IL_1_8 <- CAU$CaXX1IL_1_8 [order(-CAU$CaXX1IL_1_8$i6),]
> CAU$CaXX1IL_1_6 <- CAU$CaXX1IL_1_6 [order(-CAU$CaXX1IL_1_6$i7),]
> CAU$CaXX1IL_2_1 <- CAU$CaXX1IL_2_1 [order(-CAU$CaXX1IL_2_1$i8),]
> CAU$CaXX1IL_2_2 <- CAU$CaXX1IL_2_2 [order(-CAU$CaXX1IL_2_2$i9),]
> CAU$CaXX1IL_2_3 <- CAU$CaXX1IL_2_3 [order(-CAU$CaXX1IL_2_3$i10),]
````
````
> CAU$length <- data.frame(length1=CAU$CaXX1IL_1_1$length1, length2=CAU$CaXX1IL_1_2$length2, length3=CAU$CaXX1IL_1_3$length3, length4=CAU$CaXX1IL_1_4$length4, length5=CAU$CaXX1IL_1_7$length5, length6=CAU$CaXX1IL_1_8$length6, length7=CAU$CaXX1IL_1_6$length7, length8=CAU$CaXX1IL_2_1$length8, length9=CAU$CaXX1IL_2_2$length9, length10=CAU$CaXX1IL_2_3$length10)
> CAU$i <- data.frame(i1=CAU$CaXX1IL_1_1$i1, i2=CAU$CaXX1IL_1_2$i2, i3=CAU$CaXX1IL_1_3$i3, i4=CAU$CaXX1IL_1_4$i4, i5=CAU$CaXX1IL_1_7$i5, i6=CAU$CaXX1IL_1_8$i6, i7=CAU$CaXX1IL_1_6$i7, i8= CAU$CaXX1IL_2_1$i8, i9= CAU$CaXX1IL_2_2$i9, i10= CAU$CaXX1IL_2_3$i10)
````
````
> CAU$length$mean_length <- apply (CAU$length[,1:10], 1, mean)
> CAU$i$mean_i <- apply (CAU$i[,1:10], 1, mean)
````
````
> print(xtable(CAU$length, type = "latex"), file = "CAU_length.tex")
> print(xtable(CAU$i, type = "latex"), file = "CAU$i.tex")
````
````
> (par_dotplot <- par(mfcol=c(3,1), mai=c(0.53,0.55,0.17,0.1), font=3))
> plot(CAU$i$mean_i, CAU$length$mean_length, pch=16, col="yellow3", ylim = c(15, 45), xlim = c(0, 50), xlab = "centromeric index", ylab = "chromosomal length", ann=TRUE, las=1, abline(v=c(0, 12.5, 25, 35.5, 50), col="gray", lty=2))
````
````
> (par_dotplot <- par(mfcol=c(3,1), mai=c(0.53,0.55,0.17,0.1), font=3))
> plot(CAU$length_i$mean_i, CAU$length_i$mean_length, pch=16, col="yellow3", ylim = c(15, 45), xlim = c(0, 50), xlab = "centromeric index", ylab = "chromosomal length", ann=TRUE, las=1, abline(v=c(0, 12.5, 25, 35.5, 50), col="gray", lty=2))
> legend("bottomright", legend = "Carassius auratus", pch = 16, col = "yellow3")
````
````
> Select_chrome <- function(i,j) {chromosome <- c(CAU$CaXX1IL_1_1$i1[i:j], CAU$CaXX1IL_1_2$i2[i:j], CAU$CaXX1IL_1_3$i3[i:j], CAU$CaXX1IL_1_4$i4[i:j], CAU$CaXX1IL_1_7$i5[i:j], CAU$CaXX1IL_1_8$i6[i:j], CAU$CaXX1IL_1_6$i7[i:j], CAU$CaXX1IL_2_1$i8[i:j], CAU$CaXX1IL_2_2$i9[i:j], CAU$CaXX1IL_2_3$i10[i:j])}

> chromosome1 <- Select_chrome(1,2)
> chromosome2 <- Select_chrome(3,4)
> chromosome3 <- Select_chrome(5,6)
> chromosome4 <- Select_chrome(7,8)
> chromosome5 <- Select_chrome(9,10)
> chromosome6 <- Select_chrome(11,12)
> chromosome7 <- Select_chrome(13,14)
> chromosome8 <- Select_chrome(15,16)
> chromosome9 <- Select_chrome(17,18)
> chromosome10 <- Select_chrome(19,20)
> chromosome11 <- Select_chrome(21,22)
> chromosome12 <- Select_chrome(23,24)
> chromosome13 <- Select_chrome(25,26)
> chromosome14 <- Select_chrome(27,28)
> chromosome15 <- Select_chrome(29,30)
> chromosome16 <- Select_chrome(31,32)
> chromosome17 <- Select_chrome(33,34)
> chromosome18 <- Select_chrome(35,36)
> chromosome19 <- Select_chrome(37,38)
> chromosome20 <- Select_chrome(39,40)
> chromosome21 <- Select_chrome(41,42)
> chromosome22 <- Select_chrome(43,44)
> chromosome23 <- Select_chrome(45,46)
> chromosome24 <- Select_chrome(47,48)
> chromosome25 <- Select_chrome(49,50)
> chromosome26 <- Select_chrome(51,52)
> chromosome27 <- Select_chrome(53,54)
> chromosome28 <- Select_chrome(55,56)
> chromosome29 <- Select_chrome(57,58)
> chromosome30 <- Select_chrome(59,60)
> chromosome31 <- Select_chrome(61,62)
> chromosome32 <- Select_chrome(63,64)
> chromosome33 <- Select_chrome(65,66)
> chromosome34 <- Select_chrome(67,68)
> chromosome35 <- Select_chrome(69,70)
> chromosome36 <- Select_chrome(71,72)
> chromosome37 <- Select_chrome(73,74)
> chromosome38 <- Select_chrome(75,76)
> chromosome39 <- Select_chrome(77,78)
> chromosome40 <- Select_chrome(79,80)
> chromosome41 <- Select_chrome(81,82)
> chromosome42 <- Select_chrome(83,84)
> chromosome43 <- Select_chrome(85,86)
> chromosome44 <- Select_chrome(87,88)
> chromosome45 <- Select_chrome(89,90)
> chromosome46 <- Select_chrome(91,92)
> chromosome47 <- Select_chrome(93,94)
> chromosome48 <- Select_chrome(95,96)
> chromosome49 <- Select_chrome(97,98)
> chromosome50 <- Select_chrome(99,100)
````
````
> (par_boxplot <- par(mfcol=c(3,1), mai=c(0.53,0.55,0.1,0.1), font = 4))
> boxplot(chromosome1, chromosome2, chromosome3, chromosome4, chromosome5, chromosome6, chromosome7, chromosome8, chromosome9, chromosome10, chromosome11, chromosome12, chromosome13, chromosome14, chromosome15, chromosome16, chromosome17, chromosome18, chromosome19, chromosome20, chromosome21, chromosome22, chromosome23, chromosome24, chromosome25, chromosome26, chromosome27, chromosome28, chromosome29, chromosome30, chromosome31, chromosome32, chromosome33, chromosome34, chromosome35, chromosome36, chromosome37, chromosome38, chromosome39, chromosome40, chromosome41, chromosome42, chromosome43, chromosome44, chromosome45, chromosome46, chromosome47, chromosome48, chromosome49, chromosome50, ylim=c(-1, 50), xlim=c(1, 50), horizontal = FALSE, ylab = "centromeric index", xlab = "chromosome", las = 1, pch = 20, whisklty = 3, boxcol = "yellow3", boxfill = gray(0.95), boxlwd = 2, boxwex = 0.7, names = 1:50)
> text(51, 40, "Carassius auratus", col = "yellow3", adj = 1)


````


