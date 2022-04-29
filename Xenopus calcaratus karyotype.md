# XCA 

#### Metaphases were sorted increasingly in Google sheets according to chromosome from 1a > 1b > 2a ... 10a > 10b.

#### Vectors were written manually from measuring of each chromosome

e.g. for p1, and q1
```
p1 <- c(74.75760234,
        57.46129446,
        56.8,
        65.6,
        45.65,
        38.8,
        61.35,
        50.3,
        28.13333333,
        25.1,
        21.8,
        20,
        34.8,
        34.48125,
        37.83148148,
        39.55,
        30.5,
        27.65,
        27.1,
        26.0080292,
        47.2,
        48.9,
        47.40575916,
        43.1,
        46.45,
        41.5,
        39.93227513,
        30.01025641,
        19.4,
        24.15,
        16.15,
        20.05,
        23.2,
        19.9,
        30.55,
        28.75,
        15.55,
        13.35,
        14.7,
        12.7)
```

```
q1 <- c(105.2923977,
        99.43870554,
        90.5,
        78.9,
        78.1,
        79.9,
        75.4,
        81.95,
        87.91666667,
        83.1,
        89.55,
        86,
        62.65,
        57.46875,
        61.01851852,
        58.85,
        74.95,
        74.3,
        70.45,
        70.2919708,
        58.8,
        55.35,
        52.09424084,
        47.8,
        61.5,
        58.8,
        44.86772487,
        53.58974359,
        84.7,
        79.35,
        62.6,
        57.2,
        35.9,
        32.55,
        38.05,
        32.1,
        18.6,
        17.8,
        22.05,
        21.15)
```

#### creation of the list with each metaphase as a table

```
paste0(" data.frame(p", 1:36, "=p", 1:36, ",q", 1:36, "=q", 1:36, ",l", 1:36, "=p", 1:36, "+q", 1:36, ",r1_", 1:36, "=p", 1:36, "/q", 1:36, ",r2_", 1:36, "=q", 1:36, "/p", 1:36, ",i", 1:36, "=100/((q", 1:36, "/p", 1:36, ")+1))", collapse = ",")
```

#### "XCA <- list(" and name of individuals manually added
```
XCA <- list(XCA1_1_1=data.frame(p1=p1,q1=q1,l1=p1+q1,r1_1=p1/q1,r2_1=q1/p1,i1=100/((q1/p1)+1)), XCA1_2_5=data.frame(p2=p2,q2=q2,l2=p2+q2,r1_2=p2/q2,r2_2=q2/p2,i2=100/((q2/p2)+1)), XCA1_3_4=data.frame(p3=p3,q3=q3,l3=p3+q3,r1_3=p3/q3,r2_3=q3/p3,i3=100/((q3/p3)+1)), XCA1_3_8=data.frame(p4=p4,q4=q4,l4=p4+q4,r1_4=p4/q4,r2_4=q4/p4,i4=100/((q4/p4)+1)), XCA1_4_1=data.frame(p5=p5,q5=q5,l5=p5+q5,r1_5=p5/q5,r2_5=q5/p5,i5=100/((q5/p5)+1)), XCA1_9_3=data.frame(p6=p6,q6=q6,l6=p6+q6,r1_6=p6/q6,r2_6=q6/p6,i6=100/((q6/p6)+1)), XCA2_1_5=data.frame(p7=p7,q7=q7,l7=p7+q7,r1_7=p7/q7,r2_7=q7/p7,i7=100/((q7/p7)+1)), XCA2_4_1=data.frame(p8=p8,q8=q8,l8=p8+q8,r1_8=p8/q8,r2_8=q8/p8,i8=100/((q8/p8)+1)), XCA2_12_2=data.frame(p9=p9,q9=q9,l9=p9+q9,r1_9=p9/q9,r2_9=q9/p9,i9=100/((q9/p9)+1)), XCA3_1_2=data.frame(p10=p10,q10=q10,l10=p10+q10,r1_10=p10/q10,r2_10=q10/p10,i10=100/((q10/p10)+1)), XCA3_1_13=data.frame(p11=p11,q11=q11,l11=p11+q11,r1_11=p11/q11,r2_11=q11/p11,i11=100/((q11/p11)+1)), XCA3_7_14=data.frame(p12=p12,q12=q12,l12=p12+q12,r1_12=p12/q12,r2_12=q12/p12,i12=100/((q12/p12)+1)), XCA3_7_18=data.frame(p13=p13,q13=q13,l13=p13+q13,r1_13=p13/q13,r2_13=q13/p13,i13=100/((q13/p13)+1)), XCA3_7_19=data.frame(p14=p14,q14=q14,l14=p14+q14,r1_14=p14/q14,r2_14=q14/p14,i14=100/((q14/p14)+1)), CHR2_Image_9=data.frame(p15=p15,q15=q15,l15=p15+q15,r1_15=p15/q15,r2_15=q15/p15,i15=100/((q15/p15)+1)), CHR9_XCA_F1_2_17_Image_6=data.frame(p16=p16,q16=q16,l16=p16+q16,r1_16=p16/q16,r2_16=q16/p16,i16=100/((q16/p16)+1)), XCA28_CHR10_Image_1=data.frame(p17=p17,q17=q17,l17=p17+q17,r1_17=p17/q17,r2_17=q17/p17,i17=100/((q17/p17)+1)), XCA3_CBAND_Image_8=data.frame(p18=p18,q18=q18,l18=p18+q18,r1_18=p18/q18,r2_18=q18/p18,i18=100/((q18/p18)+1)), XCABaF1_2_7II_Image_15=data.frame(p19=p19,q19=q19,l19=p19+q19,r1_19=p19/q19,r2_19=q19/p19,i19=100/((q19/p19)+1)), XCA4_CHR8_Image_1=data.frame(p20=p20,q20=q20,l20=p20+q20,r1_20=p20/q20,r2_20=q20/p20,i20=100/((q20/p20)+1)), XCABaF1_2_19II_Image_31=data.frame(p21=p21,q21=q21,l21=p21+q21,r1_21=p21/q21,r2_21=q21/p21,i21=100/((q21/p21)+1)), XCABaF1_2_10II_Image_4=data.frame(p22=p22,q22=q22,l22=p22+q22,r1_22=p22/q22,r2_22=q22/p22,i22=100/((q22/p22)+1)), XCABaF1_2_4II_Image_7=data.frame(p23=p23,q23=q23,l23=p23+q23,r1_23=p23/q23,r2_23=q23/p23,i23=100/((q23/p23)+1)), XCABaF1_2_15II_Image_5=data.frame(p24=p24,q24=q24,l24=p24+q24,r1_24=p24/q24,r2_24=q24/p24,i24=100/((q24/p24)+1)), CHR7_Image_20=data.frame(p25=p25,q25=q25,l25=p25+q25,r1_25=p25/q25,r2_25=q25/p25,i25=100/((q25/p25)+1)), XCA20_CHR6_Image_11=data.frame(p26=p26,q26=q26,l26=p26+q26,r1_26=p26/q26,r2_26=q26/p26,i26=100/((q26/p26)+1)), XCABaF1_2_2II_Image_13=data.frame(p27=p27,q27=q27,l27=p27+q27,r1_27=p27/q27,r2_27=q27/p27,i27=100/((q27/p27)+1)), XCABaF1_2_9II_Image_16=data.frame(p28=p28,q28=q28,l28=p28+q28,r1_28=p28/q28,r2_28=q28/p28,i28=100/((q28/p28)+1)), XCAF1_2_CHR3_Image_7=data.frame(p29=p29,q29=q29,l29=p29+q29,r1_29=p29/q29,r2_29=q29/p29,i29=100/((q29/p29)+1)), XCABaF1_2_13II_Image_2=data.frame(p30=p30,q30=q30,l30=p30+q30,r1_30=p30/q30,r2_30=q30/p30,i30=100/((q30/p30)+1)), XCABaF1_2_14II_Image_4=data.frame(p31=p31,q31=q31,l31=p31+q31,r1_31=p31/q31,r2_31=q31/p31,i31=100/((q31/p31)+1)), XCAPCC5_8_Image_7ab=data.frame(p32=p32,q32=q32,l32=p32+q32,r1_32=p32/q32,r2_32=q32/p32,i32=100/((q32/p32)+1)), XCA_F1_2_16_CHR5_Image_5=data.frame(p33=p33,q33=q33,l33=p33+q33,r1_33=p33/q33,r2_33=q33/p33,i33=100/((q33/p33)+1)), CHR1_XCA2_2_Image_15=data.frame(p34=p34,q34=q34,l34=p34+q34,r1_34=p34/q34,r2_34=q34/p34,i34=100/((q34/p34)+1)), XCABaF1_2_7II_Image_7=data.frame(p35=p35,q35=q35,l35=p35+q35,r1_35=p35/q35,r2_35=q35/p35,i35=100/((q35/p35)+1)))
```

#### "l_percentage" folder into XCA list

```
> paste0(
+     "l_percentage", 1:36, "=(XCA$$l", 1:36, "*100)/sum(XCA$$l", 1:36, ")", collapse = ","
+ )
[1] "l_percentage1=(XCA$$l1*100)/sum(XCA$$l1),l_percentage2=(XCA$$l2*100)/sum(XCA$$l2),l_percentage3=(XCA$$l3*100)/sum(XCA$$l3),l_percentage4=(XCA$$l4*100)/sum(XCA$$l4),l_percentage5=(XCA$$l5*100)/sum(XCA$$l5),l_percentage6=(XCA$$l6*100)/sum(XCA$$l6),l_percentage7=(XCA$$l7*100)/sum(XCA$$l7),l_percentage8=(XCA$$l8*100)/sum(XCA$$l8),l_percentage9=(XCA$$l9*100)/sum(XCA$$l9),l_percentage10=(XCA$$l10*100)/sum(XCA$$l10),l_percentage11=(XCA$$l11*100)/sum(XCA$$l11),l_percentage12=(XCA$$l12*100)/sum(XCA$$l12),l_percentage13=(XCA$$l13*100)/sum(XCA$$l13),l_percentage14=(XCA$$l14*100)/sum(XCA$$l14),l_percentage15=(XCA$$l15*100)/sum(XCA$$l15),l_percentage16=(XCA$$l16*100)/sum(XCA$$l16),l_percentage17=(XCA$$l17*100)/sum(XCA$$l17),l_percentage18=(XCA$$l18*100)/sum(XCA$$l18),l_percentage19=(XCA$$l19*100)/sum(XCA$$l19),l_percentage20=(XCA$$l20*100)/sum(XCA$$l20),l_percentage21=(XCA$$l21*100)/sum(XCA$$l21),l_percentage22=(XCA$$l22*100)/sum(XCA$$l22),l_percentage23=(XCA$$l23*100)/sum(XCA$$l23),l_percentage24=(XCA$$l24*100)/sum(XCA$$l24),l_percentage25=(XCA$$l25*100)/sum(XCA$$l25),l_percentage26=(XCA$$l26*100)/sum(XCA$$l26),l_percentage27=(XCA$$l27*100)/sum(XCA$$l27),l_percentage28=(XCA$$l28*100)/sum(XCA$$l28),l_percentage29=(XCA$$l29*100)/sum(XCA$$l29),l_percentage30=(XCA$$l30*100)/sum(XCA$$l30),l_percentage31=(XCA$$l31*100)/sum(XCA$$l31),l_percentage32=(XCA$$l32*100)/sum(XCA$$l32),l_percentage33=(XCA$$l33*100)/sum(XCA$$l33),l_percentage34=(XCA$$l34*100)/sum(XCA$$l34),l_percentage35=(XCA$$l35*100)/sum(XCA$$l35),l_percentage36=(XCA$$l36*100)/sum(XCA$$l36)"
```
```
> names(XCA)
 [1] "XCA1_1_1"                 "XCA1_2_5"                 "XCA1_3_4"                 "XCA1_3_8"                
 [5] "XCA1_4_1"                 "XCA1_9_3"                 "XCA2_1_5"                 "XCA2_4_1"                
 [9] "XCA2_12_2"                "XCA3_1_2"                 "XCA3_1_13"                "XCA3_7_14"               
[13] "XCA3_7_18"                "XCA3_7_19"                "CHR2_Image_9"             "CHR9_XCA_F1_2_17_Image_6"
[17] "XCA28_CHR10_Image_1"      "XCA3_CBAND_Image_8"       "XCABaF1_2_7II_Image_15"   "XCA4_CHR8_Image_1"       
[21] "XCABaF1_2_19II_Image_31"  "XCABaF1_2_10II_Image_4"   "XCABaF1_2_4II_Image_7"    "XCABaF1_2_15II_Image_5"  
[25] "CHR7_Image_20"            "XCA20_CHR6_Image_11"      "XCABaF1_2_2II_Image_13"   "XCABaF1_2_9II_Image_16"  
[29] "XCAF1_2_CHR3_Image_7"     "XCABaF1_2_13II_Image_2"   "XCABaF1_2_14II_Image_4"   "XCAPCC5_8_Image_7ab"     
[33] "XCA_F1_2_16_CHR5_Image_5" "CHR1_XCA2_2_Image_15"     "XCABaF1_2_7II_Image_7"    "l_percentage_i"
```
```
XCA$l_percentage <- data.frame(
        l_percentage1=(XCA$XCA1_1_1$l1*100)/sum(XCA$XCA1_1_1$l1),
        l_percentage2=(XCA$XCA1_2_5$l2*100)/sum(XCA$XCA1_2_5$l2),
        l_percentage3=(XCA$XCA1_3_4$l3*100)/sum(XCA$XCA1_3_4$l3),
        l_percentage4=(XCA$XCA1_3_8$l4*100)/sum(XCA$XCA1_3_8$l4),
        l_percentage5=(XCA$XCA1_4_1$l5*100)/sum(XCA$XCA1_4_1$l5),
        l_percentage6=(XCA$XCA1_9_3$l6*100)/sum(XCA$XCA1_9_3$l6),
        l_percentage7=(XCA$XCA2_1_5$l7*100)/sum(XCA$XCA2_1_5$l7),
        l_percentage8=(XCA$XCA2_4_1$l8*100)/sum(XCA$XCA2_4_1$l8),
        l_percentage9=(XCA$XCA2_12_2$l9*100)/sum(XCA$XCA2_12_2$l9),
        l_percentage10=(XCA$XCA3_1_2$l10*100)/sum(XCA$XCA3_1_2$l10),
        l_percentage11=(XCA$XCA3_1_13$l11*100)/sum(XCA$XCA3_1_13$l11),
        l_percentage12=(XCA$XCA3_7_14$l12*100)/sum(XCA$XCA3_7_14$l12),
        l_percentage13=(XCA$XCA3_7_18$l13*100)/sum(XCA$XCA3_7_18$l13),
        l_percentage14=(XCA$XCA3_7_19$l14*100)/sum(XCA$XCA3_7_19$l14),
        l_percentage15=(XCA$CHR2_Image_9$l15*100)/sum(XCA$CHR2_Image_9$l15),
        l_percentage16=(XCA$CHR9_XCA_F1_2_17_Image_6$l16*100)/sum(XCA$CHR9_XCA_F1_2_17_Image_6$l16),
        l_percentage17=(XCA$XCA28_CHR10_Image_1$l17*100)/sum(XCA$XCA28_CHR10_Image_1$l17),
        l_percentage18=(XCA$XCA3_CBAND_Image_8$l18*100)/sum(XCA$XCA3_CBAND_Image_8$l18),
        l_percentage19=(XCA$XCABaF1_2_7II_Image_15$l19*100)/sum(XCA$XCABaF1_2_7II_Image_15$l19),
        l_percentage20=(XCA$XCA4_CHR8_Image_1$l20*100)/sum(XCA$XCA4_CHR8_Image_1$l20),
        l_percentage21=(XCA$XCABaF1_2_19II_Image_31$l21*100)/sum(XCA$XCABaF1_2_19II_Image_31$l21),
        l_percentage22=(XCA$XCABaF1_2_10II_Image_4$l22*100)/sum(XCA$XCABaF1_2_10II_Image_4$l22),
        l_percentage23=(XCA$XCABaF1_2_4II_Image_7$l23*100)/sum(XCA$XCABaF1_2_4II_Image_7$l23),
        l_percentage24=(XCA$XCABaF1_2_15II_Image_5$l24*100)/sum(XCA$XCABaF1_2_15II_Image_5$l24),
        l_percentage25=(XCA$CHR7_Image_20$l25*100)/sum(XCA$CHR7_Image_20$l25),
        l_percentage26=(XCA$XCA20_CHR6_Image_11$l26*100)/sum(XCA$XCA20_CHR6_Image_11$l26),
        l_percentage27=(XCA$XCABaF1_2_2II_Image_13$l27*100)/sum(XCA$XCABaF1_2_2II_Image_13$l27),
        l_percentage28=(XCA$XCABaF1_2_9II_Image_16$l28*100)/sum(XCA$XCABaF1_2_9II_Image_16$l28),
        l_percentage29=(XCA$XCAF1_2_CHR3_Image_7$l29*100)/sum(XCA$XCAF1_2_CHR3_Image_7$l29),
        l_percentage30=(XCA$XCABaF1_2_13II_Image_2$l30*100)/sum(XCA$XCABaF1_2_13II_Image_2$l30),
        l_percentage31=(XCA$XCABaF1_2_14II_Image_4$l31*100)/sum(XCA$XCABaF1_2_14II_Image_4$l31),
        l_percentage32=(XCA$XCAPCC5_8_Image_7ab$l32*100)/sum(XCA$XCAPCC5_8_Image_7ab$l32),
        l_percentage33=(XCA$XCA_F1_2_16_CHR5_Image_5$l33*100)/sum(XCA$XCA_F1_2_16_CHR5_Image_5$l33),
        l_percentage34=(XCA$CHR1_XCA2_2_Image_15$l34*100)/sum(XCA$CHR1_XCA2_2_Image_15$l34),
        l_percentage35=(XCA$XCABaF1_2_7II_Image_7$l35*100)/sum(XCA$XCABaF1_2_7II_Image_7$l35)
     )
```

#### "i" folder into XCA list

```
> paste0("i", 1:36, "=(XCA$", names(XCA[1:36]) ,"$i", 1:36, ")", collapse = ",")
[1] "i1=(XCA$XCA1_1_1$i1),i2=(XCA$XCA1_2_5$i2),i3=(XCA$XCA1_3_4$i3),i4=(XCA$XCA1_3_8$i4),i5=(XCA$XCA1_4_1$i5),i6=(XCA$XCA1_9_3$i6),i7=(XCA$XCA2_1_5$i7),i8=(XCA$XCA2_4_1$i8),i9=(XCA$XCA2_12_2$i9),i10=(XCA$XCA3_1_2$i10),i11=(XCA$XCA3_1_13$i11),i12=(XCA$XCA3_7_14$i12),i13=(XCA$XCA3_7_18$i13),i14=(XCA$XCA3_7_19$i14),i15=(XCA$CHR2_Image_9$i15),i16=(XCA$CHR9_XCA_F1_2_17_Image_6$i16),i17=(XCA$XCA28_CHR10_Image_1$i17),i18=(XCA$XCA3_CBAND_Image_8$i18),i19=(XCA$XCABaF1_2_7II_Image_15$i19),i20=(XCA$XCA4_CHR8_Image_1$i20),i21=(XCA$XCABaF1_2_19II_Image_31$i21),i22=(XCA$XCABaF1_2_10II_Image_4$i22),i23=(XCA$XCABaF1_2_4II_Image_7$i23),i24=(XCA$XCABaF1_2_15II_Image_5$i24),i25=(XCA$CHR7_Image_20$i25),i26=(XCA$XCA20_CHR6_Image_11$i26),i27=(XCA$XCABaF1_2_2II_Image_13$i27),i28=(XCA$XCABaF1_2_9II_Image_16$i28),i29=(XCA$XCAF1_2_CHR3_Image_7$i29),i30=(XCA$XCABaF1_2_13II_Image_2$i30),i31=(XCA$XCABaF1_2_14II_Image_4$i31),i32=(XCA$XCAPCC5_8_Image_7ab$i32),i33=(XCA$XCA_F1_2_16_CHR5_Image_5$i33),i34=(XCA$CHR1_XCA2_2_Image_15$i34),i35=(XCA$XCABaF1_2_7II_Image_7$i35),i36=(XCA$l_percentage$i36)"
```
```
XCA$i <- data.frame(
        i1=XCA$XCA1_1_1$i1,
        i2=XCA$XCA1_2_5$i2,
        i3=XCA$XCA1_3_4$i3,
        i4=XCA$XCA1_3_8$i4,
        i5=XCA$XCA1_4_1$i5,
        i6=XCA$XCA1_9_3$i6,
        i7=XCA$XCA2_1_5$i7,
        i8=XCA$XCA2_4_1$i8,
        i9=XCA$XCA2_12_2$i9,
        i10=XCA$XCA3_1_2$i10,
        i11=XCA$XCA3_1_13$i11,
        i12=XCA$XCA3_7_14$i12,
        i13=XCA$XCA3_7_18$i13,
        i14=XCA$XCA3_7_19$i14,
        i15=XCA$CHR2_Image_9$i15,
        i16=XCA$CHR9_XCA_F1_2_17_Image_6$i16,
        i17=(XCA$XCA28_CHR10_Image_1$i17),i18=(XCA$XCA3_CBAND_Image_8$i18),i19=(XCA$XCABaF1_2_7II_Image_15$i19),i20=(XCA$XCA4_CHR8_Image_1$i20),i21=(XCA$XCABaF1_2_19II_Image_31$i21),i22=(XCA$XCABaF1_2_10II_Image_4$i22),i23=(XCA$XCABaF1_2_4II_Image_7$i23),i24=(XCA$XCABaF1_2_15II_Image_5$i24),i25=(XCA$CHR7_Image_20$i25),i26=(XCA$XCA20_CHR6_Image_11$i26),i27=(XCA$XCABaF1_2_2II_Image_13$i27),i28=(XCA$XCABaF1_2_9II_Image_16$i28),i29=(XCA$XCAF1_2_CHR3_Image_7$i29),i30=(XCA$XCABaF1_2_13II_Image_2$i30),i31=(XCA$XCABaF1_2_14II_Image_4$i31),i32=(XCA$XCAPCC5_8_Image_7ab$i32),i33=(XCA$XCA_F1_2_16_CHR5_Image_5$i33),i34=(XCA$CHR1_XCA2_2_Image_15$i34),i35=(XCA$XCABaF1_2_7II_Image_7$i35)
)
```

#### mean and median of l percentage for each row of "l_percentage" data frame 
```
XCA$l_percentage$mean_l=apply (XCA$l_percentage, 1, mean)
XCA$l_percentage$median_l=apply (XCA$l_percentage, 1, median)
```
```
> paste0("XCA$l_percentage$l_percentage", 1:35, "[i:j]", collapse = ",")
[1] "XCA$l_percentage$l_percentage1[i:j],XCA$l_percentage$l_percentage2[i:j],XCA$l_percentage$l_percentage3[i:j],XCA$l_percentage$l_percentage4[i:j],XCA$l_percentage$l_percentage5[i:j],XCA$l_percentage$l_percentage6[i:j],XCA$l_percentage$l_percentage7[i:j],XCA$l_percentage$l_percentage8[i:j],XCA$l_percentage$l_percentage9[i:j],XCA$l_percentage$l_percentage10[i:j],XCA$l_percentage$l_percentage11[i:j],XCA$l_percentage$l_percentage12[i:j],XCA$l_percentage$l_percentage13[i:j],XCA$l_percentage$l_percentage14[i:j],XCA$l_percentage$l_percentage15[i:j],XCA$l_percentage$l_percentage16[i:j],XCA$l_percentage$l_percentage17[i:j],XCA$l_percentage$l_percentage18[i:j],XCA$l_percentage$l_percentage19[i:j],XCA$l_percentage$l_percentage20[i:j],XCA$l_percentage$l_percentage21[i:j],XCA$l_percentage$l_percentage22[i:j],XCA$l_percentage$l_percentage23[i:j],XCA$l_percentage$l_percentage24[i:j],XCA$l_percentage$l_percentage25[i:j],XCA$l_percentage$l_percentage26[i:j],XCA$l_percentage$l_percentage27[i:j],XCA$l_percentage$l_percentage28[i:j],XCA$l_percentage$l_percentage29[i:j],XCA$l_percentage$l_percentage30[i:j],XCA$l_percentage$l_percentage31[i:j],XCA$l_percentage$l_percentage32[i:j],XCA$l_percentage$l_percentage33[i:j],XCA$l_percentage$l_percentage34[i:j],XCA$l_percentage$l_percentage35[i:j]"
```

#### Function for dissection of "l_percentage" values for each haploid chromosome
```
Select_chrome <- function(i,j) {chromosome <- 
c(XCA$l_percentage$l_percentage1[i:j],XCA$l_percentage$l_percentage2[i:j],XCA$l_percentage$l_percentage3[i:j],XCA$l_percentage$l_percentage4[i:j],XCA$l_percentage$l_percentage5[i:j],XCA$l_percentage$l_percentage6[i:j],XCA$l_percentage$l_percentage7[i:j],XCA$l_percentage$l_percentage8[i:j],XCA$l_percentage$l_percentage9[i:j],XCA$l_percentage$l_percentage10[i:j],XCA$l_percentage$l_percentage11[i:j],XCA$l_percentage$l_percentage12[i:j],XCA$l_percentage$l_percentage13[i:j],XCA$l_percentage$l_percentage14[i:j],XCA$l_percentage$l_percentage15[i:j],XCA$l_percentage$l_percentage16[i:j],XCA$l_percentage$l_percentage17[i:j],XCA$l_percentage$l_percentage18[i:j],XCA$l_percentage$l_percentage19[i:j],XCA$l_percentage$l_percentage20[i:j],XCA$l_percentage$l_percentage21[i:j],XCA$l_percentage$l_percentage22[i:j],XCA$l_percentage$l_percentage23[i:j],XCA$l_percentage$l_percentage24[i:j],XCA$l_percentage$l_percentage25[i:j],XCA$l_percentage$l_percentage26[i:j],XCA$l_percentage$l_percentage27[i:j],XCA$l_percentage$l_percentage28[i:j],XCA$l_percentage$l_percentage29[i:j],XCA$l_percentage$l_percentage30[i:j],XCA$l_percentage$l_percentage31[i:j],XCA$l_percentage$l_percentage32[i:j],XCA$l_percentage$l_percentage33[i:j],XCA$l_percentage$l_percentage34[i:j],XCA$l_percentage$l_percentage35[i:j])
}

l_chromosome1 <- Select_chrome(1,2)
l_chromosome2 <- Select_chrome(3,4)
l_chromosome3 <- Select_chrome(5,6)
l_chromosome4 <- Select_chrome(7,8)
l_chromosome5 <- Select_chrome(9,10)
l_chromosome6 <- Select_chrome(11,12)
l_chromosome7 <- Select_chrome(13,14)
l_chromosome8 <- Select_chrome(15,16)
l_chromosome9 <- Select_chrome(17,18)
l_chromosome10 <- Select_chrome(19,20)
l_chromosome11 <- Select_chrome(21,22)
l_chromosome12 <- Select_chrome(23,24)
l_chromosome13 <- Select_chrome(25,26)
l_chromosome14 <- Select_chrome(27,28)
l_chromosome15 <- Select_chrome(29,30)
l_chromosome16 <- Select_chrome(31,32)
l_chromosome17 <- Select_chrome(33,34)
l_chromosome18 <- Select_chrome(35,36)
l_chromosome19 <- Select_chrome(37,38)
l_chromosome20 <- Select_chrome(39,40)
```
```
> paste0("l_chromosome", 1:20, "=l_chromosome", 1:20, collapse = ",")
[1] "l_chromosome1=l_chromosome1,l_chromosome2=l_chromosome2,l_chromosome3=l_chromosome3,l_chromosome4=l_chromosome4,l_chromosome5=l_chromosome5,l_chromosome6=l_chromosome6,l_chromosome7=l_chromosome7,l_chromosome8=l_chromosome8,l_chromosome9=l_chromosome9,l_chromosome10=l_chromosome10,l_chromosome11=l_chromosome11,l_chromosome12=l_chromosome12,l_chromosome13=l_chromosome13,l_chromosome14=l_chromosome14,l_chromosome15=l_chromosome15,l_chromosome16=l_chromosome16,l_chromosome17=l_chromosome17,l_chromosome18=l_chromosome18,l_chromosome19=l_chromosome19,l_chromosome20=l_chromosome20"
```
```
> l_chromosome1_20 <- list(l_chromosome1=l_chromosome1,l_chromosome2=l_chromosome2,l_chromosome3=l_chromosome3,l_chromosome4=l_chromosome4,l_chromosome5=l_chromosome5,l_chromosome6=l_chromosome6,l_chromosome7=l_chromosome7,l_chromosome8=l_chromosome8,l_chromosome9=l_chromosome9,l_chromosome10=l_chromosome10,l_chromosome11=l_chromosome11,l_chromosome12=l_chromosome12,l_chromosome13=l_chromosome13,l_chromosome14=l_chromosome14,l_chromosome15=l_chromosome15,l_chromosome16=l_chromosome16,l_chromosome17=l_chromosome17,l_chromosome18=l_chromosome18,l_chromosome19=l_chromosome19,l_chromosome20=l_chromosome20)
```

#### Function for dissection of "i" values for each haploid chromosome
```
> paste0("XCA$i$i", 1:35, "[i:j]", collapse = ",")
[1] "XCA$i$i1[i:j],XCA$i$i2[i:j],XCA$i$i3[i:j],XCA$i$i4[i:j],XCA$i$i5[i:j],XCA$i$i6[i:j],XCA$i$i7[i:j],XCA$i$i8[i:j],XCA$i$i9[i:j],XCA$i$i10[i:j],XCA$i$i11[i:j],XCA$i$i12[i:j],XCA$i$i13[i:j],XCA$i$i14[i:j],XCA$i$i15[i:j],XCA$i$i16[i:j],XCA$i$i17[i:j],XCA$i$i18[i:j],XCA$i$i19[i:j],XCA$i$i20[i:j],XCA$i$i21[i:j],XCA$i$i22[i:j],XCA$i$i23[i:j],XCA$i$i24[i:j],XCA$i$i25[i:j],XCA$i$i26[i:j],XCA$i$i27[i:j],XCA$i$i28[i:j],XCA$i$i29[i:j],XCA$i$i30[i:j],XCA$i$i31[i:j],XCA$i$i32[i:j],XCA$i$i33[i:j],XCA$i$i34[i:j],XCA$i$i35[i:j]"
```

```
> Select_chromeII<- function(i,j) {chromosome <- c(XCA$i$i1[i:j],XCA$i$i2[i:j],XCA$i$i3[i:j],XCA$i$i4[i:j],XCA$i$i5[i:j],XCA$i$i6[i:j],XCA$i$i7[i:j],XCA$i$i8[i:j],XCA$i$i9[i:j],XCA$i$i10[i:j],XCA$i$i11[i:j],XCA$i$i12[i:j],XCA$i$i13[i:j],XCA$i$i14[i:j],XCA$i$i15[i:j],XCA$i$i16[i:j],XCA$i$i17[i:j],XCA$i$i18[i:j],XCA$i$i19[i:j],XCA$i$i20[i:j],XCA$i$i21[i:j],XCA$i$i22[i:j],XCA$i$i23[i:j],XCA$i$i24[i:j],XCA$i$i25[i:j],XCA$i$i26[i:j],XCA$i$i27[i:j],XCA$i$i28[i:j],XCA$i$i29[i:j],XCA$i$i30[i:j],XCA$i$i31[i:j],XCA$i$i32[i:j],XCA$i$i33[i:j],XCA$i$i34[i:j],XCA$i$i35[i:j])
}

i_chromosome1 <- Select_chromeII(1,2)
i_chromosome2 <- Select_chromeII(3,4)
i_chromosome3 <- Select_chromeII(5,6)
i_chromosome4 <- Select_chromeII(7,8)
i_chromosome5 <- Select_chromeII(9,10)
i_chromosome6 <- Select_chromeII(11,12)
i_chromosome7 <- Select_chromeII(13,14)
i_chromosome8 <- Select_chromeII(15,16)
i_chromosome9 <- Select_chromeII(17,18)
i_chromosome10 <- Select_chromeII(19,20)
i_chromosome11 <- Select_chromeII(21,22)
i_chromosome12 <- Select_chromeII(23,24)
i_chromosome13 <- Select_chromeII(25,26)
i_chromosome14 <- Select_chromeII(27,28)
i_chromosome15 <- Select_chromeII(29,30)
i_chromosome16 <- Select_chromeII(31,32)
i_chromosome17 <- Select_chromeII(33,34)
i_chromosome18 <- Select_chromeII(35,36)
i_chromosome19 <- Select_chromeII(37,38)
i_chromosome20 <- Select_chromeII(39,40)
```
```
chromosome <- c("1a", "1b",  "2a", "2b",  "3a", "3b",  "4a", "4b",  "5a", "5b",  "6a", "6b",  "7a", "7b", "8a", "8b", "9a", "9b", "10a", "10b")
```
```
paste0("median(l_chromosome", 1:20, ")", collapse = ",")
[1] "median(l_chromosome1),median(l_chromosome2),median(l_chromosome3),median(l_chromosome4),median(l_chromosome5),median(l_chromosome6),median(l_chromosome7),median(l_chromosome8),median(l_chromosome9),median(l_chromosome10),median(l_chromosome11),median(l_chromosome12),median(l_chromosome13),median(l_chromosome14),median(l_chromosome15),median(l_chromosome16),median(l_chromosome17),median(l_chromosome18),median(l_chromosome19),median(l_chromosome20)"
```
```
median_l <-c(median(l_chromosome1),median(l_chromosome2),median(l_chromosome3),median(l_chromosome4),median(l_chromosome5),median(l_chromosome6),median(l_chromosome7),median(l_chromosome8),median(l_chromosome9),median(l_chromosome10),median(l_chromosome11),median(l_chromosome12),median(l_chromosome13),median(l_chromosome14),median(l_chromosome15),median(l_chromosome16),median(l_chromosome17),median(l_chromosome18),median(l_chromosome19),median(l_chromosome20))
```
```
> paste0("median(i_chromosome", 1:20, ")", collapse = ",")
[1] "median(i_chromosome1),median(i_chromosome2),median(i_chromosome3),median(i_chromosome4),median(i_chromosome5),median(i_chromosome6),median(i_chromosome7),median(i_chromosome8),median(i_chromosome9),median(i_chromosome10),median(i_chromosome11),median(i_chromosome12),median(i_chromosome13),median(i_chromosome14),median(i_chromosome15),median(i_chromosome16),median(i_chromosome17),median(i_chromosome18),median(i_chromosome19),median(i_chromosome20)"
```
```
i_chromosome1_20 <- list(i_chromosome1=i_chromosome1,i_chromosome2=i_chromosome2,i_chromosome3=i_chromosome3,i_chromosome4=i_chromosome4,i_chromosome5=i_chromosome5,i_chromosome6=i_chromosome6,i_chromosome7=i_chromosome7,i_chromosome8=i_chromosome8,i_chromosome9=i_chromosome9,i_chromosome10=i_chromosome10,i_chromosome11=i_chromosome11,i_chromosome12=i_chromosome12,i_chromosome13=i_chromosome13,i_chromosome14=i_chromosome14,i_chromosome15=i_chromosome15,i_chromosome16=i_chromosome16,i_chromosome17=i_chromosome17,i_chromosome18=i_chromosome18,i_chromosome19=i_chromosome19,i_chromosome20=i_chromosome20)
```
```
median_i <- c(median(i_chromosome1),median(i_chromosome2),median(i_chromosome3),median(i_chromosome4),median(i_chromosome5),median(i_chromosome6),median(i_chromosome7),median(i_chromosome8),median(i_chromosome9),median(i_chromosome10),median(i_chromosome11),median(i_chromosome12),median(i_chromosome13),median(i_chromosome14),median(i_chromosome15),median(i_chromosome16),median(i_chromosome17),median(i_chromosome18),median(i_chromosome19),median(i_chromosome20))
```

#### "r1" folder into XCA list
```
> paste0("r1_", 1:35, "=(XCA$", names(XCA[1:35]), "$r1_", 1:35, ")", collapse = ",")
[1] "r1_1=(XCA$XCA1_1_1$r1_1),r1_2=(XCA$XCA1_2_5$r1_2),r1_3=(XCA$XCA1_3_4$r1_3),r1_4=(XCA$XCA1_3_8$r1_4),r1_5=(XCA$XCA1_4_1$r1_5),r1_6=(XCA$XCA1_9_3$r1_6),r1_7=(XCA$XCA2_1_5$r1_7),r1_8=(XCA$XCA2_4_1$r1_8),r1_9=(XCA$XCA2_12_2$r1_9),r1_10=(XCA$XCA3_1_2$r1_10),r1_11=(XCA$XCA3_1_13$r1_11),r1_12=(XCA$XCA3_7_14$r1_12),r1_13=(XCA$XCA3_7_18$r1_13),r1_14=(XCA$XCA3_7_19$r1_14),r1_15=(XCA$CHR2_Image_9$r1_15),r1_16=(XCA$CHR9_XCA_F1_2_17_Image_6$r1_16),r1_17=(XCA$XCA28_CHR10_Image_1$r1_17),r1_18=(XCA$XCA3_CBAND_Image_8$r1_18),r1_19=(XCA$XCABaF1_2_7II_Image_15$r1_19),r1_20=(XCA$XCA4_CHR8_Image_1$r1_20),r1_21=(XCA$XCABaF1_2_19II_Image_31$r1_21),r1_22=(XCA$XCABaF1_2_10II_Image_4$r1_22),r1_23=(XCA$XCABaF1_2_4II_Image_7$r1_23),r1_24=(XCA$XCABaF1_2_15II_Image_5$r1_24),r1_25=(XCA$CHR7_Image_20$r1_25),r1_26=(XCA$XCA20_CHR6_Image_11$r1_26),r1_27=(XCA$XCABaF1_2_2II_Image_13$r1_27),r1_28=(XCA$XCABaF1_2_9II_Image_16$r1_28),r1_29=(XCA$XCAF1_2_CHR3_Image_7$r1_29),r1_30=(XCA$XCABaF1_2_13II_Image_2$r1_30),r1_31=(XCA$XCABaF1_2_14II_Image_4$r1_31),r1_32=(XCA$XCAPCC5_8_Image_7ab$r1_32),r1_33=(XCA$XCA_F1_2_16_CHR5_Image_5$r1_33),r1_34=(XCA$CHR1_XCA2_2_Image_15$r1_34),r1_35=(XCA$XCABaF1_2_7II_Image_7$r1_35)"
```
```
XCA$r1 <- data.frame(r1_1=(XCA$XCA1_1_1$r1_1),r1_2=(XCA$XCA1_2_5$r1_2),r1_3=(XCA$XCA1_3_4$r1_3),r1_4=(XCA$XCA1_3_8$r1_4),r1_5=(XCA$XCA1_4_1$r1_5),r1_6=(XCA$XCA1_9_3$r1_6),r1_7=(XCA$XCA2_1_5$r1_7),r1_8=(XCA$XCA2_4_1$r1_8),r1_9=(XCA$XCA2_12_2$r1_9),r1_10=(XCA$XCA3_1_2$r1_10),r1_11=(XCA$XCA3_1_13$r1_11),r1_12=(XCA$XCA3_7_14$r1_12),r1_13=(XCA$XCA3_7_18$r1_13),r1_14=(XCA$XCA3_7_19$r1_14),r1_15=(XCA$CHR2_Image_9$r1_15),r1_16=(XCA$CHR9_XCA_F1_2_17_Image_6$r1_16),r1_17=(XCA$XCA28_CHR10_Image_1$r1_17),r1_18=(XCA$XCA3_CBAND_Image_8$r1_18),r1_19=(XCA$XCABaF1_2_7II_Image_15$r1_19),r1_20=(XCA$XCA4_CHR8_Image_1$r1_20),r1_21=(XCA$XCABaF1_2_19II_Image_31$r1_21),r1_22=(XCA$XCABaF1_2_10II_Image_4$r1_22),r1_23=(XCA$XCABaF1_2_4II_Image_7$r1_23),r1_24=(XCA$XCABaF1_2_15II_Image_5$r1_24),r1_25=(XCA$CHR7_Image_20$r1_25),r1_26=(XCA$XCA20_CHR6_Image_11$r1_26),r1_27=(XCA$XCABaF1_2_2II_Image_13$r1_27),r1_28=(XCA$XCABaF1_2_9II_Image_16$r1_28),r1_29=(XCA$XCAF1_2_CHR3_Image_7$r1_29),r1_30=(XCA$XCABaF1_2_13II_Image_2$r1_30),r1_31=(XCA$XCABaF1_2_14II_Image_4$r1_31),r1_32=(XCA$XCAPCC5_8_Image_7ab$r1_32),r1_33=(XCA$XCA_F1_2_16_CHR5_Image_5$r1_33),r1_34=(XCA$CHR1_XCA2_2_Image_15$r1_34),r1_35=(XCA$XCABaF1_2_7II_Image_7$r1_35))
```

#### Function for dissection of "r1" values for each haploid chromosome
```
> paste0("XCA$r1$r1_", 1:35, "[i:j]", collapse = ",")
[1] "XCA$r1$r1_1[i:j],XCA$r1$r1_2[i:j],XCA$r1$r1_3[i:j],XCA$r1$r1_4[i:j],XCA$r1$r1_5[i:j],XCA$r1$r1_6[i:j],XCA$r1$r1_7[i:j],XCA$r1$r1_8[i:j],XCA$r1$r1_9[i:j],XCA$r1$r1_10[i:j],XCA$r1$r1_11[i:j],XCA$r1$r1_12[i:j],XCA$r1$r1_13[i:j],XCA$r1$r1_14[i:j],XCA$r1$r1_15[i:j],XCA$r1$r1_16[i:j],XCA$r1$r1_17[i:j],XCA$r1$r1_18[i:j],XCA$r1$r1_19[i:j],XCA$r1$r1_20[i:j],XCA$r1$r1_21[i:j],XCA$r1$r1_22[i:j],XCA$r1$r1_23[i:j],XCA$r1$r1_24[i:j],XCA$r1$r1_25[i:j],XCA$r1$r1_26[i:j],XCA$r1$r1_27[i:j],XCA$r1$r1_28[i:j],XCA$r1$r1_29[i:j],XCA$r1$r1_30[i:j],XCA$r1$r1_31[i:j],XCA$r1$r1_32[i:j],XCA$r1$r1_33[i:j],XCA$r1$r1_34[i:j],XCA$r1$r1_35[i:j]"
```
```
> Select_chromeIII <- function(i,j) {chromosome <- 
c(XCA$r1$r1_1[i:j],XCA$r1$r1_2[i:j],XCA$r1$r1_3[i:j],XCA$r1$r1_4[i:j],XCA$r1$r1_5[i:j],XCA$r1$r1_6[i:j],XCA$r1$r1_7[i:j],XCA$r1$r1_8[i:j],XCA$r1$r1_9[i:j],XCA$r1$r1_10[i:j],XCA$r1$r1_11[i:j],XCA$r1$r1_12[i:j],XCA$r1$r1_13[i:j],XCA$r1$r1_14[i:j],XCA$r1$r1_15[i:j],XCA$r1$r1_16[i:j],XCA$r1$r1_17[i:j],XCA$r1$r1_18[i:j],XCA$r1$r1_19[i:j],XCA$r1$r1_20[i:j],XCA$r1$r1_21[i:j],XCA$r1$r1_22[i:j],XCA$r1$r1_23[i:j],XCA$r1$r1_24[i:j],XCA$r1$r1_25[i:j],XCA$r1$r1_26[i:j],XCA$r1$r1_27[i:j],XCA$r1$r1_28[i:j],XCA$r1$r1_29[i:j],XCA$r1$r1_30[i:j],XCA$r1$r1_31[i:j],XCA$r1$r1_32[i:j],XCA$r1$r1_33[i:j],XCA$r1$r1_34[i:j],XCA$r1$r1_35[i:j])
}

r1_chromosome1 <- Select_chromeIII(1,2)
r1_chromosome2 <- Select_chromeIII(3,4)
r1_chromosome3 <- Select_chromeIII(5,6)
r1_chromosome4 <- Select_chromeIII(7,8)
r1_chromosome5 <- Select_chromeIII(9,10)
r1_chromosome6 <- Select_chromeIII(11,12)
r1_chromosome7 <- Select_chromeIII(13,14)
r1_chromosome8 <- Select_chromeIII(15,16)
r1_chromosome9 <- Select_chromeIII(17,18)
r1_chromosome10 <- Select_chromeIII(19,20)
r1_chromosome11 <- Select_chromeIII(21,22)
r1_chromosome12 <- Select_chromeIII(23,24)
r1_chromosome13 <- Select_chromeIII(25,26)
r1_chromosome14 <- Select_chromeIII(27,28)
r1_chromosome15 <- Select_chromeIII(29,30)
r1_chromosome16 <- Select_chromeIII(31,32)
r1_chromosome17 <- Select_chromeIII(33,34)
r1_chromosome18 <- Select_chromeIII(35,36)
r1_chromosome19 <- Select_chromeIII(37,38)
r1_chromosome20 <- Select_chromeIII(39,40)
```
```
> paste0("r1_chromosome", 1:20, "=r1_chromosome", 1:20, collapse = ",")
[1] "r1_chromosome1=r1_chromosome1,r1_chromosome2=r1_chromosome2,r1_chromosome3=r1_chromosome3,r1_chromosome4=r1_chromosome4,r1_chromosome5=r1_chromosome5,r1_chromosome6=r1_chromosome6,r1_chromosome7=r1_chromosome7,r1_chromosome8=r1_chromosome8,r1_chromosome9=r1_chromosome9,r1_chromosome10=r1_chromosome10,r1_chromosome11=r1_chromosome11,r1_chromosome12=r1_chromosome12,r1_chromosome13=r1_chromosome13,r1_chromosome14=r1_chromosome14,r1_chromosome15=r1_chromosome15,r1_chromosome16=r1_chromosome16,r1_chromosome17=r1_chromosome17,r1_chromosome18=r1_chromosome18,r1_chromosome19=r1_chromosome19,r1_chromosome20=r1_chromosome20"
```
```
> r1_chromosome1_20 <- list(r1_chromosome1=r1_chromosome1,r1_chromosome2=r1_chromosome2,r1_chromosome3=r1_chromosome3,r1_chromosome4=r1_chromosome4,r1_chromosome5=r1_chromosome5,r1_chromosome6=r1_chromosome6,r1_chromosome7=r1_chromosome7,r1_chromosome8=r1_chromosome8,r1_chromosome9=r1_chromosome9,r1_chromosome10=r1_chromosome10,r1_chromosome11=r1_chromosome11,r1_chromosome12=r1_chromosome12,r1_chromosome13=r1_chromosome13,r1_chromosome14=r1_chromosome14,r1_chromosome15=r1_chromosome15,r1_chromosome16=r1_chromosome16,r1_chromosome17=r1_chromosome17,r1_chromosome18=r1_chromosome18,r1_chromosome19=r1_chromosome19,r1_chromosome20=r1_chromosome20)
```
```
> paste0("median(r1_chromosome1_20$r1_chromosome", 1:20, ")", collapse = ",")
[1] "median(r1_chromosome1_20$r1_chromosome1),median(r1_chromosome1_20$r1_chromosome2),median(r1_chromosome1_20$r1_chromosome3),median(r1_chromosome1_20$r1_chromosome4),median(r1_chromosome1_20$r1_chromosome5),median(r1_chromosome1_20$r1_chromosome6),median(r1_chromosome1_20$r1_chromosome7),median(r1_chromosome1_20$r1_chromosome8),median(r1_chromosome1_20$r1_chromosome9),median(r1_chromosome1_20$r1_chromosome10),median(r1_chromosome1_20$r1_chromosome11),median(r1_chromosome1_20$r1_chromosome12),median(r1_chromosome1_20$r1_chromosome13),median(r1_chromosome1_20$r1_chromosome14),median(r1_chromosome1_20$r1_chromosome15),median(r1_chromosome1_20$r1_chromosome16),median(r1_chromosome1_20$r1_chromosome17),median(r1_chromosome1_20$r1_chromosome18),median(r1_chromosome1_20$r1_chromosome19),median(r1_chromosome1_20$r1_chromosome20)"
```
```
> median_r1 <- c(median(r1_chromosome1_20$r1_chromosome1),median(r1_chromosome1_20$r1_chromosome2),median(r1_chromosome1_20$r1_chromosome3),median(r1_chromosome1_20$r1_chromosome4),median(r1_chromosome1_20$r1_chromosome5),median(r1_chromosome1_20$r1_chromosome6),median(r1_chromosome1_20$r1_chromosome7),median(r1_chromosome1_20$r1_chromosome8),median(r1_chromosome1_20$r1_chromosome9),median(r1_chromosome1_20$r1_chromosome10),median(r1_chromosome1_20$r1_chromosome11),median(r1_chromosome1_20$r1_chromosome12),median(r1_chromosome1_20$r1_chromosome13),median(r1_chromosome1_20$r1_chromosome14),median(r1_chromosome1_20$r1_chromosome15),median(r1_chromosome1_20$r1_chromosome16),median(r1_chromosome1_20$r1_chromosome17),median(r1_chromosome1_20$r1_chromosome18),median(r1_chromosome1_20$r1_chromosome19),median(r1_chromosome1_20$r1_chromosome20))
```
```
 final_table <- data.frame(chromosome=chromosome, median_l=median_l, median_r1=median_r1, median_i=median_i)
```
#### Chromosomal category added
```
for(i in 1:20) {if(final_table$median_i[i]>=37.5) {final_table$category[i] = "m"} else if (final_table$median_i[i]>=25 & final_table$median_i[i]<37.5){final_table$category[i] = "sm"} else if (final_table$median_i[i]>=12.5 & final_table$median_i[i]<25){final_table$category[i] = "st"} else if (final_table$median_i[i]>0 & final_table$median_i[i]<12.5) {final_table$category[i] = "a"} else {final_table$category[i] = "T"}}```
```
```
> for (i in 1:20) {
+ cat("rm(l_chromosome", i, ")", "\n")    
+ }
rm(l_chromosome 1 ) 
rm(l_chromosome 2 ) 
rm(l_chromosome 3 ) 
rm(l_chromosome 4 ) 
rm(l_chromosome 5 ) 
rm(l_chromosome 6 ) 
rm(l_chromosome 7 ) 
rm(l_chromosome 8 ) 
rm(l_chromosome 9 ) 
rm(l_chromosome 10 ) 
rm(l_chromosome 11 ) 
rm(l_chromosome 12 ) 
rm(l_chromosome 13 ) 
rm(l_chromosome 14 ) 
rm(l_chromosome 15 ) 
rm(l_chromosome 16 ) 
rm(l_chromosome 17 ) 
rm(l_chromosome 18 ) 
rm(l_chromosome 19 ) 
rm(l_chromosome 20 ) 

rm(l_chromosome1) 
rm(l_chromosome2) 
rm(l_chromosome3) 
rm(l_chromosome4) 
rm(l_chromosome5) 
rm(l_chromosome6) 
rm(l_chromosome7) 
rm(l_chromosome8) 
rm(l_chromosome9) 
rm(l_chromosome10) 
rm(l_chromosome11) 
rm(l_chromosome12) 
rm(l_chromosome13) 
rm(l_chromosome14) 
rm(l_chromosome15) 
rm(l_chromosome16) 
rm(l_chromosome17) 
rm(l_chromosome18) 
rm(l_chromosome19) 
rm(l_chromosome20)
```
```
rm(i_chromosome1)
rm(i_chromosome2)
rm(i_chromosome3)
rm(i_chromosome4)
rm(i_chromosome5)
rm(i_chromosome6)
rm(i_chromosome7)
rm(i_chromosome8)
rm(i_chromosome9)
rm(i_chromosome10)
rm(i_chromosome11)
rm(i_chromosome12)
rm(i_chromosome13)
rm(i_chromosome14)
rm(i_chromosome15)
rm(i_chromosome16)
rm(i_chromosome17)
rm(i_chromosome18)
rm(i_chromosome19)
rm(i_chromosome20)
```
```
> for (i in 1:20) {
+     cat("rm(r1_chromosome", i, ")", "\n")    
+ }
rm(r1_chromosome 1 ) 
rm(r1_chromosome 2 ) 
rm(r1_chromosome 3 ) 
rm(r1_chromosome 4 ) 
rm(r1_chromosome 5 ) 
rm(r1_chromosome 6 ) 
rm(r1_chromosome 7 ) 
rm(r1_chromosome 8 ) 
rm(r1_chromosome 9 ) 
rm(r1_chromosome 10 ) 
rm(r1_chromosome 11 ) 
rm(r1_chromosome 12 ) 
rm(r1_chromosome 13 ) 
rm(r1_chromosome 14 ) 
rm(r1_chromosome 15 ) 
rm(r1_chromosome 16 ) 
rm(r1_chromosome 17 ) 
rm(r1_chromosome 18 ) 
rm(r1_chromosome 19 ) 
rm(r1_chromosome 20 )
```
```
 rm(r1_chromosome1) 
 rm(r1_chromosome2) 
 rm(r1_chromosome3) 
 rm(r1_chromosome4) 
 rm(r1_chromosome5) 
 rm(r1_chromosome6) 
 rm(r1_chromosome7) 
 rm(r1_chromosome8) 
 rm(r1_chromosome9) 
 rm(r1_chromosome10) 
 rm(r1_chromosome11) 
 rm(r1_chromosome12) 
 rm(r1_chromosome13) 
 rm(r1_chromosome14) 
 rm(r1_chromosome15) 
 rm(r1_chromosome16) 
 rm(r1_chromosome17) 
 rm(r1_chromosome18) 
 rm(r1_chromosome19) 
 rm(r1_chromosome20)
```

#### Dotplot created
```
plot(final_table$median_i, final_table$median_l, pch=16, col="red", ylim = c(0, 5), xlim = c(0, 50), xlab = "centromeric index", ylab = "chromosomal length (%)", ann=TRUE, las=1, abline(v=c(0, 12.5, 25, 37.5, 50), col="gray", lty=2))
```
```
XCA_dotplot <- recordPlot()
```

#### Boxplot created

```
boxplot(l_chromosome1_20$l_chromosome1,l_chromosome1_20$l_chromosome2,l_chromosome1_20$l_chromosome3,l_chromosome1_20$l_chromosome4,l_chromosome1_20$l_chromosome5,l_chromosome1_20$l_chromosome6,l_chromosome1_20$l_chromosome7,l_chromosome1_20$l_chromosome8,l_chromosome1_20$l_chromosome9,l_chromosome1_20$l_chromosome10,l_chromosome1_20$l_chromosome11,l_chromosome1_20$l_chromosome12,l_chromosome1_20$l_chromosome13,l_chromosome1_20$l_chromosome14,l_chromosome1_20$l_chromosome15,l_chromosome1_20$l_chromosome16,l_chromosome1_20$l_chromosome17,l_chromosome1_20$l_chromosome18,l_chromosome1_20$l_chromosome19,l_chromosome1_20$l_chromosome20, ylim=c(0, 5), xlim=c(1, 20), horizontal = FALSE, ylab = "chromosomal length (%)", xlab = "chromosome", las = 1, pch = 20, whisklty = 3, boxcol = "red", boxfill = gray(0.95), boxlwd = 2, boxwex = 0.7, names = chromosome)
```
```
XCA_boxplot <- recordPlot()
```

```
> paste0("i_chromosome1_20$i_chromosome", 1:20, collapse = ",")
[1] "i_chromosome1_20$i_chromosome1,i_chromosome1_20$i_chromosome2,i_chromosome1_20$i_chromosome3,i_chromosome1_20$i_chromosome4,i_chromosome1_20$i_chromosome5,i_chromosome1_20$i_chromosome6,i_chromosome1_20$i_chromosome7,i_chromosome1_20$i_chromosome8,i_chromosome1_20$i_chromosome9,i_chromosome1_20$i_chromosome10,i_chromosome1_20$i_chromosome11,i_chromosome1_20$i_chromosome12,i_chromosome1_20$i_chromosome13,i_chromosome1_20$i_chromosome14,i_chromosome1_20$i_chromosome15,i_chromosome1_20$i_chromosome16,i_chromosome1_20$i_chromosome17,i_chromosome1_20$i_chromosome18,i_chromosome1_20$i_chromosome19,i_chromosome1_20$i_chromosome20"
```

```
boxplot(i_chromosome1_20$i_chromosome1,i_chromosome1_20$i_chromosome2,i_chromosome1_20$i_chromosome3,i_chromosome1_20$i_chromosome4,i_chromosome1_20$i_chromosome5,i_chromosome1_20$i_chromosome6,i_chromosome1_20$i_chromosome7,i_chromosome1_20$i_chromosome8,i_chromosome1_20$i_chromosome9,i_chromosome1_20$i_chromosome10,i_chromosome1_20$i_chromosome11,i_chromosome1_20$i_chromosome12,i_chromosome1_20$i_chromosome13,i_chromosome1_20$i_chromosome14,i_chromosome1_20$i_chromosome15,i_chromosome1_20$i_chromosome16,i_chromosome1_20$i_chromosome17,i_chromosome1_20$i_chromosome18,i_chromosome1_20$i_chromosome19,i_chromosome1_20$i_chromosome20, ylim=c(-1, 50), xlim=c(1, 20), horizontal = FALSE, ylab = "centromeric index", xlab = "chromosome", las = 1, pch = 20, whisklty = 3, boxcol = "red", boxfill = gray(0.95), boxlwd = 2, boxwex = 0.7, names = chromosome)
```
```
XCA_boxplotII <- recordPlot()
```

#### Names of table columns changed
```
names(final_table) = c("chromosome", "median_l (%)", "median_r1", "median_i", "category")
```

#### XCA_boxplot stats
```
(boxplot(l_chromosome1_20$l_chromosome1,l_chromosome1_20$l_chromosome2,l_chromosome1_20$l_chromosome3,l_chromosome1_20$l_chromosome4,l_chromosome1_20$l_chromosome5,l_chromosome1_20$l_chromosome6,l_chromosome1_20$l_chromosome7,l_chromosome1_20$l_chromosome8,l_chromosome1_20$l_chromosome9,l_chromosome1_20$l_chromosome10,l_chromosome1_20$l_chromosome11,l_chromosome1_20$l_chromosome12,l_chromosome1_20$l_chromosome13,l_chromosome1_20$l_chromosome14,l_chromosome1_20$l_chromosome15,l_chromosome1_20$l_chromosome16,l_chromosome1_20$l_chromosome17,l_chromosome1_20$l_chromosome18,l_chromosome1_20$l_chromosome19,l_chromosome1_20$l_chromosome20, ylim=c(0, 5), xlim=c(1, 20), horizontal = FALSE, ylab = "chromosomal length (%)", xlab = "chromosome", las = 1, pch = 20, whisklty = 3, boxcol = "red", boxfill = gray(0.95), boxlwd = 2, boxwex = 0.7, names = chromosome))
$stats
         [,1]     [,2]     [,3]     [,4]     [,5]     [,6]     [,7]     [,8]     [,9]    [,10]
[1,] 3.238750 3.087458 2.818954 2.775559 2.615323 2.377114 2.304634 2.467552 2.343665 2.336440
[2,] 3.618799 3.578954 2.995260 3.088551 2.860517 2.714208 2.564137 2.680951 2.617413 2.514486
[3,] 3.781723 3.789659 3.114178 3.203917 2.984431 2.796460 2.654493 2.795698 2.731991 2.632847
[4,] 3.978187 3.939321 3.258233 3.387081 3.095660 2.943860 2.755438 2.870369 2.853383 2.764584
[5,] 4.284397 4.255518 3.644626 3.825311 3.373983 3.243612 2.953409 3.145121 3.197429 3.105986
        [,11]    [,12]    [,13]    [,14]    [,15]    [,16]    [,17]    [,18]     [,19]     [,20]
[1,] 2.405518 2.081271 2.078860 1.875698 2.082604 1.879283 1.136505 1.095441 0.6302140 0.6637839
[2,] 2.616222 2.377433 2.366186 2.063142 2.360355 2.174267 1.379060 1.369498 0.8835760 0.8421777
[3,] 2.691722 2.538577 2.482159 2.155733 2.474503 2.283615 1.474569 1.475049 0.9769945 0.9264198
[4,] 2.771300 2.592444 2.606962 2.269352 2.611833 2.449195 1.545798 1.567031 1.0800464 0.9885248
[5,] 2.896101 2.802170 2.823246 2.489405 2.784259 2.674049 1.720180 1.764630 1.2669116 1.1337334

$n
 [1] 70 70 70 70 70 70 70 70 70 70 70 70 70 70 70 70 70 70 70 70

$conf
         [,1]     [,2]     [,3]     [,4]     [,5]     [,6]     [,7]     [,8]     [,9]    [,10]
[1,] 3.713854 3.721605 3.064517 3.147541 2.940025 2.753091 2.618366 2.759927 2.687429 2.585617
[2,] 3.849592 3.857713 3.163840 3.260293 3.028837 2.839829 2.690619 2.831469 2.776553 2.680077
        [,11]    [,12]    [,13]    [,14]    [,15]    [,16]    [,17]    [,18]     [,19]     [,20]
[1,] 2.662436 2.497973 2.436689 2.116791 2.427012 2.231696 1.443081 1.437746 0.9398918 0.8987828
[2,] 2.721008 2.579181 2.527628 2.194675 2.521993 2.335534 1.506057 1.512352 1.0140972 0.9540569

$out
 [1] 4.6315113 4.5181758 4.5372288 4.5777786 3.3295577 3.4942207 3.1582776 2.2105212 3.2921502
[10] 2.2533294 1.7732723 3.3097254 3.2586018 2.1194035 2.0524109 2.3464678 3.0987769 3.1025154
[19] 3.0370160 1.9177559 3.0879059 1.6670859 1.6666676 1.4269175 1.4942721 1.4802290 1.2917354
[28] 1.6618817 1.7193953 2.9182522 1.1260339 1.9198483 2.4252013 2.2090351 0.8661211 2.0304920
[37] 1.8898360 1.4101658

$group
 [1]  1  1  1  2  6  6  7  7  7  7  7  8  9 10 10 11 11 11 11 12 13 14 14 14 14 16 16 16 16 16 17
[32] 17 17 17 18 18 18 19

$names
 [1] "1a"  "1b"  "2a"  "2b"  "3a"  "3b"  "4a"  "4b"  "5a"  "5b"  "6a"  "6b"  "7a"  "7b"  "8a" 
[16] "8b"  "9a"  "9b"  "10a" "10b"
```

#### XCA_boxplotII stats
```
(boxplot(i_chromosome1_20$i_chromosome1,i_chromosome1_20$i_chromosome2,i_chromosome1_20$i_chromosome3,i_chromosome1_20$i_chromosome4,i_chromosome1_20$i_chromosome5,i_chromosome1_20$i_chromosome6,i_chromosome1_20$i_chromosome7,i_chromosome1_20$i_chromosome8,i_chromosome1_20$i_chromosome9,i_chromosome1_20$i_chromosome10,i_chromosome1_20$i_chromosome11,i_chromosome1_20$i_chromosome12,i_chromosome1_20$i_chromosome13,i_chromosome1_20$i_chromosome14,i_chromosome1_20$i_chromosome15,i_chromosome1_20$i_chromosome16,i_chromosome1_20$i_chromosome17,i_chromosome1_20$i_chromosome18,i_chromosome1_20$i_chromosome19,i_chromosome1_20$i_chromosome20, ylim=c(-1, 50), xlim=c(1, 20), horizontal = FALSE, ylab = "centromeric index", xlab = "chromosome", las = 1, pch = 20, whisklty = 3, boxcol = "red", boxfill = gray(0.95), boxlwd = 2, boxwex = 0.7, names = chromosome))
$stats
         [,1]     [,2]     [,3]     [,4]     [,5]     [,6]     [,7]     [,8]     [,9]    [,10]
[1,] 35.84084 35.25123 29.68460 32.12840 11.36320 11.12050 32.75425 28.48249 24.07490 20.99107
[2,] 39.87568 40.82517 34.69278 37.07267 15.20434 14.69181 35.82360 35.16353 29.97802 25.38742
[3,] 42.09607 43.14983 37.03789 38.67386 16.58375 16.74142 37.47840 38.42242 33.10950 27.33259
[4,] 44.23338 45.76117 38.38949 41.52641 19.04762 18.78823 39.86246 40.00086 35.07785 29.31048
[5,] 49.01478 50.00000 43.65747 47.22297 24.24242 23.69191 45.05597 44.79629 38.25438 33.45725
        [,11]    [,12]    [,13]    [,14]     [,15]     [,16]    [,17]    [,18]    [,19]    [,20]
[1,] 43.49776 42.00992 36.65107 35.72651  8.245662  8.850932 35.35916 39.42596 34.27174 31.92834
[2,] 45.50746 45.23020 41.62866 40.96124 13.647524 13.042230 41.64856 42.58549 40.60463 39.19283
[3,] 46.93671 46.62692 43.37677 43.78446 14.733357 15.468313 44.30807 44.53656 42.78175 42.89692
[4,] 48.15213 48.24585 45.02080 45.57206 17.748756 17.825906 45.92790 46.82300 45.98535 45.11952
[5,] 49.88551 49.91618 49.08449 48.79207 23.673651 23.807496 48.78361 49.85852 49.15074 48.87833

$n
 [1] 70 70 70 70 70 70 70 70 70 70 70 70 70 70 70 70 70 70 70 70

$conf
         [,1]     [,2]     [,3]     [,4]     [,5]     [,6]     [,7]     [,8]     [,9]    [,10]
[1,] 41.27314 42.21768 36.33978 37.83279 15.85796 15.96783 36.71568 37.50890 32.14642 26.59173
[2,] 42.91900 44.08197 37.73600 39.51493 17.30953 17.51502 38.24113 39.33593 34.07259 28.07344
        [,11]    [,12]    [,13]    [,14]    [,15]    [,16]    [,17]    [,18]    [,19]    [,20]
[1,] 46.43727 46.05743 42.73618 42.91373 13.95885 14.56493 43.49993 43.73633 41.76562 41.77768
[2,] 47.43614 47.19642 44.01736 44.65520 15.50786 16.37169 45.11620 45.33680 43.79788 44.01615

$out
 [1] 33.014524 28.842832 33.121393 44.419208 44.276923 29.105575 48.896534 44.308229  8.804378
[10] 26.512739 41.291043 41.478494 32.066190 34.958512 32.993748 24.914676 25.376555 33.689064
[19] 25.954693 26.624378 35.996636 28.677673 27.472513 22.183546 29.710605

$group
 [1]  1  1  1  3  3  3  3  3  5  6 10 11 13 13 14 15 15 15 16 17 18 19 20 20 20

$names
 [1] "1a"  "1b"  "2a"  "2b"  "3a"  "3b"  "4a"  "4b"  "5a"  "5b"  "6a"  "6b"  "7a"  "7b"  "8a" 
[16] "8b"  "9a"  "9b"  "10a" "10b"
```

#### Positions of plots changed

```
> split.screen(c(2,1))
[1] 1 2
> split.screen(c(1,2), screen=2)
[1] 3 4
```
```
screen(1)
par(mar=c(3.9, 4, 0.85, 0.50), mai=c(0.8, 0.8, 0.67, 0.10))
 
plot(final_table$median_i, final_table$`median_l (%)`, pch=16, col="red", ylim = c(0, 5), xlim = c(0, 50), xlab = "centromeric index", ylab = "length (%)", ann=TRUE, las=1, abline(v=c(0, 12.5, 25, 37.5, 50), col="gray", lty=2))
```
```
screen(3)
par(mar=c(3.9, 4, 0.85, 0.50), mai=c(0.80, 0.80, 0.17, 0.10))
 boxplot(l_chromosome1_20$l_chromosome1,l_chromosome1_20$l_chromosome2,l_chromosome1_20$l_chromosome3,l_chromosome1_20$l_chromosome4,l_chromosome1_20$l_chromosome5,l_chromosome1_20$l_chromosome6,l_chromosome1_20$l_chromosome7,l_chromosome1_20$l_chromosome8,l_chromosome1_20$l_chromosome9,l_chromosome1_20$l_chromosome10,l_chromosome1_20$l_chromosome11,l_chromosome1_20$l_chromosome12,l_chromosome1_20$l_chromosome13,l_chromosome1_20$l_chromosome14,l_chromosome1_20$l_chromosome15,l_chromosome1_20$l_chromosome16,l_chromosome1_20$l_chromosome17,l_chromosome1_20$l_chromosome18,l_chromosome1_20$l_chromosome19,l_chromosome1_20$l_chromosome20, ylim=c(0, 5), xlim=c(1, 20), horizontal = FALSE, ylab = "length (%)", xlab = "chromosome", las = 1, pch = 20, whisklty = 3, boxcol = "red", boxfill = gray(0.95), boxlwd = 2, boxwex = 0.7, names = chromosome)
```
```
screen(4)
par(mar=c(3.9, 4, 0.85, 0.50), mai=c(0.80, 0.80, 0.17, 0.10))
 boxplot(i_chromosome1_20$i_chromosome1,i_chromosome1_20$i_chromosome2,i_chromosome1_20$i_chromosome3,i_chromosome1_20$i_chromosome4,i_chromosome1_20$i_chromosome5,i_chromosome1_20$i_chromosome6,i_chromosome1_20$i_chromosome7,i_chromosome1_20$i_chromosome8,i_chromosome1_20$i_chromosome9,i_chromosome1_20$i_chromosome10,i_chromosome1_20$i_chromosome11,i_chromosome1_20$i_chromosome12,i_chromosome1_20$i_chromosome13,i_chromosome1_20$i_chromosome14,i_chromosome1_20$i_chromosome15,i_chromosome1_20$i_chromosome16,i_chromosome1_20$i_chromosome17,i_chromosome1_20$i_chromosome18,i_chromosome1_20$i_chromosome19,i_chromosome1_20$i_chromosome20, ylim=c(-1, 50), xlim=c(1, 20), horizontal = FALSE, ylab = "centromeric index", xlab = "chromosome", las = 1, pch = 20, whisklty = 3, boxcol = "red", boxfill = gray(0.95), boxlwd = 2, boxwex = 0.7, names = chromosome)
```
```
rm(XCA_multiplot)
rm(XCA_multiplotII)
XCA_multiplot <- recordPlot()
```
save as image (999 x 605)
```
setwd("C:/Users/Martin/Documents/R/XCA_paper")
write.table(final_table, file = "final_table.txt")
```

#### Export data frame (Table 1) from R to LaTeX

```
library(xtable)
```
```
print(xtable(CAU_CCA_CGI_median, type = "latex"), file = "CAU_CCA_CGI_median_i.tex")
```

open table in R, ctrl+c from R and ctrl+v to LaTeX

#### Statistical test of variability

```
> paste0("l_chromosome", seq(from=1, to=20, by=2), "_", seq(from=2, to=20, by=2), " <- paste (c(l_chromosome", seq(from=1, to=20, by=2), ", l_chromosome", seq(from=2, to=20, by=2), "))")
 [1] "l_chromosome1_2 <- paste (c(l_chromosome1, l_chromosome2))"    
 [2] "l_chromosome3_4 <- paste (c(l_chromosome3, l_chromosome4))"    
 [3] "l_chromosome5_6 <- paste (c(l_chromosome5, l_chromosome6))"    
 [4] "l_chromosome7_8 <- paste (c(l_chromosome7, l_chromosome8))"    
 [5] "l_chromosome9_10 <- paste (c(l_chromosome9, l_chromosome10))"  
 [6] "l_chromosome11_12 <- paste (c(l_chromosome11, l_chromosome12))"
 [7] "l_chromosome13_14 <- paste (c(l_chromosome13, l_chromosome14))"
 [8] "l_chromosome15_16 <- paste (c(l_chromosome15, l_chromosome16))"
 [9] "l_chromosome17_18 <- paste (c(l_chromosome17, l_chromosome18))"
[10] "l_chromosome19_20 <- paste (c(l_chromosome19, l_chromosome20))"
```

Manually modifyed outputs as new scripts:
```
l_chromosome1_2 <- paste (c(l_chromosome1, l_chromosome2))    
l_chromosome3_4 <- paste (c(l_chromosome3, l_chromosome4))    
l_chromosome5_6 <- paste (c(l_chromosome5, l_chromosome6))    
l_chromosome7_8 <- paste (c(l_chromosome7, l_chromosome8))   
l_chromosome9_10 <- paste (c(l_chromosome9, l_chromosome10)) 
l_chromosome11_12 <- paste (c(l_chromosome11, l_chromosome12))
l_chromosome13_14 <- paste (c(l_chromosome13, l_chromosome14))
l_chromosome15_16 <- paste (c(l_chromosome15, l_chromosome16))
l_chromosome17_18 <- paste (c(l_chromosome17, l_chromosome18))
l_chromosome19_20 <- paste (c(l_chromosome19, l_chromosome20))
```

```
> paste0("chromosome", 1:10, " <- c(rep('", 1:10, "a', times=70), rep('", 1:10, "b', times=70))")
 [1] "chromosome1 <- c(rep('1a', times=70), rep('1b', times=70))"   
 [2] "chromosome2 <- c(rep('2a', times=70), rep('2b', times=70))"   
 [3] "chromosome3 <- c(rep('3a', times=70), rep('3b', times=70))"   
 [4] "chromosome4 <- c(rep('4a', times=70), rep('4b', times=70))"   
 [5] "chromosome5 <- c(rep('5a', times=70), rep('5b', times=70))"   
 [6] "chromosome6 <- c(rep('6a', times=70), rep('6b', times=70))"   
 [7] "chromosome7 <- c(rep('7a', times=70), rep('7b', times=70))"   
 [8] "chromosome8 <- c(rep('8a', times=70), rep('8b', times=70))"   
 [9] "chromosome9 <- c(rep('9a', times=70), rep('9b', times=70))"   
[10] "chromosome10 <- c(rep('10a', times=70), rep('10b', times=70))"
```

Manually modifyed outputs as new scripts:

```
chromosome1 <- c(rep('1a', times=70), rep('1b', times=70))   
chromosome2 <- c(rep('2a', times=70), rep('2b', times=70))   
chromosome3 <- c(rep('3a', times=70), rep('3b', times=70))   
chromosome4 <- c(rep('4a', times=70), rep('4b', times=70))   
chromosome5 <- c(rep('5a', times=70), rep('5b', times=70))   
chromosome6 <- c(rep('6a', times=70), rep('6b', times=70))   
chromosome7 <- c(rep('7a', times=70), rep('7b', times=70))   
chromosome8 <- c(rep('8a', times=70), rep('8b', times=70))   
chromosome9 <- c(rep('9a', times=70), rep('9b', times=70))   
chromosome10 <- c(rep('10a', times=70), rep('10b', times=70))
```

```
> paste0("l_chromosome", 1:10, "_ANOVA = data.frame(chromosome", 1:10, "=chromosome", 1:10, ", l_chromosome", seq(from=1, to=20, by=2), "_", seq(from=2, to=20, by=2))
 [1] "l_chromosome1_ANOVA = data.frame(chromosome1=chromosome1, l_chromosome1_2"     
 [2] "l_chromosome2_ANOVA = data.frame(chromosome2=chromosome2, l_chromosome3_4"     
 [3] "l_chromosome3_ANOVA = data.frame(chromosome3=chromosome3, l_chromosome5_6"     
 [4] "l_chromosome4_ANOVA = data.frame(chromosome4=chromosome4, l_chromosome7_8"     
 [5] "l_chromosome5_ANOVA = data.frame(chromosome5=chromosome5, l_chromosome9_10"    
 [6] "l_chromosome6_ANOVA = data.frame(chromosome6=chromosome6, l_chromosome11_12"   
 [7] "l_chromosome7_ANOVA = data.frame(chromosome7=chromosome7, l_chromosome13_14"   
 [8] "l_chromosome8_ANOVA = data.frame(chromosome8=chromosome8, l_chromosome15_16"   
 [9] "l_chromosome9_ANOVA = data.frame(chromosome9=chromosome9, l_chromosome17_18"   
[10] "l_chromosome10_ANOVA = data.frame(chromosome10=chromosome10, l_chromosome19_20"
```
```
Manually modifyed outputs as new scripts:

```
ANOVA <- list(
    l_chromosome1_ANOVA = data.frame(chromosome1=chromosome1, l_chromosome1_2),
    l_chromosome2_ANOVA = data.frame(chromosome2=chromosome2, l_chromosome3_4),
    l_chromosome3_ANOVA = data.frame(chromosome3=chromosome3, l_chromosome5_6),
    l_chromosome4_ANOVA = data.frame(chromosome4=chromosome4, l_chromosome7_8),
    l_chromosome5_ANOVA = data.frame(chromosome5=chromosome5, l_chromosome9_10),   
    l_chromosome6_ANOVA = data.frame(chromosome6=chromosome6, l_chromosome11_12),   
    l_chromosome7_ANOVA = data.frame(chromosome7=chromosome7, l_chromosome13_14), 
    l_chromosome8_ANOVA = data.frame(chromosome8=chromosome8, l_chromosome15_16), 
    l_chromosome9_ANOVA = data.frame(chromosome9=chromosome9, l_chromosome17_18 ),
    l_chromosome10_ANOVA = data.frame(chromosome10=chromosome10, l_chromosome19_20)
     )
```     
```
> paste0("one.way <- aov(l_chromosome", seq(from=1, to=20, by=2), "_", seq(from=2, to=20, by=2), " ~ chromosome", 1:10, ", data = ANOVA$l_chromosome", 1:10, "_ANOVA)")
 [1] "one.way <- aov(l_chromosome1_2 ~ chromosome1, data = ANOVA$l_chromosome1_ANOVA)"    
 [2] "one.way <- aov(l_chromosome3_4 ~ chromosome2, data = ANOVA$l_chromosome2_ANOVA)"    
 [3] "one.way <- aov(l_chromosome5_6 ~ chromosome3, data = ANOVA$l_chromosome3_ANOVA)"    
 [4] "one.way <- aov(l_chromosome7_8 ~ chromosome4, data = ANOVA$l_chromosome4_ANOVA)"    
 [5] "one.way <- aov(l_chromosome9_10 ~ chromosome5, data = ANOVA$l_chromosome5_ANOVA)"   
 [6] "one.way <- aov(l_chromosome11_12 ~ chromosome6, data = ANOVA$l_chromosome6_ANOVA)"  
 [7] "one.way <- aov(l_chromosome13_14 ~ chromosome7, data = ANOVA$l_chromosome7_ANOVA)"  
 [8] "one.way <- aov(l_chromosome15_16 ~ chromosome8, data = ANOVA$l_chromosome8_ANOVA)"  
 [9] "one.way <- aov(l_chromosome17_18 ~ chromosome9, data = ANOVA$l_chromosome9_ANOVA)"  
[10] "one.way <- aov(l_chromosome19_20 ~ chromosome10, data = ANOVA$l_chromosome10_ANOVA)"
```
```
one.way <- aov(l_chromosome1_2 ~ chromosome1, data = ANOVA$l_chromosome1_ANOVA)
```
```
summary(one.way)
```
```
one.way <- aov(l_chromosome3_4 ~ chromosome2, data = ANOVA$l_chromosome2_ANOVA)    
```
```
summary(one.way)
```
```
one.way <- aov(l_chromosome5_6 ~ chromosome3, data = ANOVA$l_chromosome3_ANOVA)    
```
```
summary(one.way)
```
```
one.way <- aov(l_chromosome7_8 ~ chromosome4, data = ANOVA$l_chromosome4_ANOVA)   
```
```
summary(one.way)
```
```
one.way <- aov(l_chromosome9_10 ~ chromosome5, data = ANOVA$l_chromosome5_ANOVA)   
```
```
summary(one.way)
```
```
one.way <- aov(l_chromosome11_12 ~ chromosome6, data = ANOVA$l_chromosome6_ANOVA)  
```
```
summary(one.way)
```
```
one.way <- aov(l_chromosome13_14 ~ chromosome7, data = ANOVA$l_chromosome7_ANOVA)  
```
```
summary(one.way)
```
```
one.way <- aov(l_chromosome15_16 ~ chromosome8, data = ANOVA$l_chromosome8_ANOVA)  
```
```
summary(one.way)
```
```
one.way <- aov(l_chromosome17_18 ~ chromosome9, data = ANOVA$l_chromosome9_ANOVA)
```
```
summary(one.way)
```
```
one.way <- aov(l_chromosome19_20 ~ chromosome10, data = ANOVA$l_chromosome10_ANOVA)
```
```
summary(one.way)
```
