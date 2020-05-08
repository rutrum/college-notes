+++
title = "Rings and Fields Theory"
description = "rings, fields, integral domains, polynomials, cyclic polynomials, factorization"
+++

Symmetric Functions
===================

#### Polynomials in $F[x]$

Let $a_0, a_1, \dots, a_n$ live in set $F$ with $a_0 \neq 0$. Let $n$ be
a nonnegative integer. Then the function
$p: \mathbb C \rightarrow \mathbb C$ defined by
$$p(x) = a_0x^n + a_1x^{n-1} + \dots + a_n$$ is called a *polynomial
over $F$* with degree $n$. The set of all polynomials over $F$ is
denoted by $F[x]$

#### Root

A complex number $\alpha$ is called a *root* or a *zero* of a polynomial
$p(x)$ if $p(\alpha) = 0$.

#### Fundamental Theorem of Algebra

A polynomial of degree $n$ has exactly $n$ indistinct roots.

#### Factor Theorem

Let $p(x)$ have $n$ roots $\alpha_1, \dots, \alpha_n$, then for the
leading coefficient $a_0$
$$p(x) = a_0(x-\alpha_1)(x-\alpha_2)\dots(x-\alpha_n).$$

#### Symmetric Functions

The *symmetric functions* are functions that describe the roots of a
polynomial in terms of the coefficients of the polynomial and are as
follows. $$\begin{aligned}
        \sum_{1 \leq i \leq n}^n\alpha_i &= -\frac{a_1}{a_0} \\\\
        \sum_{i<j}\alpha_i\alpha_j &= \frac{a_2}{a_0} \\\\
        \sum_{i<j<k}\alpha_i\alpha_j\alpha_k &= -\frac{a_3}{a_0} \\\\
        &\vdots \\\\
        \alpha_1\alpha_2\dots\alpha_n &= -\frac{a_n}{a_0}
    \end{aligned}$$

Algebraic Numbers
-----------------

#### General Definition

Let $F \subset G$. A number *$a \in F$ is algebraic over $G$* if $a$ is
a root of a nonzero polynomial $p(x) \in G[x]$.

#### Algebraic Numbers

By convention, *algebraic numbers* will be those numbers
$a \in \mathbb C$ that are algebraic over $\mathbb Z$.

#### Transcendental Numbers

A number $\alpha \in \mathbb C$ is called *transcendental* if it is not
algebraic over $\mathbb Z$.

Ways to Find Roots of Polynomials Over the Integers
---------------------------------------------------

#### Rational Zeros Theorem

Let $f(x) = c_nx^n + c_{n-1}x^{n-1} + \dots + c_1x + c_0, c_n \neq 0$ be
polynomials with integer coefficients. If a rational number
$\frac{a}{b}$, in lowest terms, is a root of $f(x)$, then $a|c_0$ and
$b|c_n$.

#### Monic Polynomial

A polynomial is called *monic* if its leading coefficient is 1.

#### Zeros of Monic Polynomials

A rational zero of a monic polynomial with integer coefficients is an
integer.

#### Descartes' Rule of Signs

If the terms of a polynomial $p(x) \in \mathbb R[x]$ are arranged in the
descending order of the powers of $x$, then the number of positive roots
of $p(x)$ does not exceed the number of sign changes between consecutive
nonzero coefficients of $p(x)$. Similarly, the number of negative roots
of $p(x)$ is at most the number of sign changes between consecutive
nonzero coefficients of $p(-x)$.

#### Newton's Identities

For a polynomial $f(x) = a_0x^n + a_1x^{n-1} + \dots + a_n$ with roots
$\alpha_1, \alpha_2, \dots, \alpha_n$, then define
$$s_k = \alpha_1^k + \alpha_2^k + \dots + \alpha_n^k.$$ The following
statements are called *Newton's identities*. $$\begin{aligned}
        a_0s_k + a_1s_{k-1} + \dots + a_{k-1}s_1 + a_kk = 0 & \hspace{.5cm} \text{for } k \leq n \\\\
        a_0s_k + a_1s_{k-1} + \dots + a_ns_{k-n} = 0 & \hspace{.5cm} \text{for } k > n 
    \end{aligned}$$

Properties of the Integers
==========================

#### Well Ordered

Any nonempty subset of $\mathbb Z^+$ contains a smallest element.

#### Divides

For $a, b \in \mathbb Z$ with $b \neq 0$, we say $b$ *divides* $a$, $b$
*is a divisor of* $a$, or $a$ *is a multiple of* $b$ if there exists an
integer $k$ such that $a = kb$. We notate this as $b\ |\ a$.

#### Greatest Common Divisor

Define $(a, b)$ as the *greatest common divisor* of $a$ and $b$.

#### When GCD is Undefined

For integers $a$ and $b$, $(a,b)$ exists if and only if at least one of
$a$ and $b$ is not 0.

#### Relatively Prime

We say $a$ and $b$ are *relatively prime* when $(a, b) = 1$.

#### Division Algorithm

If $a$ and $b$ are integers and $b \neq 0$, then there exists unique
integers $q$ and $r$ such that $a = qb + r$ with $0 \leq r \leq |b|$. We
give $a, q, b, r$ the names *dividend*, *quotient*, *divisor*, and
*remainder* respectively. This can be abstracted to not just the
integers but any integral domain.

#### GCD of Remainder

For $a, b, r$ as defined in the division algorithm, then
$(a, b) = (b, r)$.

#### Euclidean Algorithm

If $r_0, r_1 \in \mathbb Z^+$ and if $r_0 > r_1$, then there exists two
unique sets of positive integers $q_1, q_2, \dots, q_n$ and
$r_2, r_3, \dots, r_n$ such that

1.  $r_0 > r_1 > r_2 > \dots > r_{n-1} > r_n > 0$

2.  $r_{i-1} = q_ir_i + r_{i+1}$ for $1 \leq i \leq n-1$

3.  $r_{n-1} = q_nr_n$

4.  $(r_0,r_1) = r_n$

Furthermore, there exist integers $x, y$ such that
$r_n = x \cdot r_0 + y \cdot r_1$.

#### Bézout's Lemma

Let $a$ and $b$ be integers with $b \neq 0$. Then $(a, b)$ is the
smallest of the positive elements of the set
$L = \\{ax + by:x,y \in \mathbb Z\\}$.

#### Specific Case of the Above

Let $(a,b) = 1$ if and only if there exists $x$ and $y$ for which
$ax + by = 1$.

#### Relatively Prime and Divides

If $a\ |\ bc$ and $(a,b) = 1$, then $a\ |\ c$.

#### Divides and Relatively Prime

If $a\ |\ c$ and $b\ |\ c$ and if $(a, b) = 1$, then $ab\ |\ c$.

#### Fundamental Theorem of Arithmetic

Any positive integer $n$ can be uniquely expressed as
$n = p_1^{k_1}p_2^{k_2}p_3^{k_3}\dots p_m^{k_m}$ where $p_i$ are
distinct primes and $k_i$ are positive integers.

#### Euler's Phi Function

Define $\phi:\mathbb Z^+ \rightarrow Z^+$ as follows: $\phi(1) = 1$, and
$n > 1$, then $\phi(n)$ is the number of positive integers less than $n$
that are relatively prime to $n$.

#### Properties of $\phi$

Using the following properties, $phi(n)$ can be calculated given that
the prime power factorization of $n$ is known.

1.  $\phi(1) = 1$

2.  If $a, b \in Z^+$ and if $(a, b) = 1$, then
    $\phi(ab) = \phi(a)\phi(b)$.

3.  For any prime $p$ and positive integer $k$, then
    $\phi(p^k) = p^k - p^{k-1}$.

#### Number of Divisors

Suppose $n = \Pi p_i^{k_i}$, then the number of positive integer
divisors of $n$, denoted $\delta(n)$, is the following.
$$\delta(n) = \displaystyle \prod(k_i + 1)$$

Algebraic Structures
====================

Groups
------

#### Group Axioms

A group is a set $G$ and a binary operation denoted by $\circ$ such that
the following are true.

1.  *Closure*: $a, b \in G \implies a \circ b \in G$.

2.  *Associativity*:
    $a, b, c \in G \implies (a \circ b) \circ c = a \circ (b \circ c)$.

3.  *Identity*: There exists $e \in G$ such that
    $a \circ e = e \circ a = a$ for all $a \in G$.

4.  *Inverses*: For each $a \in G$ there exists $a\inv \in G$ such that
    $a \circ a\inv = a\inv \circ a = e$.

#### Abelian Group

A group is called *abelian* if the binary operation is *commutative*:
$a, b \in G \implies a \circ b = b \circ a$.

#### Order

The *order of a group* is the number of elements in the group. The
*order of an element*, say $a$, is the smallest positive integer $n$
such that $a^n = e$. If no such positive integer exists, we say the
element $a$ has *infinite order*.

#### Subgroup

A subset $H$ of a group $G$ is called a *subgroup of $G$* if $H$ is a
group under the operation by which $G$ is a group.

#### Cosets

Let $H \leq G$. Define the *right coset* of $H$ in $G$ as the set
$Hx = \\{hx:x\in H\\}$. The set of all right cosets of $H$ in $G$ is
denoted as $G/H$.

#### Cosets Partition the Subgroup

For $x,y\in G$, the right cosets $Hx$ and $Hy$ are either disjoint or
identical.

#### Bijection of Cosets

If $g_1, g_2 \in G$, then there exists a function on $G$ that sends
$x \mapsto g_2g_1\inv x$ is a permutation of $G$ that maps $Hg_1$ to
$Hg_2$. Thus, $|Hg_1| = |Hg_2|$.

#### LaGrange Theorem

Let $H$ be a subgroup of $G$, then $|G| = |H| \cdot |G/H|$.

#### Index

The *index* of $H$ in $G$ is $|G/H|$.

#### Normal Subgroup

A subgroup $H$ of $G$ is called a *normal subgroup* of $G$, denoted
$H \triangleleft G$, if $ghg\inv \in H$ for all $g \in G$ and for all
$h \in H$. We say that $H$ is closed under conjugation by the elements
in $G$.

#### Functions Between Groups

Let $G_1$ and $G_2$ be groups with identity elements $e_1$ and $e_2$
respectively. A function $f: G_1 \rightarrow G_2$ is called a *group
homomorphism* if $f(ab) = f(a)f(b)$ for $a, b$. A one-to-one
homomorphism is called a *monomorphism*. An onto homomorphism is called
a *epimorphism*. A one-to-one and onto homomorphism is called an
*isomorphism*.

$f(ab)=f(a)f(b)$ | Not 1-1 | 1-1
--- | --- | ---
Not Onto | Homomorphism | Monomorphism
Onto | Epimorphism | Isomorphism

#### Image and Kernal

Let $f: G_1 \rightarrow G_2$ be a homomorphism. Then the *image* of
$G_1$: $f(G_1) = \\{f(x): x\in G\\}$ is a subgroup of $G_2$. It also
follows that the *kernal* of $f$:
$\text{ker} f = \\{x \in G_1: f(x) = e_2\\}$ is a normal subgroup of
$G_1$.

#### Pointwise Product

Define the *pointwise product* of two subset $A$ and $B$ of a group $G$
by $A \cdot B = \\{ab: a \in A, b\in B\\}$.

#### Normality and Cosets

Let $H \triangleleft G$. Then for any $x,y \in G$, $Hx = xH$ and
$Hx \cdot Hy = Hxy$.

#### First Homomorphism Theorem

Let $G_1, G_2$ be groups and let $f: G_1 \rightarrow G_2$ be an onto
homomorphism with kernal $K$. Then $G_2$ is isomorphic to $G_1/K$.

#### Permutation Group

Define $S(X)$ as the set of all permutations of elements in set $S$. Let
$S_n$ be the set of all permutations of elements in the set
$\\{1,2,3,\dots,n\\}$. We call $S_n$ the *symmetric group of degree $n$*.

#### Alternating Group

Define $A_n$, called the *alternating group*, as the set of all even
permutations of $S_n$. Note that $A_n$ is normal in $S_n$.

#### Conjugacy

An element $a \in G$ is said to be a *conjugate* in $G$ of an element
$b$ if there exists an $x \in G$ such that $a = xbx\inv$.

#### Conjugacy Classes

Conjugacy is an equivalence relation on $G$, and thus, the action
partitions the group $G$ into *conjugacy classes*.

#### Conjugacy of Permutations

For two elements $a, b \in S_n$, $a$ and $b$ are in the same conjugacy
class if and only if they have the same cycle decomposition. It follows
that the number of conjugacy classes in $S_n$ equals the number of
partitions of $n$.

Rings
-----

#### Ring Axioms

A set $R$ with two operations defined on it called addition and
multiplication (denoted by $+$ and $\cdot$ respectively) is called a
ring if the following are true.

1.  $R$ is an abelian group under addition.

2.  $R$ is closed and is associative under multiplication

3.  The distributive laws hold: $a(b+c) = ab+ac$ and $(a+b)c = ac + bc$.

#### Commutative Ring

A ring $R$ is called *commutative* if multiplication on $R$ is
commutative: $ab = ba$.

#### Identities

Rings have a additive identity that follows from being a group under
addition. We denoted this identity as 0. Rings do not necessarily have
an identity under multiplication, a value $u \neq 0$ such that
$u \cdot x = x$ for all $x \in R$. If they do, we denote that identity
as the unity, or 1.

#### Subring

A subset $T$ of ring $R$ is called a *subring* if $T$ is a ring under
the operations defined on $R$.

#### Ideal

A subring $T$ of $R$ is called an *ideal* if for all $x \in R$ and
$t \in T$, then $xt \in T$.

#### Smallest Ideal

The smallest ideal of $R$ containing a given subset $A$ of $R$ is
denoted by $(A)$.

#### Principle Ideal

The ideal generated by a single element $a \in R$ is denoted by $(a)$ is
called a *princicple ideal* in $R$.

#### Maximal Ideal

An ideal $I$ of $R$ is called a *maximal ideal* of $R$ if $I \subset R$
and there is no ideal $J$ of $R$ such that $I \subset J \subset R$.

#### Ring Homomorphisms

Let $R_1$ and $R_2$ be commutative rings. A function
$f: R_1 \rightarrow R_2$ is called a ring homomorphism if $a, b \in R_1$
implies that $f(a+b) = f(a) + f(b)$ and $f(ab) = f(a)f(b)$. Similar
terms for group homomorphisms are analagous here.

#### Kernal

Kernals of rings are defined similarly.

#### First Isomorphism Theorem for Rings

Let $R$ and $S$ be rings and let $f:R\rightarrow S$ be an onto ring
homomorphism with kernal $K$. Then $R/K$ is isomorphic to $S$.

#### Useful Factorings On Rings

Let $a, b$ be elements in ring $R$. Then the following statements hold
for $n \in \mathbb N$. $$\begin{aligned}
            (a+b)^n &= \sum_{k=0}^n \binom{n}{k}a^{n-k}b^k \\\\
            a^n-b^n &= (a-b)\sum_{k=0}^{n-1}a^{n-1-k}b^k \\\\
            a^n+b^n &= (a+b)\sum_{k=0}^{n-1}(-1)^ka^{n-1-k}b^k &\text{if $n$ is odd} 
        \end{aligned}$$

Fields
------

#### Field Axioms

A field $F$ is a commutative ring with unity (identity under
multiplication) in which the nonzero elements form a group under
multiplication.

#### Subfield

A subset $S$ of field $F$ is called a *subfield* of $F$ it is a field
under the operations on $F$.

#### Prime Subfield

The intersections of all subfields is called the *prime subfield* of
$F$, the smallest subfield of $F$.

#### Automorphism

A one-to-one function $g$ from a field $F$ onto $F$ is called an
*automorphism* of $F$ if is a one-to-one ring homomorphism of $F$ onto
itself.

Integral Domains
----------------

#### Definition

An *integral domain* $D$ is a commutative ring with at least two
elements such that $x,y \in D$ and $xy = 0$, then $x = 0$ or $y = 0$.

#### Gaussian Integers

Define the *guassian integers* as the set
$\\{a + ib: a, b \in \mathbb Z\\}$.

#### Zero Divisor

An element $x$ of a commutative ring $R$ is called a *zero divisor* in
$R$ if $x \neq 0$ and if there is a nonzero $y \in R$ for which
$xy = 0$.

#### Fields are Integral Domains

All fields are integral domains. Not all integral domains are fields.

#### Characteristic

The *characteristic* of an integral domain $S$ is the smallest positive
integer $m$ such that
$\underbrace{x + x + \dots + x}_\text{$m$ times} = m \cdot x = 0$ for
all $x \in S$. If no such positive integer exists, the characteristic of
$S$ is defined to be 0.

#### Characteristics are Prime

The characteristic of an integral domain must either be 0 or prime.

Summary of Algebraic Structures
-------------------------------

$$\begin{aligned}
        \text{Groups} &\subset \text{Abelian Groups} \\\\
        &\subset \text{Rings} \\\\
        &\subset \text{Commutative Rings} \\\\
        &\subset \text{Integral Domains} \\\\
        &\subset \text{Fields} \\\\
        \end{aligned}$$

Integral Domains with Unity
===========================

#### Unit

A *unit* is an element that has a multiplicative inverse.

#### Associates

Two elements $a, b \in D$ are called *associates* in $D$ if there exists
a unit $u \in D$ such that $a = bu$.

#### Divides on a Domain

The relation $a | b$ between elements in $D$ have the following
properties:

1.  If $a|b$ and $b|c$, then $a | c$.

2.  If $a|b$ and $a|c$, then $a | (b \pm c)$.

3.  If $a|b$, then $a|bx$ for all $x \in D$

#### Greatest Common Divisor

An element $d$ is called the *greatest common divisor* of $a$ and $b$ if
for any element that divides $a$ and $b$, it also divides $d$.

#### Partitioning Integral Domains with Unity

Partition an integral domain $D$ into three groups:

1.  $\\{0\\}$

2.  Units in $D$

3.  All other elements denoted $\hat D$.

#### Reducible

An element $a \in D$ is said to be *reducible* in $D$ if $a \in \hat D$
and if there exists $b, c \in \hat D$ such that $a = bc$. Element
$a \in D$ is said to be *irreducible* if it is not reducible.

#### Prime

Element $x \in D$ is called *prime in $D$* if for any $y, z \in S$ such
that $x|yz$, then either $x|y$ or $x|z$.

#### Unique Factorization Domain

Domain $D$ is called a *unique factorization domain* or *UFD* if any
$x \in \hat D$ can be written as the finite product of irreducible
elements that are unique up to associates.

#### Multiplicative Norm

A function $\eta: D \rightarrow \mathbb Z$ is called a *multiplicative
norm* on $D$ if the following conditions are satisfied for $x, y \in D$.

1.  $\eta(x) \geq 0$

2.  $\eta(x) = 0$ if and only if $x = 0$

3.  $\eta(xy) = \eta(x)\eta(y)$

#### Norm of Unity is 1

$\eta(1) = 1$.

#### Norms of Associates

If $x$ and $y$ are associates then $\eta(x) = \eta(y)$.

#### Some Elements Aren't Just Irreducible

A prime element of an integral domain $D$ is irreducible.

#### Irreducibles of UFDs

Every irreducible element of a unique factorization domain is prime.

#### Principle Ideal Domain

An integral domain is called a *principal ideal domain* if any ideal of
the domain is a principal ideal.

Field Extensions
================

#### Definition

Let $K$ be a subfield of $L$. Then we say that $L$ *is an extension of*
$K$, and is notated as $L : K$.

#### Degree

If $L : K$, then $L$ is a vector space over $K$ and its dimension over
$K$, denoted as $[L : K]$, is called the *degree* of $L$ over $K$. If
the degree is finite, we call $L$ is a *finite extension*.

#### Extension on a Field

We define $F(A)$ for a field $F$ to be the set of all elements in $F$,
the set of all elements in $A$, and all the elements forced by their
union. If $A$ is a single element, we say that $F(A)$ is a *simple
extension*.

#### Simple and Finite Extentions

It turns out that every finite extension is a simple extension. But note
that not every simple extension is finite, for example: $Q(\pi)$.

#### Tower Law

Suppose $M : L$ and $L : K$ are finite field extensions. Then
$$[M:K]=[M:L]\cdot[L:K].$$

#### Extended Tower Law

The tower law can be extended to any number of field extensions. The
sequences of field extensions is called a *tower* of field extensions.

#### Algebraic Degree

An element $a \in L$ is said to be *algebraic of degree $n$* over $K$ if
there is a polynomial $p(x)$ in $K[x]$ of degree $n$ such that
$p(a) = 0$, and if no nonzero polynomial of lower degree in $K[x]$ has
this property.

#### Minimial Polynomial

If $p(x)$ is a monic with the above property, then it is called the
*minimal polynomial* for $\alpha$ over $K$.

#### Transcendental

If no polynomial $p(x)$ exists for such $a$, then we said that $a$ is
*transcendental* over $K$.

Tests for Irreducibility
========================

#### Important Facts Before We Start

-   The set $D[x]$ of the polynomials over $D$ is itself an integral
    domain.

-   The set of units of $D[x]$ is the same as that of $D$.

-   If $D$ is a UFD, then so is $D[x]$.

-   If $F$ is a field, then the set of irreducible polynomials in $F[x]$
    contains all the first degree polynomials in $F[x]$.

#### A Word on Irreducibility

Note that determining if a given polynomial is irreducible depends on
the polynomial domain in which it is being considered.

#### Primitive

A nonzero polynomial in $Z[x]$ is called *primitive* if the greatest
common divisor of its coefficients is $1$.

#### Product of Primitives

The product of two primitive polynomials is primitive.

#### One More Fact

A primitive polynomial is reducible over $\mathbb Z$ if and only if a
constant multiple of that polynomial is reducible over $\mathbb Q$.

#### Gauss's Lemma

If a primitive polynomial can be factored as a product of two
polynomials having rational coefficients, then it can be factored as a
product of two polynomials with integer coefficients.

#### The Eisenstein Criterian

If a prime divides all non-leading coefficients of a polynomial, does
not divide the leading coefficient, and the square of the prime does not
divide the constant term, then the polynomial is irreducible over the
rationals.

#### Another Fact

A polynomial of the form $x^{p-1} + x^{p-2} + \dots + x + 1$ for some
prime $p$ is irreducible over $\mathbb Z$.

Constructable Numbers
=====================

#### Definition

Suppose we are given a straight-edge, a compass, and two distinct points
$A$ and $B$ whose distance we call *unit length*. We call a real number
$\alpha$ constructable if one can construct a line segment of length
$|\alpha|$ in a finite number of steps from unit length using only a
straight-edge and compass.

#### Constructable Point

We call point $(a,b)$ in the Euclidean plane a *constructable point* if
and only if $|a|$ and $|b|$ are constructable numbers.

#### It's a Field

The constructable numbers form a field that contains $\mathbb Q$ as a
subfield.

#### It's Not Just Rationals

If $\alpha$ is constructable, then so is $\sqrt{|\alpha|}$.

#### But Not All Reals

Cube roots are not constructable. Geometrically, this means you cannot
trisect an angle.

Splitting Fields
================

#### Split

Let $L:K$ be an extension. A polynomial $f(x) \in K[x]$ is said to split
over $L$ if we can write $f(x) = a(x-\alpha_1)\dots(x-\alpha_n)$ where
$a\in K$ and $\alpha_i \in L$. Then $L:K$ is called a *splitting field
extension* for $f$ if $f$ splits over $L$ and if there exists no proper
subfield of $L$ containing $K$ such that $f$ splits over that subfield.

#### The Exact Extension

Suppose $L:K$ is an extension and $f \in K[x]$ splits over $L$ as
$f(x) = a(x-\alpha_1)\dots(x-\alpha_n)$. Then
$K(\alpha_1, \dots, \alpha_n)$ is a splitting field extension for
$f(x)$.

#### Simple Extensions Mean Reducible

Suppose $f \in K[x]$ is irreducible of degree $n \geq 1$. Then there
exists a simple algebraic extension $K(\alpha) : K$ such that
$[K(\alpha):K] = n$ and $f(\alpha) = 0$ for some $\alpha = L$.

#### Random Fact From Notes

For any prime $p$, there exists a field of order $p^n$ for any
$n \in \mathbb N$.

Roots of Unity and Cyclotomic Polynomials
=========================================

#### Roots of Unity

Let $p(x) = x^n - 1$. Applying De Moivre's Theorem we find the complex
roots to $p(x)$ to be
$$\frac{\cos 2k\pi}{n} + \frac{i\sin 2k\pi}{n} = \exp{\frac{2\pi ik}{n}}, 1 \leq k \leq n.$$
We can write these roots as $a, a^2, a^3, \dots, a^{n-1}, a^n = 1$ for
$a = \exp{\frac{2\pi ik}{n}}$.

#### Roots Make Group

The roots of unity form a cyclic group $C_n$ of order $n$. One can
partition $C_n$ into $\delta(n)$ classes, where two elements are the in
same class if and only if they have the same order in $C_n$.

#### Cyclotomic Polynomials

The $n^{th}$ cyclotomic polynomial $\Phi_n(x)$ is defined as
$$\Phi_n(x) = \prod_\epsilon (x-\alpha)$$ where the product is taken
over all primitive $n^{th}$ roots of unity. As a consequence of
partitioning $C_n$, it follows that $$x^n-1 = \prod_{m|n}\Phi_m(x).$$

Galois Group of a Polynomial
============================

#### Set of Automorphisms

Let $L : K$ be a field extension and let $\Gamma(L:K)$ denote the set of
all automorphisms $\sigma$ of $L$ such that for all $x \in K$,
$\sigma(x) = x$. In other words, all the automorphism of $L$ that fix
elements of $K$.

#### Galois Group

The set $\Gamma(L:K)$ is a group under function composition. We call
this the Galois group of $L:K$.

#### Mapping Galois Groups to Fields

Define $\phi$ to be a function that associates each subgroups $H$ of
$\Gamma(L:K)$ to a subfield $\phi(H)$ defined by
$$\phi(H) = \\{y \in L: h(y) = y \text{ for } h \in H\\}.$$ This is called
the *fixed field* of $H$.

#### Mapping Fields to Galois Groups

Define $\gamma$ to be a function that associates each field $M$ that is
intermediate between $K$ and $L$ to a subgroup $\gamma(M)$ of
$\Gamma(L:K)$ defined by
$$\gamma(M) = \\{\sigma \in \Gamma(L:K) : \sigma(m) = m \text{ for all } m \in M\\}.$$

#### Normal Extension

Field $L$ is called a *normal extension* of $K$ if it is a finite
extension of $K$ and if $K$ is the fixed field of $\Gamma(L:K)$.

#### Seperable

An element $a \in L$ is called *seperable* over $K$ if it is a root of a
polynomial over $K$ with no multiple roots. An extension $L$ of $K$ is
called seperable over $K$ if all its elements are seperable over $K$.

#### Galois Group of a Polynomial

Let $f \in K[x]$ and $L:K$ be a splitting field extension for $f$ over
$K$. Then $\Gamma(L:K)$ is called the Galois group of $f$ and it is
denoted $\Gamma_K(f)$.

#### Fundamental Theorem of Galois Theory

Suppose that $K$ is a field of characteristic $0$ or a finite field and
that $L$ is the splitting field of some polynomial $p(x) \in K[x]$. Then

1.  The map $\phi$ is a one-to-one correspondence of the set of
    subgroups of $\Gamma(L,K)$ and the subfields of $L$ which contain
    $K$. Furthermore, $\gamma$ is its inverse.

2.  $[L:M] = |\Gamma(L:M)|$

3.  $M$ is a normal extension of $K$ if and only if $\Gamma(L,M)$ is a
    normal subgroup of $\Gamma(L,K)$.

Solving a Polynomial By Radicals
================================

Some Notable Groups
-------------------

#### Commutator

An element $x$ in $G$ is said to be a commutator in $G$ if
$x = aba\inv b\inv$ for $a,b \in G$.

#### Derived Subgroup

The subgroup generated by all commutators of $G$ is called the derived
subgroup of $G$ and is notated as $G'$. Note that $G'$ is normal in $G$.
Note that the product of two commutators is not always a commutator.

#### Abelian Normal Subgroups Contain Commutators

If $K \triangleleft G$, then $G/K$ is abelian if and only if $K$
contains $G'$.

#### Derived Subgroup is Normal Too

If $H \triangleleft G$, then $H' \triangleleft G$.

#### Chaining Derivated Subgroups

Define $G' = G^{(1)}$, then $(G^{(k-1)})' = G^{(k)}$.

#### Prime and Finite means Simple

Any finite group of prime order is simple.

#### Alternating Group

Remember that $A_n$ is simple for $n \geq 5$.

Solvable
--------

#### Soluble

A group $G$ is said to be solvable or soluble if there exists a finite
series of subgroups
$$G=G_0 \triangleright G_1 \triangleright \dots \triangleright G_n = \\{e\\}$$
such that $G_{i-1}/G_i$ is cyclic.

#### Radicals

Let $L:K$ be an extension. An element $\alpha \in L$ is called a
*radical over* $K$ if $\alpha^n \in K$ for some positive integer $n$.
Extension $L:K$ is said to be an *extension by radicals* if there are
intermediate fields $$L=L_m:L_{m-1}:\dots:L_0=K$$ such that
$L_i=L_{i-1}(\alpha_i)$ with $\alpha_i$ a radical over $L_{i-1}$.

#### Polynomial Solvability

A polynomial $f(x) \in K[x]$ is said to be *solvable by radicals* if
there is an extension $L:K$ by radicals such that $f(x)$ splits over
$L$. Note that $L$ could be larger than the splitting field of $f$.

#### Three-Cycles are Special

Let $G=S_n$ where $n \geq 5$. Then $G^{(k)}$ for $k \in \mathbb N$
contains every $3$-cycle of $S_n$.

#### Subgroups of Solvable Groups are Solvable

If $G$ is solvable, then so is every subgroup of $G$.

#### Like the Alternating Group\...

Group $S_n$ is not soluable for $n \geq 5$.

#### Galois Group of an Irreducible

Suppose $p(x) \in \mathbb Q[x]$ is irreducible of prime degree $p$ such
that $p(x)$ has exactly two nonreal roots in $\mathbb C$. Then the
Galois group of $p(x)$ over $\mathbb Q$ is $S_p$.

#### The general polynomial of degree $n \geq 5$ is not solvable by radicals.

Finite Fields
=============

#### Prime Field

A field $K$ is called a *prime field* if it has no proper subfield.

#### Isomorphisms

For a field $K$, the prime field of $K$ is either isomorphic to
$\mathbb Q$ or to $\mathbb Z_p$.

#### Finite Fields have Prime Characteristic

If $F$ is a finite field, then the characteristic of $F$ is a prime
number $p$, and thus $F$ contains $\mathbb Z_p$ and it consists of $p^n$
elements.

#### No Zero Means Cyclic

If $F$ is a finite field, then the multiplicative subgroup $F^*$ of
nonzero elements of $F$ is cyclic.

#### Small Degree Roots Mean Irreducible

Let $f(x) \in K[x]$ be a polynomial of degree $2$ or $3$. Then $f(x)$ is
reducible over $K$ if and only if $f(x)$ has a root in $K$.

#### Prime Power Cardinality

If $F$ is a finite field, then its order is $p^n$ for prime $p$. This
field is also unique for every pair of $n$ and $p$.
