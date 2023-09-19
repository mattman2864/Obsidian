The confidence interval gives a range of values that you think will contain the parameter.
The confidence interval can be defined as:
$CI $=$ [[Point Estimate]] $\pm$ margin of error$
where margin of error is is the [[Critical Value]] times the [[Standard Deviation]] of the [[Statistic]].
## Confidence Level
The confidence level is the proportion of intervals out of all possible intervals created by all possible samples that capture the parameter (i.e. $\mu$ or $P$)
## Interpreting CI and CL
Confidence Level:
**AP** "\_\_% of all possible samples of size \_\_ from this population will result in an interval that captures \_\_\_\_."
**AP** "We are \_\_% confident that the interval from \_\_ to \_\_ captures \_\_\_\_."
- Interval of plausible values for the parameter
## Estimating a [[Population]] Proportion
One sample $z$ interval for population proportion
$$\displaystyle CI=\hat{p}\pm z^*\sqrt{\frac{\hat{p}(1-\hat{p})}{n}}$$
1. Check Conditions
2. find $z*$
3. Find the standard error
### Checking Conditions
1. Random
	- SRS?
	- Randomized experiment?
2. Normal
	- [[Central Limit Theorem]] 
		- $n\ge30$
	- Proportions:
		- $n\hat{p}\ge10$ and $n(1-\hat{p})\ge10$
			- use $\hat{p}$ since we don't know p
1. Independence
	- With replacement
	- $\displaystyle n\le\frac{1}{10}N$
### Find $z^*$ (critical value)
Use $^*$ to remind ourselves that this is NOT a standardized score.
#### By Hand
1. Find Probability in tails of [[Normal Distribution]]
2. Use [[Table A]] to find the point $z*$ with specified area
3. Find closest entry $-$ this is your [[Critical Value]]
	- Always use positive answer
#### On Calculator
`InvNorm(<area to left>, 0, 1)`
- Always use positive answer
### Find Standard Error
- When [[Standard Deviation]] of a [[Statistic]] is estimated from data, the result is called **standard error** of the statistic.
- Since we don't know $p$, we replace it with $\hat{p}$
Standard Error $\displaystyle=\sqrt{\frac{\hat{p}(1-\hat{p})}{n}}$
## 4-Step Process for Finding $p$
### State
We want to estimate... the define the parameter used in context... name the confidence level.
### Plan
1. State your method: **One-Sample Z interval for $p$**
2. 3 Conditions:
	1. Normal: is the [[Population]] normally distributed? If not check the following proportions:
		- $n\hat{p}\ge10$ and $n(1-\hat{p})\ge10$
	2. Independent: Are the samples independent? If sampling with out replacement check $\displaystyle n\le\frac{1}{10}N$
	3. Random: Did the problem mention that a random sample was taken?
### Do
1. Give the formula with values plugged in.
2. Using a calculator? Proportions: `Stat -> Tests -> Zinterval` (or `1-propZint` if given counts)
	- You must still record the formula
### Conclude
[[#Interpreting CI and CL|Interpret the interval in context]].