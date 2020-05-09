+++
title = "Statistical Theory"
description = "hypothesis tests, confidence intervals, bias, baysian statistics, ANOVA"
+++

Review
======

#### Random Variable

A *random variable* is a real-valued function for which the domain is a
sample space.

Discrete Random Variables
-------------------------

#### Definition

A random variable is said to be *discrete* if it can assume only finite
or a countably infinite number of distinct values.

#### Discrete Probability Distribution

The *probability distribution for a discrete variable $Y$* satisfies
that $p(y) = P(Y = y)$ for all $y$.

#### Expected Value of a Discrete Random Variable

Let $Y$ be a discrete random variable with the probability function
$p(y)$. Then the *expected value* of $Y$, denoted $E(Y)$ is defined as
the following: $$E(Y) = \sum_y{yp(y)}$$

#### Properties of Expected Value

1.  $E(c) = c$

2.  $E(cg(x)) = cE(g(x))$

3.  $E(g(x)) = \sum_{all y}g(y)p(y)$

4.  $E(g_1(x) + \dots + g_k(x)) = E(g_1(x)) + \dots + E(g_k(x))$

Moment Generating Functions
---------------------------

#### Definition

The *moment generating function of a random variable* denoted $m(t)$ for
random variable $Y$, is defined as $$m(t) = E(e^{Yt})$$ We say that a
moment generating function for $Y$ exists if there exists a positive
constant $b$ such that $m(t)$ is finite for $|t| \leq b$.

#### Properties of Moment Generating Functions

1.  $\lbrace \frac{d^km(t)}{dt^k} \rbrace_{t=0} = m^{(k)}(0) = \mu'_k$

2.  Uniquely determine a distribution

3.  If $Z = X + Y$, then $m_Z(t) = m_X(t) + m_Y(t)$, where $X, Y$ are
    independent random variables.

Continuous Random Variables
---------------------------

#### Definition

A random variable that can take any value in an interval is called
*continuous*.

#### Expected Value of a Continuous Random Variable

The *expected value of a continuous random variable Y* is
$$E(Y) = \int_{-\infty}^\infty{yf(y)dy}$$ provided the integral exists.

Variance
--------

#### Definition

If $Y$ is a random variable with the mean $E(Y) = \mu$, the *variance of
$Y$* is defined as $$V(Y) = E((Y-\mu)^2).$$

#### Properties of Variance

1.  $V(aY) = a^2V(Y)$

2.  $V(X+Y) = V(X) + V(Y)$ if $X,Y$ are independent

3.  $V(Y) = E(Y^2) - E(Y)^2$

4.  $V(\overline Y) = \frac{\sigma^2}{n}$

Frequently used Results
-----------------------

1.  $E(\overline x) = \mu$

2.  $V(\overline x) = \frac{\sigma^2}{n}$

Estimation
==========

Introduction into Statistics
----------------------------

#### Statistics

*Statistics* is a collection of procedures and principles for gaining
and analyzing information to educate people and help them make better
decisions when faced with uncertainty. It is science about data, where
you make decisions between certainty and uncertainty.

#### Population

The *population* is the collection of all individuals or items under
consideration in a statistical study.

#### Sample

The *sample* is part of the population from which information is
obtained.

#### Parameter

A *parameter* is a numerical descriptive measure of a population.

#### Statistic

A *statistic* is a numerical descriptive measure of a sample.

#### Types of Statistics

Based on its purpose, statistics can be categorized into *descriptive
statistics*, where data is examined and explored for its own intrinsic
interest as well as presented, and *inferential statistics*, where
information obtained from a sample of a population of a study and use
that information to draw conclusions about populations.

#### Estimator

An *estimator* is a rule that tells how to calculate the value of an
estimate based on the measurements in a sample.

#### Types of Estimation

Estimating a parameter can be done using a *point estimate*, a single
value, or an *interval*, an interval or real values.

#### i.d.d.

This acronym stands for *independent and identically distributed*. It
follows that if a set of events are i.d.d., then all events are
independent of each other and all share the same distribution (the same
mean, variance, etc.).

#### Typical Statistical Process

1.  Ask a question.

2.  Design a study.

3.  Collect data.

4.  Describe and summarize data.

5.  Select the appropriate statistical method.

6.  Inferential statistics.

7.  Interpret data.

8.  Answer the question.

Point Estimators
----------------

#### Sampling Distribution

A point estimator is a function of observations, random variables.
Therefore the point estimator is a random variable and has a
distribution. The distribution of a statistic is called a *sampling
distribution*.

#### Bias

For a parameter $\theta$ and an estimator $\hat \theta$ for $\theta$,
the estimator is *unbias* if and only if $E(\hat \theta) = \theta$. We
say it is *not unbias* if $E(\hat \theta) \neq \theta$. We can calculate
bias using the following: $$B(\hat \theta) = E(\hat \theta) - \theta$$

#### Variance of an Estimator

When faced with multiple unbias estimators, the best one to use is the
one of least variance.

#### Standard Error

The *standard error* is the standard deviation of an estimator or
statistic.

#### Mean Square Error

The *mean square error* is a function of both variance and bias
calculated as follows: $$\begin{aligned}
    MSE(\hat \theta) &= E((\hat \theta - \theta)^2) \\
    &= V(\hat \theta) + B(\theta)^2\end{aligned}$$

#### Unbais Estimators for Parameters

Let the following be an unbais estimator for $\mu$:
$$\overline x = \frac{\sum{Y_i}}{n}$$ Let the following be an unbias
estimator for $\sigma^2$:
$$s^2 = \frac{\sum{(Y_i-\overline Y)^2}}{n - 1}$$

Goodness of a Point Estimator
-----------------------------

#### Error of Estimation

The *error of estimation* $\epsilon$ is the distance between an
estimator and its target parameter. That is,
$$\epsilon = |\hat \theta - \theta|.$$ Even though the estimator may be
unbias, there will still likely be an error for a single sample.

#### Bounds on Error

For a given quantity $b$, we can find the probability of the error on
the estimator on parameter $\theta$ bounded by $b$ as follows:
$$\begin{aligned}
    P(\epsilon < b) &= P(|\hat \theta - \theta| < b) \\
    &= P(\theta - b < \hat \theta < \theta + b) \\
    &= \int_{\theta - b}^{\theta+b}{f(\hat \theta)d\theta}\end{aligned}$$

#### Tchebysheff's Theorem

Let $Y$ by a random variable with the mean $\mu$ and finite variance
$\sigma^2$. Then, generally, for any constant $k>0$, $$\begin{aligned}
    P(|Y-\mu| < k\sigma) &\geq 1 - \frac{1}{k^2} \\
    P(|Y-\mu| \geq k\sigma) &\leq \frac{1}{k^2}.\end{aligned}$$

Common Point Estimators
-----------------------

#### \...and their Standard Errors

` ` | ` ` | ` ` | ` `
  -------------------|-------------|----------------------------------------------------|------------------------------------------------------------------------
       $\theta$      | Sample Size | Estimator                                          | $\sigma_\theta$
         $\mu$       |     $n$     | $\displaystyle \overline Y = \frac{1}{n}\sum{Y_i}$ |                 $\displaystyle \frac{\sigma}{\sqrt n}$
          $p$        |     $n$     |        $\displaystyle \hat p = \frac{Y}{n}$        |                 $\displaystyle \sqrt \frac{p(1-p)}{n}$
     $\mu_1-\mu_2$   | $n_1, n_2$  |          $\overline Y_1 - \overline Y_2$           | $\displaystyle \sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}}$
       $p_1-p_2$     | $n_1, n_2$  |               $\hat p_1 - \hat p_2$                | $\displaystyle \sqrt{\frac{p_1(1-p_1)}{n_1} + \frac{p_2(1-p_2)}{n_2}}$

Note that $\sigma_1^2, \sigma_2^2$ are the variances of populations
$1, 2$ respectively. We assume the two sample cases are independent.

Confidence Interval
-------------------

#### Interval Estimator

An *interval estimator* is a rule specifying the method for using the
sample measurements to calculate end points on the interval. An interval
estimator will likely contain the target parameter and will be
relatively narrow. This is also commonly called a *confidence interval*.

#### Confidence Coefficient

The probability that a random confidence interval will enclose $\theta$
is called the *confidence coefficient*. This probability is denoted as
$$P(\hat \theta_L \leq \theta \leq \hat \theta_U) = 1 - \alpha$$ where
$\hat \theta_L$ and $\hat \theta_U$ are the lower and upper bounds on
the confidence interval defined as
$$\hat \theta_L = \hat \theta - z_{\alpha /2}\sigma_{\hat \theta}$$
$$\hat \theta_U = \hat \theta + z_{\alpha /2}\sigma_{\hat \theta}$$ and
$(1-\alpha)$ is the confidence coefficient.

#### One Sided Confidence Intervals

It is possible to build a *one sided confidence interval* such that
$$P(\hat \theta_L \leq \theta) = 1 - \alpha$$ or
$$P(\theta \leq \hat \theta_U) = 1 - \alpha.$$

#### Significance Level

If $(1-\alpha)$ is the confidence coefficient, then $\alpha$ is called
the *significance level*.

#### Confidence Level

In the context of confidence interval, the $100(1 - \alpha)\%$ is called
the *confidence level*.

#### Margin of Error

The *margin of error* is a value to determine how sample size affects
the accuracy of an estimated. It is calculated as half the length of the
confidence interval. It is also called the *maximum error of the
estimate*.

Properties of Point Estimators
------------------------------

#### Relative Efficiency

Given two unbias estimators $\hat \theta_1$ and $\hat \theta_2$ of a
parameter $\theta$, then the *efficiency of $\hat \theta_1$ relative to
$\hat \theta_2$* is given by the following:
$$\mathit{eff}(\hat \theta_1, \hat \theta_2) = \frac{V(\hat \theta_2)}{V(\hat \theta_1)}$$
If $\mathit{eff}(\hat \theta_1, \hat \theta_2) > 1$, then we prefer
$\hat \theta_1$ as an estimator over $\hat \theta_2$.

#### Consistency

An estimator $\hat \theta$ is said to be a *consistent estimator of
$\theta$* if for any $\epsilon > 0$,
$$\lim_{n \rightarrow \infty} P(|\hat \theta_n - \theta| < \epsilon) = 1$$
or
$$\lim_{n \rightarrow \infty} P(|\hat \theta_n - \theta| \geq \epsilon) = 0.$$
Consistency measures the variance of the estimator as the sample size
increases.

#### Consistency of Unbias Estimators

An unbias estimator $\hat \theta$ is said to be a *consistent estimator
of $\theta$* if $$\lim_{n \rightarrow \infty} V(\hat \theta_n) = 0.$$

#### Likelihood

Let $y_1 = Y_1, y_2 = Y_2, \dots, y_n = Y_n$ follow the distribution
that depends on parameter $\theta$. If $Y_i$ are discrete random
variables then the *likelihood function of the sample* is
$$L(y_1, y_2, \dots, y_n, \theta) = P(y_1, y_2, \dots, y_n, \theta) = \prod{P(y_i)}$$
Or if $Y_i$ are continuous random variables then the *likelihood
function of the sample* is
$$L(y_1, y_2, \dots, y_n, \theta) = f(y_1, y_2, \dots, y_n, \theta) = \prod{f(y_i)}$$
Sometimes $L(\theta)$ is used over $L(y_1, y_2, \dots, y_n, \theta)$.

#### Sufficiency

The statistic $U = g(Y_1,Y_2,\dots,Y_n)$ is said to be a *sufficient
statistic* if the conditional distribution of $Y_i$ given $U$ does not
depend on parameter $\theta$.

#### Method of Finding Sufficiency

The statistic $U = g(Y_1,Y_2,\dots,Y_n)$ is sufficient if and only if
the likelihood function can be factored into 2 non-negative functions as
follows.
$$L(y_1, y_2, \dots, y_n, \theta) = g(U,\theta)\cdot h(y_1, y_2, \dots, y_n)$$

#### Rao-Blackwell Theorem

Let $\hat \theta$ be an unbias estimator for $\theta$ such that
$V(\hat \theta) < \infty$. If $U$ is a sufficient statistic for
$\theta$, define $\hat \theta^* = E(\theta|U)$. Then for all $\theta$,
$MSE(\hat \theta^*) < MSE(\hat \theta)$.

#### Minimum Variance Unbias Estimator

A *minimum variance unbais estimator* is an unbias estimator with the
least variance of any other unbais estimator for the distribution.

#### How to Find MVUE

First find a sufficient statistic for given parameter. Then, confirm if
it is unbais. If not, tweat the estimator to make it unbais.

Methods of Estimation
=====================

Method of Moments
-----------------

#### $k^{th}$ Moment of a Random Variable

The *$k^{th}$ moment* taken about the origin is defined as the
following: $$\mu_k^\prime = E(Y^k)$$

#### $k^{th}$ Sample Moment

The *$k^{th}$ sample moment* of the sample $Y_1, Y_2,\dots, Y_n$ is
defined as the following: $$m_k^\prime = \frac{\sum{Y_i^k}}{n}$$

#### Method of Moments

The objective is to estimate $\mu_k^\prime$ with $m_k^\prime$. For a
distribution of $t$ random variables, we set
$\mu_k^\prime = \mu_k^\prime$ for $k \in [1, t]$ and solve for
$\theta_1, \theta_2, \dots, \theta_t$.

Method of Maximum Likelihood
----------------------------

#### Maximum Likelihood Estimators

Maximize $ln(L(\theta))$ with respect to each parameter and solve for
the parameter. We call estimators found this way *maximum likelihood
estimators*.

Hypothesis Testing
==================

#### Definition

A *hypothesis test* is a commonly used method for making a decision
about the value of a parameter by the data from samples.

#### Hypotheses

A hypothesis test is based upon two hypotheses determined by the
statistician. The first is the *null hypothesis*, denoted by $H_0$,
which is a statement of equality assumed to be true for the sake of the
test. The second is the *alternative hypothesis*, denoted $H_a$, which
is a statement of inequality.

#### Paradigm

Hypothesis tests come to one of two conclusions. They can reject $H_0$,
which shows the data would be in favor of $H_a$ and we conclude that
$H_a$ is true. Or, they can fail to reject null, which shows the data is
not strong enough to support $H_a$ and we conclude that $H_0$ is true.

#### Test Statistic

The *test statistic* is the sample statistic used to make a conclusion
on during a hypothesis test.

#### p-value

The *p-value* of a hypothesis test is the smallest level of significance
for which the observed data indicate that the null hypothesis should be
rejected. It is the probability that the test statistic, or a value more
extreme, would occur given the null hypothesis is true.

#### Conclusions

After determining the p-value, the statistician can draw a conclusion to
the experiment based on a significance level. If $p-value \leq \alpha$,
then we reject the null hypothesis. Otherwise, if $p-value > \alpha$,
then we fail to reject the null hypothesis.

#### How to Perform a Hypothesis Test

1.  Form hypotheses

2.  Choose the significance level $\alpha$

3.  Use sample data to determine the value of the test statistic

4.  Use a test to determine the p-value

5.  Make a decision about the truth of $H_0$

#### Types of Tests

Let the null hypothesis be $H_0: \theta = \theta_0$. Then given the
following alternatives, we determine the tail of the test.

-   $H_a: \theta \neq \theta_0 \rightarrow$ Two tailed test

-   $H_a: \theta > \theta_0 \rightarrow$ Right tailed test

-   $H_a: \theta < \theta_0 \rightarrow$ Left tailed test

Error Analysis
--------------

#### Type I Error

A *type I error* occurs when the result of a hypothesis test concludes
to reject $H_0$, when in reality that conclusion is false, and the $H_0$
is true. The probability of a type I error is the significance level:
$P(\text{Type I Error}) = \alpha$.

#### Type II Error

A *type II error* occurs when the result of a hypothesis test fails to
reject $H_0$, when in reality that conclusion is false, and the $H_0$ is
false. The probability of a type II error is based on the size of the
sample size: $P(\text{Type II Error}) = \beta$.

#### Decisions Made in a Hypothesis Test
                                                   
` ` | $H_0$ True  |  $H_0$ False
--- | --- | ---
 Fail to reject $H_0$ | | Type I Error
 Reject $H_0$ | Type II Error |

Power of Tests
--------------

#### Definition

Suppose $W$ is a test statistic and $RR$ be the rejection region for a
hypothesis test of parameter $\theta$. Define the *power of the test*,
denoted $power(\theta)$, to be the probability that the test rejects
$H_0$, when the actual value parameter value is $\theta$. In other
words, $$power(\theta) = P(\text{Reject } H_0 : \theta = \theta_0)$$
where $\theta_0$ is the value of the null hypothesis. Analyzing the
power of a test is contrasts the p-value approach to statistical tests.

#### Power When Null Is True

Suppose $\theta = \theta_0$. Then $$\begin{aligned}
power(\theta_0) &= P(\text{Reject } H_0 : H_0 \text{ is true}) \\
&= P(\text{Type I error}) \\
&= \alpha\end{aligned}$$

#### Power When Null Is False

Suppose $\theta = \theta_a$. Then $$\begin{aligned}
power(\theta_a) &= P(\text{Reject } H_0 : H_0 \text{ is false}) \\
&= 1 - P(\text{Fail to reject } H_0 : H_0 \text{ is false}) \\
&= 1 - P(\text{Type II error}) \\
&= 1 - \beta\end{aligned}$$

#### Power Curve

Looks kind of like 1 minus the normal distribution, with the minimum
value at $\theta_0$ having height of $\alpha$.

#### Simple Hypothesis

If a random sample is taken from a distribution of parameter $\theta$, a
hypothesis is said to be *simple* if that hypothesis uniquely identifies
the distribution.

#### Composite Hypothesis

Any hypothesis that is not simple is called *composite* and does not
uniquely identify the distribution.

#### Most Powerful Test

When determining the value of $H_0$ and $H_a$, we want to choose a
rejection region such that $\alpha = power(\theta_0)$ is fixed and
$power(\theta_a)$ is maximum. We call such a test the *most powerful
test*.

#### Neymann-Pearson Lemma

Suppose we test simple null hypothesis $H_0: \theta = \theta_0$ versus
simple alternative hypothesis $H_a: \theta = \theta_a$, based on simple
random samples $Y_1,\dots, Y_n$ from a distribution with parameter
$\theta$. Then for a given $\alpha$, the test that maximizes the power
at $\theta_a$ has a rejection region $RR$ determined by
$$\frac{L(\theta_0)}{L(\theta_a)} < k$$ where $k$ is chosen so that the
test has a desired value for $\alpha$. Note that $k$ is a bound on the
random variable $Y$.

#### Uniformly Most Powerful Test

The Neymann-Pearson Lemma can only be used on a simple alternative
hypothesis. Oftentimes a composite alternative hypothesis is used. In
order to invoke the Neymann-Pearson Lemma, we say $H_a = \theta_a$ for
$\theta_a$ in the bounds described by the composite alternative
hypothesis. When this procedure is used on a test with a composite
alternative hypothesis, the determined $\alpha$ gives the *uniformly
most powerful test*.

Analysis of Categorical Data
============================

#### Types of Data

All of data can be either *quantitative* or *qualitative*. Quantitative
data are numbers, that are either *discrete* or *continuous*.
Qualitative data are not numbers, but are categories or qualities of an
observational unit. There is *monimal* data, where the variables are not
ordered, and *ordinal*, where the variables have a natural way of being
ordered.

#### Contingency Table

When data is collected from two variables of a population it is called
*bi-variate*. When the frequency of the two variables are drawn across
each other we call this a *contingency table*.

Analysis of Variance
--------------------

#### Factor and Level

Variables that the statistician uses to partition the population into
subpopulations are called *factors*. A distinct subcategory of a factor
is called its *level*.

#### ANOVA

The *analysis of variance* (abbreviated *ANOVA*) is a procedure that
attempts to analyze the variation in a set of responses and assign
portions of this variation to each variable in a set of independent
variables. The objective is to identify important independent variables
and determine how they affect the response.

#### Experimental Units

Objects upon which measurements are taken are called *experimental
units*.

#### Blocks and Treatments

Ways to partition data is into factor variables *blocks* and
*treatments*. Generally data is partitioned into blocks are treatments
are then applied to each block. Mathematically, how this assignment is
done is arbitrary.

#### Completely Randomized Design

A *completely randomized design* to compare $k$ treatments, is one in
which a grup of $n$ relatively homogeneous experimental units are
randomly divided into $k$ subgroups of sizes $n_1, n_2, \dots, n_k$
where the sum of $n_i$ is $n$. All experimental units in each subgroup
receive the same treatment, which each treatment applied to exactly one
subgroup.

#### Randomized Block Design

A *randomized block design* containing $b$ blocks $k$ treatments
consists of $b$ blocks of $k$ experimental units each. The treatments
are randomly assigned units in each block, with each treatments
appearing exactly once in every block.

Ways to Measure Variance for Two Way ANOVA
------------------------------------------

#### Total Sum of Squares

The *sum of squares of deviations* or *total sum of squares*,
abbreviated *TSS*, is a measure of variance across the entire
population. It's value is calculated by the following:
$$TSS = \sum_{i=1}^k \sum_{j=1}^{n_i} (y_{ij} - \bar y)^2$$

#### Error Sum of Squares

The *error sum of squares*, abbreviated *SSE* is a measure of variation
within subpopulations partitioned by treatments.

#### Treatment Sum of Squares

The *error sum of squares*, abbreviated *SSE* is a measure of variation
between subpopulations partitioned by treatments.

Bayesian Statistics
===================

#### Paradigm

Up to this point in these notes, all statistical procedures are based on
treating parameters as unknown constants. Bayesian statistics treats
parameters as random variables that follow a distribution. Using data
collected, we can adjust the distribution to be more accurate given the
data using Bayes' Rule.

#### Bayes' Rule

Let $A$ and $B$ be two events with probability $P(A)$ and $P(B)$. Then
the following is true, given that $P(B) \neq 0$.
$$P(A|B) = \frac{P(B|A)\cdot P(A)}{P(B)}$$

#### Discrete Probabilities

Let $H$ be an outcome of the given parameter and let $D$ be the data
collected about that parameter.

-   Every parameter starts with an initial distribution. We call this
    the *prior distribution* notated as $P(H)$.

-   The *likelihood* is the probability that the data occurs given the
    prior distribution, notated as $P(D|H)$.

-   The probability that the data occurs is called the *marginal
    distribution* notated as $P(D)$.

-   Lastly, the distribution of the parameter given the collected data
    is called the *posterior distribution*, notated as $P(H|D)$.

In addition, we call an intermediate calculation the *joint likelihood*,
calculated by $P(H)\cdot P(D|H)$.

#### How to Calculate Posterior Distribution

Using Bayes' rule, we can calculate the posterior distribution using the
prior distribution and the data. First calculate likelihood, then joint
likelihood. The sum of the all joint likelihoods is the marginal
distribution. Then using Bayes' rule the posterior is calculated.

#### Bayesian Box

A *Bayesian box* is a way to organize calculations taken to determine
the posterior probability. Is is shown here.

   Hypotheses |  Prior   | Likelihood |          Joint          | Posterior
  ------------|----------|------------|-------------------------|------------
     $H_1$    | $P(H_1)$ | $P(D|H_1)$ | $P(H_1) \cdot P(D|H_1)$ | $P(D|H_1)$
     $H_2$    | $P(H_2)$ | $P(D|H_2)$ | $P(H_2) \cdot P(D|H_2)$ | $P(D|H_2)$
    $\vdots$  | $\vdots$ |  $\vdots$  |        $\vdots$         |  $\vdots$
     $H_2$    | $P(H_2)$ | $P(D|H_2)$ | $P(H_2) \cdot P(D|H_2)$ | $P(D|H_2)$
    $Total:$  |   $1$    |            |         $P(D)$          |    $1$

#### Continuous Probabilities

This is similar to the discrete counterpart, adjusted for continuous
random variables. Let $\theta$ be the value of the given parameter and
let $y_1, \dots, y_n$ be the data collected about that parameter.

-   We notate the prior distribution as $g(\theta)$.

-   The likelihood of the data is the application of the likelihood
    function, $L(y_1, \dots, y_n | \theta)$.

-   The joint distribution is calculated by
    $L(y_1, \dots, y_n | \theta) \cdot g(\theta)$.

-   The marginal distribution is calculated as follows:
    $$m(y_1, \dots, y_n) = \int_{-\infty}^\infty L(y_1, \dots, y_n | \theta) \cdot g(\theta)\ d\theta$$

-   Lastly, the posterior distribution is calculated as follows:
    $$g^*(\theta|y_1, \dots, y_n) = \frac{L(y_1, \dots, y_n | \theta) \cdot g(\theta)}{\int_{-\infty}^\infty L(y_1, \dots, y_n | \theta) \cdot g(\theta)\ d\theta}$$

#### Bernoulli Distribution

A discrete random variable that has binary outcomes 0 or 1 follows a
Bernoulli distribution with probability function as follows:
$$f(k) = p^k(1-p)^{1-k}$$

#### Beta Distribution

In Bayesian statistics, any beta distribution is the prior distribution
for a Bernoulli or Binomial distribution. When the prior is updated
using the data, the result is a beta posterior was altered parameter
values.

#### Conjugate Prior

Any prior distributions that result in posterior distributions that
follow the same functional form of the prior are called *conjugate
priors*.
