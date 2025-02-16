#  Pearson correlation coefficient
## Definition

$$
    \text{Covariance } cov(X,Y) = \frac{1}{n}\sum_{i=1}^{n}[(x_i-\mu_X)(y_i-\mu_Y)] = \mathbb E[(x_i-\mu_X)(y_i-\mu_Y)]
$$

$$
    \rho_{X,Y} = \frac{cov(X,Y)}{\sigma_X \sigma_Y} = \frac{E[(x_i-\mu_X)(y_i-\mu_Y)]}{\sigma_X \sigma_Y} 
$$

$$
\rho_{X,Y} \in [-1,1]
$$

Pearson correlation coefficient is the ratio between the covariance of two variables and the product of their standard deviations; thus, it is essentially a normalized measurement of the covariance, such that the result always has a value between −1 and 1. 
## Interpretation
When $|\rho_{X,Y}| = 1$, which implies that a linear equation describes the relationship between X and Y perfectly, with all data points lying on a line. More specifically, $\rho_{X,Y} = 1$ means Y increases as X increases, on contrary, $\rho_{X,Y}=-1$ implies that Y decreases as X increases.

$\rho_{X,Y}=0$ implies that there is no linear dependency between the variables X and Y.

More generally, $\rho_{X,Y} >0$ implies that the two variables X and Y are positive correlation, which means Y increases as X increases in general. On the contrary, $\rho_{X,Y}<0$ represents the two variables are negative correlation. Besides, the bigger $|\rho_{X,Y}|$ is, the stronger the correlation between the two variables.
##  Illustration
There are two variables: Students and Books. Following are 15 samples.

|Students| Books|
|---|---|
|36|31|
|28|29|
|35|34|
|39|35|
|30|29|
|30|30|
|31|30|
|38|38|
|36|34|
|38|33|
|29|29|
|26|26|

Due to the 15 group of statisics are samples, we should use sample variance and sample covariance to calculate Pearson correlation coefficient.

$$
    cov(X,Y) = \frac{1}{n-1}\sum_{i=1}^{n}[(x_i-\mu_X)(y_i-\mu_Y)]
$$

$$
    \rho_{X,Y} = \frac{cov(X,Y)}{S_X S_Y}
$$

By calculating,

$$
\begin{aligned}
    cov(X,Y) = 13.4545 \\
    S_X = 4.4721 \\
    S_Y = 3.3439\\
    r = \rho_{X,Y} = \frac{cov(X,Y)}{S_X S_Y} = \frac{13.4545}{4.4721\times 3.3439} = 0.8997
\end{aligned}
$$

# p-value
P-value is, under the assumption that the Null Hypothesis ($H_0$) is true, the probability of obtaining test results at least as extreme as the results actually observed.

There are two parameters to calculate p-value, respectively are t-score and degree of freedom. By finding the parameters in the p-table or using the t-score calculator, we can obtain the p-value.

And essentially, what we want to get is the area of the graph away from the T-value (depending on one-tailed or two-tailed hypothesis?) for a given degree of freedom

Then, compared with the given significance level $\alpha$. If $p > \alpha$ then we can accept $H_0$, otherwise, reject $H_0$.

In this problem, we hope to determine whether these two variables are correlated by calculating the P-value of Pearson correlation coefficient between Students and Books.

## Student t-test (t-test)
A Student's t-test is a statistical hypothesis test used to determine whether there is a significant difference between the means of two sets of data (or between a single set of data and a known population). The core idea is to infer whether the difference is statistically significant by calculating the T-statistic (t-value) and combining with the Student's t-distribution.
## Example
$H_0$:  Students and Books are not correlated

$H_a$: Students and Books are correlated

By using Pearson correlation coefficient r, we have

$$
    t = r\times \sqrt{\frac{n-2}{1-r^2}}
$$

$$
    df = n-2
$$

In this case,

$$
    n = 12
$$

$$
    r = 0.8997
$$

We can assume $$\alpha = 0.01$$ which is a relatively strict significance level.

By calculating,

$$
    t = 6.5178
$$

$$
    df = 10
$$

Bring the value into the calculator and select two-tailed  hypothesis

$$
    p = 0.000067 <0.0001<0.01
$$

$$
    p << a
$$

We can reject $H_0$, and consider Students and Books are correlated.
