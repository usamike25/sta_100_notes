# Focused Exercises

## Chapter 1: Primary Tools - First Part (Sets)
1. **True or False:** For any set \( A \), \( A \cap A^c = \Omega \).  
   - [ ] True  
   - [ ] False  

2. **Short Answer:** Give an example of a set that is countably infinite.  

3. **True or False:** Let \( A \) and \( B \) be two sets. If \( A \subset B \), it follows that \( A \cup B = A \).  
   - [ ] True  
   - [ ] False  

4. **Multiple Choice:** Which of the following is equivalent to \( A \setminus B \)?  
   - [ ] (A) \( A^c \cap B \)  
   - [ ] (B) \( A \cap B^c \)  
   - [ ] (C) \( B \setminus A \)  
   - [ ] (D) \( (A \cup B)^c \)  

5. **Short Answer:** Let \( A = \{\frac{1}{n} : n \in \mathbb{N}\} \). What are \( \inf A \) and \( \sup A \)? Does \( A \) have a minimum or maximum?

---

## Chapter 2: Primary Tools - Second Part (Functions, Cardinality, Euclidean Distance)
1. **True or False:** The function \( f: \mathbb{R} \to \mathbb{R} \) defined by \( f(x) = x^3 \) is a bijection.  
   - [ ] True  
   - [ ] False  

2. **Short Answer:** Let \( f: \mathbb{R} \to \mathbb{R} \) be defined by \( f(x) = \sin(x) \). Is \( f \) injective? Is it surjective?  

3. **True or False:** If \( A \) and \( B \) are two sets, and there exists an injective function from \( A \) to \( B \), then \( \#A \leq \#B \).  
   - [ ] True  
   - [ ] False  

4. **Multiple Choice:** A set \( U \subset \mathbb{R}^k \) is called open if:  
   - [ ] (A) It contains all its limit points  
   - [ ] (B) For every \( x \in U \), exists \( \varepsilon > 0 \) s.t. \( B_\varepsilon(x) \subset U \)  
   - [ ] (C) Its complement \( U^c \) is also open  
   - [ ] (D) It is a finite union of closed intervals  

5. **Short Answer:** Provide an example of a family of open sets whose union is open.

---

## Chapter 3: Primary Tools - Third Part (Sequences)
1. **True or False:** A bounded sequence \( (a_n)_{n \in \mathbb{N}} \) must converge.  
   - [ ] True  
   - [ ] False  

2. **Short Answer:** Consider \( a_n = (-1)^n \). Is it convergent? Justify.  

3. **True or False:** If \( \lim_{n \to \infty} a_n = -\infty \), then \( \liminf_{n \to \infty} a_n = -\infty \) and \( \limsup_{n \to \infty} a_n = -\infty \).  
   - [ ] True  
   - [ ] False  

4. **Short Answer:** If \( (a_n) \) converges to \( a \), what about its accumulation points?  

5. **Multiple Choice:** Which sequences converge to zero?  
   - [ ] (A) \( \frac{n^3 + n}{n^4} \)  
   - [ ] (B) \( \frac{(-1)^n}{n} \)  
   - [ ] (C) \( (-1)^n + (-1)^{n+1} + \frac{1}{n} \)  
   - [ ] (D) All above  

---

## Chapter 4: Measurable Spaces
1. **True or False:** \( \mathcal{F} = \{\emptyset, \Omega\} \) is always a \(\sigma\)-field.  
   - [ ] True  
   - [ ] False  

2. **Short Answer:** Is \( \cap_{i \in \mathbb{N}} A_i \in \mathcal{F} \) for \( \{A_i\} \subset \mathcal{F} \)?  

3. **Multiple Choice:** Which \( \mathcal{F} \) is a \(\sigma\)-field?  
   - [ ] (A) \( \{\emptyset, \{0\}, \{1\}\} \) on \( \Omega = \{0, 1\} \)  
   - [ ] (B) Left-open intervals \( \{(a, b]\} \cup \{\emptyset\} \) on \( \mathbb{R} \)  
   - [ ] (C) Borel \(\sigma\)-field \( \mathcal{B}(\mathbb{R}) \)  
   - [ ] (D) Sets where \( A \) or \( A^c \) is finite  

4. **Short Answer:** What's the largest possible \(\sigma\)-field on \( \Omega \)?  

5. **True or False:** \( \mathcal{F}_1 \cup \mathcal{F}_2 \) is always a \(\sigma\)-field.  
   - [ ] True  
   - [ ] False  

---

## Chapter 5: Measure Spaces
1. **Short Answer:** State countable additivity for measure \( \mu \).  

2. **True or False:** For \( \mu(A), \mu(B) < \infty \), \( \mu(A \cup B) = \mu(A) + \mu(B) - \mu(A \cap B) \).  
   - [ ] True  
   - [ ] False  

3. **True or False:** For \( A_n \subset A_{n+1} \), \( \mu(\cup_n A_n) = \lim_n \mu(A_n) \).  
   - [ ] True  
   - [ ] False  

4. **Short Answer:** If \( \mu(A)=0 \) and \( B \subset A \), what's \( \mu(B) \)?  

5. **Multiple Choice:** Which \( \mu \) is a measure?  
   - [ ] (A) Counting measure \( \sum \mathbf{1}_{n \in B} \)  
   - [ ] (B) Negative measure \( -\sum \mathbf{1}_{n \in B}/2 \)  
   - [ ] (C) Sum of Dirac measures \( \delta_0 + \delta_1 \)  
   - [ ] (D) All except B  

---

## Chapter 6: From Outer Measure to Measure
1. **True or False:** \( \ell^*(A) = \inf_{\text{covers}} v_A(\xi) \) is a measure on \( \mathcal{P}(\mathbb{R}) \).  
   - [ ] True  
   - [ ] False  

2. **Short Answer:** What is \( \ell^*(\{a\}) \)?  

3. **True or False:** Lebesgue measure \( \lambda \) uniquely assigns \( b-a \) to \( (a, b] \).  
   - [ ] True  
   - [ ] False  

4. **Multiple Choice:** \( A \) is \( \mu^*\)-measurable if:  
   - [ ] (A) \( \mu^*(A) = 0 \)  
   - [ ] (B) Splits all \( E \): \( \mu^*(A \cap E) + \mu^*(A^c \cap E) = \mu^*(E) \)  
   - [ ] (C) \( A \in \mathcal{M}(\mu^*) \)  
   - [ ] (D) Both B and C  

5. **Short Answer:** Give a semiring that's not a \(\sigma\)-field.  

---

## Chapter 7: Measurable Functions
1. **True or False:** Continuous \( f: \mathbb{R}^m \to \mathbb{R}^k \) is Borel-measurable.  
   - [ ] True  
   - [ ] False  

2. **Short Answer:** When is \( \mathbf{1}_A \) measurable?  

3. **True or False:** If \( f \) measurable, then \( f^+ = \max(f, 0) \) is measurable.  
   - [ ] True  
   - [ ] False  

4. **Multiple Choice:** Which are measurable for measurable \( f_n \)?  
   - [ ] (A) \( \sup f_n \)  
   - [ ] (B) \( \inf f_n \)  
   - [ ] (C) \( \limsup f_n \)  
   - [ ] (D) All  

5. **Short Answer:** Is \( g \circ f \) measurable for continuous \( g \)?

---

## Chapter 8: Integration - First Part
1. **True or False:** If \( f=0 \) except on null set \( N \), then \( \int f d\mu = 0 \).  
   - [ ] True  
   - [ ] False  

2. **Short Answer:** State Monotone Convergence Theorem (MCT).  

3. **True or False:** If \( f \leq g \), then \( \int f d\mu \leq \int g d\mu \).  
   - [ ] True  
   - [ ] False  

4. **Multiple Choice:** \( \int_{\mathbb{R}} \mathbf{1}_{[-1,1]} d\lambda = \)  
   - [ ] (A) 0  
   - [ ] (B) 1  
   - [ ] (C) 2  
   - [ ] (D) ∞  

5. **Short Answer:** Formula for \( \int f d\mu \) where \( f = \sum \alpha_i \mathbf{1}_{A_i} \).

---

## Chapter 9: Integration - Second Part
1. **True or False:** For continuous \( f \), Lebesgue integral = Riemann integral.  
   - [ ] True  
   - [ ] False  

2. **Short Answer:** \( \int_{-a}^a f(x) dx \) for odd continuous \( f \)?  

3. **True or False:** Pushforward measure \( \mu g^{-1}(A^*) = \mu(g^{-1}(A^*)) \).  
   - [ ] True  
   - [ ] False  

4. **Multiple Choice:** PDF of \( Y = (X_1, 2\sqrt{X_2}) \) for \( X_i \sim U(0,1) \)?  
   - [ ] (A) \( \mathbf{1}_{[0,1]^2}(y) \cdot 2/y_2 \)  
   - [ ] (B) \( \mathbf{1}_{[0,1]^2}(y) \)  
   - [ ] (C) \( \mathbf{1}_{[0,1]^2}(y) \cdot 1/2 \)  
   - [ ] (D) \( \mathbf{1}_{[0,1]^2}(y) \cdot y_2 \)  

5. **Short Answer:** State Fubini-Tonelli for \( f: X \times Y \to \mathbb{R}_{\geq 0} \).

---

## Chapter 10: General Probability
1. **True or False:** \( P(A) = \#A / \#\Omega \) is probability measure.  
   - [ ] True  
   - [ ] False  

2. **Short Answer:** \( E[X] \) for \( X \) with \( P(X=0)=0.3 \), \( P(X=1)=0.5 \), \( P(X=2)=0.2 \).  

3. **True or False:** Discrete \( X \) implies \( F_X \) is step function.  
   - [ ] True  
   - [ ] False  

4. **Multiple Choice:** Variance formulas:  
   - [ ] (A) \( E[X^2] - (E[X])^2 \)  
   - [ ] (B) \( E[(X - E[X])^2] \)  
   - [ ] (C) \( \text{Cov}(X,X) \)  
   - [ ] (D) All  

5. **Short Answer:** \( E[X] \) for \( X \sim \text{Poisson}(\lambda) \).

---

## Chapter 11: Random Vectors
1. **True or False:** \( P(A \cap B) = P(A)P(B) \) implies independence.  
   - [ ] True  
   - [ ] False  

2. **Short Answer:** \( E[XY] \) for independent \( X,Y \).  

3. **True or False:** For independent \( X_1,...,X_n \), \( E[\sum X_i] = \sum E[X_i] \).  
   - [ ] True  
   - [ ] False  

4. **Multiple Choice:** PDF of \( X = (X_1,...,X_n) \) independent:  
   - [ ] (A) \( \sum \phi_i(x_i) \)  
   - [ ] (B) \( \prod \phi_i(x_i) \)  
   - [ ] (C) \( \max \phi_i(x_i) \)  
   - [ ] (D) \( \frac{1}{n} \sum \phi_i(x_i) \)  

5. **Short Answer:** Distribution of \( X+Y \) for independent \( X \sim N(\mu_X, \sigma_X^2) \), \( Y \sim N(\mu_Y, \sigma_Y^2) \).

---

## Chapter 12: Convergence
1. **True or False:** \( X_n \to_{a.s.} X \) implies \( X_n \to_P X \).  
   - [ ] True  
   - [ ] False  

2. **Short Answer:** Borel-Cantelli conclusion if \( \sum P(A_n) < \infty \).  

3. **True or False:** \( X_n \to_P X \) implies \( X_n \to_{L^1} X \).  
   - [ ] True  
   - [ ] False  

4. **True or False:** If \( X_n \to_P X \), exists subsequence \( X_{s(n)} \to_{a.s.} X \).  
   - [ ] True  
   - [ ] False  

5. **Short Answer:** Example: converges in \( L^2 \) but not a.s.

---
