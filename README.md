[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/fbkbKZ5N)
# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

Given $T(n) \in O(\log_2 n)$, we know there exist constants $c_1$ and $n_0$ such that:

$T(n) \leq c_1 \log_2 n: \forall n \geq n_0$

Rewrite $\log_2 n$ in terms of $\log_5 n$. 

$T(n) \leq c_1 \cdot \frac{\log_5 n}{\log_5 2}: \forall n \geq n_0$

Let $c_2 = \frac{c_1}{\log_5 2}$, then we have:

$T(n) \leq c_2 \log_5 n: \forall n \geq n_0$

Given $T(n) \in O(\log_5 n)$ we know there exist constants $c_3$ and $n_1$ such that:

$T(n) \leq c_3 \log_5 n: \forall n \geq n_1$

Rewrite $\log_5 n$ in terms of $\log_2 n$. We know that $\log_5 n = \frac{\log_2 n}{\log_2 5}$.

Let $c_4 = c_3 \log_2 5$, then we have:

$T(n) \leq c_4 \log_2 n: \forall n \geq n_1$

So $T(n) \in O(\log_2 n)$.

Therefore, $O(\log_2 n)$ is the same as $O(\log_5 n)$.




 




