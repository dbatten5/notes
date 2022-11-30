### 1.

a). They could all be the same? But more likely not forward stepwise selection
since $\mathcal{M}_p^{fss} \sube \mathcal{M}_p^{bs}$. Backward selection likely
to have minimum $RSS$ since that's the criteria for $\mathcal{M}_p$. Best subset
surely will end up with the model with smallest RSS as it looks at all possible
models.

b).

c).
i.) True
ii.) False
iii.) False
iv.) False
v.) False

### 3.

a.) This is lasso. When $s$ is 0 then $RSS$ is likely to be large since we need
all $\beta_i = 0$ to enforce the constraint. As $s$ increases then the $RSS$
will decrease as the problem tends to an ordinary least squares solution, so iv
is correct

**Correct**

b.) You loose sparsity as $s \rightarrow \infty$ which may mean that the test
RSS goes up. So ii is correct

c.) When coefficients are pushed towards zero, variance is reduced. Therefore,
as $s$ is increased, the coefficients likely move away from zero and the
variance increases, so iii is correct.

d.) Opposite to above iv is correct.

e.)

### 5.
