
$$
Y_i = \beta_0 + \beta_1x_{i1} + \beta_2x_{i2} + \beta_3x_{i3} + \epsilon_i
$$

With $\beta_0, \beta_1, \beta_2, \beta_3 \in \R$

This is Gaussian linear regression, our assumption is:

$$
\epsilon_i \backsim \mathcal{N}(0, \sigma^2)
$$

And $\epsilon_i$ is *iid*.

Can therefore say that

$$
Y_i \backsim \mathcal{N}(\beta_0 + \beta_1x_{i1} + \beta_2x_{i2} + \beta_3x_{i3}, \sigma^2)
$$

Note that $Y_i$ is **not** iid (even though they are independent), since their
mean values will be different.
