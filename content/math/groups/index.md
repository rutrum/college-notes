+++
title = "Group Theory"
+++

Preliminaries
=============

Common Sets
-----------

-   Integers: $\mathbb Z = \\{0, \pm 1, \pm 2, \dots \\}$

-   Rationals:
    $\mathbb Q = \\{\frac{a}{b} : a,b\in \mathbb Z, b \neq 0\\}$

-   Reals: $\mathbb R = \\{$all decimal expansions$\\}$

-   Complex: $\mathbb C = \\{a + bi : a,b \in \mathbb R, i^2 = -1\\}$

Functions
---------

#### Definition

For a function $f : A \rightarrow B$, $f$ is the *function name*, $A$ is
the *domain*, and $B$ is the *codomain*.

#### Mapping

For a function $f : a \mapsto b$, we say that $f$ maps $a \in A$ to
$b \in B$.

#### Image

The *image* of a function is the set of all outputs of the function.
This is also known as the range.

#### Preimage and Fiber

The *preimage* of a function is the set of all inputs to the function.
The *fiber* of a value is the set of inputs that map to that value.

#### Injectivity

Let $f$ be *injective* if for all $a, b$, then $f(a) = f(b)$ implies
$a = b$. We also say $f$ is *one-to-one*.

#### Surjectivity

Let $f$ be *surjective* if for all elements in the codomain, there
exists an element in the domain that maps to it. We also say $f$ is
*onto*.

#### Bijectivity

Let $f$ be *bijective* if it is both injective and surjective.

Equivalence Relations
---------------------

#### Definition

Let $a$ be related $b$, denoted $a \sim b$ . Then $a \sim b$ is an
*equivalence relation* if and only if the following are true:

1.  Reflexivity: $a \sim a$

2.  Symmetry: $a \sim b \implies b \sim a$

3.  Transitivity: $(a \sim b) \wedge (b \sim c) \implies a \sim c$

We say that $a$ is *equivalent* to $b$.

#### Integers Modulo $n$

Define $a \sim b$ only if $a \equiv b \pmod n$. Define
$\mathbb Z/n\mathbb Z$ to be the set of $n$ distinct integers $a_i > 0$
such that $a_i \sim i$ for $0 \leq i < n$. We call
$\mathbb Z/n\mathbb Z$ the *set of integers modulo $n$*. Every $a_i$
represents a single value from a *residue class*. The least value of
these $a_i$ is called the *least residue*.

#### Integers Modulo $n$ Cross

Define $(\mathbb Z/n\mathbb Z)^\times$ to be the set of all elements of
$\mathbb Z/n\mathbb Z$ with multiplicative inverses. This also happens
to be the set of all elements that are relatively prime to $n$.

Group Introduction
==================

Binary Operation
----------------

#### Definition

A *binary operation* $\cdot$ on a set $G$ is a function as follows:
$$\cdot : G \times G \rightarrow G$$ Typically we will not write
$\cdot(a, b)$ but instead $a \cdot b$.

#### Closure

A binary operation is by definition *closed* on the set it acts upon.

#### Associativity

A binary operation is *associative* if the following is true:
$$a \cdot (b \cdot c) = (a \cdot b) \cdot c$$

#### Commutivity

A binary operation is *commutative* if the following is true:
$$a \cdot b = b \cdot a$$

Groups
------

#### Definition

An ordered pair $(G, \cdot)$ of a set and a binary operation on the set
is a *group* if the following are satisfied:

1.  Associativity:
    $\forall a, b, c \in G : a \cdot (b \cdot c) = (a \cdot b) \cdot c$

2.  Identity:
    $\exists e \in G, \forall a \in G : a \cdot e = e \cdot a = a$

3.  Inverse:
    $\exists a^{-1} \in G, \forall a \in G : a \cdot a^{-1} = a^{-1} \cdot a = e$

#### Abelian

A group is called *abelian* if any two elements of the group commute.

#### Properties of the Group

If $G$ is a group under operation $\cdot$ then

1.  The identity is unique.

2.  The inverse is unique for every element.

3.  $(a^{-1})^{-1} = a$

4.  $(a \cdot b)^{-1} = b^{-1} \cdot a^{-1}$

#### Cancellation Laws

Let $a, b \in G$, then $ax = b, ya = b$ have unique solutions for
$x, y$. In other words, the *left and right cancellation laws* exists
for groups: $$au = av \implies u = v$$ $$ub = vb \implies u = v$$

#### Order

The *order of an element* $x$ is the smallest positive integer $n$ such
that
$$x^n = \underbrace{x \cdot x \cdot x \cdot \dots \cdot x}_\text{n elements} = e$$
If does not exist a finite $n$, then the element has *infinite order*.
The order of $x$ is also denoted $|x|$. The *order of a group* is the
cardinality of the set.

Subgroups
---------

#### Definition

A subset $H$ of a group $G$ is a *subgroup* of $G$ if it closed under
the binary operation of $G$ and satisfies the axioms to be a group under
the binary operation of $G$.

#### How to prove $H$ is a subgroup

$H$ is a subgroup of $G$ if for any $h, k \in H$, then $h \cdot k \in H$
and $e \in H$.

Dihedral Groups
---------------

#### Definition

The *dihedral group $D_{ 2n}$* is a group of symmetries of an $n$-sided
regular polygon. Formally we express this group in *group presentation*
as follows:
$$D_{2n} = \langle r, s : r^n = s^2 = 1, rs = sr^{-1}\rangle$$

#### How to Identify

Using the following steps, we can identify if a group of is a dihedral
group:

1.  $1, r, r^2, \dots, r^{n-1}$ are distinct; $r^n = 1$

2.  $s^2 = 1$

3.  $s \neq r^i, \forall i$

4.  $sr^i \neq sr^j, \forall i, j$

5.  $rs = sr^{-1}$

6.  $r^is = sr^{-i}$

Symmetric Groups
----------------

#### Definition

Let $\Omega = \\{1, 2, \dots, n\\}$. Let $S\_n$ be the set of all
bijections from $\Omega$ to itself, or in other words, the set of all
permutations of $\Omega$. Then we call $S\_n$ a *symmetric group of
degree $n$*. Note that the order of $S\_n$ is $n!$.

#### Cycle Decomposition

Let the *cycle decomposition* of an element of $S\_n$ be the composition
of cycles. A *cycle* is a string of integers $(a\_1, a\_2, \dots, a\_m)$
such that $a\_i \mapsto a\_{i+1}$ and $a\_m \mapsto a\_1$. By convention, we
do not write cycles such as $(a\_i)$, in other words when
$a\_i \mapsto a\_i$, as it is implied.

#### Length

The *length* of a cycle is number of integers within it.

#### Disjoint Cycles

Two cycles are called *disjoint* if there are no integers in common.
Disjoint cycles commute.

Quarternions
------------

#### Definition

We define the *Quartenions* as the group represented by the following
group representation: 
$$\begin{aligned} Q\_8 = \langle &1, -1, i, -i, j, -j, k, -k : \\\\ &i^2 = j^2 = k^2 = -1, \\\\ &-1 \cdot a = a \cdot -1 = -a, \forall a \in Q\_8, \\\\ &i \cdot j = k, j \cdot k = i, k \cdot i = j, j \cdot i = -k, k \cdot j = -i, i \cdot k = -j \rangle\end{aligned}$$ 

Isomorphisms
------------

#### Homomorphism

Let $(G, \bullet), (H, \circ)$ be groups and $x,y \in G$. Then
$\varphi: G \rightarrow H$ is a *homomorphism* if
$$\varphi(x \bullet y) = \varphi(x) \circ \varphi(y).$$ Shorthand
notations is used where the operations are omitted and implied.

#### Isomorphism

Let $\varphi: G \rightarrow H$ be an *isomorphism* if and only if
$\varphi$ is both a homomorphism and a bijection. If there exists a
isomorpism between groups $G$ and $H$ then we say those groups are
*isomorphic*.

#### Order

If $\varphi: G \rightarrow H$ is an isomorphism, then
$|\varphi(x)| = |x|$.

Small Order Group Structure
---------------------------

#### Groups of Order 1

All groups of order 1 are of the form $(\\{e\\}, \circ)$. This is also
called the *trivial group*.

#### Groups of Order 2

All groups of order 2 are of the form $(\\{e, a\\}, \circ)$ such that
$a^2 = 1$.

#### Groups of Order 3

All groups of order 3 are of the form $(\\{e, a, b\\}, \circ)$ such that
$a^{-1} = b$.

#### Groups of Order 4

All groups of order 4 are of the form $(\\{e, a, b, c\\}, \circ)$ such
that either $a^{-1} = b$ and $c^2 = 1$, which is isomorphic to
$\mathbb{Z}/n\mathbb{Z}$ or $a^2 = b^2 = c^2 = e$, which is isomorphic
to $(\mathbb Z/n\mathbb Z)^\times$.

#### Commutivity

All groups of order 4 or less are abelian.

Group Actions
-------------

#### Definition

A *group action* is a map from $G \times A \rightarrow A$ satisfying the
following:

1.  $g_1 \cdot (g_2 \cdot a) = (g_1 \cdot g_2) \cdot a$

2.  $e_G \cdot a = a \cdot e_G = a$

We say that *$G$ acts on $A$*.

#### Trivial Action

The *trivial group action* is $g \cdot a \mapsto a$ for all
$g \in G, a \in A$.

#### Faith

A group action is called *faithful* if it maps every element of $G$ to a
unique permutation of $A$.

#### Kernal

The kernal of the action of $G$ onto $A$ is defined as
$$\\{g \in G : g \cdot a = a, \forall a \in A\\}$$

#### Orbit

The *orbit* of an element $a \in A$ under the action of $G$, is every
element in $A$ obtained by an element of $g$ acting on $a$, as follows:
$$G\cdot a = \\{b \in A : g \cdot a = b \text{ for some } g \in G\\}$$

Subgroups
=========

Review
------

#### Alternate Definition

A subset of $H$ of group $G$ is a subgroup if and only if

1.  $H \neq \emptyset$

2.  $\forall x,y \in H, xy^{-1} \in H$

We will donate $H$ as a proper subgroup of $G$ as $H < G$.

#### Transitivity

If $H < K$ and $K < G$ then $H < G$.

Notable Subgroups
-----------------

#### Centralizer

Define the *centralizer* of $A$ in $G$ to be the following:
$$C_G(A) = \\{g \in G : ga = ag, \forall a \in A\\}$$

#### Center

Define the *center* of group $G$ to be the following:
$$Z(G) = \\{g \in G : gx = xg, \forall x \in G\\}$$

#### Normalizer

Define the *normalizer* of $A$ in $G$ to be the following:
$$N_G(A) = \\{g \in G : gAg^{-1} = A\\}$$ such that
$$gAg^{-1} = \\{gag^{-1} : a \in A\\}$$

#### Stabilizer

Let $G$ be a group acting on a set $S$. Define the *stabilizer* of
$s \in G$ for some fixed $s \in S$ to be the following:
$$G_S = \\{g\in G : g \cdot s = s\\}$$

Cyclic Groups
-------------

#### Generator

A *generator* $\langle x \rangle$ is defined as the following:
$$\langle x \rangle = \\{x^n : n \in \mathbb Z\\}$$ We say the set
$\langle x \rangle$ is *generated* by $x$.

#### Cyclic Group

A group $H$ is *cyclic* if $H$ can be generated by a single element.

#### Countable

All cyclic groups are either finite or countably infinite.

#### Abelian

Cyclic groups are abelian.

#### Cyclic Groups of Equal Order

If two cyclic groups have the same order, then they are isomorphic.

#### Subgroups of Cyclic Groups

Let $H = \langle x \rangle$ be a cyclic group. Then

1.  Every subgroup of $H$ is cyclic.

2.  If $|H| = \infty$, then
    $\langle x^a \rangle \neq \langle x^b \rangle$ for $a \neq b$.

3.  If $|H| = n < \infty$, then for $a \in \mathbb Z$ dividing $n$,
    there is a unique subgroup of $H$ with order $a$.

Quotient Groups and Homomorphisms
=================================

Quotient Groups
---------------

#### Definition

Let $\varphi : G \rightarrow H$ be a homomorphism with kernal $K$. Then
define the *quotient group* $G/K$ to be the group whose elements are the
fibers of $\varphi$, the sets of elements of $G$ that map to a single
element of $H$, with group operation defined such that if $X$ is the
fiber above $a$ and $Y$ is the fiber above $b$, then $XY$ is the fiber
above $ab$.

#### Cosets

Let $N \leq G$ and $g \in G$. Then the *left coset* of $N$ is the
following: $$gN = \\{gn : n \in N\\}$$ Let the *right coset* of $N$ be the
following: $$Ng = \\{ng : n \in N\\}$$

#### Alternative Definition of Quotient Group

Let $G$ be a group where $K$ is the kernal of a homomorphism on the
group. Then the set elements of the cosets that solve
$$uK \circ vK = (uv)K$$ forms the *quotient group* $G/K$.

#### Coset Factoring

The property that $uK \circ vK = (uv)K$ is well defined if and only if
$gng^{-1} \in N$ for all $g\in G, n \in N$.

#### Normal Subgroups

For $N \leq G$, $N$ is *normal* if every element normalizes $G$. That is
that $gNg^{-1} = N$ for all $g \in G$. We write $N \trianglelefteq G$.

#### Equivalent Statements on Normality

The following are equivalent:

-   $N \trianglelefteq G$

-   $N_G(N) = G$

-   $gN = Ng$ for all $g \in G$

-   The operation on the set of left cosets of $N$ is a subgroup

-   $gNg^{-1} \subseteq N$ for all $g \in G$

Simple Groups
-------------

#### Lagrange’s Theorem Again

The cardinality of any subgroup of $G$ divides the cardinality of $G$
and the number of left cosets of the subgroup is their quotient if $G$
is finite.

#### Index

The *index* of a subgroup $H$ is the number of cosets of $H$ in $G$. We
write the index as the following: $$[G:H] = \frac{|G|}{|H|}$$ Note the
equality is only true if $G$ is finite.

#### Order of an Element

If $G$ is finite, then the order of an element $x$ must divide the order
of $G$.

#### Prime Order

If $G$ is a group with prime order $p$, then $G$ is cyclic and
$G \cong \mathbb Z_p$.

#### Subgroups of Index 2

Any subgroup of index 2 must be normal.

#### Simple Groups

Any non-trivial group is called *simple* if the only subgroups are the
trivial group and the group itself.

#### Converse of Lagrange’s Theorem

You are guaranteed that there exists a subgroup of order for every
integer that divides the cardinality of the group only if the group is a
finite abelian group.

#### Cauchy’s Theorem

If $G$ is finite and $p$ is a prime dividing $|G|$, then $G$ has an
element of order $p$.

#### Sylow Theorem

If $G$ is a finite group of order $p^\alpha m$, where $p$ is a prime
such that $p \nmid m$, then $G$ has a subgroup of order $p^\alpha$.

#### Product of Subgroups

We define $HK$ for subgroups $H, K$ of $G$ as the following:
$$HK = \bigcup_{h \in H}hK = \\{hk : h \in H, k \in K\\}$$

The Isomorphism Theorems
------------------------

#### The First Isomorphism Theorem

If $\varphi : G \rightarrow H$ is a homomorphism, then
$ker \varphi \trianglelefteq G$, $\varphi(G) \leq H$, and
$G/ker \varphi \cong \varphi(G)$. This is the group theory analog to the
rank nullity theorem.

#### The Second (Diamond) Isomorphism Theorem

Let $A \leq G, B \leq G$ and assume $A \leq N_G(B)$. Then $AB$ is a
subgroup of $G$, $B \trianglelefteq AB$, $A\cap B \trianglelefteq A$,
and $AB/B \cong A/A\cap B$.

#### The Third Isomorphism Theorem

Let $H \trianglelefteq G, K \trianglelefteq G$ where $H \leq K$. Then
$K/H \trianglelefteq G/H$ and $(G/H)/(K/H) \cong (G/K)$.

The Holder Program
------------------

#### A Weak Cauchy’s Theorem

If $G$ is a finite abelian group and $p$ is a prime dividing $|G|$, then
$G$ contains an element of order $p$.

#### The Holder Program

The goal of the Holder Program is to classify all finite simple groups
and to find ways of putting the simple groups together to form other
groups.

#### The Classifications of Finite Simple Groups

There are 18 infinite families of simple groups and 26 simple groups
that do not belong to these such that every finite simple group is
isomorphic to a group in the list.

The Alternating Group
---------------------

#### Transposition

A *transposition* is a 2-cycle.

#### A Parity Function

Define the function $\epsilon : S_n \rightarrow \\{\pm 1\\}$ to be the
following: $$\epsilon(\sigma) = \begin{cases}
1, &\text{if $\sigma$ is the product of even number of transpositions} \\
-1, &\text{if $\sigma$ is the product of odd number of transpositions}
\end{cases}$$ We call the output of $\epsilon$ the sign of $\sigma$.

#### The Alternating Group

The *alternating group* $A_n$ is the subgroup of even permutations of
$S_n$.

#### Normal and Simple

The alternating group $A_n$ is normal in $S_n$ and is simple for
$n \geq 5$.

Group Actions
=============

Revisit
-------

#### Definition

A *group action* is a homomorphism from a group $G$ to the symmetric
group of a set $A$. We say that $G$ acts on $A$.

#### Orbit

Let $a \in A$ such that $G$ acts on $A$, then the orbit of $a$ is the
image of all elements in $G$ acting on $a$:
$$O_a = \\{b \in A : g \cdot a = b, \forall g \in G\\}$$

#### Cayley’s Theorem

Every group is isomorphic to the subgroup of a symmetric group. Note
that this isn’t necessarily the smallest group.

#### Orbit-Stabilizer Theorem

Let $G$ act on $A$ and let $x \in A$. Then the size of the orbit of $x$
is the same as the index of the stabilizer of $x$: $$|O_x| = |G:G_x|$$

#### Transitivity

A group acts *transitively* if there is only one orbit induced by the
action.

Conjugacy
---------

#### Definition

Two elements $a,b$ are called *conjugate* to each other if there exists
some $x \in G$ such that $$xax{^{-1}}= b.$$

#### Conjugacy Classes

Elements that are conjugate to each other are part of the same
*conjugacy class*. The orbits of the conjugation action of a group onto
itself are also the conjugacy classes of that group. Conjugacy classes
partition the group. The identity is always in its own conjugacy class.

#### Conjugate Permutations

Two elements in $S_n$ are conjugate if and only if they have the same
cycle structure, or the same number of cycles of a given length.

#### Class Equation

The following is true for a group $G$:
$$|G| = |Z(G)| + \sum_{i=1}^r[G:C_G(g_i)]$$

Sylow Theorems
--------------

#### $p$-group

If $|G| = p^\alpha$ for some prime $p$ then $G$ is called a *$p$-group*.

#### $p$-subgroup

If a subgroup of a group is a $p$-group, then it is called a
*$p$-subgroup*. Note that it does not necessarily need to be a subgroup
of a $p$-group.

#### Sylow $p$-subgroup

If a $p$-subgroup has order $p^\alpha$ such that $|G| = p^\alpha m$
where $p$ does not divide $m$, then we call this a *Sylow $p$-subgroup*.

#### Sylow Theorem

Let $G$ be a group of order $p^\alpha m$ where $p$ is prime,
$\alpha > 0$, and $p$ does not divide $m$. Define $n_p$ to be the number
of Sylow $p$-subgroups. Then the following are true.

1.  Group $G$ contains a Sylow $p$-subgroup.

2.  Any two Sylow $p$-subgroups are conjugate.

3.  Where $P$ is any Sylow $p$-subgroup, then $n_p \equiv 1 \pmod p$ and
    $n_p = [G~:~N_G(P)]$.

#### Unique Sylow $p$-subgroup

If $H$ is the unique Sylow $p$-subgroup of $G$ for some prime $p$, then
$H$ is normal in $G$.

Finitely Generated Abelian Groups
---------------------------------

#### Finitely Generated Group

A group is *finitely generated* if $G = \langle A \rangle$ where
$|A| = n < \infty$.

#### Fundamental Theorem of Finitely Generated Abelian Groups

If $G$ is a finitely generated abelian group, then
$$G \cong \mathbb Z^r \times Z_{n_1} \times Z_{n_2} \times \dots \times Z_{n_s}$$
for integers $r \geq 0$, $n_i \geq 2$, and $n_{j+1}$ divides $n_j$ for
$1 \leq j \leq s - 1$. This expression is unique. Thus, every finitely
generated abelian group is the product of cyclic groups.
