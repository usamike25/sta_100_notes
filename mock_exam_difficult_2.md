***

**Universität Zürich**
**FS 2025**
**STA110 Introduction to Probability**
**Advanced Mock Exam**

* **The exam is open book** — the use of AI or any form of communication is not allowed.
* Please make sure that every paper you hand in has your **name and student number** on it.
* Unless otherwise stated, **full points will not be awarded for solutions without a clear explanation**.
* Do not use a pencil or pens in red or green ink.

**Last Name:**
**First Name:**
**Student Number:**

***

### **Notation**

We recall some of the terminology:
* Given a nonempty set Ω, $\mathcal{P}(\Omega)$ is the power set on Ω.
* $\mathcal{B}(\mathbb{R}^k)$ denotes the Borel σ-field on $\mathbb{R}^k$, $k \ge 1$.
* The measure $\mu(A) = \#A$ if $A$ is finite, and $\infty$ otherwise, for $A \in \mathcal{P}(\Omega)$, is the **counting measure** on $\mathcal{P}(\Omega)$.
* Given a measurable space $(\Omega, \mathcal{F})$ and $x \in \Omega$, we write $\delta_x$ for the measure $\mathcal{F} \ni A \mapsto \delta_x(A) = \mathbf{1}_{A}(x)$.
* The Lebesgue measure on $\mathcal{B}(\mathbb{R}^k)$ is denoted by $\lambda_k$. When $k=1$, we write $\lambda$.
* If not mentioned explicitly, a random vector is assumed to be defined on a probability space $(\Omega, \mathcal{F}, \mathbb{P})$.

---

### **Exercise 1 (10 points)**

**(a) Borel-Cantelli Lemmas** [2 points]
State the first and second Borel-Cantelli Lemmas.

**(b) Not a Measure** [1.5 points — single choice, no explanation needed]
Given the measurable space $(\mathbb{R}, \mathcal{B}(\mathbb{R}))$, which of the following set functions $\mu_i$ is **not** a measure?
* $\mu_1(A) = \sum_{q \in \mathbb{Q} \cap A} 1$, where $\mathbb{Q}$ is the set of rational numbers.
* Let $C$ be the standard Cantor set. $\mu_2(A) = \lambda(A \cap C^c)$, where $C^c = \mathbb{R} \setminus C$.
* $\mu_3(A) = \begin{cases} 0 & \text{if } \lambda(A) = 0 \\ \infty & \text{if } \lambda(A) > 0 \end{cases}$

**(c) Not a Probability Measure** [1.5 points — single choice, no explanation needed]
Which of the following definitions for $\mathbb{P}_i$ does **not** describe a valid probability measure?
* Let $X \sim \text{Exp}(1)$. $\mathbb{P}_1(A) = \mathbb{P}(X^2 \in A)$ for $A \in \mathcal{B}(\mathbb{R})$.
* $\mathbb{P}_2(A) = \frac{6}{\pi^2} \sum_{n=1}^{\infty} \frac{1}{n^2} \delta_n(A)$ for $A \in \mathcal{P}(\mathbb{N})$.
* Let $F(x) = \frac{1}{2} + \frac{1}{\pi} \arctan(x)$. $\mathbb{P}_3((-\infty, x]) = F(x)$ for all $x \in \mathbb{R}$.

**(d) Calculate the following integrals:** [1 point each]
1.  $\int_{\mathbb{N}} \frac{1}{x!} \mu(dx)$, where $\mu$ is the counting measure on $\mathcal{P}(\mathbb{N})$.
2.  $\int_{\mathbb{R}} \sin^2(\pi x) \mathbb{P}(dx)$, where $\mathbb{P}$ is the law of a random variable $X \sim \text{Uniform}[0, 2]$.
3.  $\int_{\mathbb{R}^2} \frac{1}{y} \mathbb{P}(d(x,y))$, where $\mathbb{P}$ is the law of a random vector $(X, Y)$ with density $f(x,y) = \frac{1}{2\pi} e^{-(x^2+y^2)/2}$.

**(e) Modes of Convergence** [1.5 points — single choice, no explanation needed]
Let $X_n$ be a sequence of random variables on $(\Omega, \mathcal{F}, \mathbb{P})$. Which statement is **false**?
1.  If $X_n \to X$ almost surely, then $X_n \to X$ in probability.
2.  If $X_n \to X$ in $L^2$, then $\text{Var}(X_n) \to \text{Var}(X)$.
3.  If $X_n \to c$ in probability, where $c$ is a constant, then $X_n \to c$ in distribution.

**(f) True or False?** [0.5 point each — no explanation needed]
1.  Let $X, Y$ be random variables. If $\mathbb{E}[X|Y] = \mathbb{E}[X]$ almost surely, then $X$ and $Y$ are independent.
2.  The characteristic function $\phi_X(v) = \cos(v)$ corresponds to a random variable $X$ with a well-defined probability density function.

---

### **Exercise 2 (13 points)**

Let $a \in (0, 1)$ be a fixed parameter. Consider a discrete random variable $X$ with support on the set of all integers $\mathbb{Z}$ and a probability mass function (PMF) given by:
$$\mathbb{P}(X=k) = C_a \cdot a^{|k|}, \quad k \in \mathbb{Z}$$
where $C_a$ is a normalization constant.

**(a)** Find the constant $C_a$. [2 points]
**(b)** Calculate $\mathbb{E}[X]$ and $\text{Var}(X)$. [3 points]
**(c)** Let $Y = X^2$. Find the law of $Y$, i.e., its PMF. [2 points]
**(d)** Let $X_1, X_2$ be two independent copies of $X$. Find the probability $\mathbb{P}(X_1 + X_2 = 1)$. [3 points]
**(e)** Calculate the conditional probability $\mathbb{P}(X_1 = 1 | X_1 + X_2 = 0)$. [3 points]

---

### **Exercise 3 (18 points)**

Let $\alpha > 0$ and $\beta > 0$ be parameters. A random variable $X$ has a probability density function (PDF) $f_X$ given by:
$$f_X(x) = \begin{cases} C x^{\alpha-1}(1-x)^{\beta-1} & \text{if } x \in (0,1) \\ 0 & \text{otherwise} \end{cases}$$
This defines the Beta distribution, $X \sim \text{Beta}(\alpha, \beta)$. The normalization constant is given by $C = \frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)}$, where $\Gamma(z) = \int_0^\infty t^{z-1}e^{-t}dt$ is the Gamma function. You may use the property $\Gamma(z+1) = z\Gamma(z)$ for $z>0$.

**(a)** For the specific case $\alpha=2, \beta=3$, verify that $C=12$. [2 points]
**(b)** For the general case, calculate $\mathbb{E}[X]$. [4 points]
**(c)** For the general case, calculate $\mathbb{E}[X^2]$ and find $\text{Var}(X)$. [5 points]
**(d)** Let $X \sim \text{Beta}(1, 3)$. Find the distribution function $F_X(t)$ of $X$. [4 points]
**(e)** Let $X \sim \text{Beta}(\alpha, \beta)$. Find the density of the random variable $Y = -\ln(X)$. You do not need to identify the name of the resulting distribution. [3 points]

---

### **Exercise 4 (6 points)**

Let $X$ and $Y$ be independent random variables with $X \sim \text{Exponential}(\lambda)$ and $Y \sim \text{Exponential}(\mu)$. Their respective PDFs are $f_X(x) = \lambda e^{-\lambda x}$ for $x>0$ and $f_Y(y) = \mu e^{-\mu y}$ for $y>0$.

Find the probability density function of the random variable $Z = X - Y$.

*Hint: Consider the cases $Z>0$ and $Z<0$ separately. This may involve a convolution-style integral.*

---

### **Exercise 5 (6 points)**

Let $(X_n)_{n \in \mathbb{N}}$ be a sequence of independent and identically distributed random variables with $\mathbb{P}(X_n = 1) = p$ and $\mathbb{P}(X_n = -1) = 1-p$, where $p \in (0,1)$ and $p \neq 1/2$. Let $S_n = \sum_{k=1}^n X_k$ be the simple random walk starting at $S_0=0$. Define the random variable $M_n = \left(\frac{1-p}{p}\right)^{S_n}$.

Show that $(M_n)_{n \in \mathbb{N}}$ is a martingale with respect to the natural filtration $\mathcal{F}_n = \sigma(X_1, \dots, X_n)$.

*Recall: To show $M_n$ is a martingale, you must verify three conditions:*
1.  $M_n$ is $\mathcal{F}_n$-measurable for all $n$.
2.  $\mathbb{E}[|M_n|] < \infty$ for all $n$.
3.  $\mathbb{E}[M_{n+1} | \mathcal{F}_n] = M_n$ for all $n$.