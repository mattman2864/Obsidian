#
Errors can occur during [[Statistical Test]]s of significance. There are two types of statistical errors: **Type I** and **Type II**.
- Type I Error: reject $H_o$ when $H_o$ is true
- Type II Error: fail to reject $H_o$ when $H_o$ is false

|                      | $H_o$ true       | $H_o$ false ($H_a$ true) |
| -------------------- | ---------------- | ------------------------ |
| Reject $H_o$         | **Type I Error** | **Correct**              |
| Fail to reject $H_o$ | Correct      | Type II Error        |
## Probabilities of Type I and II Errors
$P($Type I Error$)=\alpha$
$P($Type II Error$)=\beta$
$P($rejecting correctly$)=1-\beta=$ **Power**
**Power**: probability that the test will reject $H_o$ at a chosen $\alpha$ when  $H_a$ is true
- Power = $1-\beta$
- Power close to $0$: test has almost no chance of detecting $H_o$ is false
- Power close to $1$: test is very likely to reject $H_o$ in favor of $H_a$ when $H_o$ is false
## Error Analogies
$H_o$: the person is innocent
$H_a$: the person is not innocent
- Type I error
	- You say that the person is guilty when actually they are innocent
- Type II error
	- You can't conclude that the person is guilty when they are guilty
- Which is worse?
	- Type I because you're convicting someone of a crime they didn't commit and the guilty person is still out there.
- So, choose low significance level $\alpha$