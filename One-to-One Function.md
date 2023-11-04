A function is a rule that assigns a single value in its range to each point in its domain. Some functions assign the same output to more than one input. For example, $f(x)=x^2$ assigns the output 4 to both 2 and -2. 

```functionplot
---
title: 
xLabel: 
yLabel: 
bounds: [-4,4,-1,7]
disableZoom: false
grid: true
---
f(x)=x^2
```

Other functions never output a given value more than once. For example, the cubes of different numbers are always different.

```functionplot
---
title: 
xLabel: 
yLabel: 
bounds: [-5,5,-5,5]
disableZoom: false
grid: true
---
f(x)=x^3
```

>[!Definition]
>A function $F(x)$ is **one-to-one** on a domain $D$ if $f(a)\ne f(b)$ whenever $a\ne b$.

The graph of a one-to-one function $y=f(x)$ can intersect any horizontal line at most once (the horizontal line test). If it intersects such a line more than once it assumes the same y-value more than once, and is therefore not one-to-one.