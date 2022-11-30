### 9.4

$$
\mathcal{X} = \left( x^1, x^2, \ldots, x^{n} \right)
$$

And

$$
\log p(\mathcal{X}) = \sum_{n=1}^{N} \sum_{i=1}^{K}
\log p(x_i^n|pa(x_i^n))
$$

$$
\begin{align*}
p(\mathcal{X}) &= \prod_{n=1}^{N} p(x^n) \\[0.5em]
p(x^n) &= \prod_{i=1}^{K} p(x_i^n|pa(x_i^n)) \\[0.5em]
\Rarr p(\mathcal{X}) &= \prod_{n=1}^{N} \prod_{i=1}^{K}
p(x_i^n|pa(x_i^n))
\\[0.5em]
\end{align*}
$$

Aim is to write the log-likelihood in terms of the params of our model. We also
have $g = 0$ and $f = \log(p(\mathcal{X}))$

$$
\begin{align*}
\theta_s^i|t^i &= p(x_i = s|pa(x_i) = t^i) \\[0.5em]
\sum_{s} \theta_s^i(t^i) &= 1  \Rarr g_{t^i}^s = 1 - \sum_{s} \theta_s^i(t^i) = 0 \\[0.5em]
\end{align*}
$$

Following the steps in for a Lagrange multiplier

$$
\mathcal{L} = \sum_{n=1}^{N} \sum_{i=1}^{K} \log (p(x_i^n)|pa(x_i^n)) +
\sum_{i=1}^{K} \sum_{t^i} \lambda_{t^i}^i (1 - \sum_{s} \theta_s^i(t^i))
$$

Need "f" to be a function of $\theta_s^i(t^i)$

Use the trick

$$
p(x_i^n|pa(x_i^n)) = \sum_{s} \sum_{t}
\mathbb{I}[x_i^n = s]\mathbb{I}[pa(x_i) = t^i]\theta_s^i(t^i)
$$

Write like

$$
p(x_i^n|pa(x_i^n)) = \prod_{s} \prod_{t^i} \theta_s^i(t^i)^{\mathbb{I}[x_i^n = s]\mathbb{I}[pa(x_i) = t^i]}
$$

