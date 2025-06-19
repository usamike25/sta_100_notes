# Mock Exam 3

## Notation

We recall some of the terminology:
- Given a nonempty set $\Omega$, $P(\Omega)$ is the power set on $\Omega$;
- $B(\mathbb{R}^k)$ denotes the Borel $\sigma$-field on $\mathbb{R}^k$, $k \geq 1$;
- The measure $\mu(A) = \begin{cases} \#A, & \text{if } A \text{ is finite} \\ \infty, & \text{otherwise} \end{cases}$, $A \in P(\Omega)$, is referred to as the counting measure on $P(\Omega)$;
- Given a measurable space $(\Omega,\mathcal{F})$ and $x \in \Omega$, we write $\delta_x$ for the measure $\mathcal{F} \ni A \mapsto \delta_x(A) = \begin{cases} 1, & \text{if } x \in A \\ 0, & \text{otherwise} \end{cases}$;
- If not mentioned explicitly, a random vector is assumed to be defined on a probability space $(\Omega,\mathcal{F}, \mathbb{P})$.

---

**Exercise 1** (10 points)  

(a) Given a nonempty set $\Omega$, write down the definition of an outer measure $\mu^*$ on $P(\Omega)$. [1 point]  
> **Exercise 1(a) Solution**  
> An outer measure $\mu^*$ on $P(\Omega)$ is a function $\mu^*: P(\Omega) \to [0,\infty]$ satisfying:  
> 1. $\mu^*(\emptyset) = 0$  
> 2. Monotonicity: $A \subseteq B \Rightarrow \mu^*(A) \leq \mu^*(B)$  
> 3. Countable subadditivity: $\mu^*\left(\bigcup_{i=1}^\infty A_i\right) \leq \sum_{i=1}^\infty \mu^*(A_i)$  


(b) Given a measurable space $(\Omega,\mathcal{F})$, which of the following set functions $\mu_i$, $i = 1, 2, 3$, is not a measure on $\mathcal{F}$? [1.5 point — single choice, no explanation is needed to earn full points]  
  • $\mu_1(A) = \sqrt{\lambda(A)}$, $A \in B(\mathbb{R})$, where $\lambda$ is the Lebesgue measure on $B(\mathbb{R})$.  
  • $\mu_2(A) = \sum_{n \in A \cap \mathbb{N}} n$, $A \in B(\mathbb{R})$.  
  • $\mu_3(A) = \mu(A) + \nu(A)$, $A \in \mathcal{F}$, where $\mu$ and $\nu$ are measures on $\mathcal{F}$.  
> **Exercise 1(b) Solution**  
> $\mu_2(A)$
​
 

(c) Given a measurable space $(E,\mathcal{B})$, which of the following set functions $P_i$, $i = 1, 2, 3$, is not a probability measure on $\mathcal{B}$? [1.5 point — single choice, no explanation is needed to earn full points]  
  • $E = \mathbb{R}$, $\mathcal{B} = B(\mathbb{R})$ and $P_1(A) = \int_A x^2 e^{-x^3/3} dx$, $A \in B(\mathbb{R})$.  
  • $E = \mathbb{N}$, $\mathcal{B} = P(\mathbb{N})$ and $P_2(A) = \sum_{n \in A \cap \mathbb{N}} (1/2)^n$, $A \in P(\mathbb{N})$.  
  • $E = \mathbb{R}$, $\mathcal{B} = B(\mathbb{R})$ and $P_3(A) = \int_A e^{-|x|} dx$, $A \in B(\mathbb{R})$.  

(d) Calculate the following integrals: [1 point each]  
  1. $\int_{\mathbb{R}} |x| \mathbf{1}_{[-1,1]} \lambda(dx)$, where $\lambda$ is the Lebesgue measure on $B(\mathbb{R})$.  
> **Solution**:  
> The indicator function $\mathbf{1}_{[-1,1]}$ restricts the domain to $[-1,1]$, and $|x|$ is symmetric. Using Lebesgue measure properties:  
> $$
> \int_{\mathbb{R}} |x| \mathbf{1}_{[-1,1]} \lambda(dx) = \int_{-1}^{1} |x|  dx = 2\int_{0}^{1} x  dx = 2 \left[ \frac{x^2}{2} \right]_{0}^{1} = 1.
> $$

  2. $\int_{\mathbb{R}} e^{-|x|} P(dx)$, where $P(A) = (1/2)\delta_{-1}(A) + (1/2)\delta_1(A)$, $A \in B(\mathbb{R})$.  
> **Solution**:  
> $P$ is a discrete measure concentrated at $\{-1, 1\}$. The integral simplifies to:  
> $$
> \int_{\mathbb{R}} e^{-|x|} P(dx) = \frac{1}{2} e^{-|-1|} + \frac{1}{2} e^{-|1|} = \frac{1}{2} e^{-1} + \frac{1}{2} e^{-1} = e^{-1}.
> $$

  3. $\int_{\mathbb{N}} (1/n^2) \mu(dn)$, where $\mu$ is the counting measure on $P(\mathbb{N})$.  
> **Solution**:  
> The counting measure $\mu$ assigns mass $1$ to each $n \in \mathbb{N}$. Thus:  
> $$
> \int_{\mathbb{N}} \frac{1}{n^2} \mu(dn) = \sum_{n=1}^{\infty} \frac{1}{n^2} = \frac{\pi^2}{6}.
> $$

(e) Which of the following laws $P_i$, $i = 1, 2, 3$, is not discrete? [1.5 point — single choice, no explanation is needed to earn full points]  
  1. The law $P_1$ where $P_1(X = k) = (1/e) / k!$ for $k = 0, 1, 2, \dots$  
  2. The law $P_2$ of a random variable $X$ with probability density function $\phi(x) = \cos(x)$ for $x \in [0, \pi/2]$, and $0$ otherwise.  
  3. The law $P_3$ where $P_3(X = k) = (1/3)^k / (2 - 1/3)$ for $k = 0, 1, 2, \dots$  
> **Solution**:  
> 2

(f) Decide whether the following statements are true or false: [0.5 point each — no explanation is needed to earn full points]  
  1. If $X_1$ and $X_2$ are two independent Gaussian random variables, then $(X_1, X_2)$ is a Gauss vector.  
  2. If a sequence of random variables $(X_n)_{n \in \mathbb{N}}$ converges to $X$ in probability, then there exists a subsequence $(X_{s(n)})_{n \in \mathbb{N}}$ that converges almost surely to $X$.  
  3. The union of two $\sigma$-fields on $\Omega$ is always a $\sigma$-field on $\Omega$.  
> **Solution**:  
> T,T,F
---
**Exercise 2** (13 points)  
Let $X$ be a discrete random variable with support $\{0, 1, 2\}$ and law $\mathbb{P}(X=0) = 1/4$, $\mathbb{P}(X=1) = 1/2$, $\mathbb{P}(X=2) = 1/4$.  
(a) What are $\mathbb{P}(X=0)$, $\mathbb{P}(X=1)$ and $\mathbb{P}(X=2)$? [1 point]  
 
> **Solution**  
> **(a)**  
> $\mathbb{P}(X=0) = \frac{1}{4}$, $\mathbb{P}(X=1) = \frac{1}{2}$, $\mathbb{P}(X=2) = \frac{1}{4}$  

(b) Calculate $\mathbb{E}[|X|^2]$. [1.5 point]  

> **(b)**  
> $\mathbb{E}[|X|^2] = \mathbb{E}[X^2] = \sum x^2 \mathbb{P}(X=x) = 0^2 \cdot \frac{1}{4} + 1^2 \cdot \frac{1}{2} + 2^2 \cdot \frac{1}{4} = 0 + 0.5 + 1 = 1.5$  

(c) Find $\mathbb{E}[X]$ and $\text{Var}(X)$. [2 points]  

> **(c)**  
> $\mathbb{E}[X] = \sum x \mathbb{P}(X=x) = 0 \cdot \frac{1}{4} + 1 \cdot \frac{1}{2} + 2 \cdot \frac{1}{4} = 1$  
> $\text{Var}(X) = \mathbb{E}[X^2] - (\mathbb{E}[X])^2 = 1.5 - 1^2 = 0.5$  

(d) What is the law of $|X-1|$? [1.5 points]  
Let $X_1, \dots, X_n$ be $n$ independent copies of $X$, i.e., for any $i = 1, \dots, n$, $X_i$ has law $P_X$ and $X_1, \dots, X_n$ are independent. Define the random vector $Y = (X_1, \dots, X_n)$.  

> **(d)**  
> $|X-1|$ takes values:  
> - $0$ when $X=1$ ($\mathbb{P} = \frac{1}{2}$)  
> - $1$ when $X=0$ or $X=2$ ($\mathbb{P} = \frac{1}{4} + \frac{1}{4} = \frac{1}{2}$)  
> Law: $\mathbb{P}(|X-1|=0) = \frac{1}{2}$, $\mathbb{P}(|X-1|=1) = \frac{1}{2}$  

Let $X_1, \dots, X_n$ be $n$ independent copies of $X$, i.e., for any $i = 1, \dots, n$, $X_i$ has law $P_X$ and $X_1, \dots, X_n$ are independent. Define the random vector $Y = (X_1, \dots, X_n)$.  
(e) Calculate $\mathbb{P}(Y = (0, 1, 0, 1, \dots, 0))$ assuming $n$ is an even integer. [1 point]  

> **(e)**  
> For $Y = (0,1,0,1,\dots,0)$ ($n$ even):  
> Each pair $(0,1)$ has probability $\mathbb{P}(X_i=0)\mathbb{P}(X_{i+1}=1) = \frac{1}{4} \cdot \frac{1}{2} = \frac{1}{8}$  
> With $n/2$ such pairs: $\left(\frac{1}{8}\right)^{n/2} = 8^{-n/2}$  

(f) Calculate the characteristic function of $X$, $\Phi_X(v)$. [3 points]  

> **(f)**  
> $\Phi_X(v) = \mathbb{E}[e^{ivX}] = \sum e^{ivx} \mathbb{P}(X=x)$  
> $= e^{iv\cdot0} \cdot \frac{1}{4} + e^{iv\cdot1} \cdot \frac{1}{2} + e^{iv\cdot2} \cdot \frac{1}{4} = \frac{1}{4} + \frac{1}{2}e^{iv} + \frac{1}{4}e^{2iv}$  

(g) What is the law of $Z = X_1 + X_2$? [3 points] 
> **(g)**  
> $Z = X_1 + X_2$ takes values $\{0,1,2,3,4\}$:  
> | $z$ | $(X_1,X_2)$ | $\mathbb{P}(Z=z)$ |  
> |---|---|---|  
> | 0 | (0,0) | $\frac{1}{4}\cdot\frac{1}{4} = \frac{1}{16}$ |  
> | 1 | (0,1),(1,0) | $2 \cdot \frac{1}{4}\cdot\frac{1}{2} = \frac{1}{4}$ |  
> | 2 | (0,2),(1,1),(2,0) | $2\cdot\frac{1}{4}\cdot\frac{1}{4} + \frac{1}{2}\cdot\frac{1}{2} = \frac{1}{8} + \frac{1}{4} = \frac{3}{8}$ |  
> | 3 | (1,2),(2,1) | $2 \cdot \frac{1}{2}\cdot\frac{1}{4} = \frac{1}{4}$ |  
> | 4 | (2,2) | $\frac{1}{4}\cdot\frac{1}{4} = \frac{1}{16}$ |  
---
**Exercise 3** (18 points)  
Let $X$ be a random variable with law $P_X(dx) = \phi(x)dx$, where  
$$
\phi(x) = \begin{cases}
3x^2 & \text{if } 0 \le x \le 1 \\
0 & \text{otherwise}
\end{cases}
$$
(a) Verify that $\int_{\mathbb{R}} \phi(x)dx = 1$. [2 points]  
> $\int_{\mathbb{R}} \phi(x)dx = \int_0^1 3x^2  dx = \left[ x^3 \right]_0^1 = 1^3 - 0^3 = 1$  

(b) Find the distribution function $F_X$ of $X$. [4 points]  
> $F_X(x) = P(X \leq x) = \int_{-\infty}^x \phi(t)  dt$  
> - For $x < 0$: $\int_{-\infty}^x 0  dt = 0$  
> - For $0 \leq x \leq 1$: $\int_0^x 3t^2  dt = \left[ t^3 \right]_0^x = x^3$  
> - For $x > 1$: $\int_0^1 3t^2  dt = 1$  
> $$
> F_X(x) = \begin{cases} 
> 0 & x < 0 \\
> x^3 & 0 \leq x \leq 1 \\
> 1 & x > 1 
> \end{cases}
> $$

(c) Calculate the expected value $\mathbb{E}[X]$ and the variance $\text{Var}(X)$. [4.5 points]  
> $\mathbb{E}[X] = \int_{\mathbb{R}} x \phi(x)  dx = \int_0^1 x \cdot 3x^2  dx = 3 \int_0^1 x^3  dx = 3 \left[ \frac{x^4}{4} \right]_0^1 = \frac{3}{4}$  
> $\mathbb{E}[X^2] = \int_0^1 x^2 \cdot 3x^2  dx = 3 \int_0^1 x^4  dx = 3 \left[ \frac{x^5}{5} \right]_0^1 = \frac{3}{5}$  
> $\text{Var}(X) = \mathbb{E}[X^2] - (\mathbb{E}[X])^2 = \frac{3}{5} - \left( \frac{3}{4} \right)^2 = \frac{48}{80} - \frac{45}{80} = \frac{3}{80}$  

(d) Show that $F_X \restriction_{(0,1)} : (0, 1) \to (0, 1)$ is a bijection. [3 points]  
> - **Injective**: Let $a, b \in (0,1)$ with $F_X(a) = F_X(b)$. Then $a^3 = b^3 \implies a = b$.  
> - **Surjective**: For any $y \in (0,1)$, let $x = y^{1/3} \in (0,1)$. Then $F_X(x) = (y^{1/3})^3 = y$.  
> Thus $F_X$ is bijective on $(0,1)$.  

(e) Verify that $F_X \restriction_{\{1\}} : \{1\} \to \{1\}$ is a bijection. [1.5 points]  
> $F_X(1) = 1^3 = 1$, so $F_X|_{\{1\}}(1) = 1$.  
> - **Injective**: Only one element in domain/codomain.  
> - **Surjective**: $1$ maps to $1$, covering the codomain.  
> Thus it is a bijection.  

(f) Calculate the inverse $F^{-1}_X \restriction_{\{1\}}$ of $F_X \restriction_{\{1\}}$. [3 points]  
> $F_X|_{\{1\}} : \{1\} \to \{1\}$ is defined by $1 \mapsto 1$.  
> Its inverse is $F^{-1}_X|_{\{1\}} : \{1\} \to \{1\}$ defined by $1 \mapsto 1$.  

---

**Exercise 4** (6 points)  

Let $X_1$ and $X_2$ be two random variables that are independent with common law that is exponential with parameter $\lambda=1$. That is, $P_{X_1}(dx) = e^{-x}\mathbf{1}_{[0,\infty)}(x)dx$ and $P_{X_2}(dx) = e^{-x}\mathbf{1}_{[0,\infty)}(x)dx$. What is the probability density function of the random vector $Y = (X_1 + X_2, X_1)$?  

---

**Exercise 5** (6 points)  

Let $X$ be a discrete random variable with support $\{0, 1, 2, \dots\}$. Suppose that $X$ has law defined upon: $\mathbb{P}(X = k) = C / k!$, $k = 0, 1, 2, \dots$  
Find $C$.