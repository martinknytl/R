### Table creation

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

