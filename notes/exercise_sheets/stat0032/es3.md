### Question 7 (and a bit of 8)

$$
\begin{array}{c}
   \text{subjects} & \text{placebo} & \text{old} & \text{new} \\
   1 & \ldots & \ldots & \ldots \\
   \vdots \\
   8
\end{array}
$$

We have $X_i = \left( X_{i1}, X_{i2}, X_{i3} \right), i=1, \ldots, 8$

$$
\theta = \frac{\mathbb{E}[Y]}{\mathbb{E}[X]} \hspace{1em}
\hat{\theta} = \frac{\overline{Y}}{\overline{Z}}
$$

And

$$
Y_i = X_{i3} - X_{i2} \\[0.5em]
Z_i = X_{i2} - X_{i1}
$$

And

$$
\overline{Y} = \frac{1}{8}\sum_{i=1}^{8} Y_i \approx \mathbb{E}[Y] \\[0.5em]
\overline{Z} = \frac{1}{8}\sum_{i=1}^{8} Z_i \approx \mathbb{E}[Z] \\[0.5em]
$$

Why is the CLT not a good idea? Because we have a ratio of sample means. A ratio
of sample means is itself not a sample mean.

Appropriate to use bootstrap for this.

1. Draw new samples $X_1^*, \ldots, X_8^*$ from the observed data (with
   replacement). Important to sample the same number of data points (8 in this
   case).
2. Calculate $Y_1^*, \ldots, Y_8^*$, $Z_1^*, \ldots, Z_8^*$, $\overline{Y}^*,
   \overline{Z}^*, \theta^*$. Note our $\theta^*$ is one estimate of the real
   $\theta$.
3. Repeat steps 1 and 2 $B$ times: $\theta_1^*, \ldots, \theta_B^*$. To get our
   95% confidence interval, we "discard" the outermost 2.5% of $\theta_i^*$,
   i.e. the interval is the innermost 95% of the range of $\theta_i^*$.

How do we decide our $B$? As large as possible (taking into account
computational limitations).

### Question 3

With $Y^{(i)} = \theta + X^{(i)}$

$$
P(X = 1) = P(X = -1) = \frac{1}{2}
$$

$$
C = \begin{cases}
Y^{(1)} - 1 \hspace{1em} \text{if } Y^{(1)} = Y^{(2)} \\
\frac{Y^{(1)} + Y^{(2)}}{2} \hspace{1.2em} \text{if } Y^{(1)} \ne Y^{(2)} \\
\end{cases}
$$

To calculate our confidence interval, we need to calculate $P(\theta \in C)$. 
To do so we use law of total probability to make

$$
\begin{align*}
P(\theta \in C) &= P(\theta \in C | Y^{(1)} - Y^{(2)}) * P(Y^{(1)} - Y^{(2)}) \\[0.5em] 
&+ P(\theta \in C | Y^{(1)} + Y^{(2)}) * P(Y^{(1)} + Y^{(2)})
\end{align*}
$$

