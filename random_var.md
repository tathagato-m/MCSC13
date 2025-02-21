# Concept of Random Variable

If any experiment or process has multiple mututally exclusive outcomes, mathematical or statistical modelling requires each outcome to be mapped onto a numerical value. Sometimes the numerical values are inherent into the outcomes, sometimes not. For example, if the experiment is to check if a train arrives at a station on time or not, the mutually exclusive outcomes are 
- the train arrives on time
- it arrives earlier than schedule
- it arrives late.  

If these outcomes are mapped between 0 - 2 as follows :
- 0 - on time
- 1 - earlier than schedule
- 2 - late.

Let X denote the above mapping. Hence possible values of X are 0, 1 or 2. Hence X can be viewed as a variable, whose values in successive occurrances of the experiment can vary with a certain degree of uncertainty. For this reason, X is called a random variable to denote the outcomes of the above experiment.

## Definition of random variable : 

Random variable is a mapping of mutually exclusive outcomes of an exeriment or process to a number, either discrete or continuous.  

## Significance of random variable : 

In the above experiment, let probability 
of the train arriving ahead of time, on time and late is 0.1, 0.6 and 0.3 respectively. This can be written as <br /> 
$Prob(X=0) = 0.1,~Prob(X=1) = 0.6,~Prob(X=2) = 0.3. $ Or <br />
$Prob(X=x) = P(x)~where $

$$
P(x)=
\begin{cases}
  0.1,& \text{if } x = 0,\\
  0.6,& \text{if } x=1, \\
  0.4,& \text{if } x=2.
\end{cases}
$$

Here, probability of different outcomes can be written in the form of function of numbers. More examples are given below to explain this point in more detail.

## Examples

### Example 1

Let there be a box of components. If any component is chosen at randome from the box, Probability of that component being faulty = p. 10 components are chosen from the box. Probability of number of components being faulty among the chosen 10 componets are calculated as follows: 

The mutually exclusive outcomes are : no fault, 1 among 10 is faulty, 2 among 10 are faulty, ... 10 among 10 are faulty. <br />
Let $X$ be he random variable denoting number of faulty components within the set of 10. So possible values of $X = 0,1,\cdots 10$. So the mapping from outcomes to numbers is trivial.

Let probability($x$ components within 10 are faulty) be denoted as $P_X(x)$. This probability is the same as the probability($X=x$).

$P_X(x) = ^{10}C_x p^x (1-p)^{10-x}$ where $x=0,1,2,\cdots 10$.

### Example 2

Let the experiment be to count the number of bit errors in a received frame of 40 bytes or $320$ bits. Let the probability of any bit being received in error = $p$. 
Let a random variable $X$ denote the number of bit errors in a frame. Hence $X$ can take values between $0,1,2,\cdots 320$. Let $P_X(n)$ denote the probability that $n$ bits are in error in the frame. Hence

$P_X(n)=^{320}C_n p^n (1-p)^{320-n}$ 

## Discrete random variable and Probability Mass Function

In the above two examples, X is a random variable which takes only discrete values. Such random variables are called discrete random variable. And the 
Probability of $(X=n)$ where $n$ is within the set of possible values of X is called Probability Mass Function or PMF. <br />
Hence $P_X(x)$ in example 1, which indicates $Probability(X=x)$ and $P_X(n)$ in example 2 which indicates $Probability(X=n)$ are PMFs of Random variable $X$.   

### Cumulative distribution function (CDF)

Cumulative distribution function or CDF of a random variable X (denoted by $F_X(x)$) is defined to be the Probability of $X$ being less than or equal to $x$.

From example 1 given above,    
$F_X(x)$ = Probability($X \leq x$) = Probability($X=0$) + probability($X=1$) $\cdots$ + Probability($X=x$) = $P_X(0) + P_X(1) + \cdots P_X(x) = \sum\limits_{i=0}^{x} P_X(i)$

So, for any discrete random variable $X$, the CDF $F_X(x) = \sum\limits_{i=min}^{max} P_X(i)$ where $min$ and $max$ are the minimum and maximum limit of the range of X.

## Continuous random variable


If a random variable maps outcomes of a process or an experiment to non-discrete real numbers, then the random variable is called continuous random variable.

Example : Measuring minimum temperature of a day during a season. If X be the random variable denoting the observed minimum temperature of a day, then value of X is continuous.   

### Probability Density function

In the above example, the probability of observed minimum temperature being within a very small interval $t$ and $t+\delta t$ would be of interest. That probability would be a function of $t$. Let that function be called as $f(t)$. So<br />
$f(t)$ = probability of observed minimum temperature being within $t$ and $t+\delta t$ is called the probability density function of $X$. Normally this function is denoted as $f_X(t)$. <br />
In this example let the PDF be <br />
$$
f_X(t)=
\begin{cases}
  0,& \text{if } t \lt 7 \\
  V_{max} + \frac{V_{max}(t-7)}{4},& \text{if } 7 \le t \lt 11 \\
  \frac{V_{max}(t-11)}{9},& \text{if } 11 \le t \lt 20 \\
\end{cases}
$$  

This function indicates that, probability of minimum temperature being in the neighbouthood of 7 degrees, goes up linearly to $V_{max}$ in the neighbourhood of 11 degrees and comes down linearly to 0 in the neighbourhood of 20 degrees.

### Probability/Cumulative Distribution Function

If X is a continuous random variable, probability of $(X \leq x)$ can be computed similar to the case of discrete random variables, and that would be a function of $x$. Let that function be called as $F_X(x)$, which is given as follows:

$$F_X(x) = \int\limits_{t=t_{min}}^{x} f_X(t) dt $$

In the earlier example, $t_{min} = 7$, $t_{max} = 20$.

#### Property of CDF

The CDF has the following properties :
- Value is between 0 and 1, (as it is a probability value)
- It is a monotonically increasing function
- $$F_X(t_{max}) = \int\limits_{t=t_{min}}^{t_{max}} f_X(t) dt = 1$$ as total probability of the random variable within the entire range of $X$ is 1.

## Some examples using PMF, PDF and CDF

### Uniform PMF

#### Example 1

A discrete uniform random variable may have integer values between 0 - 15 with probability $p$. <br/>
- find the value of $p$.
- find the CDF function.

Solution :

Let $X$ be the discrete uniform random variable which can take values between $0,1,\cdots,15$. So,<br />
$ Probability(X=x)=p~for~0 \leq x \lt 16.$
    
If $F_X(x)$ is the CDF for the given PMF, then
$F_X(15) = \sum \limits_{x=0}^{x=15} p = 16p = 1$, hence $p=\frac{1}{16}$.

$F_X(x) = \sum \limits_{i=0}^{i=x} p = (x+1)p = \frac{x+1}{16}.$

<p align="center">
<img src=/home/tathagato/classes/2024_25/MCSC13/probability/discrete_uniform_cdf.png alt="CDF of discrete uniform RV">
</p>


#### Example 2: 

A person needs to travel from his home to the railway station and it takes him 15 minutes. He has to catch a train scheduled to depart at 9 am, and the train 
starts between 9.00 AM to 9.10 AM as given below.

<p align="center">
<img src=./train_from_station.png alt="Train starting from station">
</p>

The person starts from his home between 8.45 AM to 8.55 AM as given below. 

<p align="center">
<img src=./man_starting_from_home.png alt="Man starting from Home">
</p>

Find the probability that the person misses the train.

##### Solution :

Person misses the train when he arrives at the station after the train has left.<br />
Let X be the random variable denoting the delay of arrival time of the person wrt 9.00 AM, and T be the random variable denoting the delay in the train leaving the station after 9.00 AM. So, both $X$ and $T$ are uniform discrete random variable with PMF as follows: <br />

$P_X(x) = \frac{1}{10}~ for~ 0 \le x \lt 9$ <br />
$P_T(t) = \frac{1}{11}~ for~ 0 \le t \lt 10$ <br /> 
Probability of miss = probability of ($T$ < $X$) = <br />
$ \sum \limits_{t=1}^{t=9} \sum \limits_{x=0}^{t-1} P_X(x) P_T(t) = P_X(1).P_T(0) + P_X(2)(P_T(0)+P_T(1)) + P_X(3)(P_T(0)+P_T(1)+P_T(2)) \cdots + \\ 
  P_X(9)(P_T(0)+P_T(1) \cdots + P_T(8)).$ <br />
$ = \frac{1}{10}(\frac{1}{11} + 2.\frac{1}{11} + \cdots + 8.\frac{1}{11})$ <br />
 = $\frac{1}{10}\frac{1}{11}(1+2+\cdots+8)$ <br />
= $36.\frac{1}{110} = \frac{36}{110}$ 

### Binomial PMF

If a random variable $X$ denotes number of successes within $N$ trials of a Bernoulli trial, PMF of $X$ ($P_X(x)$) is as follows :

$ P_X(x) =$ Probability of x successes in N Bernoulli trials $= ^NC_x p^x(1-p)^{N-x}$.

Let $F_X(x)$ denote the Cumulative distribution or CDF of $X$. <br />
$F_X(x)= $ Probability of ($X \le x$) =  $\sum\limits_{i=0}^x P_X(x) = $ $\sum\limits_{i=0}^{x} {^NC_i} p^i (1-p)^{N-i} $ 

#### Example

A component manufacturing factory has a quality control process where probability of a faulty component going into market = 0.0001. Components are packaged and sent to market in 100 component boxes. If 2 or more components are found faulty in a box, the box needs to be returned. What is the probability of a box getting returned ?

##### Solution 

As per given problem statement, $p$ = 0.0001. If 2 or more components are found faulty, the box is returned.

Probability(2 or moe components faulty in a box) = 1 - probability(0 or 1 component are faulty in the box). <br />
Let $X$ be the random variable denoting number of faulty components in a box. So <br />
Probability($X = 0$)$ = ^{100}C_0 (0.0001)^0 (1-0.0001)^{100} $
Probability($X=1$) $ = ^{100}C_1 (0.0001)^1 (1-0.0001)^{99} $

Hence probability($X<=1$) $=^{100}C_0 (0.0001)^0 (1-0.0001)^{100} + {^{100}}C_1 (0.0001)^1 (1-0.0001)^{99} =$ <br /> 
$0.9999+100X0.0001.(0.9999)^{99} = 0.9999+0.01X0.9999^{99}. $


### Poisson PMF

Poisson PMF is a special case of binomial PMF, where the number of Bernoulli Trials ($N$) is very high, and probability of success of each Bernoulli Trial ($p$) is very low, such that $Np$ is finite. In such case, probability of $n$ successes in $N$ trials is $P_X(n) = \frac{{\lambda}^n exp(-\lambda)}{n!}$, where $\lambda = N.p = $Average number of successes in $N$ trials.

Basically, the binomial PMF is approximted to Poisson PMF for large $N$ and small $p$. The derivation of approximation is given in the next section.

#### Poisson Approximation for Binomial PMF

Binomial PMF $P_X(n) = ^NC_n p^n (1-p)^{N-n}$. ----- (1) <br /> 
Let $\lambda = N.p$, or $p = \frac{\lambda}{n}$.  ------ (2)  <br />
From (1) and (2), the binomial PMF can be written as <br />
$P_X(n) = ^N C_n (\frac{\lambda}{n})^n (1-\frac{\lambda}{n})^{N-n} =$  <br />
$\frac{N!}{n! (N-n)!} (\frac{\lambda}{n})^n (1-\frac{\lambda}{n})^{N-n} $  ------- (3).<br /> 

If N is very large, then (3) can be written as <br />
$\lim \limits_{N\to\infty} (\frac{{\lambda}^n}{n!}) (\frac{N!}{(N-n)!} \frac{1}{N^n}) (1-\frac{\lambda}{N})^{N-n} $ ------ (4)

In this term, $(\frac{{\lambda}^n}{n!})$ is indepenent of N; so this is invarient under the limit condition. So, the term can be simplified further as <br />
$ (\frac{{\lambda}^n}{n!}) \lim \limits_{N\to\infty} T_1\times T_2\times T_3$ where $T_1 = (\frac{N!}{(N-n)!} \frac{1}{N^n}), T_2= (1-\frac{\lambda}{N})^N, T_3 =  (1-\frac{\lambda}{N})^{-n}$.  ------------- (5)

Now, from (5), $\lim \limits_{N\to\infty} T_1 = \lim \limits_{N\to\infty} (\frac{N!}{(N-n)!} \frac{1}{N^n}) = \lim \limits_{N\to\infty} \frac{N}{N} \frac{N-1}{N} \cdots \frac{N-n+1}{N} = 1.1.1\cdots 1 = 1$. ------- (6)

From (5) $\lim \limits_{N\to\infty} T_2 = \lim \limits_{N\to\infty} (1-\frac{\lambda}{N})^N$ can be evaluated to be $exp(-\lambda)$ as follows :<br />
Let $x=\frac{N}{-\lambda}$, so $N=-\lambda x$. So $T2 = \lim \limits_{x\to\infty} (1+\frac{1}{x})^{-\lambda x} = exp(-\lambda)$ as $ \lim \limits_{x\to\infty} (1+\frac{1}{x})^{x} = e $ is a known result. ---------- (7)

From (5), $\lim \limits_{N\to\infty} T_3 = \lim \limits_{N\to\infty}(1-\frac{\lambda}{N})^{-n} = 1$, because $\frac{\lambda}{N}\to 0$ as $N\to \infty$. ---- (8)

Hence, from (5), (6), (7) and (8), $P_X(n) = ^NC_n p^n (1-p)^{N-n} = \frac{{\lambda}^n}{n!} exp(-\lambda)$.

Physically speaking, if the number of Bernoulli trials $N$ are very large, probability of success of individual trials $p$ are very small so that average number of successes $N.p$ is finite, and $X$ is the random variable denoting number of successes in $N$ trials, then PMF of $X$ is Poisson PMF. 

A very typical application of Poisson PMF is to model the PMF of arrival of entities or requests in a queue within an interval of time, where average number of arrivals per unit time is finite and each arrival is independent of the other. 

### Example

Let $\lambda$ be the average number of people arriving at a queue of a particular counter in unit time. Find the probability that more than 4 people arrive at the counter within time interval $T$.

#### Solution :

If rate of arrival per unit time = $\lambda$, then average number of arrival within $T$ = $\lambda T$.

Probability of more than 4 people arriving = 1 - (probability of 3 or less number of people arriving).

Probability of ($n$ arrivals within $T) = \frac{(\lambda T)^n}{n!} exp(-\lambda T)$. 

So, probability of more than 4 people arriving = $1 - exp(-\lambda T) [1 + \lambda T + \frac{(\lambda T)^2}{2!} + \frac{(\lambda T)^3}{3!}]$  

### Exponential density, Gamma Density and basics of queuing theory
 
Refer to [queuing basics pdf](gamma_dist_from_queuing.pdf)

### Normal or Gaussian PDF

If $N$ is very large and $p$ is close to $\frac{1}{2}$, the binomial densot can be approximated to be a Normal or Gaussian distribution as follows :

$ P(x) = \frac{1}{\sqrt{2 \pi N p q}}exp(-\frac{(x-Np)^2}{2 N p q}) $ where $q$ = $(1-p)$. Refer to [Normal Approx Binomial PDF](NormalApprox_binomial.pdf) to see the actual derivation.

The generic expression of normal or Gaussian PDF is 
$f_X(x) = \frac{1}{\sigma \sqrt{2 \pi}} exp(-\frac{(x-\mu)^2}{2 {\sigma}^2})$ where $\mu$ and ${\sigma}^2$ are the mean and variance respectively.

The distribution function of random variable $X$ having normal density cannot be analytically calculated as $f_X(x)$ is not analytically integrable. Hence the distribution function does not have a closed-form answer.

### Important results, theorems and distributions related to Gaussian 

#### Law of large numbers

If a finite number of samples of a random variable is taken and the mean value is observed to be $\bar X$, then $\bar X$ approaches the actual mean value of the random variable $\mu$ as the number of samples approaches $\infty$. <br />
There are two versions :<br />
- Weak law of large numbers : Given an arbitrarily small value $\epsilon$, Probability $(|\bar X - \mu| \ge \epsilon) \to 0$ as $N \to 0$.
- Strong law of large numbers : Probability$(\lim \limits_{n\to\infty} \bar X = \mu) = 1$. 

#### Central Limit Theorem

Sum of $N$ independent and identically distributed random variables, each with finite mean $\mu$ and variance ${{\sigma}^2}$ approximately follows a normal distribution for very large $N$. Mean and variance of the resultant normal distributed random variable are $N \mu$ and $N {\sigma}^2$. This theorem is of immense importance in probability theory - which helps to approximate outputs of a large number of statistical phenomena to be having Gaussian density. A common example is to model the noise in communication channel to be of Gaussian density.  

#### Addition of iid Gaussian Random variables

If $X = \sum\limits_{i=1}^{N} X_i$ where $X_i$'s are independent and identically distributed (iid) Gaussian random variables with mean = $\mu$ and variance = ${\sigma}^2$, then <br />
$X$ is also a gaussian distributed random variable with mean = $N\mu$ and variance = $N {\sigma}^2$. 

#### Sum of Squares of two independent Gaussian random variable and Rayleigh density

If $X$ and $Y$ are independent and identically distributed Gaussian random variables with mean = 0 and variance = ${\sigma}^2$, then $Z = \sqrt{(X^2+Y^2)}$ is Rayleigh distributed.

##### Proof

$f_X(x) = \frac{1}{\sigma \sqrt{2 \pi}} exp(-\frac{x^2}{2 {\sigma}^2})$ and $f_X(x) = \frac{1}{\sigma \sqrt{2 \pi}} exp(-\frac{x^2}{2 {\sigma}^2})$ and $f_Y(y) = \frac{1}{\sigma \sqrt{2 \pi}} exp(-\frac{y^2}{2 {\sigma}^2})$. 

Now, the joint probability density of of $x,y$ = $f(x,y)$. So, <br />
probability($X \leq  x, Y \leq y) = probability(X \leq x)\times probability(Y \leq y) = f_X(x) \times f_Y(y)$ = <br /> 
$\frac{1}{\sigma \sqrt{2 \pi}} exp(-\frac{x^2}{2 {\sigma}^2}) \times \frac{1}{\sigma \sqrt{2 \pi}} exp(-\frac{y^2}{2 {\sigma}^2})$= $\frac{1}{2 \pi {\sigma}^2} exp(-\frac{(x^2+y^2)}{2 {\sigma}^2})$     

If $X$ and $Y$ are considered on a cartesian coordinate plane and a change to polar coordinate is effected, then <br />
let $R^2 = X^2 + Y^2$, and $\Theta = {tan}^{-1}(\frac{Y}{X})$  

So, the region between ($x$ and $x+dx$, $y$ and $y+dy$) = region between ($r$ and $r+dr$, $\theta$ and $r d\theta$). Hence <br /> 
$\frac{1}{2 \pi {\sigma}^2} exp(-\frac{(x^2+y^2)}{2 {\sigma}^2})dxdy = \frac{1}{2 \pi {\sigma}^2} exp (-\frac{r^2}{2 {\sigma}^2})r dr d \theta = \frac{r}{2 \pi {\sigma}^2} exp (-\frac{r^2}{2 {\sigma}^2}) drd \theta$ <br />
$ = \frac{r}{{\sigma}^2} exp(-\frac{r^2}{2 {\sigma}^2})dr \times \frac{1}{2 \pi}d \theta$.

Hence, $f_R(r)$ denoting the PDF of $R = \frac{r}{{\sigma}^2} exp(-\frac{r^2}{2 {\sigma}^2})$, $F_{\Theta}(\theta) = \frac{1}{2 \pi}$.

The density function of $R$ is called Rayleigh density; and $\Theta$ is exponentially distributed.

#### Chi-Square distribution and density

The chi-square distribution is a probability distribution that arises when summing the squares of independent standard normal variables. <br />
If $X_1, X_2, \cdots X_k$ are independent standard normal random variable (mean 0 and variance = 1), the sum of their squares follow a Chi-Square distribution. <br />
Let $Y = {X_1}^2 + {X_2}^2 + \cdots {X_k}^2$ where $k$ is called the degree of freedom. Each of $X_k$ contributes to one degree of freedom.  

##### Chi-Square density function

The PDF of Y is $f_Y(y;k) = \frac{x^{(\frac{k}{2}-1)}e^{-\frac{y}{2}}}{2^{\frac{k}{2}} \Gamma(\frac{k}{2})}$ where <br />
$\Gamma(\frac{k}{2}) = (\frac{k}{2}-1)!$  if $k \ge 2$ and even number, <br />
$\Gamma(\frac{1}{2}) = \sqrt{(\pi)}$, <br />
and $\Gamma(\frac{k}{2}) = \frac{k}{2}\Gamma(\frac{k}{2}-1)$. <br />

Using the last recurrence relation, $\Gamma(\frac{1}{2}) = \sqrt{(\pi)}, \Gamma(\frac{3}{2}) = \frac{1}{2} \Gamma(\frac{1}{2}) = \frac{\sqrt{\pi}}{2}$, <br />
$\Gamma(\frac{5}{2}) = \frac{5}{2} \Gamma(\frac{3}{2}) = \frac{5}{4} \sqrt{\pi}$ and so on for odd $k$.

##### Chi-Square distribution function

The Cumulative Distribution Function (CDF) gives the probability that a chi-square statistic is less than or equal to a given value: <br />
$ F(y;k)=P(Y \leq y) $
where $Y$ follows a chi-square distribution with $k$ degrees of freedom.

The CDF or cumulative distribution function is computed using lower-incomplete Gamma function as follows : <br />
$F(y;k)=\frac{\gamma(\frac{k}{2},\frac{y}{2})}{\Gamma(k/2)}$ where $\gamma(\frac{k}{2},\frac{y}{2})$ is the lower incomplete gamma function given by the formula <br />
$\gamma(\frac{k}{2}, \frac{y}{2}) = \int \limits_{0}^{y/2} t^{\frac{k}{2}-1} e^{-t} dt$, and $\Gamma(\frac{k}{2}) = \int \limits_{0}^{\infty} t^{\frac{k}{2}-1} e^{-t}dt$.

As $\gamma(\frac{k}{2}, \frac{x}{2})$ integrates only upto $\frac{x}{2}$, it can be normalized using $\Gamma(\frac{k}{2})$ to have a value between $0$ and $1$. Hence <br />
the regularized lower incomplete gamma function $P(y;k) = \frac{\gamma(\frac{k}{2}, \frac{x}{2})}{\Gamma(\frac{k}{2})}$ is a valid probability density function same as $F(y;k)$, which is also denoted as $P$-value. Thus, $P$ value or the Chi-Square distribution is used as the metric to do Chi-Square test.

#### Chi-Square test

The chi-square test is a statistical hypothesis test that uses the chi-square distribution to determine whether observed data differ significantly from expected data. There are two common types:

- Chi-square goodness-of-fit test: Checks whether a sample follows a specific distribution.
- Chi-square test for independence: Determines whether two categorical variables are independent.

##### Rationale

1. Pearson's Chi-Square test takes a metric ${\chi}^2 = \sum \limits_{i=1}^n \frac{(O_i - E_i)^2}{E_i}$, which is assumed to be having Chi-Square distribution where <br />
- $O_i$ : observed frequency of category $i$
- $E_i$ : Expected frequency of category $i$
- n : Number of categories   

2. For each category, a standardized normal distribution is assumed for $O_i$ around the expected value $E_i$ and variance $E_i$. So, a syandardized normal random variable $Z_i$ with mean = 0 and standard deviation $\sqrt(E_i)$ in the form of $Z_i = \frac{(O_i - E_i)}{\sqrt{E_i}}$. Here it is assumed that the variance of $O_i$ = $E_i$ (as in the case of Poisson distribution - only assumtion which can be made in absence of other variance data).

3. $\sum \limits_{i=1}^n {Z_i}^2$ follows a Chi-Square distribution with degree of freedom = $n$. Here is also an assumption that $Z_i$'s are independent, and there is no dependency on them. This is the NULL hypothesis - which means there is no dependency between $O_i$ and $E_i$'s.

##### Example 1

Let there be some data regarding the public transport modes preferred used by Male and female in a city within some time.

| Mode of transport | Male | Female | Total | 
| --- | --- | --- | --- |  
| Bus | 1050 | 950 | 2000 | 
| Metro | 2032 | 1980 | 4012 | 
| Taxi | 744 | 556 | 1300 | 
| Auto | 956 | 784 | 1740 |
| Total | 4782 | 4270 | 9052 | 

Now, <br />
1. Expected values $E_i$'s are calculated as : <br />
- $E_1 = 2000*4782/9052 = 1056.562$
- $E_2 = 4012*4782/9052 = 2119.464$
- $E_3 = 1300*4782/9052 =  686.765$
- $E_4 = 1740*4782/9052 = 919.209$
- $E_5 = 2000*4270/9052 = 943.438$
- $E_6 = 4012*4270/9052 = 1892.536$
- $E_7 = 1300*4270/9052 = 713.235$
- $E_8 = 1740*4270/9052 = 820.791$

2. $Z_i$ values :
- $Z_1 = \frac{(1050-1056.562)}{\sqrt{1056.562}} = -0.202$  
- $Z_2 = \frac{(2032-2119.464)}{\sqrt{2119.464}} = -1.9$  
- $Z_3 = \frac{(744-686.765)}{\sqrt{686.765}} = 2.184$  
- $Z_4 = \frac{(956-919.209)}{\sqrt{919.209}} = 1.213$  
- $Z_5 = \frac{(950-943.438)}{\sqrt{943.438}} = 0.213$  
- $Z_6 = \frac{(1980-1892.536)}{\sqrt{1892.536}} = 2.01$  
- $Z_7 = \frac{(556-713.235)}{\sqrt{713.235}} = -5.89$  
- $Z_8 = \frac{(784-820.791)}{\sqrt{820.791}} = -1.284$  

3. Sum up these values : $\sum \limits_{i=1}^8 {Z_i}^2$ = 50.318

4. Degree of freedom - (number of rows - 1) * (number of columns - 1) = 3.

5. Let the significance level $\alpha = 0.05$, now find the critical value from
Chi-Square table with degree of freedom = 3, significance level = 0.05. 	From Chi-squre table and $\alpha = 0.05$, the critical value = 7.81.

6. The obtained value is way above the critical value - hence the null hypothesis that there is no dependency between male/female and type of public transport is rejected.  
