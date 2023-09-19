One sample intervals are [[Confidence Interval]]s where there is only a single sample being estimated, whether it be a proportion or a mean.
## Estimating $\mu$
### One Sample $z$-interval for $\mu$
$\displaystyle\bar{x}\pm z^*\frac{\sigma}{\sqrt{n}}$ **Not Realistic**
### One Sample $t$ interval for $\mu$
$\displaystyle\bar{x}\pm t^*\frac{S_x}{\sqrt{n}}$ **Realistic**
### $t$ distribution
- $t$ distributions are similar to standard Normal distributions
	- Symmetric, centered at 0, single peaked, bell-shaped
- However, the spread is larger
	- i.e. There is more probability in the tails and less in the center
### Degrees of Freedom
- There is a different $t$ distribution for each sample size, so we use degrees of freedom
- $df=n-1$
- as $df$ increase, $t$ distribution gets closer to [[Normal Distribution]]
### To find $t^*$
use $df$ and % in tail
Methods:
1. `invT(area, df)`
	- When the actual $df$ does not appear in the table, use the greatest $df$ available that is less than your desired $df$
2. [[Table B]]
	- $df$ on left
	- % on top
### Two Methods for Confidence Intervals
- One sample $z$-interval for [[Population]] proportion
	- $\displaystyle\hat{p}\pm z^*\sqrt{\frac{\hat{p}(1-\hat{p})}{n}}$
- One sample $t$-interval for [[Population]] mean
	- $\displaystyle\bar{x}\pm t^*\frac{S_x}{\sqrt{n}}$
### Using $t$ Procedures Wisely
- CL and CI are exactly correct when [[Population]] distribution is exactly [[Normal Distribution|Normal]]
	- Not realistic
- An inference procedure is robust if the probability calculations involved remain fairly accurate when a condition for using the procedure is violated.
- $t$ procedures:
	- NOT robust against [[Outlier]]s because $\mu$ and $\sigma$ aren't
	- Robust against non-normality of [[Population]]
		- For small samples *always* plot your data to check for [[Outlier]]s/[[Skew]]ness
### The Normal Condition and $t$ Procedures
- $n\lt15$: can use $t$ only if data appear close to [[Normal Distribution]]
- $n\ge15$: can use $t$ unless there are outliers or strong skewness
- $n\ge30$: can use $t$
	- Randomness is more important than normality