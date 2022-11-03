### 4.3

$$
p(\bold{x}) = \frac{1}{Z(\bold{W}, \bold{b})} \exp \left(
\underbrace{\bold{x}^{\top}\bold{W}\bold{x} + \bold{x}^{\top}\bold{b}}_{\text{energy}}
\right)
$$

Symmetric if $\bold{W} = \bold{W}^{\top}$

Let $\phi = \bold{x}^{\top}\bold{W}\bold{x}$, with
$\phi^{\top} = \bold{x}^{\top} \bold{W}^{\top} \bold{x}$

We also know that $\phi = \phi^{\top}$ since $\phi$ is a scalar. This implies
that $\bold{W} = \bold{W}^{\top}$ from the previous expression.

<!-- Let $\phi^* = \frac{\phi + \phi^{\top}}{2} = \bold{x}^{\top}\left( -->
<!-- \frac{\bold{W} + \bold{W}^{\top}}{2} -->
<!-- \right)\bold{x}$ -->

### 4.4

$$
p(\bold{v}, \bold{h}) =
p(v1, \ldots, v_T, h_1, \ldots, h_T) =
\frac{1}{Z(\bold{W}, \bold{a}, \bold{b})}
\exp \left(
\bold{v}^{\top}\bold{W}\bold{h} + \bold{a}^{\top}\bold{v} + \bold{b}^{\top}\bold{h}
\right)
$$

We want to show $p(\bold{h}|\bold{h}) = \prod_{i=1} p(\bold{h}_i|\bold{v})$

Using Bayes'

$$
\begin{align*}
p(\bold{h}|\bold{v}) &= \frac{p(\bold{h},\bold{v})}{p(\bold{v})} \\[0.5em]
&= \frac{1}{p(\bold{v)}Z(\bold{W},\bold{a},\bold{b})}
\exp \left(
\bold{v}^{\top}\bold{W}\bold{h} + \bold{a}^{\top}\bold{v} + \bold{b}^{\top}\bold{h}
\right) \\[1em]
&= \ldots \exp\left( \bold{v}^{\top}\bold{W}\bold{h} \right)
\cdot \exp \left( \bold{a}^{\top} \bold{v} \right)
\cdot \exp \left( \bold{b}^{\top}\bold{h} \right)
\\[0.5em]
&= \frac{1}{Z'}\exp \left( \bold{v}^{\top}\bold{W}\bold{h} + \bold{b}^{\top}\bold{h} \right)  \\[0.5em]
&= \frac{1}{Z'}\exp \left(
\sum_{j=1}^{n} b_j h_j + \sum_{j=1}^{n} \bold{v}^{\top}\underbrace{\bold{W}_{:,j}}_{\text{j col of W}}h_j
\right)  \\[0.5em]
&= \frac{1}{Z'} \prod \exp\left( b_jh_j + \bold{v}^{\top}\bold{W}_{:,j}h_j \right)   \\[0.5em]
\end{align*}
$$

