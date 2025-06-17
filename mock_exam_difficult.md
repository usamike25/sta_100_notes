Here is an additional mock exam, designed to be more challenging, drawing on concepts and question styles from the provided sources.

***

### Mock Exam 3 (More Difficult)

*   The exam is open book — the use of AI or any form of communication is not allowed;
*   Please make sure that every paper you need has your name and student number on it;
*   Unless otherwise stated, full points will not be awarded for solutions without explanation;
*   Do not use pencil, red or green pens.

Last Name:
First Name:
Student Number:

Notation: We recall some of the terminology:
*   Given a nonempty set $\Omega$, $\mathcal{P}(\Omega)$ is the power set on $\Omega$.
*   $\mathcal{B}(\mathbb{R}^k)$ denotes the Borel $\sigma$-field on $\mathbb{R}^k$, $k \ge 1$.
*   The measure $\mu(A) = \#A$, if $A$ is finite, and $\infty$, otherwise, for $A \in \mathcal{P}(\Omega)$, is referred to as the counting measure on $\mathcal{P}(\Omega)$.
*   Given a measurable space $(\Omega, \mathcal{F})$ and $x \in \Omega$, we write $\delta_x$ for the measure $\mathcal{F} \ni A \mapsto \delta_x(A) = 1$, if $x \in A$, and $0$, otherwise.
*   If not mentioned explicitly, a random vector is assumed to be defined on a probability space $(\Omega, \mathcal{F}, P)$.

***

**Exercise 1 (10 points).**

(a) Given a measurable space $(\Omega, \mathcal{F})$, write down the definition of a **measure** $\mu$ on $\mathcal{F}$. [1 point]
*(Inspired by Mock Exam 1 (a) and Mock Exam 2 (a), and Definition 5.1 in "The Metamorphosis")*

(b) Given a measurable space $(\Omega, \mathcal{F})$, which of the following set functions $\mu_i, i = 1, 2, 3$, is not a measure on $\mathcal{F}$? [1.5 point — single choice, no explanation is needed to earn full points]
*   $\mathcal{F} = \mathcal{P}(\mathbb{N})$ and $\mu_1(A) = \#A$, for $A \in \mathcal{P}(\mathbb{N})$.
*   $\Omega = \mathbb{R}$, $\mathcal{F} = \mathcal{B}(\mathbb{R})$ and $\mu_2(A) = \int_A (e^x + 1) \lambda(dx)$, $A \in \mathcal{B}(\mathbb{R})$, where $\lambda$ is the Lebesgue measure on $\mathcal{B}(\mathbb{R})$.
*   $\Omega = \mathbb{R}$, $\mathcal{F} = \mathcal{B}(\mathbb{R})$ and $\mu_3(A) = \delta_0(A) + \delta_1(A) - \delta_2(A)$, where $\delta_x$ is the Dirac measure at $x$.

(c) Given a measurable space $(E, \mathcal{B})$, which of the following set functions $P_i, i = 1, 2, 3$, is not a probability measure on $\mathcal{B}$? [1.5 point — single choice, no explanation is needed to earn full points]
*   $E = \mathbb{N}$, $\mathcal{B} = \mathcal{P}(\mathbb{N})$ and $P_1(A) = \sum_{n \in A \cap \mathbb{N}} 2^{-n}$, $A \in \mathcal{P}(\mathbb{N})$.
*   $E = \mathbb{R}$, $\mathcal{B} = \mathcal{B}(\mathbb{R})$ and $P_2(A) = \int_A \frac{1}{\pi(1+x^2)} dx$, $A \in \mathcal{B}(\mathbb{R})$.
*   $E = \mathbb{R}$, $\mathcal{B} = \mathcal{B}(\mathbb{R})$ and $P_3(A) = \frac{1}{2} \lambda(A)$, $A \in \mathcal{B}(\mathbb{R})$, where $\lambda$ is the Lebesgue measure on $\mathcal{B}(\mathbb{R})$.

(d) Calculate the following integrals: [1 point each]
1.  $\int_{\mathbb{N}} \mathbf{1}_{\{3,4,5\}}(x) \mu(dx)$, where $\mu$ is the counting measure on $\mathcal{P}(\mathbb{N})$.
2.  $\int_{\mathbb{R}} e^x \mathbf{1}_{(-\infty,0]}(x) \lambda(dx)$, where $\lambda$ is the Lebesgue measure on $\mathcal{B}(\mathbb{R})$.
3.  $\int_{\mathbb{R}} x^2 \mu(dx)$, where $\mu(A) = \sum_{x=0}^2 (x+1) \delta_x(A)$, $A \in \mathcal{B}(\mathbb{R})$.

(e) Which of the following laws $P_i, i = 1, 2, 3$, is not discrete? [1.5 point — single choice, no explanation is needed to earn full points]
1.  The law $P_1$ of a random variable $X$ such that $P_1(\mathbb{Z}) = 1$.
2.  The law $P_2$ of a random variable $X$ with probability density function $\phi(x) = \mathbf{1}_{}(x)$.
3.  The law $P_3$ of a random variable $X$ with distribution function $F_X(t) = \begin{cases} 0, & \text{if } t < 0 \\ 1/4, & \text{if } 0 \le t < 1 \\ 3/4, & \text{if } 1 \le t < 2 \\ 1, & \text{if } t \ge 2 \end{cases}$.

(f) Decide whether the following statements are true or false: [0.5 point each — no explanation is needed to earn full points]
1.  The set $\mathcal{F} = \{\emptyset, \{1\}, \{1,2,3\}\}$ is a $\sigma$-field on $\Omega = \{1,2,3\}$.
2.  If $A$ and $B$ are two sets, then $A \cup (B \setminus A) = A \cup B$.
3.  If $X_n \to_P X$, then $X_n \to_{L^1} X$.
4.  If $X_1$ and $X_2$ are two independent random variables, then $E[X_1 X_2] = E[X_1] E[X_2]$.

---

**Exercise 2 (13 points).**

Let $X$ be a discrete random variable with support $\{-1, 0, 1\}$ and law $P_X(A) = \frac{1}{4} \delta_{-1}(A) + \frac{1}{2} \delta_{0}(A) + \frac{1}{4} \delta_{1}(A)$, $A \in \mathcal{B}(\mathbb{R})$.

(a) What are $P(X = -1)$, $P(X = 0)$ and $P(X = 1)$? [1 point]
(b) Calculate $E[|X|^3]$. [1.5 point]
(c) Find $E[X]$ and $\text{Var}(X)$. [2 points]
(d) What is the law of $(X + 1)^2$? [1.5 points]

Let $X_1, \ldots, X_n$ be $n$ independent copies of $X$, i.e., for any $i = 1, \ldots, n$, $X_i$ has law $P_X$ and $X_1, \ldots, X_n$ are independent. Define the random vector $Y = (X_1, \ldots, X_n)$.

(e) What is the law of $Y$? Calculate $P(Y \in \{0\}^n)$. [1 point]
(f) Find $E[\sum_{i=1}^n X_i^2]$ and $\text{Var}(\sum_{i=1}^n X_i^2)$. [3 points]
(g) What is the law of $Z = X_1 + X_2$? [3 points]

---

**Exercise 3 (18 points).**

Let $\phi(x) = \begin{cases} 0 & x < -1 \\ \frac{3}{2}(1+x)^2 & -1 \le x < 0 \\ \frac{3}{2}(1-x)^2 & 0 \le x < 1 \\ 0 & x \ge 1 \end{cases}$.

(a) Verify that $\int_{\mathbb{R}} \phi(x)dx = 1$. [2 points]
Let $X$ be a random variable with law $P_X(dx) = \phi(x)dx$.

(b) Find the distribution function $F_X$ of $X$. [4 points]
(c) Calculate the expected value and the variance of $X$. [4.5 points]
(d) Show that $F_X|_{(-1,1)} : (-1, 1) \to (0, 1)$ is a bijection. [3 points]
(e) Verify that $F_X|_{[-1,1]} : [-1, 1] \to$ is a bijection. [1.5 points]
(f) Calculate the inverse $F_X^{-1}|_{[-1,1]}$ of $F_X|_{[-1,1]}$. [3 points]
Note: You can use the fact that:
*   $p = \frac{1}{2}(1+t)^3 \implies t = (2p)^{1/3} - 1$
*   $p = 1 - \frac{1}{2}(1-t)^3 \implies t = 1 - (2(1-p))^{1/3}$

---

**Exercise 4 (6 points).**

Let $X_1$ and $X_2$ be two random variables that are independent with common law that is continuous uniform on the interval $[0, 1]$. What is the probability density function of the random vector $Y = (X_1 + X_2, X_1 - X_2)$?

---

**Exercise 5 (6 points).**

Let $X$ be a discrete random variable with support $\{0, 1, \ldots, N\}$, where $N \ge 1$. Suppose that $X$ has law defined upon:
$P(X = k) = C_N k (N-k)$, for $k = 0, \ldots, N$, where $C_N \in \mathbb{R}$. Find $C_N$.

***