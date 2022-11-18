### 10.1

$$
y = \begin{cases}
1 \text{ if younger than 60 } \\
0 \text{ otherwise }
\end{cases}
$$

For $y = 0$ we have, for $C, F, S, B$

$$
\begin{align*}
&(1,0,0,0) \rightarrow \text{likes C, dislikes the rest} \\[0.5em]
&(1,0,0,1) \\[0.5em]
&(1,1,1,1) \\[0.5em]
&(0,0,0,1) \\[0.5em]
\end{align*}
$$

For $y = 1$ we have

$$
(0,1,1,0) \\[0.5em]
(1,1,1,0) \\[0.5em]
$$

First step is to construct a table

|y|C|F|S|B|
|---|---|---|---|---|
|0|1|0|0|0|
|0|1|0|0|1|
|0|1|1|1|1|
|0|0|0|0|1|
|1|0|1|1|0|
|1|1|1|1|1|

We want to find $p(y = 1|C=0, F=1, S=1, B=0)$

Apply Bayes':

$$
\begin{align*}
p(y = 1|C=0, F=1, S=1, B=0) = \frac{p((0,1,1,0)|y=1)p(y=1)}
{p((0,1,1,0))}
\end{align*}
$$

Using naive Bayes, we assume that the variables are conditionally independent,
so we can expand out the denominator.

$$
\begin{align*}
p(y = 1|C=0, F=1, S=1, B=0) &= \frac{p((0,1,1,0)|y=1)p(y=1)}
{p((0,1,1,0)|y=1) + p((0,1,1,0)|y=0)}
\end{align*}
$$

So

$$
\begin{align*}
p((0,1,1,0)|y=1) = \hspace{0.3em} &p(C=0|y=1) \times \\[0.5em]
&p(F=0|y=1) \times \\[0.5em]
&p(S=1|y=1) \times \\[0.5em]
&p(B=0|y=1) \times \\[0.5em]
\end{align*}
$$

and

$$
\begin{align*}
p((0,1,1,0)|y=0) = \hspace{0.3em} &p(C=0|y=0) \times \\[0.5em]
&p(F=0|y=0) \times \\[0.5em]
&p(S=1|y=0) \times \\[0.5em]
&p(B=0|y=0) \times \\[0.5em]
\end{align*}
$$

Now we apply maximum likelihood, looking at the table

$$
\begin{align*}
p(C=0|y=1) &\approx \frac{1}{2} \\[0.5em]
p(F=0|y=1) &\approx 1 \\[0.5em]
p(F=0|y=0) &\approx \frac{1}{2} \\[0.5em]
\vdots \\
p((0,1,1,0)|y=0) &= \frac{1}{4} \times \frac{1}{4} \times \frac{1}{4} \times \frac{1}{4}
\end{align*}
$$

### 10.2

Do the same steps as above basically.

$$
p(c=1|(0,1,1)) = \frac{p((0,1,1)|c=1)p(c=1)}{p((0,1,1))} = ...
$$

For part 2... do the same

For part 3, if the attributes are not independent of the class variable, then we
cannot use naive Bayes' (conditional independence). See chapter 10.4 in BRML for
more details.
