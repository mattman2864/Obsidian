#Statistics #Math 
- Sampling Distribution of $\hat{p}_1-\hat{p}_2$
	- Shape
		- If $n_1(p_1)$, $n_1(1-p_1)$ and for $n_2$ and $p_2$ are all at least 10, then the sampling distribution of $p_1-p_2$ is approximately [[Normal Distribution|normal]].
	- Center
		- $\mu_{\hat{p}_1-\hat{p}_2}=p_1-p_2$
	- Spread
		- Check 10% conditon
- Significance tests of $H_0$ :$p_1-p_2$
	- Pooled (combined sample proportion)
		- Assuming $H_0$ is true means we assume $p_1=p_2$
		- Combine sample to get a more precise estimate of $p$
		- $\hat{p}_c=\frac{\text{total successes}}{\text{total samples}}$
	- two sample $z$ test for $p_1-p_2$
$$z=\frac{(\hat{p}_1-\hat{p}_2)}{\displaystyle\sqrt{\frac{\hat{p}_c(1-\hat{p}_c)}{n_1}+\frac{\hat{p}_c(1-\hat{p}_c)}{n_2}}}$$
- Two sample $z$ interval test for $p_1-p_2$
	- Recall: $\text{test statistic}\pm\text{(critical value)(std of statistic)}$
	- $\hat{p}_1-\hat{p}_2\pm z^*\sqrt{\frac{p_1(1-p_1)}{n_1}+\frac{p_2(1-p_2)}{n_2}}$
	- We can't use $\hat{p}_c$ because we didn't hypothesize that $p_1=p_2$