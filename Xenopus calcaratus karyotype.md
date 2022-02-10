# XCA 

#### Metaphases were sorted increasingly in Google sheets according to chromosome from 1a > 1b > 2a ... 10a > 10b.

#### Vectors were written manually from measuring of each chromosome

e.g. for p1, and q1
```
p1 <- c(74.75760234,
        57.46129446,
        56.8,
        65.6,
        61.35,
        50.3,
        45.65,
        38.8,
        28.13333333,
        21.8,
        25.1,
        46.45,
        47.2,
        20,
        30.5,
        48.9,
        19.4,
        24.15,
        27.65,
        41.5,
        47.40575916,
        37.83148148,
        39.55,
        27.1,
        34.8,
        26.0080292,
        34.48125,
        43.1,
        39.93227513,
        30.01025641,
        16.15,
        20.05,
        30.55,
        28.75,
        23.2,
        19.9,
        14.7,
        15.55,
        12.7,
        13.35)
```

```
q1 <- c(105.2923977,
       99.43870554,
       90.5,
       78.9,
       75.4,
       81.95,
       78.1,
       79.9,
       87.91666667,
       89.55,
       83.1,
       61.5,
       58.8,
       86,
       74.95,
       55.35,
       84.7,
       79.35,
       74.3,
       58.8,
       52.09424084,
       61.01851852,
       58.85,
       70.45,
       62.65,
       70.2919708,
       57.46875,
       47.8,
       44.86772487,
       53.58974359,
       62.6,
       57.2,
       38.05,
       32.1,
       35.9,
       32.55,
       22.05,
       18.6,
       21.15,
       17.8)
```

#### creation of the list with each metaphase as a table

```
paste0(" data.frame(p", 1:36, "=p", 1:36, ",q", 1:36, "=q", 1:36, ",l", 1:36, "=p", 1:36, "+q", 1:36, ",r1_", 1:36, "=p", 1:36, "/q", 1:36, ",r2_", 1:36, "=q", 1:36, "/p", 1:36, ",i", 1:36, "=100/((q", 1:36, "/p", 1:36, ")+1))", collapse = ",")
```

#### "XCA <- list(" and name of individuals manually added
```
XCA <- list(XCA1_1_1=data.frame(p1=p1,q1=q1,l1=p1+q1,r1_1=p1/q1,r2_1=q1/p1,i1=100/((q1/p1)+1)), XCA1_2_5=data.frame(p2=p2,q2=q2,l2=p2+q2,r1_2=p2/q2,r2_2=q2/p2,i2=100/((q2/p2)+1)), XCA1_3_4=data.frame(p3=p3,q3=q3,l3=p3+q3,r1_3=p3/q3,r2_3=q3/p3,i3=100/((q3/p3)+1)), XCA1_3_8=data.frame(p4=p4,q4=q4,l4=p4+q4,r1_4=p4/q4,r2_4=q4/p4,i4=100/((q4/p4)+1)), XCA1_4_1=data.frame(p5=p5,q5=q5,l5=p5+q5,r1_5=p5/q5,r2_5=q5/p5,i5=100/((q5/p5)+1)), XCA1_9_3=data.frame(p6=p6,q6=q6,l6=p6+q6,r1_6=p6/q6,r2_6=q6/p6,i6=100/((q6/p6)+1)), XCA2_1_5=data.frame(p7=p7,q7=q7,l7=p7+q7,r1_7=p7/q7,r2_7=q7/p7,i7=100/((q7/p7)+1)), XCA2_4_1=data.frame(p8=p8,q8=q8,l8=p8+q8,r1_8=p8/q8,r2_8=q8/p8,i8=100/((q8/p8)+1)), XCA2_12_2=data.frame(p9=p9,q9=q9,l9=p9+q9,r1_9=p9/q9,r2_9=q9/p9,i9=100/((q9/p9)+1)), XCA3_1_2=data.frame(p10=p10,q10=q10,l10=p10+q10,r1_10=p10/q10,r2_10=q10/p10,i10=100/((q10/p10)+1)), XCA3_1_13=data.frame(p11=p11,q11=q11,l11=p11+q11,r1_11=p11/q11,r2_11=q11/p11,i11=100/((q11/p11)+1)), XCA3_7_14=data.frame(p12=p12,q12=q12,l12=p12+q12,r1_12=p12/q12,r2_12=q12/p12,i12=100/((q12/p12)+1)), XCA3_7_18=data.frame(p13=p13,q13=q13,l13=p13+q13,r1_13=p13/q13,r2_13=q13/p13,i13=100/((q13/p13)+1)), XCA3_7_19=data.frame(p14=p14,q14=q14,l14=p14+q14,r1_14=p14/q14,r2_14=q14/p14,i14=100/((q14/p14)+1)), CHR2_Image_9=data.frame(p15=p15,q15=q15,l15=p15+q15,r1_15=p15/q15,r2_15=q15/p15,i15=100/((q15/p15)+1)), CHR9_XCA_F1_2_17_Image_6=data.frame(p16=p16,q16=q16,l16=p16+q16,r1_16=p16/q16,r2_16=q16/p16,i16=100/((q16/p16)+1)), XCA28_CHR10_Image_1=data.frame(p17=p17,q17=q17,l17=p17+q17,r1_17=p17/q17,r2_17=q17/p17,i17=100/((q17/p17)+1)), XCA3_CBAND_Image_8=data.frame(p18=p18,q18=q18,l18=p18+q18,r1_18=p18/q18,r2_18=q18/p18,i18=100/((q18/p18)+1)), XCABaF1_2_7II_Image_15=data.frame(p19=p19,q19=q19,l19=p19+q19,r1_19=p19/q19,r2_19=q19/p19,i19=100/((q19/p19)+1)), XCA4_CHR8_Image_1=data.frame(p20=p20,q20=q20,l20=p20+q20,r1_20=p20/q20,r2_20=q20/p20,i20=100/((q20/p20)+1)), XCABaF1_2_19II_Image_31=data.frame(p21=p21,q21=q21,l21=p21+q21,r1_21=p21/q21,r2_21=q21/p21,i21=100/((q21/p21)+1)), XCABaF1_2_10II_Image_4=data.frame(p22=p22,q22=q22,l22=p22+q22,r1_22=p22/q22,r2_22=q22/p22,i22=100/((q22/p22)+1)), XCABaF1_2_4II_Image_7=data.frame(p23=p23,q23=q23,l23=p23+q23,r1_23=p23/q23,r2_23=q23/p23,i23=100/((q23/p23)+1)), XCABaF1_2_15II_Image_5=data.frame(p24=p24,q24=q24,l24=p24+q24,r1_24=p24/q24,r2_24=q24/p24,i24=100/((q24/p24)+1)), CHR7_Image_20=data.frame(p25=p25,q25=q25,l25=p25+q25,r1_25=p25/q25,r2_25=q25/p25,i25=100/((q25/p25)+1)), XCA20_CHR6_Image_11=data.frame(p26=p26,q26=q26,l26=p26+q26,r1_26=p26/q26,r2_26=q26/p26,i26=100/((q26/p26)+1)), XCABaF1_2_2II_Image_13=data.frame(p27=p27,q27=q27,l27=p27+q27,r1_27=p27/q27,r2_27=q27/p27,i27=100/((q27/p27)+1)), XCABaF1_2_9II_Image_16=data.frame(p28=p28,q28=q28,l28=p28+q28,r1_28=p28/q28,r2_28=q28/p28,i28=100/((q28/p28)+1)), XCAF1_2_CHR3_Image_7=data.frame(p29=p29,q29=q29,l29=p29+q29,r1_29=p29/q29,r2_29=q29/p29,i29=100/((q29/p29)+1)), XCABaF1_2_13II_Image_2=data.frame(p30=p30,q30=q30,l30=p30+q30,r1_30=p30/q30,r2_30=q30/p30,i30=100/((q30/p30)+1)), XCABaF1_2_14II_Image_4=data.frame(p31=p31,q31=q31,l31=p31+q31,r1_31=p31/q31,r2_31=q31/p31,i31=100/((q31/p31)+1)), XCAPCC5_8_Image_7ab=data.frame(p32=p32,q32=q32,l32=p32+q32,r1_32=p32/q32,r2_32=q32/p32,i32=100/((q32/p32)+1)), XCA_F1_2_16_CHR5_Image_5=data.frame(p33=p33,q33=q33,l33=p33+q33,r1_33=p33/q33,r2_33=q33/p33,i33=100/((q33/p33)+1)), CHR1_XCA2_2_Image_15=data.frame(p34=p34,q34=q34,l34=p34+q34,r1_34=p34/q34,r2_34=q34/p34,i34=100/((q34/p34)+1)), XCABaF1_2_7II_Image_7=data.frame(p35=p35,q35=q35,l35=p35+q35,r1_35=p35/q35,r2_35=q35/p35,i35=100/((q35/p35)+1)))
```

=data.frame(p36=p36,q36=q36,l36=p36+q36,r1_36=p36/q36,r2_36=q36/p36,i36=100/((q36/p36)+1)))


#### "l_i" folder into XCA list

XCA$l_i <- 
data.frame(lenght1=CAU$CaXX1IL_1_1$lenght1, lenght2=CAU$CaXX1IL_1_2$lenght2, lenght3=CAU$CaXX1IL_1_3$lenght3, lenght4=CAU$CaXX1IL_1_4$lenght4, lenght5=CAU$CaXX1IL_1_7$lenght5, lenght6=CAU$CaXX1IL_1_8$lenght6, lenght7=CAU$CaXX1IL_1_6$lenght7, lenght8=CAU$CaXX1IL_2_1$lenght8, lenght9=CAU$CaXX1IL_2_2$lenght9, lenght10=CAU$CaXX1IL_2_3$lenght10, i1=CAU$CaXX1IL_1_1$i1, i2=CAU$CaXX1IL_1_2$i2, i3=CAU$CaXX1IL_1_3$i3, i4=CAU$CaXX1IL_1_4$i4, i5=CAU$CaXX1IL_1_7$i5, i6=CAU$CaXX1IL_1_8$i6, i7=CAU$CaXX1IL_1_6$i7, i8= CAU$CaXX1IL_2_1$i8, i9= CAU$CaXX1IL_2_2$i9, i10= CAU$CaXX1IL_2_3$i10)





XCA$XCA1_1_1 <- XCA$XCA1_1_1[order(XCA$XCA1_1_1$chromosome1),]
XCA$XCA1_2_5 <- XCA$XCA1_2_5[order(XCA$XCA1_2_5$chromosome2),]


XCA$XCA1_3_4 <- XCA$XCA1_2_5[order(XCA$XCA1_2_5$chromosome2),]
XCA$XCA1_3_8 <- XCA$XCA1_2_5[order(XCA$XCA1_2_5$chromosome2),]
XCA$XCA1_4_1 <- XCA$XCA1_2_5[order(XCA$XCA1_2_5$chromosome2),]
XCA$XCA1_9_3  <- XCA$XCA1_2_5[order(XCA$XCA1_2_5$chromosome2),]
XCA$XCA2_1_5 <- XCA$XCA1_2_5[order(XCA$XCA1_2_5$chromosome2),]
XCA$XCA2_4_1 <- XCA$XCA1_2_5[order(XCA$XCA1_2_5$chromosome2),]
XCA$XCA2_12_2  <- XCA$XCA1_2_5[order(XCA$XCA1_2_5$chromosome2),]
XCA$XCA3_1_2 <- XCA$XCA1_2_5[order(XCA$XCA1_2_5$chromosome2),]
XCA$XCA3_1_13 <- XCA$XCA1_2_5[order(XCA$XCA1_2_5$chromosome2),]
XCA$XCA3_7_14 <- XCA$XCA1_2_5[order(XCA$XCA1_2_5$chromosome2),]
XCA$XCA3_7_18 <- XCA$XCA1_2_5[order(XCA$XCA1_2_5$chromosome2),]
XCA$XCA3_7_19 <- XCA$XCA1_2_5[order(XCA$XCA1_2_5$chromosome2),]
XCA$CHR2_Image_9 <- XCA$XCA1_2_5[order(XCA$XCA1_2_5$chromosome2),]
XCA$CHR9_XCA_F1_2_17_Image_6 <- XCA$XCA1_2_5[order(XCA$XCA1_2_5$chromosome2),]
XCA$XCA28_CHR10_Image_1 <- XCA$XCA1_2_5[order(XCA$XCA1_2_5$chromosome2),]
XCA$XCA3_CBAND_Image_8 <- XCA$XCA1_2_5[order(XCA$XCA1_2_5$chromosome2),]
XCA$XCABaF1_2_7II_Image_15 <- XCA$XCA1_2_5[order(XCA$XCA1_2_5$chromosome2),]
XCA$XCA4_CHR8_Image_1 <- XCA$XCA1_2_5[order(XCA$XCA1_2_5$chromosome2),]
XCA$XCABaF1_2_19II_Image_31 <- XCA$XCA1_2_5[order(XCA$XCA1_2_5$chromosome2),]
XCA$XCABaF1_2_10II_Image_4 <- XCA$XCA1_2_5[order(XCA$XCA1_2_5$chromosome2),]
XCA$XCABaF1_2_4II_Image_7 <- XCA$XCA1_2_5[order(XCA$XCA1_2_5$chromosome2),]
XCA$XCABaF1_2_15II_Image_5 <- XCA$XCA1_2_5[order(XCA$XCA1_2_5$chromosome2),]

```
XCA$XCA1_1_1$l1_percentage <- (XCA$XCA1_1_1$l1*100)/sum(XCA$XCA1_1_1$l1)
```
 
