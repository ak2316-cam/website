---
layout: post
date: 2021-06-26 15:40:15 +0000
title: The 5/8 Theorem -- Maximum Probability of Group Elements Commuting
summary:
tags: maths groups
# index:
#   best_of: true
---

Today we are going to attack a group theory problem that has a little bit of a combinatorial flavour.

> **Problem**. Find an upper bound on the maximum probability that two randomly chosen elements of a finite non-abelian group commute, and show that it is attained.

## Discussion

Suppose that we have a group $G$, and a random element $g \in G$. We have then got two cases.

1. If $g$ commutes with everything, then the probability that $g$ commutes with another element is obviously 1.
2. If $g$ does not commute with everything, we need to find the probability that it commutes with a random other element.

This gives us two things to compute (or more correctly, to bound): the probability that a random element commutes with everything, and the probability that if it does not commute with everything, then it commutes with a random element.
The natural approach is then clearly thinking about centers and centralisers.

## Solution

Let $G$ be a finite group. If it is non-abelian, then its center $Z(G)$ is not the entire group, that is, $G$ has some element $g \not \in Z(G)$.
Then $C_G(g)$, centraliser of $g$, also cannot be the entire group, as that would contradict $z \not \in Z(G)$.

Noting that $C_G(g) \leq G$, and $Z(G) \leq C_G(g)$, we can then apply Lagrange's theorem twice to get

$$|Z(G)| \leq \frac{1}{2} |C_G(g)| \leq \frac{1}{4}|G|.$$

Now let $x$, $y$ be a random elements of $G$. We can bound the probability that they commute with

$$
\mathbb{P}(x\in Z(G)) + \mathbb{P}(x \not \in Z(G)) \cdot \mathbb{P}(y \in C_G(x)) \leq \frac{1}{4} + \frac{3}{4} \cdot \frac{1}{2} = \frac{5}{8}.
$$

This bound is achieved by the Quaternion group $Q_8$.
