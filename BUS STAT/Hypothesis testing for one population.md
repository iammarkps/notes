# Hypothesis testing

We want to test whether the claim about statistics sample is accurate. We setup hypotheses with $H_0$ (null hypothesis, with equality sign) and $H_1$ (alternative hypothesis). A notion for understanding hypothesis testing lies within the criminal justice system.

 >Jurors examine the evidence to see whether it convincingly shows a defendant is guilty. Even if the jurors leave unconvinced of guilt beyond a reasonable doubt, this does not mean they believe the defendant is innocent

It means that if we have sufficient evidence, we will *reject* $H_0$ in favor of $H_1$. In contrast, if we don't have enough evidence we *fail to reject* $H_0$. Note that it does not mean that we accept $H_0$. A useful intuition about rejecting null hypothesis is we would expect a sample mean or proportion falls in rejection area just $\alpha$ of the time.

# Methods

1. Compare test statistic with critical value (Traditional method)
2. Compare p-value with $\alpha$ (p-value method)

# Standard Framework
1. Forming hypothesis
2. Select a significant level ($\alpha$)
3. Compute test statistics

## Forming hypothesis

We formulate $H_1$ with
| Sign ($H_1$) |       Type        |
|:------------ |:-----------------:|
| $\neq$       |  two-tailed test  |
| $>$          | right-tailed test |
| $<$          | left-tailed test  |

## Select $\alpha$
Type I Error = Reject $H_0$ when $H_0$ is actually true $$P(Reject \; H_0 \; | \; H_0 \; is \; true) = \alpha$$Normally, in social science $\alpha = 0.05$. Area under rejection area is $\alpha$ 

## Compute test statistics
### Known $\sigma$ or unknown $\sigma$ with $n > 30$
If unknown $\sigma$ replace $\sigma$ with $s$
$$z = \frac{\bar{x} - \mu_0}{\frac{\sigma}{\sqrt{n}}}$$
### Unknown $\sigma$ with $n \leq 30$
Use Student's t-distribution, with degree of freedom $n-1$
$$t = \frac{\bar{x} - \mu_0}{\frac{s}{\sqrt{n}}}$$
## Traditional Method
Determine a type of tail, and setup rejection area. Then look up z or t table accordingly.

*In R use `qnorm(a)` for left-tailed, `qnorm(1-a)` for right-tailed, and `qnorm(a/2)` for two-tailed test. 

If test statistic falls in rejection area, reject $H_0$

![[MIT's_NHST_Rejection.png]]

## p-value method
Compute p-value and compare it with $\alpha$. Reject $H_0$ if $p-value \leq \alpha$ and failed to reject $H_0$ if $p-value > \alpha$.

### p-value computation
p-value is a probability of getting a value equal to or more extreme as the one you observed, assuming $H_0$ is true. Compute by R's `pnorm(z)` for left-tailed, `1-pnorm(z)` for right-tailed, and `2pnorm(z)` for two-tailed test.