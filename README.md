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

# General Proof  

Starting with the formal definition of $O$:  
$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$  
That is to say $T(n)$ is an element of $O(f(n))$ if, and only if, there exists at  
least one value of $c$, and some value, $n_0$, where, for all  
$n \ge n_0$, it is true that $T(n) \le c \cdot f(n)$.  

Via the Change of Base rule,  
$\log_{a} n = \frac{\log_{b} n}{\log_{b} a}$  
any logarithm, $\log_{a} n$, with any positive base, $a \neq 1 \in \mathbb{N}$ can be represented  
in terms of any logarithm, $\log_{b} n$, with any positive base, $b \neq 1 \in \mathbb{N}$ for any  
variable $n$, where $n \geq n_0, n_0 = 2$  

As, for any given $a$, $b$ which satisfies the previously established conditions, $\log_{b} a$ is  
representative of a constant value, we can represent $\frac{1}{\log_{b} a}$ as a constant, $c_1$.

This gives us $\log_{a} n=c_1 \cdot \log_{b} n$, where $c_1= \frac{1}{\log_{b} a}$.  
That is to say for all $n \geq n_0$, $\log_{a} n=c_1 \cdot \log_{b} n \implies \log_{a} n \leq c_1 \cdot \log_{b} n$.

Let $T(n)= \log_{a} n$, $c=c_1$, and $f(n)=\log_{b} n$, by definition $T(n) \in O(f(n))$

# Specific Proof

For $\log_{2} n \in O(\log_{5} n)$  
For any $n \geq n_0 = 2$,  
$\log_{2} n = \frac{\log_{5} n}{\log_{5} 2}$  
$\log_{2} n = \frac{1}{\log_{5} 2} \cdot \log_{5} n$  
$\log_{2} n = c \cdot \log_{5} n$, where $c = \frac{1}{\log_{5} 2}$  
$\log_{2} n = c \cdot \log_{5} n \implies log_{2} n \leq c \cdot \log_{5}$  
Thus $\log_{2} n \in O(\log_{5} n)$.  

And for $\log_{5} n \in O(\log_{2} n)$  
For any $n \geq n_0 = 2$,  
$\log_{5} n = \frac{\log_{2} n}{\log_{2} 5}$
$\log_{5} n = \frac{1}{\log_{2} 5} \cdot \log_{2} n$  
$\log_{5} n = c \cdot \log_{2} n$, where $c = \frac{1}{\log_{2} 5}$  
$\log_{5} n = c \cdot \log_{2} n \implies log_{5} n \leq c \cdot \log_{2}$  
Thus $\log_{5} n \in O(\log_{2} n)$.  

# Sources

For the Chance of Base Log rule:  
https://www.khanacademy.org/math/algebra2/x2ec2f6f830c9fb89:logs/x2ec2f6f830c9fb89:change-of-base/a/logarithm-change-of-base-rule-intro  

# Plagiarism Notice

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
