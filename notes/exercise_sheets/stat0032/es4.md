### 1.

$$H_0: \beta_i = 0$$
$$H_1: \beta_i \ne 0$$

Note that the p-values in the table only make sense if all the other variables
are there. E.g. for the newspaper row, assuming we have measured the right
coefficients for intercept, tv and radio, we do not have enough evidence to
reject $H_0$ (based on the p-value)

### 2.

$$
Y_i = \beta_0 + \beta_1x_{i1} + \beta_2x_{i2} + \beta_3x_{i3} +
\beta_3x_{i3} + \beta_4x_{i1}x_{i2} + \beta_5x_{i1}x_{i3} + \epsilon_i
$$

Given that

$$
x_{i3} = \begin{cases}
  1 \text{ if female } \\
  0 \text{ if male } \\
\end{cases}
$$

We can create separate models, one for male ($M$) and one for female ($F$) and
compare the two.

$$
Y_i^M = \beta_0 + \beta_1x_{i1} + \beta_2x_{i2} + \beta_4x_{i1}x_{i2} + \epsilon_i
$$

$$
Y_i^F = \beta_0 + (\beta_1 + \beta_5)x_{i1} + \beta_3 + \beta_2x_{i2} + \beta_4x_{i1}x_{i2} + \epsilon_i
$$

$$
Y_i^F - Y_i^M = \beta_3 + \beta_5x_{i1}
$$

We can see that the difference depends on $x_{i1}$.

Note that when making a prediction, should really be using e.g. $\hat{Y}$
instead of $Y$.

**c**. Wrong, the absolute value of the coefficient has no impact on the
interaction as the units of the covariate may be very large.

### 3.

$$
Y_i = \beta_1^1 + \beta_1^1x_{i1} + \epsilon_i^1 \\[0.5em]
Y_i = \beta_0^2 + \beta_1^2x_{i1} +
\beta_2^2x_{i1}^2 + \beta_3^2x_{i1}^2 + \epsilon_i^2 \\[0.5em]
$$

$$
RSS^1 = \sum_{i=1}^{n} (Y_i - \beta_0^1 - \beta_1^1x_{i1})^2 \\[0.5em]
RSS^2 = \sum_{i=1}^{n} (
Y_i - \beta_0^2 - \beta_1^2x_{i1} - \beta_2^2x_{i1}^2 - \beta_3^2x_{i1}^2
)^2 \\[0.5em]
$$

### 5.


