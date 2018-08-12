# 算法框架

suffix array的实现包含下面的主要步骤：

```code
n <- length(A)
for i <- 0,n-1
    P[0, i] <- A[i]在A的所有字符排序后的位置
cnt <- 1
for k <- 1,[logn]
    for i <- 0,n-1
        L[i] <- (P[k-1][i], P[k-1][i+cnt], i)
    sort L
    compute P[k][i], i=0,n-1
    cnt <- 2*cnt
```