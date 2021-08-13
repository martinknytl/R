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

> CAU$length_i <- data.frame(length1=CAU$CaXX1IL_1_1$length1, length2=CAU$CaXX1IL_1_2$length2, length3=CAU$CaXX1IL_1_3$length3, length4=CAU$CaXX1IL_1_4$length4, length5=CAU$CaXX1IL_1_7$length5, length6=CAU$CaXX1IL_1_8$length6, length7=CAU$CaXX1IL_1_6$length7, length8=CAU$CaXX1IL_2_1$length8, length9=CAU$CaXX1IL_2_2$length9, length10=CAU$CaXX1IL_2_3$length10, i1=CAU$CaXX1IL_1_1$i1, i2=CAU$CaXX1IL_1_2$i2, i3=CAU$CaXX1IL_1_3$i3, i4=CAU$CaXX1IL_1_4$i4, i5=CAU$CaXX1IL_1_7$i5, i6=CAU$CaXX1IL_1_8$i6, i7=CAU$CaXX1IL_1_6$i7, i8= CAU$CaXX1IL_2_1$i8, i9= CAU$CaXX1IL_2_2$i9, i10= CAU$CaXX1IL_2_3$i10)

> CAU$length_i$mean_length <- apply (CAU$length_i[,1:10], 1, mean)
> CAU$length_i$mean_i <- apply (CAU$length_i[,11:20], 1, mean)

> par_dotplot <- par(mfcol=c(3,1), mai=c(0.53,0.55,0.17,0.1), font=3)
> plot(CAU$length_i$mean_i, CAU$length_i$mean_length, pch=16, col="yellow3", ylim = c(15, 45), xlim = c(0, 50), xlab = "centromeric index", ylab = "chromosomal length", ann=TRUE, las=1, abline(v=c(0, 12.5, 25, 35.5, 50), col="gray", lty=2))
````


