# Exercises
## I. Sets & Functions (Chapters 1 & 2)
1. **True or False**: For any two sets $A$ and $B$, $(A \cup B)^c = A^c \cap B^c$. [Exercise 1.11]  
    > **True** (De Morgan's Law: $(A \cup B)^c = A^c \cap B^c$ holds universally.)

2. **Short Answer**: Let $\Omega = \{1, 2, 3\}$. List all elements of the power set $\mathcal{P}(\Omega)$. [Example 4.2]  
    > $\mathcal{P}(\Omega) = \{\emptyset, \{1\}, \{2\}, \{3\}, \{1,2\}, \{1,3\}, \{2,3\}, \{1,2,3\}\}$ (Power set includes all subsets.)

3. **True or False**: The function $f: \mathbb{R} \to \mathbb{R}$ defined by $f(x) = \sin(x)$ is an injective function. [Definition 2.5]  
    > **False** ($\sin(x_1) = \sin(x_2)$ does not imply $x_1 = x_2$, e.g., $\sin(0) = \sin(\pi)$.)

4. **Short Answer**: Let $f(x) = x^3 - x$. Is $f$ a strictly monotonic function on $\mathbb{R}$? Justify your answer. [Definition 2.9, Proposition 2.5]  
    > **No**, since $f'(x) = 3x^2 - 1$ changes sign (e.g., decreasing around $x=0$, increasing when $|x| > \frac{1}{\sqrt{3}}$).

5. **True or False**: The set of rational numbers $\mathbb{Q}$ is countable. [Proposition 2.6]  
    > **True** ($\mathbb{Q}$ is countable because it can be enumerated as a sequence.)

## II. Sequences (Chapter 3)
1. **True or False**: Every bounded sequence of real numbers converges. [Proposition 3.3]   
    > **False** (Bounded sequences need not converge; e.g., $a_n = (-1)^n$ is bounded but divergent.)

2. **Short Answer**: Consider the sequence $a_n = (-1)^n \cdot \left(1 + \frac{1}{n}\right)$ for $n \in \mathbb{N}$. Find its limit inferior ($\liminf_{n\to\infty} a_n$) and limit superior ($\limsup_{n\to\infty} a_n$). [Definition 3.10, Example 3.12]  
    > $\liminf_{n \to \infty} a_n = -1$, $\limsup_{n \to \infty} a_n = 1$ (Odd terms $\to -1$, even terms $\to 1$.)

3. **True or False**: If a sequence $(a_n)_{n \in \mathbb{N}}$ diverges to $-\infty$, then $\liminf_{n\to\infty} a_n = -\infty$ and $\limsup_{n\to\infty} a_n = -\infty$. [Exercise 3.10]  
    > **True** (Divergence to $-\infty$ implies both $\liminf$ and $\limsup$ are $-\infty$.)

## III. Measurable Spaces & Measures (Chapters 4 & 5)
1. **True or False**: The family $\mathcal{F} = \{\emptyset, \{a\}, \{b, c\}\}$ is a $\sigma$-field on $\Omega = \{a, b, c\}$. [Definition 4.1]  
    > **False** (Missing $\{a, b, c\}$; a $\sigma$-field must include $\Omega$ itself.)

2. **Short Answer**: For a non-empty set $\Omega$, what is the smallest possible $\sigma$-field on $\Omega$? What is the largest possible $\sigma$-field on $\Omega$? [Example 4.1, Example 4.2]  
    > **Smallest**: $\{\emptyset, \Omega\}$. **Largest**: $\mathcal{P}(\Omega)$.

3. **True or False**: Given a measurable space $(\Omega, \mathcal{F})$, the set function $\mu(A) = 5 \cdot \#A$ (if $A$ is finite, $\infty$ otherwise) for $A \in \mathcal{P}(\Omega)$ is a measure on $\mathcal{P}(\Omega)$. [Proposition 5.2, Definition 5.1]   
    > **True** (It satisfies $\mu(\emptyset) = 0$ and countable additivity.)

4. **Short Answer**: Let $\delta_x$ be the Dirac measure at a point $x \in \Omega$. What is $\delta_x(A)$ if $x \notin A$? [Definition 2, Example 5.1]  
    > $\delta_x(A) = 0$ (Dirac measure assigns 1 only if $x \in A$; else 0.)

5. **True or False**: For any two sets $A, B$ in a measurable space $(\Omega, \mathcal{F})$ with measure $\mu$, if $A \subset B$, then $\mu(B \setminus A) = \mu(B) - \mu(A)$ is always true. [Proposition 5.3 (iii)]  
    > **False** (Only true if $\mu(A) < \infty$; else $\mu(B) - \mu(A)$ is undefined.)

## IV. Measurable Functions & Integration (Chapters 7, 8 & 9)
1. **True or False**: Any continuous function $f: \mathbb{R}^m \to \mathbb{R}^k$ is a Borel function. [Proposition 7.2]  
    > **True** (Continuous functions are Borel-measurable since pre-images of open sets are open.)

2. **Short Answer**: Let $(\Omega, \mathcal{F}, \mu)$ be a measure space. If $f: \Omega \to \mathbb{R}$ is a non-negative $\mathcal{F}$-measurable function such that $f(\omega) = 0$ for all $\omega$ except for a set $N \in \mathcal{F}$ with $\mu(N) = 0$, what can you say about $\int_\Omega f(\omega) \mu(d\omega)$? [Example 8.3]  
    > $\int_\Omega f(\omega) \mu(d\omega) = 0$ (Integral over a null set is zero.)

3. **Short Answer**: Calculate the integral: $\int_{\mathbb{N}} \mathbf{1}_{\{1,2,3\}}(x) \mu(dx)$, where $\mu$ is the counting measure on $\mathcal{P}(\mathbb{N})$. [Exercise 1 (d) from Mock Exam 1 (Solutions).pdf, Section 5.1.2]  
    > $= 3$ (Counting measure gives 1 for each of $\{1,2,3\}$, sum $= 3$.)

4. **True or False**: If $f: \mathbb{R} \to \mathbb{R}$ is a Borel measurable function, then $|f|$ is also Borel measurable. [Exercise 7.5 (c) and (b)]  
    > **True** (Absolute value preserves measurability.)

5. **Short Answer**: Let $\phi(x) = \frac{1}{2}\mathbf{1}_{[-1,1]}(x)$. Calculate $\int_{\mathbb{R}} x \phi(x) dx$. [Proposition 9.4, Example 9.2]  
    > $= 0$ (Odd function $x\phi(x)$ integrated over symmetric interval $[-1,1]$.)

## V. Probability (Chapter 10, 11 & 12)
1. **True or False**: If $A$ and $B$ are two events such that $P(A \cap B) = P(A)P(B)$, then $A$ and $B$ are independent. [Definition 11.1]  
    > **True** (Definition of independence.)

2. **Short Answer**: A discrete random variable $X$ has support $E = \{0, 1, 2\}$ and $P(X=0) = 0.3$, $P(X=1) = 0.5$, $P(X=2) = 0.2$. Calculate $E[X]$ and $\text{Var}(X)$. [Section 10.3, Definition 10.11]  
    > - $E[X] = 0.9$, $\text{Var}(X) = 0.49$:  
    > - $E[X] = 0 \cdot 0.3 + 1 \cdot 0.5 + 2 \cdot 0.2 = 0.9$.  
    > - $E[X^2] = 0^2 \cdot 0.3 + 1^2 \cdot 0.5 + 2^2 \cdot 0.2 = 1.3 \implies \text{Var}(X) = 1.3 - 0.9^2 = 0.49$.

3. **True or False**: If a sequence of random variables $(X_n)_{n \in \mathbb{N}}$ converges in probability to $X$ (i.e., $X_n \to_P X$), then it must also converge almost surely to $X$ (i.e., $X_n \to_{a.s.} X$). [Proposition 12.3 and Example 12.2]  
    > **False** (Convergence in probability does not imply a.s. convergence; e.g., "drifting spikes" counterexample.)

4. **True or False**: If $X$ and $Y$ are two independent random variables, then $E[XY] = E[X]E[Y]$. [Proposition 11.2]  
    > **True** (Independence implies $E[XY] = E[X]E[Y]$.)

5. **Short Answer**: Let $X \sim \text{Poisson}(\lambda)$, where $\lambda > 0$. What is $E[X]$? [Example 10.11, Exercise 10.3]  
    > $E[X] = \lambda$ (Mean of $\text{Poisson}(\lambda)$.)