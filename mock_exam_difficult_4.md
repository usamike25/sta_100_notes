## Universität Zürich FS 2025 STA110 Introduction to Probability Michael Hediger
## Mock Exam 3
### Instructions
* The exam is open book — the use of AI or any form of communication is not allowed;
* Please make sure that every paper you need has your name and student number on it;
* Unless otherwise stated, full points will not be awarded for solutions without explanation;
* Do not use pencil, red or green pens.
### Notation
We recall some of the terminology:
* Given a nonempty set Ω, $P(Ω)$ is the power set on Ω.
* $B(R^k)$ denotes the Borel σ-field on $R^k$, $k ≥ 1$.
* The measure $µ(A) = \begin{cases} \#A, & \text{if A is finite;} \\ ∞, & \text{otherwise,} \end{cases} A ∈ P(Ω)$ is referred to as the counting measure on $P(Ω)$.
* Given a measurable space $(Ω,F)$ and $x ∈ Ω$, we write $δ_x$ for the measure $F ∋ A ↦ δ_x(A) = \begin{cases} 1, & \text{if x ∈ A;} \\ 0, & \text{otherwise.} \end{cases}$
* If not mentioned explicitly, a random vector is assumed to be defined on a probability space $(Ω,F ,P)$.
### Exercise 1 (10 points)
#### (a) Definition of a Semiring
Given a nonempty set Ω, write down the definition of a semiring on Ω. [1 point]
> A semiring on Ω is a collection of subsets $S ⊂ P(Ω)$ such that:
> 1. $∅ ∈ S$
> 2. $S$ is closed under finite intersections, i.e., $A, B ∈ S ⇒ A ∩ B ∈ S$
> 3. For any $A, B ∈ S$, there exists a finite sequence of disjoint sets $C_1, ..., C_n ∈ S$ such that $A \setminus B = ∪_{i=1}^{n} C_i$
#### (b) Measures on a Measurable Space
Given a measurable space $(Ω,F)$, which of the following set functions $µ_i$, $i = 1, 2, 3$, is not a measure on $F$? [1.5 point — single choice, no explanation is needed to earn full points]
1. $F = P(Ω)$ and $µ_1(A) = 5µ(A)$, where $µ$ is the counting measure on $P(Ω)$.
2. $F$ any σ-field on Ω, $µ$ any measure on $F$ and $µ_2(A) = ∫_A f(ω)µ(dω)$, $A ∈ F$, where $f : Ω → R$ is nonnegative and $F$ measurable.
3. $Ω = N$, $F = P(N)$ and $µ_3(A) = (\#A)^2$, $A ∈ P(N)$.
> The correct answer is 3.
#### (c) Probability Measures on a Measurable Space
Given a measurable space $(E,B)$, which of the following set functions $P_i$, $i = 1, 2, 3$, is not a probability measure on $B$? [1.5 point — single choice, no explanation is needed to earn full points]
1. $E = N$, $B = P(N)$ and $P_1(A) = ∑_{n∈A∩N} (1/2)^n$, $A ∈ P(N)$.
2. $E = R$, $B = B(R)$, and $P_2(A) = λ(A)$, $A ∈ B(R)$, where $λ$ is the Lebesgue measure on $B(R)$.
3. $E = R$, $B = B(R)$ and $P_3(A) = ∫_A (1/2) 1_{[0,1]}(x) dx$, $A ∈ B(R)$.
> The correct answer is 2 and 3.
#### (d) Integrals
Calculate the following integrals: [1 point each]
1. $∫_R x^2 1_{[-2,2]}(x)λ(dx)$, where $λ$ is the Lebesgue measure on $B(R)$.
> $∫_{-2}^{2} x^2 dx = \frac{x^3}{3} \Big|_{-2}^{2} = \frac{8}{3} - \frac{-8}{3} = \frac{16}{3}$
2. $∫_R |x| P(dx)$, where $P(A) = (1/3)δ_{-1}(A) + (2/3)δ_{1}(A)$, $A ∈ B(R)$.
> $∫ |x| P(dx) = |-1| \cdot \frac{1}{3} + |1| \cdot \frac{2}{3} = \frac{1}{3} + \frac{2}{3} = 1$
3. $∫_N \frac{1}{x+1}µ(dx)$, where $µ$ is the counting measure on $P(N)$.
> $∑_{n \in N} \frac{1}{n+1}$. Since $N$ is the natural numbers, this sum diverges to infinity. Thus, $∫_N \frac{1}{x+1}µ(dx) = ∞$
#### (e) Discrete Laws
Which of the following laws $P_i$, $i = 1, 2, 3$, is not discrete? [1.5 point — single choice, no explanation is needed to earn full points]
1. The law $P_1$ of a random variable $X$ with distribution function $F_X(t) = \begin{cases} 0, & \text{if t < 0;} \\ 0.3, & \text{if 0 ≤ t < 1;} \\ 0.7, & \text{if 1 ≤ t < 2;} \\ 1, & \text{if t ≥ 2} \end{cases}$.
2. The law $P_2$ of a random variable $X$ with distribution function $F_X(t) = \begin{cases} 0, & \text{if t < 0;} \\ t, & \text{if 0 ≤ t < 1;} \\ 1, & \text{if t ≥ 1} \end{cases}$.
3. The law $P_3$ of the random variable $X$ defined on $Ω = {a, b, c}$ with $P(X=a) = 1/3$, $P(X=b) = 1/3$, $P(X=c) = 1/3$.
> The correct answer is 2.
#### (f) True or False
Decide whether the following statements are true or false: [0.5 point each — no explanation is needed to earn full points]
1. The family of all subsets of Ω, denoted $P(Ω)$, is the largest possible σ-field on Ω.
> True
2. If $f: R → R$ is continuous, then $f$ is measurable $B(R)/B(R)$.
> True
3. If $X$ and $Y$ are two independent random variables, then $Cov(X,Y) = 0$.
> True
4. Convergence in probability implies almost sure convergence.
> False
### Exercise 2 (13 points)
Let $X$ be a discrete random variable with support ${-2, 2}$ and law $P_X(A) = (1/2)δ_{-2}(A) + (1/2)δ_{2}(A)$, $A ∈ B(R)$.
#### (a) Probabilities
What are $P(X = -2)$ and $P(X = 2)$? [1 point]
> $P(X = -2) = \frac{1}{2}$ and $P(X = 2) = \frac{1}{2}$
#### (b) Expected Value
Calculate $E[|X|^2]$. [1.5 point]
> $E[|X|^2] = \frac{1}{2} |-2|^2 + \frac{1}{2} |2|^2 = \frac{1}{2}(4) + \frac{1}{2}(4) = 4$
#### (c) Expected Value and Variance
Find $E[X]$ and $Var(X)$. [2 points]
> $E[X] = \frac{1}{2}(-2) + \frac{1}{2}(2) = 0$
> $Var(X) = E[X^2] - (E[X])^2 = \frac{1}{2}(-2)^2 + \frac{1}{2}(2)^2 - 0^2 = 4$
#### (d) Law of $(X/2)^2$
What is the law of $(X/2)^2$? [1.5 points]
> $(X/2)^2 = 1$ with probability 1. The law is $P((X/2)^2 = 1) = 1$.
### Exercise 3 (18 points)
Let $ϕ(x) = \begin{cases} x, & \text{if 0 ≤ x < 1;} \\ 2-x, & \text{if 1 ≤ x < 2;} \\ 0, & \text{otherwise} \end{cases}$.
#### (a) Integral of $ϕ(x)$
Verify that $∫_R ϕ(x)dx = 1$. [2 points]
> $∫_0^1 x dx + ∫_1^2 (2-x) dx = \left[ \frac{x^2}{2} \right]_0^1 + \left[ 2x - \frac{x^2}{2} \right]_1^2 = \frac{1}{2} + (4-2) - (2 - \frac{1}{2}) = \frac{1}{2} + 2 - \frac{3}{2} = 1$
### Exercise 4 (6 points)
Let $X_1$ and $X_2$ be two random variables that are independent with common law that is continuous uniform on the interval $[0,1]$. What is the probability density function of the random vector $Y = (X_1 + X_2, X_1 - X_2)$?
### Exercise 5 (6 points)
Let $X$ be a discrete random variable with support ${0, 1, ..., M}$, where $M$ is a positive integer. Suppose that $X$ has law defined upon: $P(X = k) = C(k+1)$, $k = 0, 1, ..., M$, where $C ∈ R$. Find $C$.
> To find $C$, we need $\sum_{k=0}^{M} P(X = k) = 1$. Thus, $\sum_{k=0}^{M} C(k+1) = 1$.
> $C \sum_{k=0}^{M} (k+1) = C \sum_{j=1}^{M+1} j = C \frac{(M+1)(M+2)}{2} = 1$.
> $C = \frac{2}{(M+1)(M+2)}$