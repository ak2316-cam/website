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

In 1946, Paul Erdős proved a lovely result[^1] about such functions, which we are going to prove!

---

> **Theorem**. If $f: \mathbb{N} \rightarrow \mathbb{R}$ is increasing and totally multiplicative, then $f(n) = n^{\alpha}$, for some $\alpha \in \mathbb{R}$.

*Proof*. Suppose that $f(2) = 2^{\alpha}$, and take $n > 2$ such that $f(n) = n^{\beta}$. Then for any $\ell \in \mathbb{N}$, we can write

$$
2^a < n^{\ell} < 2^{a + 1},
$$

for $a = \lfloor \log_2(n) \ell \rfloor$. Since $f$ is increasing, evaluating the function at each of the above must still satsify the inequality 

$$
\begin{aligned}
2^{\alpha a} < n^{\beta \ell} &< 2^{\alpha(a + 1)} \\
\implies \lfloor \log_2(n) \ell\rfloor < \frac{\beta}{\alpha} \log_2(n) \ell &< \lceil \log_2(n) \ell\rceil.
\end{aligned}
$$

This implies the inequality

$$
\log_2(n) \ell \left|\frac{\beta}{\alpha} - 1\right| \leq 1.
$$

But this has to hold for all $\ell \in \mathbb{N}$, and thus we must have $\beta = \alpha$, and we're done.



[^1]: He actually proved a slightly different result about *additive functions*, which you can imagine the definition of, but the results are equivalent by taking logs. See *Erdos, P., 1946. On the distribution function of Additive Functions. The Annals of Mathematics, 47(1)*.

