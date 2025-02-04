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
<img src=/home/tathagato/classes/2024_25/MCSC13/probability/train_from_station.png alt="Train starting from station">
</p>

The person starts from his home between 8.45 AM to 8.55 AM as given below. 

<p align="center">
<img src=/home/tathagato/classes/2024_25/MCSC13/probability/man_starting_from_home.png alt="Man starting from Home">
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


