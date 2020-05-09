+++
title = "Algorithms"
description = "run-time analysis, greedy algorithms, tree searching, divide and conquer, dynamic programming" 
+++

Order
=====

Order Notation
--------------

#### Big-Oh Notation

For a given complexity function $f(n)$, define $O(f(n))$ as the set of
complexity functions $g(n)$ such that there exists constants $c > 0$ and
$N \in \mathbb Z^+$ such that $\forall n \geq N$,
$g(n) \leq c \cdot f(n)$.

#### Little-oh Notation

For a given complexity function $f(n)$, define $O(f(n))$ as the set of
complexity functions $g(n)$ such that there exists constants $c > 0$ and
$N \in \mathbb Z^+$ such that $\forall n \geq N$, $g(n) < c \cdot f(n)$.

#### Big-Omega Notation

For a given complexity function $f(n)$, define $O(f(n))$ as the set of
complexity functions $g(n)$ such that there exists constants $c > 0$ and
$N \in \mathbb Z^+$ such that $\forall n \geq N$,
$g(n) \geq c \cdot f(n)$.

#### Little-omega Notation

For a given complexity function $f(n)$, define $O(f(n))$ as the set of
complexity functions $g(n)$ such that there exists constants $c > 0$ and
$N \in \mathbb Z^+$ such that $\forall n \geq N$, $g(n) > c \cdot f(n)$.

#### Theta Notation

For a given complexity function $f(n)$, define $O(f(n))$ as the set of
complexity functions $g(n)$ such that there exists constants
$d \geq c > 0$ and $N \in \mathbb Z^+$ such that $\forall n \geq N$,
$c \cdot f(n) \leq g(n) \leq d \cdot f(n)$.

Notation Table
--------------

Name | Notation | Idea
--- | --- | ---
big-Oh | $g(n) \in O(f(n))$        | $g(n) \leq c \cdot f(n)$
little-oh | $g(n) \in o(f(n))$        | $g(n) < c \cdot f(n)$
big-Omega | $g(n) \in \Omega(f(n))$   | $g(n) \geq c \cdot f(n)$
little-omega | $g(n) \in \omega(f(n))$   | $g(n) > c \cdot f(n)$
theta | $g(n) \in \Theta(f(n))$   | $c \cdot f(n) \leq g(n) \leq d \cdot f(n)$

Rules of Order
--------------

#### Oh and Omega are Inverses

$g(n) \in O(f(n)) \Leftrightarrow f(n) \in \Omega(g(n))$

#### Theta and Theta are Inverses

$g(n) \in \Theta(f(n)) \Leftrightarrow f(n) \in \Theta(g(n))$

#### Bases of Logs are Constants

For any $a, b > 1$, $\log_an \in \Theta(\log_bn)$.

#### Bases of Exponents are Not

For any $0 < a < b$, $a^n \in o(b^n)$.

#### Factorials Grow Fast

For any $a > 0$, $a^n \in o(n!)$.

Techniques For Determining Complexity
-------------------------------------

#### Limit of Quotient

$$\lim_{n\rightarrow\infty} \frac{g(n)}{f(n)}=
        \begin{cases} 
            0 & \implies g(n) \in o(f(n)) \\
            \infty & \implies g(n) \in \omega(f(n)) \\
            c>0 & \implies g(n) \in \Theta(f(n))
        \end{cases}$$

#### L'Hopital's Rule

You can invoke L'Hopital's rule only if

-   $f(n)$ and $g(n)$ are both differentiable

-   $\displaystyle \lim_{n\rightarrow\infty}f(n) = \lim_{n\rightarrow\infty}g(n) = \infty$

-   $\displaystyle \lim_{n\rightarrow\infty^+} \frac{g(n)}{f(n)}$ exists

L'Hopital's rule can be used to simplify the limit of a ratio, and is as
follows:
$$\lim_{n\rightarrow\infty} \frac{g(n)}{f(n)}=\lim_{n\rightarrow\infty} \frac{g'(n)}{f'(n)}$$

Master Theorem
--------------

#### Definition

Give a recurrence relation of the form $$\begin{aligned}
        T(n) &= a\cdot T\left(\frac{n}{b}\right) + c\cdot n^k \\\\
        T(1) &= d
        \end{aligned}$$ where $n > 1$, $n$ is multiple of $b$,
$b \geq 2$, $a > 0$, $c > 0$, and $d \geq 0$, then the following is
true. $$T(n) \in \begin{cases}
        \Theta(n^k) &\text{if } \log_ba < k \\\\
        \Theta(n^k\log n) &\text{if } \log_ba = k \\\\
        \Theta(n^{\log_ba}) &\text{if } \log_ba > k 
        \end{cases}$$

Summations
----------

#### Arithmetic Series

$$\sum_{i=1}^n i^d = \Theta(n^{d+1})$$

#### Geometric Series

$$\sum_{i=1}^n i^dx^i = \frac{x^{n+1}-1}{x-1} = \Theta(x^n)$$

#### Harmonic Series

$$\sum_{i=1}^n i^d\frac{1}{n} = \Theta(\log n)$$

Greedy Algorithms
=================

#### Paradigm for Algorithms

1.  Idea/intuition

2.  Pseudocode

3.  Real code

4.  Evaluate experimental runtime

5.  Prove running time

6.  Proof of correctness

#### Coin Change Problem

Given so much change to return, how can you minimize the number of coins
to be given.

#### Paradigm for Greedy Algorithms

1.  Examine all immediate options

2.  Select best option

3.  Update solution

4.  Confirm if complete

#### Union-Find Data Structure

The *union-find data structure*, or simply *UFDS*, is defined with the
following functions.

Function | Runtime | About
--- | --- | ---
    `initialize(n)`|$O(n)$      | creates $n$ disjoint sets, each with a single element
          `find(i)`|$O(\log n)$ | returns a pointer $p$ to the subset containing element $i$
       `union(p,q)`|$O(\log n)$ | returns a pointer $r$ to a new subset that merges the subsets pointed to by $p$ and $q$ and then destroys $p$ and $q$
       `equal(i,j)`|$O(\log n)$ | returns `find(i) == find(j)`

Data Compression
----------------

#### Fixed Length Compression

Given a string of characters (which take a byte of data for every
character) can be compressed into fewer bits by representing each
character by a smaller number of bits. Fixed length compression ensures
that these replacement bit patterns, called *prefix codes*, are of the
same length.

#### Variable Length Compression

The replacement bit patterns can also be done in different lengths. To
ensure that the string can be decoded unambiguously, a specific set of
prefix codes must be chosen.

#### Prefix Tree

Prefix codes can be represented as a *prefix tree*. When no one bit
pattern is the subset of another (on the tree) then the prefix codes
represent compression that can be decoded.

#### Optimal Compression

A problem that can be solved: find the optimal prefix code to represent
a given string $T$ composed of symbols from alphabet $A$. In this case,
"optimal" means to produce an encoding that minimizes the number of
bits. This can be solved using *Huffman's Algorithm*.

Divide and Conquer
==================

#### Paradigm

1.  Divide the problem into smaller versions of the same problem.

2.  Conquer (or solve) the problem.

    1.  By applying a base case.

    2.  Using recursion.

3.  Rejoin the solutions (if necessary).

#### Guessing Game

Find out a unique number that was drawn between the numbers $1$ and $n$
inclusive.

#### Dynamic Programming

Often times recursion will involve solving the same subproblem multiple
times. To avoid this, we solve each subproblem first, but only once.
This process is called *memoizing* and is what we call dynamic
programming.

Backtracking
============

#### Depth First Search

That's all it is. Try every option, period.

#### Pruning

We can do better though. We can set a condition for which we know that
no leaf of the tree will have a more optimal solution than one we have
already found. This will cut down on checking every possible node.

Branch and Bound
================

#### Best First Search

Just don't always pick the left child to expand. You can select any
unexpanded node in a more meaningful way. This is called "best first
search".

Computational Complexity and Intractibility
===========================================

#### Polynomial-Time Algorithm

If $n$ is the input size, there exists some polynomial $p(n)$ such that
$T(n) \in O(p(n))$.

#### Intractable Problem

A problem that is known to have no polynomial time algorithm to solve is
called *intractable*.

#### Categories of Problems

1.  Problems for which polynomial-time algorithms have been found.

2.  Problems that are provably intractable.

    1.  Unreasonable problems (where the output size is unreasonable)

    2.  Reasonable problems (such as Halting problem)

3.  Problems that have not been proven to be intractable, but for which
    no polynomial-time algorithm has ever been found.

Some Problems
-------------

#### Traveling Salesperson Problem (TSP)

Let $G$ be a weighted directed graph. A tour in $G$ is a path that
starts at a vertex $a$ and visits all other vertices exactly once and
ends at vertex $a$.

` ` | ` `
--- | ---
    Optimization|Find the tour with the lowest overall weight.
        Decision|Let $D$ be some constant. Is there a tour with total weight less than $D$?

#### Graph Coloring Problem

Let $G$ be a graph. Each vertex may be assigned a color. The goal is to
color the graph in such a way that no two adjacent vertices have the
same color.

` ` | ` `
--- | ---
    Optimization|What's the smallest number of colors needed to color the graph?
        Decision|Let $m$ be some constant. Is there a coloring that uses less than $m$ colors?

#### Clique Problem

Let $G=(V,E)$ be an undirected graph. A clique is a subset
$W \subseteq V$ such that each vertex $v \in W$ is adjacent to every
other vertex in $W$.

` ` | ` `
--- | ---
    Optimization|Find the largest subset $W \subseteq V$. Set $W$ is called the maximal clique.
        Decision|Let $k$ be some constant. Is there a maximal clique with cardinality of at least $k$?

#### Conjuctive Normal Form Satisfiablility Problem

CNF is also known as SAT or 3-SAT. Let $x_1, \dots, x_n$ be boolean
statments. A *literal* is either a variable or its negation. A *clause*
is a sequence of literals seperated by 'or' operators. Then *conjuctive
normal form* is a sequence of clauses seperated by 'and' operators.

` ` | ` `
--- | ---
    Decision|Is there an assignment for the boolean variables such that the CNS is true?

Types of Algorithms
-------------------

#### Polynomial-time Verification Algorithm

An algorithm that can verify the correctness of a proposed solution in
polynomial time.

#### Non-Deterministic Algorithm

An algorithm that involves blind guessing or randomness to create a
solution and then tries to verify that answer. These are used to solve
decision problems only.

#### Poly-Time Non-Deterministic Algorithm

Any non-deterministic algorithm where the verification stage takes
polynomial time.

#### Polynomial Time Reduction

If there is a polynomial time transformation algorithm that translates
problem $A$ into an instance of problem $B$, we call that algorithm a
*poly-time reduction*. We write this is $A \leq_p B$ for algorithm $p$.

Sets of Problems
----------------

#### P

The set *P* is the set of decision problems that can be solved using a
polynomial time algorithm.

#### NP

The set *NP* is the set of decision problems that can be solved with a
nondeterministic polytime algorithm.

#### NP-Complete

A problem $B$ is called *NP-Complete* if the following are true.

1.  $B \in \mathit{NP}$

2.  For every other problem $A$ in $\mathit{NP}$, $A$ is polynomial time
    reducible to $B$. In other words, $A \leq_p B$.

#### Another NP-Complete Definition

A problem $C$ is called *NP-Complete* if the following are true.

1.  $C \in \mathit{NP}$

2.  For some other $\mathit{NP}$-complete problem $B$, $B \leq_p C$.

#### Stephen Cook's Really Cool Thing

Stephen Cook proved that CNF-SAT is $\mathit{NP}$-complete. Which has
the consequence that if CNF-SAT is in $P$, then $P = \mathit{NP}$.

