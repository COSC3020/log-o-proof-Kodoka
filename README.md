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
least one value of $c$, and some value, $n_0$, where, for all  
$n \ge n_0$, it is true that $T(n) \le c \cdot f(n)$.  

Using the change of base rule, for positive logarithms, with positive bases not equal  
to 1, we can change the base to any value, thus we can represent $\log_{2} n$ in terms  
of $\log_{5} n$.  
$\log_{2} n = \frac{\log_{5} n}{\log_{5} 2} = \frac{1}{\log_{5} 2} \cdot \log_{5} n$  
or:  
$c \cdot \log_{5} n$, where $c = \frac{1}{\log_{5} 2}$  
Thus we've demonstrated there exists a value of $c$:  
$c = \frac{1}{\log_{5} 2}$  
such that, for some value of $n_0$, all $n \ge n_0$ that $T(n) \le c \cdot f(n)$.  
That is to say, for the purpose of asymptotic complexity, $O(\log_{2} n)=O(\log_{5} n)$  

# Sources

For the Chance of Base Log rule:  
https://www.khanacademy.org/math/algebra2/x2ec2f6f830c9fb89:logs/x2ec2f6f830c9fb89:change-of-base/a/logarithm-change-of-base-rule-intro  

# Plagiarism Notice

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
