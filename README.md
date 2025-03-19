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

# The Most Amazing and Flawless Proof of All Time

Assume some $T(n) \in O(\log_{5} n)$, then there must exist some constant,  
$c$, and $n_0$, such that, for all $n > n_0$, $T(n) \leq c \cdot \log_{5} n$, or:  
$T(n) \in O(\log_{5} n) \iff \exists c, n_0: T(n) \leq c \cdot \log_{5} n$, $\forall n \geq n_0$.  
Via change of base, we can write that expression as:  
$T(n) \in O(\log_{5} n) \iff \exists c, n_0: T(n) \leq c \cdot \frac{\log_{2} n}{\log_{2} 5}$, $\forall n \geq n_0$.  
As $\frac{1}{\log_{2} 5}$ represents a constant, we then have:  
$T(n) \in O(\log_{5} n) \iff \exists c, n_0: T(n) \leq c \cdot \log_{2} n$, $\forall n \geq n_0$, where we define $c$ as $\frac{1}{\log_{2} 5}$.  
Thus, for any $T(n)$, $T(n) \in O(\log_{5} n)$.  

Criss-Cross Applesauce  

Assume some $T(n) \in O(\log_{2} n)$, then there must exist some constant,  
$c$, and $n_0$, such that, for all $n > n_0$, $T(n) \leq c \cdot \log_{2} n$, or:  
$T(n) \in O(\log_{2} n) \iff \exists c, n_0: T(n) \leq c \cdot \log_{2} n$, $\forall n \geq n_0$.  
Via change of base, we can write that expression as:  
$T(n) \in O(\log_{2} n) \iff \exists c, n_0: T(n) \leq c \cdot \frac{\log_{5} n}{\log_{5} 2}$, $\forall n \geq n_0$.  
As $\frac{1}{\log_{5} 2}$ represents a constant, we then have:  
$T(n) \in O(\log_{2} n) \iff \exists c, n_0: T(n) \leq c \cdot \log_{5} n$, $\forall n \geq n_0$, where we define $c$ as $\frac{1}{\log_{5} 2}$.  
Thus, for any $T(n)$, $T(n) \in O(\log_{2} n)$, and consequently $T(n) \in O(\log_{5} n)$.

# Sources

For the Change of Base Log rule:  
https://www.khanacademy.org/math/algebra2/x2ec2f6f830c9fb89:logs/x2ec2f6f830c9fb89:change-of-base/a/logarithm-change-of-base-rule-intro  

Wasn't happy with my original proof, so I reworked it. I referenced the proof: https://github.com/COSC3020/log-o-proof-regtoga/tree/main, as of commit: ab9ae62. I thought their proof was very readable, well formated, and better conveyed they idea than mine. Hopefully my work emulates that.

For help writing proofs:  
https://www.hamilton.edu/documents/Writing%20Mathematical%20Proofs1.pdf  
https://ananddeopurkar.org/teaching/algebra1/cheng.pdf  

# Plagiarism Notice

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
