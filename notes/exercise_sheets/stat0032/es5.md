### 3

$X =$ percentage return last year

$$
Y = \begin{cases}
1 \hspace{1em} \text{stock issues dividends} \\
0 \hspace{1em} \text{else}
\end{cases}
$$

We want to make a prediction on $Y$ given $X$, $P(Y = 1|X = x)$. We know from
the question

$$
\begin{align*}
\tag{1.0} P(X = x|Y = 1) &= \frac{1}{\sqrt{2 \pi \sigma^2}} \exp \left( -(x - \mu)^2/2 \sigma^2 \right)  \\[0.5em]
P(X = x|Y = 0) &= 1
\end{align*}
$$

Note that $(1.0)$ is using incorrect notation since the RHS is a density
function (?). The correct notation would be $f(x|Y=1) =$ RHS

We also have $P(Y = 1) = 0.8$ and $P(Y = 0) = 0.2$.

Using Bayes'

$$
\begin{align*}
P(Y = 1|X = x) &= \frac{P(Y = 1, X = x)}{P(X = x)} \\[0.5em]
&= \frac{P(X = x|Y = 1) \times P(Y = 1)}{P(X = x)} \\[0.5em]
\end{align*}
$$

Can expand the denominator as

$$
P(X = x|Y = 1) \times P(Y = 1) + P(X = x|Y = 0) \times P(Y = 0)
$$

### 1

We have

$$
p(X) = \frac{\exp(\beta_0 + \beta_1X)}{1 + \exp(\beta_0 + \beta_1X)}
$$

And

$$
\frac{p(X)}{1 - p(X)} = \exp(\beta_0 + \beta_1X)
$$

Just need to expand out $\frac{p(X)}{1 - p(X)}$

### 2

$$
\begin{align*}
Y &= \text{receive an A} \\[0.5em]
X_1 &= \text{hours studied} \\[0.5em]
X_2 &= \text{undergrad GPA} \\[0.5em]
\end{align*}
$$

We have $\hat{\beta_0} = -6$, $\hat{\beta_1} = 0.05$ and $\hat{\beta_2} = 1$

Let's take $F \rightarrow \text{Bernoulli}$, and then $\theta = P(Y = 1)$
so $\theta = \text{sigmoid}[\eta]$.

b). We have $\theta = 0.5$

Need to solve

$$
\begin{align*}
\frac{1}{1 + \exp(-\eta)} &= 0.5 \\[0.5em]
0.5 + 0.5 \exp(-\eta) &= 1 \\[0.5em]
\exp(-\eta) &= 1 \\[0.5em]
\eta &= 0 \\[0.5em]
\end{align*}
$$

Need to solve

$$
\eta = -6 + 0.05X_1 + 1 \times 3.5 = 0 \\[0.5em]
\Rarr X_1 = 50
$$

