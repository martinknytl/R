# Table creation

```
CcVi3CZ_5_5 <- data.frame(p4=p4, q4=q4, d4=q4-p4, r4=q4/p4, i4=100/((q4/p4)+1))
```

# Order in the table according to column "r4"

```
CcVi3CZ_5_5 <- CcVi3CZ_5_5[order(CcVi3CZ_5_5$r4),]
```

```
CcVi3CZ_5_6$chromosome <- factor(c(rep(0, times=15), rep(1, times=37), rep(2, times=16), 3,3, rep(4, times=30)), labels = c("m", "sm", "st", "a", "T"))
```

```
CcVi3CZ_5_9$chromosome <- factor(c(rep(0, times=19), rep(1, times=19), rep(2, times=11), rep(4, times=51)), levels = 0:4, labels = c("m", "sm", "st", "a", "T"))
```

# Order according column "chromosome" (ascending) and then according chromosomal length (descending)
```
CcVi3CZ_5_6 <- CcVi3CZ_5_6 [order(CcVi3CZ_5_6$chromosome, -CcVi3CZ_5_6$d),]
```

# column "no" added
```
CcVi3CZ_5_6$no <- c(1:15, 1:37, 1:16, 1,2, 1:30)
```

# list added
```
CCA <- list(CcVi3CZ_5_10=CcVi3CZ_5_10, CcVi3CZ_5_9=CcVi3CZ_5_9, CcVi3CZ_5_6=CcVi3CZ_5_6)
```

chromosome ratio "r" column extracted from each table and sorted ascendingly:
```
r <- sort(CCA$CcHe6Fi_1_2$r)
```
r2, r3 ... r10

table r_sorted for statistics of each ratio in each row:
```
r_sorted <- data.frame(r=r, r2=r2, r3=r3, r4=r4, r5=r5, r6=r6, r7=r7, r8=r8, r9=r9, r10=r10)
```

```
r_sorted[50, "mean"] <- mean (c(r_sorted[50, "r"], r_sorted[50, "r3"], r_sorted[50, "r4"], r_sorted[50, "r5"], r_sorted[50, "r6"], r_sorted[50, "r7"], r_sorted[50, "r8"], r_sorted[50, "r9"], r_sorted[50, "r10"]))
```
