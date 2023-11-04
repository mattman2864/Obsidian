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
# Inverses
Since each output of a one-to-one function comes from just one input, a one-to-one function can be reversed to send outputs back to the inputs from which they came. The function defined by reversing a one-to-one function $f$ is the **inverse of $f$**. The symbol for inverse of $f$ is $f^{-1}$, read "$f$ inverse." The $-1$ in $f^{-1}$ is not an exponent; $f^{-1}(x)$ does not mean $1/f(x)$.

Composing a function with its inverse in either order sends each output back to the input from which it came. Ino