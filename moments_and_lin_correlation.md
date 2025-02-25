# Mean, variance, skewness and curtosis of probability distributions and samples

Mean value of any function $g(X)$ of a discrete random variable X is defined by
$\overline{g(X)} = \sum \limits_{i=0}^{max} g(x_i) P(x_i)$ where $max$ is the maximum index of the samples $x_i$, and $P(x)$ is the probability mass function of X.

Mean value of any function $g(X)$ of a continuous random variable X is defined by
$\overline{g(X)} = \int \limits_{x_{min}}^{x_{max}} g(x) f(x)$ where ${x_{min}}$ and $x_{max}$ are the minimum and maximum values of $X$. 

Variance of $X$ is defined as $\overline{(X-\bar X)^2}$, which is also called the second order central moment. First order central moment for any distribution wold be 0.  Variance is the measure of dispersion of values around the mean value. Standard deviation is the square-root of variance.

Skewness is the third-order central moment of a random variable, which is a measure of assymmetry of the PMF in either side of the mean value. If skewness is 0, the ditribution is symmetric, if skewness > 0, the distribution is positively skewed or skewed on the right side, if skewess is negative, it indicates the distribution is skewed on the left side. <br />

Curtosis is the measure of steepness of the peak value or "tailedness" of PMF. It is actually the fourth order central moment of a random variable. <br />

## Mean, variance, skewness and curtosis of Discrete random variables

If $X$ is a discrete random variable with maximum sample index = $max$, then </br >
mean of $X$= $\bar{X} = \sum \limits_{i=0}^{max} x_i P(x_i)$, <br />
mean of ${X^2}$ = $\overline{X^2} = \sum \limits_{i=0}^{max} {x_i}^2 P(x_i)$.

$var(X) = \sum \limits_{i=0}^{max} (x_i-\bar X)^2 P(x_i) = \sum \limits_{i=0}^{max} ({x_i}^2 - 2 x_i \bar{X} + {\bar X}^2) P(x_i)$ <br />
$=\sum \limits_{i=0}^{max} {x_i}^2 P(x_i) - 2 \bar{X} \sum \limits_{i=0}^{max} {x_i} P(x_i) + {\bar x}^2 \sum \limits_{i=0}^{max} P(x_i) = \overline{X^2} - 2 \bar{X} \bar{X} + {\bar{X}}^2 = \overline{X^2} - {\bar{X}}^2$ 


skewness = $\frac{\overline{{X-\bar{X}}^3}}{{\sigma}^3} = \frac{\sum \limits_{i=0}^{max} (x_i - \bar{X})^3 P(x_i)}{{\sigma}^3}$ where $\sigma = \sqrt{var(X)}$   

curtosis = $\frac{\overline{{X-\bar{X}}^4}}{{\sigma}^4} = \frac{\sum \limits_{i=0}^{max} (x_i - \bar{X})^4 P(x_i)}{{\sigma}^4}$


## Mean, variance, skewness and curtosis of continuous random variables

For a random variable $X$ with a continuous PDF function $f_X(x)$, <br />

mean = $\bar{X} = \int \limits_{x=x_{min}}^{x=x_{max}} x f_X(x) dx$, <br />
variance = $\overline{(X-\bar{X})^2} = \int \limits_{x=x_{min}}^{x=x_{max}} (x-\bar{X})^2 f_X(x) dx = \int \limits_{x=x_{min}}^{x=x_{max}} x^2 f_X(x) dx - {\bar{X}}^2$ in the same way as in case of discrete random variable, and $\sigma = \sqrt{\overline{X^2}}$, <br />
skewness = $\frac{\overline{(X-\bar{X})^3}}{{\sigma}^3} =  \frac{\int \limits_{x=x_{min}}^{x=x_{max}} (x-\bar{X})^3 f_X(x) dx}{{\sigma}^3}$, <br />
curtosis = $\frac{\overline{(X-\bar{X})^4}}{{\sigma}^4} = \frac{\int \limits_{x=x_{min}}^{x=x_{max}} (x-\bar{X})^4 f_X(x) dx}{{\sigma}^4}$


# Linear correlation between columns of dataset

Refer to [linear correlation basics](./pearson_basics.pdf) for the best fit straight line, calculation of gradient, variance and covariance etc. According to the basics, the three quantities are of interest :
- $SS_{xx} = N var(x)$,
- $SS_{yy} = N var(y)$,
- $SS_{xy} = N Cov(x,y)$.

It is also observed that, if the equation of the best fit line is assumed to be $y=mx+c$, then $m = \frac{SS_{xy}}{SS_{xx}}$. And if the equation of the line is taken as $x=by+c^{\prime}$, $b = \frac{SS_{xy}}{SS_{yy}}$.

Pearson's linear correlation coefficient $r$ is given by <br />
$r^2 = m.b = \frac{{SS_{xy}}^2}{SS_{xx}.SS_{yy}}$

## Example of computation of $r$

Let us take the scores of 10 students (in %-age) in a subject paper in 1st semester, and the final aggregate in the final semester. It needs to be verified what is the linear correlation coefficient of these two columns. 

| x | y |
| --- | --- |
| 65.5 | 56.5 |
| 73.3 | 67.9 |
| 82.4 | 68.5 |
| 91.7 | 80.8 |
| 96.4 | 85.7 |
| 75.7 | 72.3 |
| 83.4 | 84.5 |
| 87.6 | 90.1 |
| 81.7 | 86.0 |
| 59.0 | 68.3 |

Here, $N = 10$. The quantities need to be computed as : <br />
- $\bar x$ : Average of x = $\frac{\sum \limits_{i=1}^{10} {x_i}}{N} = \frac{65.5+73.3+\cdots+59.0}{10}$
- $\bar y$ : Average of y = $\frac{\sum \limits_{i=1}^{10} {y_i}}{N} = \frac{56.6+67.9+\cdots+68.3}{10}$
- $\overline {x^2}$ : Average of $x^2$ = $\frac{\sum \limits_{i=1}^{10} {x_i}^2}{N} = \frac{{65.5}^2+{73.3}^2+\cdots+{59.0}^2}{10}$
- $\bar {y^2}$ : Average of $y^2$ = $\frac{\sum \limits_{i=1}^{10} {y_i}^2}{N} = \frac{{56.5}^2+{67.9}^2+\cdots+{68.3}^2}{10}$
- $\bar {xy}$ : Average value of $xy$ = $\frac{\sum \limits_{i=1}^{10} {x_i}{y_i}}{N} = \frac{65.5\times56.5+73.3\times67.9+\cdots+59.0\times68.3}{10}$

Now, $SS_{xy} = N \bar{xy} - N \bar{x} \bar{y}$, <br />
$SS_{xx} = N \bar{x^2} - N {\bar{x}}^2$, <br />
$SS_{yy} = N \bar{y^2} - N {\bar{y}}^2$ <br />

Hence $r = \sqrt{\frac{SS_{xy}}{SS_{xx} SS_{yy}}} = \sqrt{\frac{\bar{xy}-\bar{x} \bar{y}}{(\bar{x^2}-{\bar{x}}^2)(\bar{y^2}-{\bar{y}}^2)}}$

$r$ is called the Pearson's linear correlation coefficient.
