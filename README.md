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

# Proof  

Starting with the formal definition of $O$:  
$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$  
That is to say $T(n)$ is an element of $O(f(n))$ if, and only if, there exists at  
least one value of $c$, where there exists some value, $n_0$, where, for all  
$n \ge n_0$ it is true that $T(n) \le cf(n)$.  

Using the change of base rule, we can represent $\log_{2} n$ as $\log_{5} n/\log_{5} 2$
