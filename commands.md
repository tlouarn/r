### How to plot a function

```R
density = function(x) {3 * x^2}
curve(density, from=0, to=1)
```

![image](https://github.com/tlouarn/financial-econometrics/assets/77942575/5a70bb70-bab0-4d42-8e9f-a783e2a1178a)


### How to write nested loops

```R
means = c()
for (j in c(10, 100, 1000, 10000, 100000)) {
  vec = c()
  for (i in 1:j) {
    value=density(i/j)
    vec = c(vec, value)
   }
   means = c(means, mean(vec))
}
means()
```

```cmd
1.155000 1.015050 1.001500 1.000150 1.000015
```
