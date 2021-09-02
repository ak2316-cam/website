---
layout: post
date: 2021-09-01 12:25:40 +0000
title: Erdős Theorem on Monotone Multiplicative Functions
summary:
tags: maths number-theory analysis
index:
  best_of: true
---

In number theory, a *totally multiplicative function* is a function $f: \mathbb{N} \rightarrow \mathbb{R}$ such that
$$
  f(mn) = f(m)f(n),
$$
for all $m, n \in \mathbb{N}$.

In 1946, Paul proved a lovely result[^1] about such functions. In this short article, we are going to prove it.

[^1]: He actually proved a slightly different result about *additive functions*, which you can imagine the definition of, but the results are equivalent by taking logs. See Erdos, P., 1946. On the distribution function of Additive Functions. The Annals of Mathematics, 47(1).


<!-- 

The following problem appeared as part of [this years Part IA exams](https://www.maths.cam.ac.uk/undergrad/pastpapers/files/2021/paperia_4_2021.pdf).

> **Problem**. Show that
>
> $$
> \sum_{r=0}^{n}(-1)^{r}\binom{n}{r}^2 = \begin{cases}
>            0 &\mbox{if $n$ is odd}, \\
>             (-1)^{n/2} \binom{n}{n/2} &\mbox{if $n$ is even}.
>            \end{cases}
> $$

The normal solution involves looking at the coefficient of $x^n$ in the equation

$$
(1-x)^n(1+x)^n=(1-x^2)^n,
$$

but it is possible to solve the problem without resorting to the binomial theorem.

## A Combinatorial Solution

*Solution*. 
We begin by noting that

$$
\binom{n}{r}^2 = \binom{n}{r}\binom{n}{n - r}
$$

is the number of ways of choosing $r$ elements from $\\{1, \dots, n\\}$ followed by $n - r$ elements from $\\{n + 1, \dots, 2n\\}$. Then as we sum over $r$, the sum (ignoring the minus sign) counts the total number of $n$ element subsets from $\\{1, \dots, 2n\\}$.

Now to each $n$-element subset of $\\{1, \dots, 2n\\}$, we assign '1' if the subset contains an even number of elements in $\\{1, \dots, n\\}$, and a '-1' if it contains an odd number. Summing over all of these assigned numbers then is equivalent to our original sum.

Consider the following mapping. Given a subset of size $n$, let $1 \leq x \leq n$ be the smallest integer for which exactly one of $x, n + x$ is in the set. We then toggle $x$ and $n + x$ in the subset, giving us another subset of $\\{1, \dots, 2n\\}$ of size $n$, but maps between elements of different sign. It's also clearly an involution (applying it twice gives you back the original subset).

If $n$ is odd, then this mapping is well defined, since if there was no such element $x$, then $x$ and $n + x$ would always be in the subset, and there would have to then be an even number of elements in the subset (which isn't the case).
If $n$ is even, then this mapping is only not well defined when we always have both $x$ and $n + x$ in the subset. Thus the mapping is not defined on $\binom{n}{n/2}$ subsets, since we can fully specify each of these by choosing the $n/2$ elements of $\\{1, \dots, n\\}$ to include. Also all such subsets were given the sign $(-1)^{n/2}$.

Thus if $n$ is odd, we can use this mapping to pair each element with a positive sign to an element with a negative sign, and the total sum is zero. If $n$ is even, then we can do this for all but $\binom{n}{n/2}$ elements, all of which have sign $(-1)^{n/2}$, and thus summing up we get the desired answer, 

$$
\sum_{r=0}^{n}(-1)^{r}\binom{n}{r}^2 = \begin{cases}
          0 &\mbox{if $n$ is odd}, \\
           (-1)^{n/2} \binom{n}{n/2} &\mbox{if $n$ is even}.
          \end{cases}
$$ -->