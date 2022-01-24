# XCA 

#### Vectors were written manually from measuring of each chromosome

e.g. for chromosome1, p1, and q1
```
chromosome1 <- c("1a",
+                 "1a",
+                 "1b",
+                 "1b",
+                 "2b",
+                 "2b",
+                 "2a",
+                 "2a",
+                 "3a",
+                 "3b",
+                 "3a",
+                 "7a",
+                 "6a",
+                 "3b",
+                 "5a",
+                 "6a",
+                 "8a",
+                 "8a",
+                 "5a",
+                 "7a",
+                 "6b",
+                 "4a",
+                 "4a",
+                 "5b",
+                 "4b",
+                 "5b",
+                 "4b",
+                 "6b",
+                 "7b",
+                 "7b",
+                 "8b",
+                 "8b",
+                 "9a",
+                 "9a",
+                 "9b",
+                 "9b",
+                 "10b",
+                 "10a",
+                 "10b",
+                 "10a")
```
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
paste0(" data.frame(p", 1:24, "=p", 1:24, ",q", 1:24, "=q", 1:24, ",l", 1:24, "=p", 1:24, "+q", 1:24, ",r1_", 1:24, "=p", 1:24, "/q", 1:24, ",r2_", 1:24, "=q", 1:24, "/p", 1:24, ",i", 1:24, "=100/((q", 1:24, "/p", 1:24, ")+1)", ",chromosome", 1:24, "=chromosome", 1:24, ")", collapse = ",")
```

#### "XCA <- list(" and name of individuals manually added
```
XCA <- list(XCA1_1_1=data.frame(p1=p1,q1=q1,l1=p1+q1,r1_1=p1/q1,r2_1=q1/p1,i1=100/((q1/p1)+1),chromosome1=chromosome1), XCA1_2_5=data.frame(p2=p2,q2=q2,l2=p2+q2,r1_2=p2/q2,r2_2=q2/p2,i2=100/((q2/p2)+1),chromosome2=chromosome2), XCA1_3_4=data.frame(p3=p3,q3=q3,l3=p3+q3,r1_3=p3/q3,r2_3=q3/p3,i3=100/((q3/p3)+1),chromosome3=chromosome3), XCA1_3_8=data.frame(p4=p4,q4=q4,l4=p4+q4,r1_4=p4/q4,r2_4=q4/p4,i4=100/((q4/p4)+1),chromosome4=chromosome4), XCA1_4_1=data.frame(p5=p5,q5=q5,l5=p5+q5,r1_5=p5/q5,r2_5=q5/p5,i5=100/((q5/p5)+1),chromosome5=chromosome5), XCA1_9_3=data.frame(p6=p6,q6=q6,l6=p6+q6,r1_6=p6/q6,r2_6=q6/p6,i6=100/((q6/p6)+1),chromosome6=chromosome6), XCA2_1_5=data.frame(p7=p7,q7=q7,l7=p7+q7,r1_7=p7/q7,r2_7=q7/p7,i7=100/((q7/p7)+1),chromosome7=chromosome7), XCA2_4_1=data.frame(p8=p8,q8=q8,l8=p8+q8,r1_8=p8/q8,r2_8=q8/p8,i8=100/((q8/p8)+1),chromosome8=chromosome8), XCA2_12_2=data.frame(p9=p9,q9=q9,l9=p9+q9,r1_9=p9/q9,r2_9=q9/p9,i9=100/((q9/p9)+1),chromosome9=chromosome9), XCA3_1_2=data.frame(p10=p10,q10=q10,l10=p10+q10,r1_10=p10/q10,r2_10=q10/p10,i10=100/((q10/p10)+1),chromosome10=chromosome10), XCA3_1_13=data.frame(p11=p11,q11=q11,l11=p11+q11,r1_11=p11/q11,r2_11=q11/p11,i11=100/((q11/p11)+1),chromosome11=chromosome11), XCA3_7_14=data.frame(p12=p12,q12=q12,l12=p12+q12,r1_12=p12/q12,r2_12=q12/p12,i12=100/((q12/p12)+1),chromosome12=chromosome12), XCA3_7_18=data.frame(p13=p13,q13=q13,l13=p13+q13,r1_13=p13/q13,r2_13=q13/p13,i13=100/((q13/p13)+1),chromosome13=chromosome13), XCA3_7_19=data.frame(p14=p14,q14=q14,l14=p14+q14,r1_14=p14/q14,r2_14=q14/p14,i14=100/((q14/p14)+1),chromosome14=chromosome14), CHR2_Image_9=data.frame(p15=p15,q15=q15,l15=p15+q15,r1_15=p15/q15,r2_15=q15/p15,i15=100/((q15/p15)+1),chromosome15=chromosome15), CHR9_XCA_F1_2_17_Image_6=data.frame(p16=p16,q16=q16,l16=p16+q16,r1_16=p16/q16,r2_16=q16/p16,i16=100/((q16/p16)+1),chromosome16=chromosome16), XCA28_CHR10_Image_1=data.frame(p17=p17,q17=q17,l17=p17+q17,r1_17=p17/q17,r2_17=q17/p17,i17=100/((q17/p17)+1),chromosome17=chromosome17), XCA3_CBAND_Image_8=data.frame(p18=p18,q18=q18,l18=p18+q18,r1_18=p18/q18,r2_18=q18/p18,i18=100/((q18/p18)+1),chromosome18=chromosome18), XCABaF1_2_7II_Image_15=data.frame(p19=p19,q19=q19,l19=p19+q19,r1_19=p19/q19,r2_19=q19/p19,i19=100/((q19/p19)+1),chromosome19=chromosome19), XCA4_CHR8_Image_1=data.frame(p20=p20,q20=q20,l20=p20+q20,r1_20=p20/q20,r2_20=q20/p20,i20=100/((q20/p20)+1),chromosome20=chromosome20), XCABaF1_2_19II_Image_31=data.frame(p21=p21,q21=q21,l21=p21+q21,r1_21=p21/q21,r2_21=q21/p21,i21=100/((q21/p21)+1),chromosome21=chromosome21), XCABaF1_2_10II_Image_4=data.frame(p22=p22,q22=q22,l22=p22+q22,r1_22=p22/q22,r2_22=q22/p22,i22=100/((q22/p22)+1),chromosome22=chromosome22), XCABaF1_2_4II_Image_7=data.frame(p23=p23,q23=q23,l23=p23+q23,r1_23=p23/q23,r2_23=q23/p23,i23=100/((q23/p23)+1),chromosome23=chromosome23), XCABaF1_2_15II_Image_5=data.frame(p24=p24,q24=q24,l24=p24+q24,r1_24=p24/q24,r2_24=q24/p24,i24=100/((q24/p24)+1),chromosome24=chromosome24))
```

#### The rest of metaphases were sorted in Google sheets according to chromosome from 1a > 1b > 2a ... 10a > 10b. The following command does not include chromosome categories.
```
paste0(" data.frame(p", 25:35, "=p", 25:35, ",q", 25:35, "=q", 25:35, ",l", 25:35, "=p", 25:35, "+q", 25:35, ",r1_", 25:35, "=p", 25:35, "/q", 25:35, ",r2_", 25:35, "=q", 25:35, "/p", 25:35, ",i", 25:35, "=100/((q", 25:35, "/p", 25:35, ")+1))", collapse = ",")
```

```
XCA$XCA1_1_1$l1_percentage <- (XCA$XCA1_1_1$l1*100)/sum(XCA$XCA1_1_1$l1)
```
 
