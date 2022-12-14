### Question 1

We follow the steps in [Hypothesis testing procedure](202210151102.md).

1. State the model of the data generating process:
$$
X_i = \begin{cases}
  \text{heads with prob p} \\[0.5em]
  \text{tails with prob 1 - p} \\
\end{cases}
$$

Our hypotheses are $H_0$: $p = \frac{1}{2}$ and $H_1$: $p \ne \frac{1}{2}$.

2. Choose the [level](202210151146.md) as $\alpha = 0.05$.

3. Choose the sum of the trials as our test statistic $H = \sum_{i=1}^{1000}
   X_i$

4. Since a sum of Bernoulli is a binomial, we'll assume $H$ has a binomial
   distribution $H \backsim \text{Bin}(1000, \frac{1}{2})$

5 & 6. A two-sided test here is appropriate, and our critical region is something
   like $[0, H_1) \cup (H_2, 1000]$. We want that $P_{H_0}(H \in CR) = 0.05$.
   Therefore $P(H \in [0, H_1)) + P(H \in (H_2, 1000]) = 0.05$. This gives us
   $H_1 = 469$ and  $H_2 = 531$ (using some statistical software).

7. Since the observed test statistic is in the critical region, we reject the
   null hypothesis.

Here we have gone about this using the critical region argument. We could have
used the p-values instead.

### Question 6

We have $X_i \backsim \mathcal{N}(\mu, \sigma^2)$, and 
$$
H_0: \mu = 0 \\[0.5em]
H_1: \mu \ne 0
$$

We choose $T = \frac{1}{n}\sum_{1=1}^{n} X_i$ and therefore $\mathbb{E}[T] = \mathbb{E}[\frac{1}{n}\sum_{i=1}^{n} X_i] = \frac{1}{n}\sum_{i=1}^{n} \mathbb{E}[X_i] = \mu$

And 
$$
\begin{align*}
\text{Var}(T) &= \text{Var}\left( \frac{1}{n}\sum_{i=1}^{n} X_i \right) \\[0.5em]
&= \frac{1}{n}\sum_{i=1}^{n} \text{Var}(X_i) \\[0.5em]
&= \frac{n \times \sigma^2}{n^2} \\[0.5em]
&= \frac{\sigma^2}{n} \\[0.5em]
\end{align*}
$$

Therefore, $T \backsim \mathcal{N}(\mu, \frac{\sigma^2}{n})$ and under $H_0$ we
have $T \backsim \mathcal{N}\left( 0, \frac{\sigma^2}{n} \right)$


