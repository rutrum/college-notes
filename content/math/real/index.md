+++
title = "Real Analysis"
description = "infinity, field axioms, sequences, series, convergence, derivatives, integration"
+++

Construction of Real Numbers
============================

The Natural Numbers
-------------------

#### The Peano Axioms

We construct the *natural numbers* $\mathbb N$ by the following axioms.

1.  1 is a natural number.

2.  If $n$ is a natural number, then it has a successor $S(n)$ that is
    also a natural number.

3.  1 is not a successor of any natural number.

4.  If $n$ and $m$ are natural numbers with the same successor, then $n$
    and $m$ are equal.

5.  *Induction Axiom:* A subset containing 1 and containing $S(n)$
    whenever $n$ is in the subset must be the set of all natural numbers
    $\mathbb N$.

#### Mathematical Induction

Let $P_1, P_2, \dots$ be a list of statements, all of which could either
be true or false. If $P_1$ is true, and $P_n$ being true implies
$P_{n+1}$ is true, then $P_n$ is true for all $n$.

Proving $P_1 \equiv T$ is called the *base case*. Proving
$P_n \equiv T \implies P_{n+1} \equiv T$ is called the *inductive step*.

More Sets of Numbers
--------------------

#### Integers

Define the *integers* $\mathbb Z$ as the set of natural numbers, their
additive inverses, and zero.

#### Rationals

Define the *rationals* $\mathbb Q$ as the set of ratios $\frac{a}{b}$
such that $a$ and $b$ are integers and $b$ is nonzero.

#### Rational Zeros Theorem

Let $f(x) = c_nx^n + c_{n-1}x^{n-1} + \dots + c_1x + c_0, c_n \neq 0$ be
polynomials with integer coefficients. If a rational number
$\frac{a}{b}$, in lowest terms, is a root of $f(x)$, then $a|c_0$ and
$b|c_n$.

#### Rationals are Incomplete

A full intuitive sense of numbers requires numbers that lie outside the
set of rationals. For example, the hypotenus of a right triangle with
legs both of length 1 has a length of $\sqrt{2}$, a nonrational number.
We can use the rational zeros theorem to prove that this is true.

Fields
------

#### The Field Axioms

We construct the *real numbers* $\mathbb R$ by the following axioms.

1.  There exist two operations:
    $$+:\mathbb R \times \mathbb R \rightarrow \mathbb R \hspace{1cm} \cdot:\mathbb R \times \mathbb R \rightarrow \mathbb R$$
    We abbreviate these functions as follows:
    $$a + b := +(a,b)\hspace{1cm} a \cdot b = ab := \cdot(a,b)$$

2.  Addition is associative: $a + (b + c) = (a + b) + c$.

3.  Addition is commutative: $a + b = b + a$.

4.  There exists a real number, denoted by 0, such that $a + 0 = a$ for
    all $a |in \mathbb R$.

5.  For all $a \in \mathbb R$, there exists an element
    $-a \in \mathbb R$ such that $a + (-a) = 0$.

6.  Multiplication is associative: $a(bc) = (ab)c$.

7.  Multiplication is commutative: $ab = ba$.

8.  There exists a real number, distinct from 0, denoted by 1, such that
    $a \cdot 1 = a$ for all $a |in \mathbb R$.

9.  For all nonzero $a \in \mathbb R$, there exists an element
    $a\inv \in \mathbb R$ such that $a \cdot a\inv = 0$.

10. For all $a,b,c \in \mathbb R$, it is true that $a(b+c) = ab + ac$.

#### Fun Facts

-   $a + c = b + c \implies a = b$

-   $a \cdot 0 = 0$

-   $(-a) \cdot b = -(a \cdot b)$

-   $-a \cdot -b = a \cdot b$

-   $a \cdot c = b \cdot c, c \neq 0 \implies a = b$

-   $a \cdot b = 0 \implies a = 0 \text{ or } b = 0$

#### Order Axiom

There exists a subset $\mathbb R^+$ of $\mathbb R$ called the set of
positive numbers that satisfies the following:

1.  Set $\mathbb R^+$ is closed under addition and multiplication.

2.  *Law of Trichotomy*: For any real number, one and only one of the
    following is true:
    $$a \in \mathbb R^+ \hspace{1cm} -a \in \mathbb R^+ \hspace{1cm} a = 0$$

We define the following relations on $\mathbb R$: $$\begin{aligned}
        x \leq y \hspace{.5cm} \text{iff} &\ y-x \in \mathbb R^+ \cup \{0\} \\\\
        x \geq y \hspace{.5cm} \text{iff} &\ x-y \in \mathbb R^+ \cup \{0\} \\\\
        x < y \hspace{.5cm} \text{iff} &\ y-x \in \mathbb R^+ \\\\
        x > y \hspace{.5cm} \text{iff} &\ x-y \in \mathbb R^+
        \end{aligned}$$

#### Fun Facts with Order

-   $a \leq b \implies -b \leq -a$

-   $a \leq b \text{ and } c \leq 0 \implies bc \leq ac$

-   $0 \leq a \text{ and } 0 \leq b \implies 0 \leq ab$

-   $0 \leq a^2$

-   $0 < 1$

-   $0 \leq a \implies 0 \leq a\inv$

-   $0 < a < b \implies 0 < b\inv < a\inv$

Metric
------

#### Definition

A *metric* is a function $d: X \times X \rightarrow \mathbb R$ such that
the following are true.

1.  $d(x,y) \geq 0$

2.  $d(x,x) = 0$

3.  $d(x,y) = d(y,x)$

4.  $d(x,z) \leq d(x,y) + d(y,z)$

Note that $d(x,y)$ is read as "the distance from $x$ to $y$". A set is
called a *metric space* if a metric function is defined that satisfies
the above.

#### Metric Space $\mathbb R$

Set $\mathbb R$ is a metric space under
$d: \mathbb R \times \mathbb R \rightarrow \mathbb R$ where
$$d(x,y) = |x - y|.$$

Bounds
------

#### Maximum

Let $S \subseteq \mathbb R$. If for some $s \in S$ and $x \leq s$ for
all $s$, then $s$ is called the *maximum* of $S$, denoted $\max S$.

#### Minimum

Let $S \subseteq \mathbb R$. If for some $s \in S$ and $x \geq s$ for
all $s$, then $s$ is called the *minimum* of $S$, denoted $\min S$.

#### Upper Bound

An *upper bound* for $S$ is an element $m \in \mathbb R$ such that
$x \leq m$ for all $x \in S$. If such $m$ exists we say $S$ is *bounded
above* by $m$.

#### Lower Bound

An *lower bound* for $S$ is an element $m \in \mathbb R$ such that
$x \geq m$ for all $x \in S$. If such $m$ exists we say $S$ is *bounded
below* by $m$.

#### Supremum

Let $S \subseteq \mathbb R$ be bounded above. The *supremum* of $S$,
denoted $\sup S$, is the minimum of all upperbounds of $S$.

#### Infemum

Let $S \subseteq \mathbb R$ be bounded below. The *infemum* of $S$,
denoted $\inf S$, is the maximum of all lowerbounds of $S$.

#### Difference Between the Reals and Rationals

So far, the 4 additive axioms, the 4 multiplicative axioms, the
distributive axiom, and the order axiom, construct both the real numbers
and rational numbers with no distinction between the two. Therefore, the
completeness axiom was construction to make such distinction.

#### Completeness Axiom

If $S$ is bounded above in $\mathbb R$, then the set of upperbounds of
$S$ has a minimum. If $S$ is bounded below in $\mathbb R$, then the set
of lowerbounds of $S$ has a maximum.

#### Density

We say that set $A$ *is dense in* $B$ if for any two values
$b, \beta \in B$, where $b < \beta$, there exists a number $a \in A$
such that $b < a < \beta$.

#### Archimedean Property

For any $x \in \mathbb R$, there exists $n \in \mathbb N$ such that
$n > x$. As a consequence of this property we know that $\mathbb Q$ is
dense in $\mathbb R$.

The Symbols $\infty$ and $-\infty$
----------------------------------

#### Notation

Note that $\infty$ and $-\infty$ are not elements of $\mathbb R$.
Rather, they are symbols used in the following ways: $$\begin{aligned}
        [a, \infty) &:= \{x \in \mathbb R: x \geq a\} \\\\
        (a, \infty) &:= \{x \in \mathbb R: x > a\} \\\\
        (-\infty, b] &:= \{x \in \mathbb R: x \leq b\} \\\\
        (-\infty, b) &:= \{x \in \mathbb R: x < b\}
        \end{aligned}$$

#### Extended Real Numbers

The set of the *extended real numbers* is defined as
$\mathbb R \cup \{-\infty, \infty\}$ with associated definitions of
operations on elements $-\infty$ and $\infty$.

Sequences
=========

#### Definition

Define a *sequence* to be a function $f: \mathbb N \rightarrow X$. We
call this a *sequence in $X$* that is notated as
$(S_n) = (f(1), f(2), \dots )$ where $f(n) = a_n$.

Convergence of Sequences
------------------------

#### Definition

Let $(S_n)$ in $\mathbb R$ *converge* to $L \in \mathbb R$ if for any
$\epsilon > 0$, there exists an $N \in \mathbb N$ (dependent on epsilon)
such that for all $n > N$, $$|S_n - L| < \epsilon.$$ We say that $(S_n)$
*converges* to $L$. We can denote this as
$\displaystyle \lim_{n \rightarrow \infty}S_n = L$. If there does not
exist any $L$ for which this is true, we say that $(S_n)$ *diverges*.

#### Uniqueness

The limit of a sequence is unique.

Cardinality
-----------

#### Definition

Let $S$ be a set. The *cardinality* of $S$ is the number of elements in
$S$, denoted $|S|$.

#### Comparing Sizes

We say that $|A| = |B|$ if and only if there exists an
$f: A \rightarrow B$ that is a bijection. We say that $|A| < |B|$ if and
only if there exists an $f: A \rightarrow B$ that is injective and not
surjective.

#### Countable

-   If $|A| < |\mathbb N|$ then we say $A$ is *countable*.

-   If $|A| = |\mathbb N|$ then we say $A$ is *countably infinite*.

-   If $|A| > |\mathbb N|$ then we say $A$ is *uncountably infinite*.

#### Enumeration

A list of all elements of a set is called an *enumeration* of the set.
This list is not unique.

#### Power Set

The *power set* of $A$, denoted $\mathcal P(A)$, is the set of all
subsets of $A$.

#### Union of Countable Sets

The union of countable sets is also countable.

#### Continuum Hypothesis

Does there exist a set with cardinality greater than the integers but
less than the reals? It has been proved that this cannot be proved true.
It also been proved that this cannot be proven false. The conclusion is
called *undecidable*.

Limits of Sequences
-------------------

#### Boundedness

A sequence is said to be *bounded above* if the set of its terms is
bounded above. A sequence is said to be *bounded below* if the set of
its terms is bounded below.

#### Bounds and Convergence

If a sequence converges, then it must be bounded.

#### Properties of Limits

Let $(a_n)$ and $(b_n)$ be convergent series. Then the following
properties hold.

Rule | Notation
--- | ---
Constant Multiple | $\displaystyle \lim_{n\rightarrow \infty} ca_n = c\lim_{n\rightarrow \infty} a_n$
Sum Rule | $\displaystyle \lim_{n\rightarrow \infty}(a_n + b_n) = \lim_{n\rightarrow \infty} a_n + \lim_{n\rightarrow \infty} b_n$
Product Rule | $\displaystyle \lim_{n\rightarrow \infty}(a_n\cdot b_n) = \lim_{n\rightarrow \infty} a_n \cdot \lim_{n\rightarrow \infty} b_n$
Quotient Rule | $\displaystyle \lim_{n\rightarrow \infty}\frac{a_n}{b_n} = \frac{\displaystyle \lim_{n\rightarrow \infty} a_n}{\displaystyle \lim_{n\rightarrow \infty} b_n}$

#### Infinite Limits

We say that $\lim S_n = \infty$ if for every $M>0$ then there exists
$N \in \mathbb N$ such that $S_n > M$ for all $n > N$. Likewise, this is
defined for $-\infty$.

#### Monotone Sequence

We say $(S_n)$ is increasing if $S_{n+1} \geq S_n$ for all
$n \in \mathbb N$. We say $(S_n)$ is decreasing if $S_{n+1} \leq S_n$
for all $n \in \mathbb N$.

#### Bounded Means Converges

An increasing (decreasing) sequence bounded above (below) converges.

#### Unbounded Means It Doesn't

If $(S_n)$ is increasing (decreasing) and is not bounded, then
$\lim S_n = \infty$ ($-\infty$).

Limits of Bounds on Sequences
-----------------------------

#### Limit Superior

The limit of the supremum of the tails of a sequence.
$$\lim \sup S_n = \lim_{N\rightarrow \infty} \sup\{S_n:n>N\}$$

#### Limit Inferior

The limit of the infemum of the tails of a sequence.
$$\lim \inf S_n = \lim_{N\rightarrow \infty} \inf\{S_n:n>N\}$$

#### They Always Exist

For any sequence $(S_n)$, one of the following is true.

1.  $\lim \sup S_n = L \in \mathbb R$.

2.  $\lim \sup S_n = \infty$.

3.  $\lim \sup S_n = -\infty$.

Similarly, this holds for the infemum.

Cauchy Sequences
----------------

#### Definition

A sequence $(S_n)$ is said to be *Cauchy* if for every $\epsilon > 0$,
there exists an $N \in \mathbb N$ such that for any $m, n > N$,
$$d(S_m-S_n) < \epsilon.$$

#### Convergence

Note that Cauchy sequences don't always converge. This depends on the
metric space in which the sequence is defined. A metric space where
these converge is called *complete*. However, if a sequence does
converge then it must be Cauchy, no matter the space.

#### But in the Reals!

In the reals all Cauchy sequence converge.

Subsequences
------------

#### Definition

A subsequence of $(S_n)$ is a sequence of the form
$(S_{n_i})_{i=1}^\infty$ such that $(n_i)$ is a strictly increasing
sequence in $\mathbb N$.

#### Suprisingly Useful Fact

If $n_i$ is a strictly increasing sequence in $\mathbb N$, then
$n_i \geq i$ for all $i \in \mathbb N$.

#### Subsequence Convergence

If a sequence $(S_n)$ converges to $L, \infty, -\infty$ then every
subsequence of $(S_n)$ converges to $L, \infty, -\infty$.

#### Unbounded Subsequences

If $(s_n)$ is an unbounded-above sequence, it has an increasing sequence
diverging to $\infty$. If $(s_n)$ is an unbounded-below sequence, it has
a decreasing sequence diverging to $-\infty$.

#### Monotonic Subsequences Exist

Every sequence contains a monotonic subsequence.

#### Bolzano-Weierstrass Theorem

Every bounded sequence in $\mathbb R$ has a convergent subsequence.

#### Subsequential Limits

A *subsequential limit* of $(s_n)$ is a limit of a subsequence. If
$\lim(s_n)$ has a limit $L$, all subsequential limits are $L$.

#### Limsups are Subsequential Limits

The limit supremum and limit infemum are subsequential limits.

#### Topology

A *topology* is a pair $(X,T)$ where $X$ is a set, and $T$ is a set of
subsets of $X$ such that

1.  $X \in T, \emptyset \in T$

2.  An arbitrary union of sets in $T$ is also in $T$

3.  A finite intersection of sets in $T$ is also in $T$

An element of $T$ is called an *open set*.

#### Best Definition of a Limit

Let $\lim s_n = L$ if for any open set $\mathcal O$ containing $L$,
there exists $N \in \mathbb N$ such that $n>N$, $s_n \in \mathcal O$.

#### Accumulation Point

A *limit point* or *accumulation point* of a set $S \subseteq X$ is a
point $x \in X$ such that every open set $\mathcal O$ containing $x$
also contains an element of $S-\{x\}$.

#### Bolzano-Weierstrass in a Different Way

Every bounded infinite subset of $\mathbb R$ possesses an accumulation
point.

Series
======

#### Definition

Let $(a_n)$ be a sequence. We define $(s_n)$ by
$$s_n = \sum_{k=1}^na_k.$$ So $(s_n)$ is a new sequence called a
*series*. Note that $(a_n)$ is called the *$n^{th}$ term* and $(s_i)$ is
called the *$i^{th}$ partial sum*.

#### Convergence

If $\lim s_n = L$, we say that the series converges to $L$, or that the
sum of the series is $L$.

#### Harmonic Series

$$\sum_{k=1}^\infty \frac{1}{k}$$

#### Geometric Series

$$\sum_{k=1}^\infty ar^k$$

#### Geometric Convergence

The geometric series converges only when $|r| < 1$.

#### Cauchy Criteria

Suppose $\sum a_n$ converges. It is true that for some $n \geq m > N$,
$$\left|\sum_{k=m}^n\right|<\epsilon$$

Tests of Convergence
--------------------

#### $N^{th}$ Term Test

If $\lim a_k \neq 0$, then $\sum a_k$ diverges.

#### Comparison Test

Let $\sum a_k$ converge, where $a_k \geq 0$. If $|b_k| \leq a_k$, for
all $k$, then $\sum b_k$ converges.

#### Root Test

Let $\sum a_k$ be a series. Let $\alpha:= \lim\sup|a_n|^{\frac{1}{n}}$.
If $\alpha < 1$, then the series converges. If $\alpha > 1$, then the
series diverges. If $\alpha = 1$, then the test is inconclusive.

#### Ratio Test

Let $\sum a_k$ be a series of nonzero terms. Let
$\alpha:= \lim\sup\left|\frac{a_n+1}{a_n}\right|$. If $\alpha < 1$, then
the series converges absolutely. If $\alpha > 1$, then the series
diverges. If $\alpha = 1$, then the test is inconclusive.

#### p-series

The series $\sum \frac{1}{n^p}$ converges when $p > 1$ and diverges when
$p \leq 1$ for some $n > 1$.

#### Alternating Series Test

Suppose $a_n$ is a non-negative, decreasing sequence. Suppose that
$\lim a_n = 0$. Then $\sum (-1)^{n+1} a_n$.

#### Integration Test

Let $a_n$ be a sequence. Let $f:[1,\infty) \rightarrow \mathbb R$ such
that $f$ is continuous, nonnegative, nonincreasing, and that
$f(n) = a_n$. Then $\sum_{n=1}^\infty a_n$ converges if and only if
$\int_1^\infty f(x)dx$ converges.

Continuity
==========

#### Refresher on Domain and Range

Define the domain of $f$, denoted $dom(f)$ as the set of all $x$ such
that $f(x)$ is defined. Define the range of $f$ to be the set of $f(x)$
where $x$ is in the domain of $f$.

#### Limit at a Point

The notation $\lim_{x\rightarrow a} f(a) = L$ is defined as, for any
$\epsilon > 0$, there exists a $\delta > 0$, dependent on $0$, such that
if $x \in dom(f)$ and $0 < |x-a| < \delta$, then $|f(x)-L| < \epsilon$.

#### Continuity

Let $f(x)$ be *continuous* at $x=a$ if
$$\lim_{x\rightarrow a} f(x) = f(a).$$ In other words, for any
$\epsilon > 0$, there exists $\delta > 0$ such that if $x \in dom(f)$
and $|x-a| < \delta$, then $|f(x)-f(a)| < \epsilon$.

#### Limit at a Point Sequence Style

The notation $\lim_{x\rightarrow a} f(a) = L$ is defined as, for any
sequence $(x_n)$ in $dom(f)$ such that if
$\lim_{n\rightarrow\infty}x_n = a$, then $(f(x))$ converges to $L$.

#### Limit Rules

All limit rules about limits at infinity also apply to limits at points.

#### Continuity Sequence Style

Let $f(x)$ be *continuous* at $x=a$ if for any sequence $(x_n)$ in
$dom(f)$ converging to $a$, $(f(x))$ converges to $f(a)$.

#### Continuity on Operations

If $f(x)$ and $g(x)$ are continuous at $x=a$, then $f+g$, $f\cdot g$ and
$f/g$, where $g(a) \neq 0$, are all also continuous at $x=a$. In
addition, if $g(x)$ is continuous at $x=a$ and $f(x)$ is continuous at
$x=g(a)$, then $f(g(a))$ is continuous at $x=a$.

#### Extreme Value Theorem

Let $f$ be continuous and bounded on $[a,b]$. Then there exists
$x_{min}, x_{max} \in [a,b]$ such that
$f(x_{min})\leq f(x) \leq f(x_{max})$ for all $x \in [a,b]$.

#### Intermediate Value Theorem

Let $a<b$, and let $f$ be continuous on $[a,b]$. If
$f(a) \leq \gamma \leq f(b)$ or $f(b) \leq \gamma \leq f(a)$, then there
exists $c \in [a,b]$ such that $f(c) = \gamma$.

#### Uniform Continuity

We say that $f$ is *uniformly continuous* on $X$ if for any
$\epsilon > 0$, there exists $\delta > 0$ such that for all $x,y \in X$,
$|x-y| < \delta$ implies $|f(x)-f(y)| < \epsilon$. In other words,
$\delta$ is not dependent on $x$.

#### Continuity on a Closed Interval is Uniform

If $f$ is continuous on $[a,b]$, then $f$ is uniformly continuous on
$[a,b]$.

#### Uniform Continuity on Bounded Interval is Bounded

Let $X$ be a bounded set. If $f(x)$ is uniformly continuous on $X$, then
$f$ is bounded on $X$.

Differentiation
===============

#### Definition

Let $f$ be a real valued function. We say $f$ is differentiable at $x=a$
if there exists $\alpha, \beta \in \mathbb R$ where
$\alpha < a < \beta$, such that $(\alpha, \beta) \subset dom(f)$ and
$\lim_{x\rightarrow a} \frac{f(x)-f(a)}{x-a}$ converges.

#### Derivative of a Function

Define $f':X\rightarrow \mathbb R$ by
$f'(a) = \lim_{x\rightarrow a} \frac{f(x)-f(a)}{x-a}$, where
$X = \{x:f\text{ is differentiable at } x\}$.

#### Differentiation implies Continuity

If $f(x)$ is differentiable at $x=a$, then it is continuous at $x=a$.

#### Properties of the Derivative

Let $f$ and $g$ be differentiable at $x=a$, or $x=g(a)$ when applicable.

Rule | Notation
--- | ---
Constant Rule | $\frac{d}{dx}(cf(x)) = c \cdot \frac{d}{dx}f(x)$
Sum Rule | $\frac{d}{dx}(f(x)+g(x)) = \frac{d}{dx}f(x) + \frac{d}{dx}g(x)$
Product Rule | $\frac{d}{dx}(f(x)g(x)) = f(x)g'(x) + f'(x)g(x)$
Quotient Rule | $\frac{d}{dx}(\frac{f(x)}{g(x)}) = \frac{g(x)f'(x) - f(x)g'(x)}{(g(x))^2}$
       Chain Rule | $\frac{d}{dx}(f(g(x)) = f'(g(x))g'(x)$

Sequences of Functions
======================

#### Pointwise Convergence

Let $f_n(x)$ be a sequence of functions, with $dom(f_n) = S$ for all
$n \in \mathbb N$. We say that $\lim_{n\rightarrow \infty}f_n(x)=f(x)$
pointwise if for every fixed point $x_0 \in S$,
$\lim_{n\rightarrow \infty}f_n(x_0)=f(x_0)$ as a sequence in
$\mathbb R$. We also denote this as "$f_n\rightarrow f$ pointwise".

#### Uniform Convergence

Let $(f_n(x))$ be a sequence of functions on $S$. We say that $f_n$
converges to $f$ uniformly if for every $\epsilon > 0$, there exists
$N \in \mathbb N$ such that for $n > N$, $|f_n(x)-f(x)|<\epsilon$ for
all $x \in S$.

#### Uniqueness

If $(f_n)$ has a pointwise limit, it is unique. If it has a uniformly
continuous limit, it is also unique.

#### Uniform Implies Pointwise

If $f_n$ converges to $f$ uniformly, then it converges to $f$ pointwise.

#### Uniform Convergence of Continuous is Continuous

Let $f_n$ be a series of continuous functions on $S$. If $f_n$ converges
to $f$ uniformly, then $f$ is continuous.

Power Series
============

#### Definition

Let $(a_n)$ be a sequence in $\mathbb R$. Then
$\sum_{n=0}^\infty a_nx^n$ is a power series.

#### Pointwise Convergence

We may define
$$f(x) := \sum_{n=0}^\infty a_nx^n = a_0 + a_1x + a_2x^2 + a_3x^3 + \dots$$
where $dom(f) = \{x: \sum a_nx^n \text{ converges}\}$. Then if we set
$f_k(x)$ to be the partial sum of the first $k$ terms, then $f_k$
converges to $f$ pointwise.

#### Radius of Convergence

Let $\sum a_nx^n$ be a power series. Let
$\beta = \lim\sup |a_n|^\frac{1}{n}$. Let $R$ be defined as follows.
$$R=\begin{cases}
            \frac{1}{\beta} & 0 < \beta < \infty \\\\
            \infty & \beta = 0 \\\\
            0 & \beta = \infty
        \end{cases}$$ We call $R$ the *radius of convergence*.

#### Uniformly Cauchy

Let $(f_n)$ be a sequence of functions. Sequence $(f_n)$ on $S$ is
*uniformly Cauchy* if for $\epsilon > 0$, there exists $N \in \mathbb N$
such that for all $m, n \geq N$, $|f_n(x)-f_m(x)| < \epsilon$ for all
$x \in S$.

#### Cauchy Sequences Converge Still

Suppose $(f_n)$ is uniformly Cauchy on $S$. Then there exists $f$ on $S$
such that $f_n$ converge to $f$ uniformly.

#### Weierstrass $M$-Test

Let $(M_k)$ be a sequence on nonnegative numbers such that
$\sum M_k < \infty$. If $|g_k(x)| < M_k$ for all $x$ in $S$, this series
converges uniformly on $S$.

#### Uniformly Convergence on Closed Radius

Let $\sum a_nx^n$ be a power series with radius of convergence $R$. Let
$0 < T < R$. Then $\sum a_nx^n$ converges uniformly on $[-T,T]$.
Furthermore, $\sum a_nx^n$ converges to a continuous function on
$(-R,R)$.

Riemann Integration
===================

#### Partition

Let a *partition* $P$ of an interval $D = [a,b]$ be a set
$P = \{x_0, x_1, \dots, x_n\}$ such that
$a = x_0 < x_1 < \dots < x_n = b$. We also define a sampling set of $P$
to be $P^* = \{x_1^*,x_2^*,\dots,x_n^*\}$ such that
$x_k \in [x_{k-1}, x_k]$.

#### Mesh

The *mesh* of a partition $P$, denoted $||P||$, be defined as
$$||P|| = \max\{x_k-x_{k-1}\}.$$

#### Riemann Integration

Let $f$ be a bounded function on $[a,b]$. Let $\epsilon > 0$. We say
that $f$ is *Riemann Integrable* if there exists $\delta > 0$ such that
for any partition $P$ and cooresponding sampling set $P^*$, if
$||P|| < \delta$ then
$$\left|\sum f(x^*_k)(x_k-x_{k-1}) - I\right| < \epsilon.$$

#### You can Integrate on Continuous Functions

Continuous are Riemann integrable.

#### Darboux Sum

Fix a partition $P=\{x_0,\dots,x_n\}$. Let
$M_k = \sup\{f(x):x\in[x_{k-1},x_k]\}$ and
$m_k = \inf\{f(x):x\in[x_{k-1},x_k]\}$. Then we define the *lower
Darboux sum* as $$\mathcal L(f,P) = \sum m_k(x_k-x_{k-1})$$ and define
the *upper Darboux sum* as $$\mathcal U(f,P) = \sum M_k(x_k-x_{k-1}).$$
If $R(f,P)$ is a Riemann sum then we know that
$$\mathcal L(f,P) \leq R(f,P) \leq \mathcal U(f,P).$$

#### Refinement

Let $Q$ and $P$ be partitions. We say that $Q$ is a refinement of $P$ if
$P \subseteq Q$.

#### Refinements on Partitions Tighten the Noose

If $Q$ is a refinement of $P$, then
$$\mathcal L(f,P) \leq \mathcal L(f,Q) \leq \mathcal U(f,Q) \leq \mathcal U(f,P).$$

#### Cauchy Criterian for Integral Existance

Let $f:[a,b]\rightarrow \mathbb R$. Suppose for every $\epsilon > 0$,
there exists $\delta > 0$ such that for any partition $P$ with
$||P|| < \delta$, $$\mathcal U(f,P)-\mathcal L(f,P) < \epsilon.$$ Then
$f$ is Riemann integrable on $[a,b]$.

#### Fundamental Theorem of Calculus

If $f(x)$ is Riemann integrable on $[a,b]$, then
$$A(x) = \int_a^xf(t)dt$$ is a uniformly continuous function on $[a,b]$.
Furthermore, if $f$ is also continuous at $x_0\in (a,b)$, then $A(x)$ id
differentiable at $x_0$ and $$\frac{d}{dx}A(x_0)=f(x_0).$$
