We want to compare two population mean. First we need to identify what type of data we are working with: dependent (paired) or independent data.

# Independent (Two-population are normally distributed)

## Large samples or small sample with known variances  (z-test)

Samples are large if $n_1 \geq 30$ and $n_2 \geq 30$ 

Test statistics is $$z = \frac{(\bar{x_1} - \bar{x_2}) - k}{SE}$$
where standard error is $\sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}}$, if $\sigma$ is unknown and sample is large, then use $s$ in place of $\sigma$

## Small sample with variance assumed to be equal

In this case we use *pooled variance* $s^2 = \frac{(n_1 - 1)s_1^2 - (n_2 - 2)s_2^2}{n_1 + n_2- 2}$ and test statistics is $$t = \frac{(\bar{x_1} - \bar{x_2}) - k}{SE} \sim t_{d_1 + d_2 -2} $$
where standard error is $\sqrt{s^2(\frac{1}{n_1} + \frac{1}{n_2})}$ 

## Small sample with variance assumed to be unequal

$$t = \frac{(\bar{x_1} - \bar{x_2}) - k}{SE} \sim t_{df}$$
in this case we need to define $df$ with $$df = \frac{(s^{2}_{1}/N_{1} + s^{2}_{2}/N_{2})^{2}} {(s^{2}_{1}/N_{1})^{2}/(N_{1}-1) + (s^{2}_{2}/N_{2})^{2}/(N_{2}-1) }$$
where standard error is $\sqrt{\frac{s_1^2}{n_1} + \frac{s_2^2}{n_2}}$

# Variance Test (F-tests)

We test variance equality in order to determined which test to use for t-test 
Hypothesis for this test is $H_0 : \sigma_1^2 = \sigma_2^2$  and $H_1 : \sigma_1^2 = \sigma_2^2$
$$F = \frac{s_1^2}{s_2^2}$$
where $s_1^2 > s_2^2$ 
Reject $H_0$ if $F > F_{\alpha/2;\, df_1;\, df_2}$
