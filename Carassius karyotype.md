#Table creation

```
CcVi3CZ_5_6$chromosome <- factor(c(rep(0, times=15), rep(1, times=37), rep(2, times=16), 3,3, rep(4, times=30)), labels = c("m", "sm", "st", "a", "T"))
```

#Order according chromosome column (ascending) and then according chromosomal length (descending)
```
CcVi3CZ_5_6 [order(CcVi3CZ_5_6$chromosome, -CcVi3CZ_5_6$d),]
```
