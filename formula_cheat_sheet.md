
---

# **FS20 MNF AtK**  
**Introduction to Probability — Formula Sheet**  

---

## **Lecture 1: Combinatorial Analysis**  
### **Principles**  
1. **Addition Principle**:  
   \[ |S| = |S_1| + |S_2| + \dots + |S_n| \]  

2. **Multiplication Principle**:  
   \[ \text{Number of outcomes for } r \text{ experiments} = n_1 \times n_2 \times \dots \times n_r \]  

3. **Subtraction Principle**:  
   \[ |S| = |U| - |\overline{A}| \quad \text{where } S \subseteq U \]  

4. **Division Principle**:  
   \[ \text{Number of objects in a part} = \frac{|S|}{n} \]  

### **Multinomial Coefficient**  
\[ \binom{n}{n_1, n_2, \dots, n_k} = \frac{n!}{n_1! n_2! \dots n_k!} \]  

---

## **Lecture 2: Axioms of Probability**  
### **De Morgan’s Laws**  
1. \[ \left( \bigcup_{i=1}^n E_i \right)^c = \bigcap_{i=1}^n E_i^c \]  
2. \[ \left( \bigcap_{i=1}^n E_i \right)^c = \bigcup_{i=1}^n E_i^c \]  

### **Axioms of Probability**  
1. **(A1)** \( P(E) \geq 0 \)  
2. **(A2)** \( P(S) = 1 \)  
3. **(A3)** For any sequence of mutually exclusive events \( E_1, E_2, \dots \):  
   \[ P\left( \bigcup_{i=1}^\infty E_i \right) = \sum_{i=1}^\infty P(E_i) \]  

### **Properties**  
1. \( P(E^c) = 1 - P(E) \)  
2. \( E \subseteq F \implies P(E) \leq P(F) \)  
3. \( P(E \cup F) = P(E) + P(F) - P(E \cap F) \)  

### **Equally Likely Outcomes**  
\[ P(E) = \frac{\text{Number of outcomes in } E}{\text{Number of outcomes in } S} \]  

---

## **Lecture 3: Conditional Probability & Independence**  
### **Conditional Probability**  
\[ P(B|A) = \frac{P(A \cap B)}{P(A)} \]  

### **Bayes' Formula**  
\[ P(B|A) = \frac{P(A|B)P(B)}{P(A)} \]  

### **Alternative Bayes' Formula**  
If \( \{A_i\} \) partitions the sample space:  
\[ P(B) = \sum_{i=1}^n P(B|A_i)P(A_i) \]  

### **Independence**  
Two events \( A \) and \( B \) are independent if:  
\[ P(A \cap B) = P(A)P(B) \]  

### **Mutual Independence (for Sequences)**  
For \( n \) events \( A_1, A_2, \dots, A_n \):  
\[ P\left( \bigcap_{i=1}^n A_i \right) = \prod_{i=1}^n P(A_i) \]  

---

## **Lecture 4: Discrete Random Variables**  
### **Probability Mass Function (PMF)**  
\[ p_X(x) = P(X = x), \quad \forall x \in \mathbb{R} \]  

### **Cumulative Distribution Function (CDF)**  
\[ F_X(x) = P(X \leq x), \quad \forall x \in \mathbb{R} \]  
**Properties**:  
1. \( F_X \) is non-decreasing.  
2. \( F_X \) is right-continuous.  
3. \(\lim_{x \to -\infty} F_X(x) = 0 \)  
4. \(\lim_{x \to +\infty} F_X(x) = 1 \)  

### **Expectation & Variance**  
\[ E(X) = \sum_x x P(X = x) \]  
\[ \text{Var}(X) = E(X^2) - [E(X)]^2 \]  

### **Discrete Distributions**  
| **Distribution**       | **PMF**                      | **Mean** | **Variance** |
|------------------------|-----------------------------|----------|--------------|
| Bernoulli \( \text{Bin}(1, p) \) | \( P(X=1) = p \)            | \( p \)  | \( p(1-p) \) |
| Binomial \( \text{Bin}(n,p) \)  | \( \binom{n}{k} p^k (1-p)^{n-k} \) | \( np \) | \( np(1-p) \) |
| Poisson \( \text{Pois}(\lambda) \) | \( \frac{e^{-\lambda} \lambda^k}{k!} \) | \( \lambda \) | \( \lambda \) |
| Geometric \( G(p) \)   | \( (1-p)^{k-1} p \)          | \( \frac{1}{p} \) | \( \frac{1-p}{p^2} \) |

### **Key Remarks**  
1. **Memoryless Property (Geometric)**:  
   \( P(X=n+k | X \geq n) = P(X = k) \)  
2. **Poisson Approximation (Law of Rare Events)**:  
   If \( n \to \infty, p \to 0 \) but \( np \to \lambda \), then \( \text{Bin}(n,p) \approx \text{Pois}(\lambda) \).  

---

## **Lecture 5/6: Continuous Random Variables**  
### **Probability Density Function (PDF)**  
\[ P(a \leq X \leq b) = \int_a^b f_X(x) \, dx \]  

### **CDF Relationships**  
1. \( P(a \leq X \leq b) = F_X(b) - F_X(a) \)  
2. \( P(X < a) = F_X(a^-) \)  

### **Expectation & Variance**  
\[ E(X) = \int_{-\infty}^\infty x f_X(x) \, dx \]  
\[ \text{Var}(X) = E(X^2) - [E(X)]^2 \]  

### **Continuous Distributions**  
| **Distribution** | **PDF**                      | **Mean** | **Variance** |
|-------------------|-----------------------------|----------|--------------|
| Uniform \( U(a,b) \) | \( \frac{1}{b-a}, \quad x \in [a,b] \) | \( \frac{a+b}{2} \) | \( \frac{(b-a)^2}{12} \) |
| Normal \( N(\mu, \sigma^2) \) | \( \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{(x-\mu)^2}{2\sigma^2}} \) | \( \mu \) | \( \sigma^2 \) |
| Exponential \( \text{Exp}(\lambda) \) | \( \lambda e^{-\lambda x} \) | \( \frac{1}{\lambda} \) | \( \frac{1}{\lambda^2} \) |

### **Key Remarks**  
1. **Standard Normal \( Z \sim N(0,1) \)**:  
   \( Z = \frac{X - \mu}{\sigma} \)  
2. **68-95-99.7 Rule**:  
   - \( P(-1 \leq Z \leq 1) \approx 0.68 \)  
   - \( P(-2 \leq Z \leq 2) \approx 0.95 \)  
   - \( P(-3 \leq Z \leq 3) \approx 0.997 \)  

---

*(Continues similarly for Joint Distributions, MGFs, Limit Theorems, etc.)*  

**Edge Cases**:  
- For discrete RVs, ensure summations converge.  
- For continuous RVs, check domains of PDFs.  
- Independence assumptions must hold in related computations.  

---