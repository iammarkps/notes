We define $X$ to be continuous random variables if there exists a non-negative function $f$, defined for all real $x \in (-\infty,\infty)$ , having the property that, for any set $B$ of real numbers,
$$ P\{X \in B\} = \int_{B} f(x) \,dx$$
We can obtain probability statements about $X$ in term of $f$.
$$ P\{a \leq X \leq b \} = \int_{a}^{b} f(x) \, dx$$
## Normal Distribution
We say that $X$ is normally distributed with parameters $\mu$ and $\sigma^2$ if the PDF of X is define by $$f(x) = \frac{1}{\sqrt{2\pi}\sigma} e^{-\frac{1}{2} (\frac{x - \mu}{\sigma})^2}$$for $-\infty < x < \infty$
We standardize $X$ as **z-score** $$z = \frac{x - \mu}{\sigma}$$which has mean of 0 and standard deviation of 1.  We can calculate cumulative area under normal curve by looking up **z-table**. A cumulative areas under curve is a proportion of observation.

### Empirical rule
| Interval          | Percentage |
| ----------------- |:----------:|
| $\mu \pm \sigma$  |   68.26%   |
| $\mu \pm 2\sigma$ |   95.44%   |
| $\mu \pm 3\sigma$ |   99.73%   |
z-scores more than 3 or less than -3 indicate a possible outlier

## Sampling
### Central Limit Theorem (Mean)
For sufficiently large sample size (normally, more than 30), $\bar{X}$'s distribution will be approximately normal with mean $\mu$ and standard deviation (or standard error) $\frac{\sigma}{\sqrt{n}}$ , so z-scores of $\bar{X}$ distribution is $$z = \frac{x - \mu}{\frac{\sigma}{\sqrt{n}}}$$
### Central Limit Theorem, sampling Distribution of the Sample Proportion (Proportion)
Random samples of size $n$ selected from a binomial population with parameter $p$ . The sampling distribution of the sample proportion ($\hat{p} = \frac{x}{n}$) will have mean $p$ and standard deviation $\sqrt{\frac{pq}{n}}$ , where $q = 1 - p$. If $n$ is large  ($np>5$ and $nq>5$) and $p$ is not too close to 0 or 1, the said sampling distribution will be *approximately normal*. Note that the standard deviation of $\hat{p}$ are sometime called the **standard error (SE)**. Thus, z-scores of normally distributed $\hat{p}$ is $$z = \frac{\hat{p} - p}{\sqrt{\frac{pq}{n}}}$$
