## Conditions and Principles
Conditions are the same as they were for [[Confidence Interval]]s
- Normal, Random, Independent
Principles apply to [[Statistical Test|Significance Test]] for $p$
- Test compares sample statistics to [[Population]] parameters from $H_o$
- Statistic values far from the $H_o$ parameter in the direction of $H_a$ give evidence against $H_a$
- To assess how far [[Statistic]] is from [[Parameter]] we standardize
## One Sample $z$-test for $p$

$\displaystyle z=\frac{\hat{p}-p_0}{\displaystyle\sqrt{\frac{p_0(1-p_0)}{n}}}$ 
Then we can use [[Table A]] or `normalcdf` to find the area under the [[Normal Distribution|normal curve]] - this is $p$-value