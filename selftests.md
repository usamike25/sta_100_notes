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

# Mathematics and Probability Questions
## Chapter 1: Primary tools: First part
1. Define the Cartesian product of A₁,...,Aₙ sets.  
   > A set of all ordered n-tuples (a₁,...,aₙ) where aᵢ ∈ Aᵢ for each i: A₁ × ⋯ × Aₙ = {(a₁,...,aₙ) | a₁ ∈ A₁, ..., aₙ ∈ Aₙ}.

2. State the distributive law relating union and intersection of sets.  
   > A ∩ (B ∪ C) = (A ∩ B) ∪ (A ∩ C) and A ∪ (B ∩ C) = (A ∪ B) ∩ (A ∪ C).

3. Explain the concept of the empty set and provide one of its elementary properties with respect to any given set A.  
   > The empty set ∅ contains no elements. Elementary property: ∅ ⊆ A for any set A.

4. Given a set Ω, define the complement of a subset A in Ω, denoted Aᶜ.  
   > Aᶜ = {ω ∈ Ω | ω ∉ A}.

5. What is the purpose of the principle of induction in mathematics, as indicated in the text?  
   > To prove statements for all natural numbers by verifying a base case and an inductive step.

## Chapter 2: Primary tools: Second part
1. What is the difference between a surjective function and an injective function?  
   > Surjective: Range = codomain (every element in codomain is mapped to). Injective: Distinct inputs map to distinct outputs.

2. When are two sets A and B said to have the same cardinality (#A = #B)?  
   > When there exists a bijection (one-to-one correspondence) between them.

3. Provide the definition of an open set U ⊂ ℝᵏ.  
   > ∀x ∈ U, ∃ε > 0 such that the open ball B(x,ε) ⊆ U.

4. If f: I → ℝ, where I ⊂ ℝ, is a strictly monotonic function, what can be concluded about its inverse function on f(I)?  
   > The inverse f⁻¹ exists and is strictly monotonic on f(I).

5. State the Euclidean norm of a vector x ∈ ℝᵏ and the Euclidean distance between two points x, y ∈ ℝᵏ.  
   > ‖x‖ = √(∑ᵢxᵢ²), d(x,y) = ‖x - y‖.

## Chapter 3: Primary tools: Third part
1. Define a real-valued sequence.  
   > A function from ℕ to ℝ, denoted (aₙ)ₙ∈ℕ where aₙ ∈ ℝ.

2. What is a monotonic sequence?  
   > Non-decreasing (aₙ ≤ aₙ₊₁ ∀n) or non-increasing (aₙ ≥ aₙ₊₁ ∀n).

3. Explain the concept of a series ∑_{i∈ℕ} aᵢ as a sequence.  
   > Defined via partial sums Sₙ = ∑ᵢ₌₁ⁿ aᵢ; the series converges if (Sₙ) converges.

4. Define an accumulation point of a sequence (aₙ)_{n∈ℕ}.  
   > A point L such that ∀ε>0, infinitely many aₙ lie in (L-ε, L+ε).

5. If a sequence (aₙ)_{n∈ℕ} is increasing and diverges, what is its limit?  
   > lim aₙ = +∞.

## Chapter 4: Measurable spaces
1. List the three properties that define a σ-field ℱ on a nonempty set Ω.  
   > (i) Ω ∈ ℱ, (ii) A ∈ ℱ ⇒ Aᶜ ∈ ℱ, (iii) Aₙ ∈ ℱ ∀n ⇒ ∪ₙ Aₙ ∈ ℱ.

2. What is the largest possible σ-field on a nonempty set Ω, and what is it commonly denoted as?  
   > The power set of Ω, denoted 𝒫(Ω).

3. If {Aᵢ : i ∈ ℕ} is a collection of sets belonging to a σ-field ℱ, what can be said about their intersection?  
   > ∩ᵢ Aᵢ ∈ ℱ (closed under countable intersections).

4. Define the Borel σ-field ℬ(ℝᵏ) on ℝᵏ.  
   > The σ-field generated by all open sets in ℝᵏ.

5. Is the union of two σ-fields on Ω necessarily a σ-field on Ω?  
   > No, not necessarily (fails closure properties).

## Chapter 5: Measure spaces
1. What two conditions must a function μ: ℱ → ℝ⁺ satisfy to be considered a measure on a measurable space (Ω,ℱ)?  
   > (i) μ(∅) = 0, (ii) Countable additivity: μ(∪ᵢ Aᵢ) = ∑ᵢ μ(Aᵢ) for disjoint Aᵢ ∈ ℱ.

2. Define a "point measure" μ(A) = ∑_{i∈I} αᵢδ_{xᵢ}(A).  
   > Dirac masses: δ_{xᵢ}(A) = 1 if xᵢ ∈ A, else 0. μ assigns weights αᵢ to points xᵢ.

3. In the context of a finite set Ω, how is the counting measure μ(A) defined on the power set 𝒫(Ω)?  
   > μ(A) = number of elements in A.

4. Given a measure μ on (Ω,ℱ), if A, B ∈ ℱ such that A ⊂ B, what relationship holds between μ(A) and μ(B)?  
   > μ(A) ≤ μ(B) (monotonicity).

5. List the three properties that define a semiring on Ω.  
   > (i) ∅ ∈ 𝒜, (ii) Closed under finite intersections, (iii) If A,B ∈ 𝒜, A ⊆ B, then B\A is a finite disjoint union of sets in 𝒜.

## Chapter 6: From outer measure to measure
1. Define a countable covering of a set A by sets from a collection 𝒜.  
   > A sequence (Eₙ) ∈ 𝒜 such that A ⊆ ∪ₙ Eₙ.

2. What is an outer measure μ*, and what three properties does it satisfy?  
   > (i) μ*(∅)=0, (ii) Monotonicity: A ⊆ B ⇒ μ*(A) ≤ μ*(B), (iii) Subadditivity: μ*(∪Aₙ) ≤ ∑μ*(Aₙ).

3. How is the outer measure ℓ* defined for a set A ∈ 𝒫(ℝ)?  
   > ℓ*(A) = inf{∑ᵢ(bᵢ - aᵢ) : A ⊆ ∪ᵢ(aᵢ,bᵢ]} (inf over countable open coverings by intervals).

4. Is every Borel set also Lebesgue measurable?  
   > Yes.

5. What is the relationship between μ*(A ∩ E) + μ*(Aᶜ ∩ E) and μ*(E) for a μ*-measurable set A?  
   > μ*(A ∩ E) + μ*(Aᶜ ∩ E) = μ*(E) ∀E ⊆ Ω (Carathéodory condition).

## Chapter 7: Measurable functions
1. When is a function f: (Ω,ℱ) → (Ω*,ℱ*) considered measurable?  
   > f⁻¹(B) ∈ ℱ for all B ∈ ℱ*.

2. Can any continuous function f: ℝᵐ → ℝᵏ be classified as a Borel function?  
   > Yes (preimages of open sets under continuous functions are Borel measurable).

3. What defines a "standard" simple function?  
   > f = ∑ᵢ₌₁ⁿ αᵢ𝟙_{Aᵢ} with αᵢ ∈ ℝ, disjoint Aᵢ ∈ ℱ.

4. For ℱ-measurable functions f, g: Ω → ℝ, what can be said about the set {ω ∈ Ω: f(ω) = g(ω)}?  
   > It belongs to ℱ.

5. If a function f: Ω → ℝ is ℱ-measurable and nonnegative, does there exist a sequence of standard simple functions (fₙ)_{n∈ℕ} that approximates f?  
   > Yes, 0 ≤ fₙ ↑ f pointwise.

## Chapter 8: Integration: First part
1. What is a partition of a set Ω?  
   > A disjoint collection {A₁,...,Aₙ} ⊆ ℱ with ∪ᵢAᵢ = Ω.

2. How is the integral of a simple function f(ω) = ∑_{i=1}^N αᵢAᵢ(ω) defined over Ω with respect to a measure μ?  
   > ∫f dμ = ∑ᵢ αᵢ μ(Aᵢ) (assuming μ(Aᵢ) < ∞ or αᵢ ≥ 0).

3. What does it mean for a random variable X to be "integrable" with respect to a probability measure P?  
   > 𝔼[|X|] = ∫|X| dP < ∞.

4. For a measure space (Ω,ℱ,μ) and a ℱ-measurable function f: Ω → ℝ, if {Aᵢ : i ∈ I} ⊂ ℱ is a disjoint collection with I ⊂ ℕ, how can the integral of f over ∪_{i∈I}Aᵢ be expressed?  
   > ∫_{∪Aᵢ} f dμ = ∑ᵢ ∫_{Aᵢ} f dμ.

5. In a measure space (ℕ,𝒫(ℕ),μ) where μ is the counting measure, how does the integral of a nonnegative 𝒫(ℕ)-measurable function f: ℕ → ℝ relate to summation?  
   > ∫f dμ = ∑_{n=1}^∞ f(n).

## Chapter 9: Integration: Second part
1. What is the effect of a measure μ on (Ω,ℱ) being pushed forward by a measurable function g: (Ω,ℱ) → (Ω*,ℱ*)?  
   > Defines a measure μ∘g⁻¹ on (Ω*,ℱ*) by μ∘g⁻¹(B) = μ(g⁻¹(B)) for B ∈ ℱ*.

2. How is the integral of a continuous function f: [a,b] → ℝ defined in terms of its antiderivative?  
   > Via the fundamental theorem: If F' = f, then ∫_{a}^{b} f dx = F(b) - F(a).

3. State the Substitution Rule for integrals involving continuous and differentiable functions.  
   > ∫_{a}^{b} f(g(x))g'(x) dx = ∫_{g(a)}^{g(b)} f(u) du.

4. If a continuous function f: [-a,a] → ℝ is odd, what is the value of ∫_{-a}^a f(x)dx?  
   > 0.

5. What is the Fubini-Tonnelli theorem, and what conditions does it require for measures?  
   > Allows interchange of integration order for product measures. Requires nonnegativity or integrability of the integral of absolute values.

## Chapter 10: General notions in probability
1. How is a probability P defined on a measurable space (Ω,ℱ)?  
   > A measure P: ℱ → [0,1] satisfying P(Ω) = 1.

2. What distinguishes a random variable from a random vector?  
   > Random variable: maps to ℝ. Random vector: maps to ℝᵏ, k ≥ 1.

3. When is a random vector X considered "discrete"?  
   > Takes values in a countable subset of ℝᵏ.

4. Define a "continuous" random vector, and what is its associated function called?  
   > Has an absolutely continuous law w.r.t. Lebesgue measure; characterized by a probability density function (pdf).

5. State Chebyshev's inequality.  
   > For X with mean μ and variance σ²: P(|X - μ| ≥ kσ) ≤ 1/k² ∀k > 0.

## Chapter 11: Collections of random vectors
1. If X₁,...,Xₙ are n independent random vectors, what relationship holds for P({X₁ ∈ B₁}∩···∩{Xₙ ∈ Bₙ}) for measurable sets B₁,...,Bₙ?  
   > P(⋂ᵢ{Xᵢ ∈ Bᵢ}) = ∏ᵢ P(Xᵢ ∈ Bᵢ).

2. What is the law of an independent collection of random vectors in terms of their individual laws?  
   > Joint law is the product measure: P_{(X₁,...,Xₙ)} = P_{X₁} ⊗ ⋯ ⊗ P_{Xₙ}.

3. If X₁,...,Xₙ are independent random variables such that 𝔼[|Xᵢ|] < ∞ for all i, what can be said about 𝔼[∑_{i=1}^n Xᵢ]?  
   > 𝔼[∑Xᵢ] = ∑𝔼[Xᵢ].

4. What is the characteristic function of the sum of n independent random vectors?  
   > φ_{∑Xᵢ}(t) = ∏ᵢ φ_{Xᵢ}(t).

5. If X = (X₁,...,Xₖ) is a Gauss vector, what can be said about each of its components X₁,...,Xₖ?  
   > Each is a univariate Gaussian random variable.

## Chapter 12: Convergence of random vectors
1. When does a sequence of random vectors (Xₙ) converge to X in Lᵖ (p≥1)?  
   > If lim 𝔼[|Xₙ - X|ᵖ] = 0.

2. If ∑_{n=1}^∞ P(Aₙ) < ∞ for a sequence of events {Aₙ: n∈ℕ} ⊂ ℱ, what does the Borel-Cantelli lemma state about P(lim sup_{n→∞}Aₙ)?  
   > P(lim sup Aₙ) = 0 (infinitely many Aₙ occur with probability 0).

3. What is the relationship between convergence in L¹ and convergence in probability?  
   > Convergence in L¹ implies convergence in probability.

4. If a sequence of random vectors (Xₙ) converges to X in probability, what can be said about the existence of a subsequence that converges almost surely?  
   > ∃ subsequence (X_{nₖ}) such that X_{nₖ} → X a.s.

5. State the Law of Large Numbers for a sequence of i.i.d. random variables.  
   > If Xₙ i.i.d. with 𝔼[|X₁|] < ∞, then (1/n)∑ᵢ₌₁ⁿ Xᵢ → 𝔼[X₁] almost surely and in L¹.

---
# part 2
### Mathematics and Probability Questions

#### Chapter 1: Primary tools: First part

1. **Define what it means for two sets A and B to be equal.**  
   > Two sets are equal ($A = B$) if $A \subset B$ and $B \subset A$.

2. **Given three sets A, B, and C, state the associative law for union.**  
   > $(A \cup B) \cup C = A \cup (B \cup C)$.

3. **Let A and B be two sets. Show that $A ∩ B ⊂ A$.**  
   > For any $x \in A \cap B$, by definition $x \in A$ and $x \in B$, thus $x \in A$.

4. **Given a set Ω, what is the complement of the empty set $\emptyset^c$ and the complement of Ω itself $\Omega^c$?**  
   > $\emptyset^c = \Omega$ and $\Omega^c = \emptyset$.

5. **State the definition of an upper bound for a set $A \subset \mathbb{R}$.**  
   > $b \in \mathbb{R}$ is an upper bound for $A$ if $\forall a \in A$, $a \leq b$.

#### Chapter 2: Primary tools: Second part

1. **Let $f: A \to B$ be a function. Define its image $f(C)$ for a subset $C \subset A$.**  
   > $f(C) = \{f(x) \in B : x \in C\}$.

2. **Provide an example of a function $f: \mathbb{R} \to [0,\infty)$ that is surjective but not injective.**  
   > $f(x) = x^2$.

3. **Given an open set $U_1 \subset \mathbb{R}^k$ and $U_2 \subset \mathbb{R}^k$, is their intersection $U_1 \cap U_2$ necessarily open?**  
   > Yes - finite intersection of open sets is open.

4. **Define what it means for a set $V \subset \mathbb{R}^k$ to be closed.**  
   > Its complement $V^c$ is open.

5. **When are two sets $A$ and $B$ said to have cardinality $\#A \leq \#B$?**  
   > If there exists an injective mapping from $A$ to $B$.

#### Chapter 3: Primary tools: Third part

1. **What condition must a sequence $(a_n)_{n\in\mathbb{N}}$ satisfy to be considered convergent?**  
   > $\exists L \in \mathbb{R}$ such that $\forall \epsilon > 0$, $\exists N$ with $|a_n - L| < \epsilon$ for $n \geq N$.

2. **If a sequence $(a_n)_{n\in\mathbb{N}}$ is convergent, what can be concluded about its boundedness?**  
   > All convergent sequences are bounded.

3. **Let $(a_n)$ and $(b_n)$ be two convergent sequences with limits $a$ and $b$. What is $\lim(a_nb_n)$?**  
   > $ab$.

4. **Define divergence to $\infty$ for a sequence $(a_n)_{n\in\mathbb{N}}$.**  
   > $\forall M > 0$, $\exists N$ such that $a_n > M$ for $n \geq N$.

5. **State the Bolzano-Weierstrass theorem.**  
   > Every bounded sequence in $\mathbb{R}^k$ has a convergent subsequence.

#### Chapter 4: Measurable spaces

1. **What is the smallest σ-field on a nonempty set Ω?**  
   > $\{\emptyset, \Omega\}$. 

2. **Show that if $\{A_i\} \subset \mathcal{F}$, then $\cap_i A_i \in \mathcal{F}$.**  
   > By De Morgan's: $\cap_i A_i = (\cup_i A_i^c)^c \in \mathcal{F}$.

3. **Can $G = \{A \subset \Omega : A$ finite or $A^c$ finite$\}$ be a σ-field if $\Omega$ infinite?**  
   > No, because infinite unions of finite sets may not be in $G$.

4. **Define $\mathcal{B}(\mathbb{R})$.**  
   > The σ-field generated by $\{(a,b] : a < b\}$.

5. **Define $\sigma(f)$ where $f: X \to Y$.**  
   > $\sigma(f) = \{f^{-1}(B) : B \in \mathcal{B}\}$.

#### Chapter 5: Measure spaces

1. **Define the Dirac measure $\delta_x$.**  
   > $\delta_x(A) = 1$ if $x \in A$, else $0$.

2. **If $A \subset B$ and $\mu(A) < \infty$, what is $\mu(B \setminus A)$?**  
   > $\mu(B) - \mu(A)$.

3. **State the relationship between $\mu(A \cup B)$ and $\mu(A) + \mu(B)$.**  
   > $\mu(A \cup B) = \mu(A) + \mu(B) - \mu(A \cap B)$.

4. **For nested sets $A_i$, what is $\mu(\cup_i A_i)$?**  
   > $\lim_n \mu(A_n)$ (continuity from below).

5. **Is $\{(a,b]\} \cup \{\emptyset\}$ a semiring?**  
   > Yes, because intersection of two left-open intervals satisfies semiring properties.

#### Chapter 6: From outer measure to measure

1. **State Lebesgue measure $\lambda$ on $(a,b]$.**  
   > $\lambda((a,b]) = b - a$.

2. **What is $\ell^*(\{a\})$?**  
   > $0$ (singletons are null sets).

3. **Is outer measure $\mu^*$ finitely additive?**  
   > No, only countably subadditive.

4. **Are there non-Lebesgue measurable sets?**  
   > Yes (Vitali sets exist under AC).

5. **When is measure unique?**  
   > If two measures agree on a π-system generating the σ-field.

#### Chapter 7: Measurable functions

1. **Define Borel function $f: \mathbb{R}^m \to \mathbb{R}^k$.**  
   > Preimages of Borel sets are Borel.

2. **Sufficient condition for measurability?**  
   > $f^{-1}((-\infty,a]) \in \mathcal{F}$ for all $a \in \mathbb{R}$.

3. **Measurability of composition $g(f_1,...,f_k)$?**  
   > It remains measurable.

4. **Define $f^+$ and $f^-$.**  
   > $f^+ = \max(f,0)$, $f^- = \max(-f,0)$.

5. **Can any measurable $f$ be approximated by simple functions?**  
   > Yes, via $f_n = \sum_{k=-n2^n}^{n2^n} k2^{-n}1_{\{k2^{-n}\leq f <(k+1)2^{-n}\}}$.

#### Chapter 8: Integration: First part

1. **Monotonicity of integral:**  
   > $\int f d\mu \leq \int g d\mu$.

2. **Monotone Convergence Theorem:**  
   > If $f_n \uparrow f$, then $\int f_n d\mu \uparrow \int f d\mu$.

3. **Linearity of integral:**  
   > $\int (\alpha f + \beta g) d\mu = \alpha \int f d\mu + \beta \int g d\mu$.

4. **Integral over null set:**  
   > $0$ (since $\mu$-a.e. equal to $0$).

5. **Integral with respect to sum measure:**  
   > $\int f d(\sum_i \mu_i) = \sum_i \int f d\mu_i$.

#### Chapter 9: Integration: Second part

1. **Integral with density $\phi$:**  
   > $\int_A f(\omega) \phi(\omega)\mu(d\omega)$.

2. **Lebesgue integrability:**  
   > When both $\int_E f^+ d\lambda$ and $\int_E f^- d\lambda$ are finite.

3. **Integration by parts:**  
   > $\int_a^b fg' = f(b)g(b) - f(a)g(a) - \int_a^b f'g$.

4. **Even function integral:**  
   > $\int_{-a}^a f = 2\int_0^a f$.

5. **Product σ-field:**  
   > $\sigma(\{A \times B : A \in \mathcal{X}, B \in \mathcal{Y}\})$.

#### Chapter 10: General probability

1. **Law of random vector $X$:**  
   > $P_X(B) = P(X \in B)$.

2. **Discrete law:**  
   > $P_X = \sum_{x \in E} P(X = x)\delta_x$.

3. **Classical discrete distributions:**  
   > Bernoulli and Poisson.

4. **Expectation of continuous $X$:**  
   > $E[X] = \int_{-\infty}^\infty x\phi(x)dx$.

5. **Properties of variance:**  
   > 1) $\text{Var}(X) \geq 0$  
   > 2) $\text{Var}(aX + b) = a^2\text{Var}(X)$  
   > 3) $\text{Var}(X) = E[X^2] - E[X]^2$

#### Chapter 11: Random vectors

1. **Independent vectors:**  
   > $P_X = \otimes_{i=1}^n P_{X_i}$ (product measure).

2. **Covariance of independent variables:**  
   > $0$.

3. **PDF of sum:**  
   > $\phi_{X_1+X_2} = \phi_1 * \phi_2$ (convolution).

4. **Gauss vector:**  
   > $X$ where $\langle v, X \rangle$ is Gaussian $\forall v$.

5. **Characteristic function:**  
   > $\Phi_X(v) = \exp(i\langle \mu, v \rangle - \frac{1}{2}v^T \Sigma v)$.

#### Chapter 12: Convergence

1. **Almost sure convergence:**  
   > $P(\lim_n X_n = X) = 1$.

2. **limsup of events:**  
   > $\cap_{n=1}^\infty \cup_{k=n}^\infty A_k$ ("infinitely often").

3. **a.s. implies in probability?**  
   > Yes.

4. **Does convergence in probability imply a.s. of subsequence?**  
   > Yes (via Bolzano-Weierstrass argument).

5. **$L^1$ convergence condition:**  
   > When dominated by integrable $Y$ ($|X_n| \leq Y$).