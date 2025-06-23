# Normalization Constant Exercises for PMF/PDF 1

**Exercise 5 (6 points).**  
Let \( X \) be a discrete random variable with support \( \mathbb{N} = \{1, 2, 3, \dots\} \). Suppose \( X \) has law defined by:  
\[ P(X = k) = C_\theta \cdot \theta^{k+1}(1 - \theta)^{k-1} \quad \text{for } k \in \mathbb{N}, \; \theta \in (0,1), \]  
where \( C_\theta \in \mathbb{R} \). Find \( C_\theta \).

>**Solution:**  
The normalization condition requires summing probabilities over the support:  
\[ \sum_{k=1}^\infty C_\theta \theta^{k+1}(1 - \theta)^{k-1} = 1. \]  
Factorize \( \theta^2 \):  
\[ C_\theta \theta^2 \sum_{k=1}^\infty \left[\theta(1 - \theta)\right]^{k-1} = 1. \]  
Recognize the geometric series \( \sum_{k=1}^\infty r^{k-1} = \frac{1}{1 - r} \):  
\[ C_\theta \theta^2 \cdot \frac{1}{1 - \theta(1 - \theta)} = 1. \]  
Simplify the denominator (\( 1 - \theta + \theta^2 \)):  
\[ C_\theta = \frac{1 - \theta + \theta^2}{\theta^2}. \]  

---

### **Progressive Variations**  

#### **Variation 1: Geometric Distribution with Offset Support**  
**Exercise:**  
A discrete random variable \( X \) has support \( \{2, 3, 4, \dots\} \) and PMF:  
\[ P(X = k) = C_p (1 - p)^{k-1} \quad \text{for } p \in (0,1). \]  
Find \( C_p \).  

>**Solution:**  
Shift index \( j = k-1 \):  
\[ \sum_{j=1}^\infty C_p (1 - p)^j = 1. \]  
Geometric series sum:  
\[ C_p \cdot \frac{1 - p}{p} = 1 \implies C_p = \frac{p}{1 - p}. \]  

---

#### **Variation 2: Poisson Distribution via Taylor Series**  
**Exercise:**  
Let \( X \) have support \( \mathbb{N}_0 = \{0, 1, 2, \dots\} \) and PMF:  
\[ P(X = k) = C_\lambda \frac{\lambda^k}{k!} \quad \text{for } \lambda > 0. \]  
Find \( C_\lambda \).  

>**Solution:**  
Sum over support:  
\[ C_\lambda \sum_{k=0}^\infty \frac{\lambda^k}{k!} = 1. \]  
Recognize Taylor series for \( e^\lambda \):  
\[ C_\lambda e^\lambda = 1 \implies C_\lambda = e^{-\lambda}. \]  

---

#### **Variation 3: Weighted Geometric Series (Expectation Form)**  
**Exercise:**  
Let \( X \) have support \( \mathbb{N} \) and PMF:  
\[ P(X = k) = C_p \cdot k \cdot p^k \quad \text{for } p \in (0,1). \]  
Find \( C_p \).  

>**Solution:**  
Use the derivative of the geometric series:  
\[ \sum_{k=1}^\infty k p^k = \frac{p}{(1 - p)^2}. \]  
Thus:  
\[ C_p \cdot \frac{p}{(1 - p)^2} = 1 \implies C_p = \frac{(1 - p)^2}{p}. \]  

---

#### **Variation 4: Joint Distribution with Double Sum**  
**Exercise:**  
Let \( (X, Y) \) have support \( \mathbb{N}_0 \times \mathbb{N}_0 \) and joint PMF:  
\[ P(X = k, Y = j) = C \cdot \frac{2^k 3^j}{k! j!}. \]  
Find \( C \).  

>**Solution:**  
Separate sums using independence:  
\[ C \left( \sum_{k=0}^\infty \frac{2^k}{k!} \right) \left( \sum_{j=0}^\infty \frac{3^j}{j!} \right) = 1. \]  
Recognize \( e^2 \) and \( e^3 \):  
\[ C e^5 = 1 \implies C = e^{-5}. \]  

---

#### **Variation 5: Gamma Distribution via Gamma Function**  
**Exercise:**  
Let \( X \) be continuous with support \( (0, \infty) \) and PDF:  
\[ f(x) = C_{\alpha, \beta} \cdot x^{\alpha-1} e^{-\beta x} \quad \text{for } \alpha, \beta > 0. \]  
Find \( C_{\alpha, \beta} \).  

>**Solution:**  
Substitute \( u = \beta x \):  
\[ C_{\alpha, \beta} \int_0^\infty \left( \frac{u}{\beta} \right)^{\alpha-1} e^{-u} \frac{du}{\beta} = 1. \]  
Simplify and identify \( \Gamma(\alpha) \):  
\[ C_{\alpha, \beta} \cdot \frac{\Gamma(\alpha)}{\beta^\alpha} = 1 \implies C_{\alpha, \beta} = \frac{\beta^\alpha}{\Gamma(\alpha)}. \]  

---
# Part 2

## Original Exercise & Solution

**Exercise 5 (6 points)**  
Let \( X \) be a discrete random variable with support \( \{1,\ldots,N\} \), where \( N \geq 2 \) and \( N \) is even. Suppose \( X \) has PMF:  
$$
P(X=k) = C_N \cdot \max\{k, N-k\}, \quad \text{for } k=1,\ldots,N,
$$  
where \( C_N \in \mathbb{R} \). Find \( C_N \).

> ### Solution
> **Normalization Condition**:  
   \[
   \sum_{k=1}^N C_N \cdot \max\{k, N-k\} = 1  
   \]  
   **Split the Sum**:  
>   - For \( k \leq N/2 \): \( \max\{k, N-k\} = N-k \)  
>   - For \( k > N/2 \): \( \max\{k, N-k\} = k \)  
   Thus:  
   \[
   S = \underbrace{\sum_{k=1}^{N/2} (N - k)}_{\text{Sum 1}} + \underbrace{\sum_{k=N/2+1}^N k}_{\text{Sum 2}}
   \]  
>1. **Evaluate Sums**:  
>   - **Sum 1**: Arithmetic series \( (N-1) + (N-2) + \cdots + N/2 \)  
     \[
     \frac{N/2}{2} \left(\frac{N}{2} + (N-1)\right) = \frac{3N^2}{8} - \frac{N}{4}
     \]  
>   - **Sum 2**: Arithmetic series \( (N/2+1) + \cdots + N \)  
     \[
     \frac{N/2}{2} \left(\frac{N}{2} + 1 + N\right) = \frac{3N^2}{8} + \frac{N}{4}
     \]  
>2. **Total Sum \( S \)**:  
   \[
   S = \left(\frac{3N^2}{8} - \frac{N}{4}\right) + \left(\frac{3N^2}{8} + \frac{N}{4}\right) = \frac{3N^2}{4}
   \]  
>3. **Normalization Constant**:  
   \[
   C_N \cdot \frac{3N^2}{4} = 1 \implies C_N = \frac{4}{3N^2}
   \]  

---

## Progressive Variations

### Variation 1: Odd \( N \)  
**Exercise**:  
Same as original, but \( N \geq 3 \) is odd.  

>**Solution**:  
Split sums at \( k \leq (N-1)/2 \) (terms: \( N-1, \ldots, \frac{N+1}{2} \)) and \( k \geq (N+1)/2 \) (same terms).  
>\[
S = 2 \cdot \frac{(N+1)/2}{2}\left(\frac{N+1}{2} + N\right) = \frac{(N+1)(3N+1)}{4}  
\]  
\[
C_N = \frac{4}{(N+1)(3N+1)}
\]

---

### Variation 2: Sum of Squares  
**Exercise**:  
\( P(X=k) = C_N \cdot k^2 \) for support \( \{1,\ldots,N\} \).  

>**Solution**:  
Using \( \sum_{k=1}^N k^2 = \frac{N(N+1)(2N+1)}{6} \):  
\[
C_N = \frac{6}{N(N+1)(2N+1)}
\]  

---

### Variation 3: Symmetric Absolute Function  
**Exercise**:  
\( P(X=k) = C_N \cdot \left|k - \frac{N+1}{2}\right| \).  

>**Solution**:  
>- **Odd \( N \)**:  
  \[
  S = \frac{N^2 - 1}{4}, \quad C_N = \frac{4}{N^2 - 1}
  \]  
>- **Even \( N \)**:  
  \[
  S = \frac{N^2}{4}, \quad C_N = \frac{4}{N^2}
  \]  

---

### Variation 4: 2D Joint Distribution  
**Exercise**:  
\( (X,Y) \) on grid \( \{1,\ldots,N\}^2 \) with PMF \( P(X=k, Y=j) = C_N \cdot (k + j) \).  

>**Solution**:  
Double summation yields:  
\[
S = N \cdot \frac{N(N+1)}{2} + N \cdot \frac{N(N+1)}{2} = N^2(N+1)  
\]  
\[
C_N = \frac{1}{N^2(N+1)}
\]  

---

### Variation 5: Continuous 2D Square (Hardest)  
**Exercise**:  
\( (X,Y) \) on \( [0,L]^2 \) with PDF \( f(x,y) = C_L \cdot \max\{x,y\} \).  

>**Solution**:  
>1. Split domain via \( y = x \):  
   Lower triangle (\( \max\{x,y\} = x \)), upper triangle symmetric.  
>2. Compute integral:  
   \[
   S = 2 \int_0^L \left( \int_0^x x \, dy \right) dx = \frac{2L^3}{3}  
   \]  
>3. Normalization:  
   \[
   C_L = \frac{3}{2L^3}
   \]  

---

### Key Techniques
1. **Symmetry Splitting**: Divide sums/integrals at symmetry points (e.g., midpoint \( N/2 \), diagonal \( y = x \)).  
2. **Arithmetic Series**: \( \sum_{k=1}^n k = \frac{n(n+1)}{2} \), \( \sum k^2 = \frac{n(n+1)(2n+1)}{6} \).  
3. **Case Handling**: Separate solutions for even/odd \( N \).  
4. **Dimensionality**: Extend logic to joint PMFs/PDFs with multivariate summations/integrals.

---------------
# Part 3
### Variation 1 (Simplest)  
**Exercise (2 points)**  
Let \(X\) be a discrete random variable with support \(\{1, 2\}\). Suppose its probability mass function is given by \(P(X = k) = C \cdot k\) for \(k = 1, 2\). Find the constant \(C\).

> **Solution**  
> \(\sum_{k=1}^{2} P(X=k) = 1\)  
> \(C \cdot 1 + C \cdot 2 = 1\)  
> \(3C = 1\)  
> \(C = \frac{1}{3}\)

---

### Variation 2 (Slightly Harder)  
**Exercise (4 points)**  
Let \(X\) be a discrete random variable with support \(\{1, 2, 3\}\). The probability mass function is \(P(X = k) = C_3 \cdot |k - 1.5|\) for \(k = 1, 2, 3\). Find \(C_3\).

> **Solution**  
> Values: \(|1-1.5| = 0.5\), \(|2-1.5| = 0.5\), \(|3-1.5| = 1.5\)  
> Sum: \(0.5 + 0.5 + 1.5 = 2.5\)  
> \(C_3 \cdot 2.5 = 1\)  
> \(C_3 = \frac{2}{5}\)

---

### Variation 3 (Moderate)  
**Exercise (5 points)**  
Let \(X\) be a discrete random variable with support \(\{1, 2, 3, 4\}\). The probability mass function is \(P(X = k) = C_4 \cdot \max(k, 5 - k)\). Find \(C_4\).

> **Solution**  
> Values:  
> \(k=1: \max(1,4)=4\)  
> \(k=2: \max(2,3)=3\)  
> \(k=3: \max(3,2)=3\)  
> \(k=4: \max(4,1)=4\)  
> Sum: \(4+3+3+4=14\)  
> \(C_4 \cdot 14 = 1\)  
> \(C_4 = \frac{1}{14}\)

---

### Variation 4 (Challenging)  
**Exercise (7 points)**  
Let \(X\) be a discrete random variable with support \(\{1, \dots, N\}\), where \(N \geq 2\) is even. The probability mass function is \(P(X = k) = C_N \cdot \left| k - \frac{N}{2} \right|\). Find \(C_N\).

> **Solution**  
> Let \(m = N/2\)  
> Sum splits:  
> \(\sum_{k=1}^{m} (m - k) + \sum_{k=m+1}^{N} (k - m)\)  
> First sum: \(\sum_{j=0}^{m-1} j = \frac{(m-1)m}{2}\)  
> Second sum: \(\sum_{j=1}^{m} j = \frac{m(m+1)}{2}\)  
> Total: \(\frac{(m-1)m}{2} + \frac{m(m+1)}{2} = m^2\)  
> Substitute \(m = N/2\): Sum = \(N^2/4\)  
> \(C_N \cdot \frac{N^2}{4} = 1\)  
> \(C_N = \frac{4}{N^2}\)

---

### Variation 5 (Hardest)  
**Exercise (9 points)**  
Let \(X\) be a discrete random variable with support \(\{1, \dots, N\}\), where \(N \geq 4\) is even. The probability mass function is:  
\[
P(X = k) = C_N \cdot \left( \left| k - \frac{N}{2} \right| + 1 \right)
\]  
Find \(C_N\) and compute \(E[X]\).

> **Solution**  
> Let \(m = N/2\)  
> **Part 1: Find \(C_N\)**  
> Sum: \(\sum_{k=1}^{m} (m - k + 1) + \sum_{k=m+1}^{N} (k - m + 1)\)  
> First sum: \(\sum_{i=1}^{m} i = \frac{m(m+1)}{2}\)  
> Second sum: \(\sum_{j=1}^{m} (j + 1) = \frac{m(m+1)}{2} + m\)  
> Total: \(\frac{m(m+1)}{2} + \frac{m(m+1)}{2} + m = m^2 + 2m\)  
> Substitute \(m = N/2\): Sum = \(\frac{N^2}{4} + N\)  
> \(C_N \cdot \left( \frac{N^2}{4} + N \right) = 1\)  
> \(C_N = \frac{4}{N(N+4)}\)  
>  
> **Part 2: Compute \(E[X\)]**  
> \(E[X] = C_N \left[ \sum_{k=1}^{m} k(m - k + 1) + \sum_{k=m+1}^{N} k(k - m + 1) \right]\)  
> First sum: \((m+1)\sum k - \sum k^2 = \frac{m(m+1)^2}{2} - \frac{m(m+1)(2m+1)}{6} = \frac{m(m+1)(m+2)}{6}\)  
> Second sum: \(\sum (j+m)(j+1) = \frac{m(5m^2+15m+4)}{6}\) (after substitution \(j = k-m\))  
> Total inner sum: \(\frac{m(m+1)(m+2)}{6} + \frac{m(5m^2+15m+4)}{6} = m(m^2+3m+1)\)  
> \(E[X] = \frac{4}{N(N+4)} \cdot \frac{N}{2} \left( \frac{N^2}{4} + \frac{3N}{2} + 1 \right) = \frac{N^2 + 6N + 4}{2(N+4)}\)

# Normalization Constant Exercises for PMF/PDF 1
**Exercise 5 (6 points).**  
Let \( X \) be a discrete random variable with support \( \mathbb{N} = \{1, 2, 3, \dots\} \). Suppose \( X \) has law defined by:  
\[ P(X = k) = C_\theta \cdot \theta^{k+1}(1 - \theta)^{k-1} \quad \text{for } k \in \mathbb{N}, \; \theta \in (0,1), \]  
where \( C_\theta \in \mathbb{R} \). Find \( C_\theta \).
>**Solution:**  
The normalization condition requires summing probabilities over the support:  
\[ \sum_{k=1}^\infty C_\theta \theta^{k+1}(1 - \theta)^{k-1} = 1. \]  
Factorize \( \theta^2 \):  
\[ C_\theta \theta^2 \sum_{k=1}^\infty \left[\theta(1 - \theta)\right]^{k-1} = 1. \]  
Recognize the geometric series \( \sum_{k=1}^\infty r^{k-1} = \frac{1}{1 - r} \):  
\[ C_\theta \theta^2 \cdot \frac{1}{1 - \theta(1 - \theta)} = 1. \]  
Simplify the denominator (\( 1 - \theta + \theta^2 \)):  
\[ C_\theta = \frac{1 - \theta + \theta^2}{\theta^2}. \]  
---
### **Progressive Variations**  
#### **Variation 1: Geometric Distribution with Offset Support**  
**Exercise:**  
A discrete random variable \( X \) has support \( \{2, 3, 4, \dots\} \) and PMF:  
\[ P(X = k) = C_p (1 - p)^{k-1} \quad \text{for } p \in (0,1). \]  
Find \( C_p \).  
>**Solution:**  
Shift index \( j = k-1 \):  
\[ \sum_{j=1}^\infty C_p (1 - p)^j = 1. \]  
Geometric series sum:  
\[ C_p \cdot \frac{1 - p}{p} = 1 \implies C_p = \frac{p}{1 - p}. \]  
---
#### **Variation 2: Poisson Distribution via Taylor Series**  
**Exercise:**  
Let \( X \) have support \( \mathbb{N}_0 = \{0, 1, 2, \dots\} \) and PMF:  
\[ P(X = k) = C_\lambda \frac{\lambda^k}{k!} \quad \text{for } \lambda > 0. \]  
Find \( C_\lambda \).  
>**Solution:**  
Sum over support:  
\[ C_\lambda \sum_{k=0}^\infty \frac{\lambda^k}{k!} = 1. \]  
Recognize Taylor series for \( e^\lambda \):  
\[ C_\lambda e^\lambda = 1 \implies C_\lambda = e^{-\lambda}. \]  
---
#### **Variation 3: Weighted Geometric Series (Expectation Form)**  
**Exercise:**  
Let \( X \) have support \( \mathbb{N} \) and PMF:  
\[ P(X = k) = C_p \cdot k \cdot p^k \quad \text{for } p \in (0,1). \]  
Find \( C_p \).  
>**Solution:**  
Use the derivative of the geometric series:  
\[ \sum_{k=1}^\infty k p^k = \frac{p}{(1 - p)^2}. \]  
Thus:  
\[ C_p \cdot \frac{p}{(1 - p)^2} = 1 \implies C_p = \frac{(1 - p)^2}{p}. \]  
---
#### **Variation 4: Joint Distribution with Double Sum**  
**Exercise:**  
Let \( (X, Y) \) have support \( \mathbb{N}_0 \times \mathbb{N}_0 \) and joint PMF:  
\[ P(X = k, Y = j) = C \cdot \frac{2^k 3^j}{k! j!}. \]  
Find \( C \).  
>**Solution:**  
Separate sums using independence:  
\[ C \left( \sum_{k=0}^\infty \frac{2^k}{k!} \right) \left( \sum_{j=0}^\infty \frac{3^j}{j!} \right) = 1. \]  
Recognize \( e^2 \) and \( e^3 \):  
\[ C e^5 = 1 \implies C = e^{-5}. \]  
---
#### **Variation 5: Gamma Distribution via Gamma Function**  
**Exercise:**  
Let \( X \) be continuous with support \( (0, \infty) \) and PDF:  
\[ f(x) = C_{\alpha, \beta} \cdot x^{\alpha-1} e^{-\beta x} \quad \text{for } \alpha, \beta > 0. \]  
Find \( C_{\alpha, \beta} \).  
>**Solution:**  
Substitute \( u = \beta x \):  
\[ C_{\alpha, \beta} \int_0^\infty \left( \frac{u}{\beta} \right)^{\alpha-1} e^{-u} \frac{du}{\beta} = 1. \]  
Simplify and identify \( \Gamma(\alpha) \):  
\[ C_{\alpha, \beta} \cdot \frac{\Gamma(\alpha)}{\beta^\alpha} = 1 \implies C_{\alpha, \beta} = \frac{\beta^\alpha}{\Gamma(\alpha)}. \]  
---
# Part 2
## Original Exercise & Solution
**Exercise 5 (6 points)**  
Let \( X \) be a discrete random variable with support \( \{1,\ldots,N\} \), where \( N \geq 2 \) and \( N \) is even. Suppose \( X \) has PMF:  
$$
P(X=k) = C_N \cdot \max\{k, N-k\}, \quad \text{for } k=1,\ldots,N,
$$  
where \( C_N \in \mathbb{R} \). Find \( C_N \).
> ### Solution
> **Normalization Condition**:  
   \[
   \sum_{k=1}^N C_N \cdot \max\{k, N-k\} = 1  
   \]  
   **Split the Sum**:  
>   - For \( k \leq N/2 \): \( \max\{k, N-k\} = N-k \)  
>   - For \( k > N/2 \): \( \max\{k, N-k\} = k \)  
   Thus:  
   \[
   S = \underbrace{\sum_{k=1}^{N/2} (N - k)}_{\text{Sum 1}} + \underbrace{\sum_{k=N/2+1}^N k}_{\text{Sum 2}}
   \]  
>1. **Evaluate Sums**:  
>   - **Sum 1**: Arithmetic series \( (N-1) + (N-2) + \cdots + N/2 \)  
     \[
     \frac{N/2}{2} \left(\frac{N}{2} + (N-1)\right) = \frac{3N^2}{8} - \frac{N}{4}
     \]  
>   - **Sum 2**: Arithmetic series \( (N/2+1) + \cdots + N \)  
     \[
     \frac{N/2}{2} \left(\frac{N}{2} + 1 + N\right) = \frac{3N^2}{8} + \frac{N}{4}
     \]  
>2. **Total Sum \( S \)**:  
   \[
   S = \left(\frac{3N^2}{8} - \frac{N}{4}\right) + \left(\frac{3N^2}{8} + \frac{N}{4}\right) = \frac{3N^2}{4}
   \]  
>3. **Normalization Constant**:  
   \[
   C_N \cdot \frac{3N^2}{4} = 1 \implies C_N = \frac{4}{3N^2}
   \]  
---
## Progressive Variations
### Variation 1: Odd \( N \)  
**Exercise**:  
Same as original, but \( N \geq 3 \) is odd.  
>**Solution**:  
Split sums at \( k \leq (N-1)/2 \) (terms: \( N-1, \ldots, \frac{N+1}{2} \)) and \( k \geq (N+1)/2 \) (same terms).  
>\[
S = 2 \cdot \frac{(N+1)/2}{2}\left(\frac{N+1}{2} + N\right) = \frac{(N+1)(3N+1)}{4}  
\]  
\[
C_N = \frac{4}{(N+1)(3N+1)}
\]
---
### Variation 2: Sum of Squares  
**Exercise**:  
\( P(X=k) = C_N \cdot k^2 \) for support \( \{1,\ldots,N\} \).  
>**Solution**:  
Using \( \sum_{k=1}^N k^2 = \frac{N(N+1)(2N+1)}{6} \):  
\[
C_N = \frac{6}{N(N+1)(2N+1)}
\]  
---
### Variation 3: Symmetric Absolute Function  
**Exercise**:  
\( P(X=k) = C_N \cdot \left|k - \frac{N+1}{2}\right| \).  
>**Solution**:  
>- **Odd \( N \)**:  
  \[
  S = \frac{N^2 - 1}{4}, \quad C_N = \frac{4}{N^2 - 1}
  \]  
>- **Even \( N \)**:  
  \[
  S = \frac{N^2}{4}, \quad C_N = \frac{4}{N^2}
  \]  
---
### Variation 4: 2D Joint Distribution  
**Exercise**:  
\( (X,Y) \) on grid \( \{1,\ldots,N\}^2 \) with PMF \( P(X=k, Y=j) = C_N \cdot (k + j) \).  
>**Solution**:  
Double summation yields:  
\[
S = N \cdot \frac{N(N+1)}{2} + N \cdot \frac{N(N+1)}{2} = N^2(N+1)  
\]  
\[
C_N = \frac{1}{N^2(N+1)}
\]  
---
### Variation 5: Continuous 2D Square (Hardest)  
**Exercise**:  
\( (X,Y) \) on \( [0,L]^2 \) with PDF \( f(x,y) = C_L \cdot \max\{x,y\} \).  
>**Solution**:  
>1. Split domain via \( y = x \):  
   Lower triangle (\( \max\{x,y\} = x \)), upper triangle symmetric.  
>2. Compute integral:  
   \[
   S = 2 \int_0^L \left( \int_0^x x \, dy \right) dx = \frac{2L^3}{3}  
   \]  
>3. Normalization:  
   \[
   C_L = \frac{3}{2L^3}
   \]  
---
### Key Techniques
1. **Symmetry Splitting**: Divide sums/integrals at symmetry points (e.g., midpoint \( N/2 \), diagonal \( y = x \)).  
2. **Arithmetic Series**: \( \sum_{k=1}^n k = \frac{n(n+1)}{2} \), \( \sum k^2 = \frac{n(n+1)(2N+1)}{6} \).  
3. **Case Handling**: Separate solutions for even/odd \( N \).  
4. **Dimensionality**: Extend logic to joint PMFs/PDFs with multivariate summations/integrals.
---------------
# Part 3
### Variation 1 (Simplest)  
**Exercise (2 points)**  
Let \(X\) be a discrete random variable with support \(\{1, 2\}\). Suppose its probability mass function is given by \(P(X = k) = C \cdot k\) for \(k = 1, 2\). Find the constant \(C\).
> **Solution**  
> \(\sum_{k=1}^{2} P(X=k) = 1\)  
> \(C \cdot 1 + C \cdot 2 = 1\)  
> \(3C = 1\)  
> \(C = \frac{1}{3}\)
---
### Variation 2 (Slightly Harder)  
**Exercise (4 points)**  
Let \(X\) be a discrete random variable with support \(\{1, 2, 3\}\). The probability mass function is \(P(X = k) = C_3 \cdot |k - 1.5|\) for \(k = 1, 2, 3\). Find \(C_3\).
> **Solution**  
> Values: \(|1-1.5| = 0.5\), \(|2-1.5| = 0.5\), \(|3-1.5| = 1.5\)  
> Sum: \(0.5 + 0.5 + 1.5 = 2.5\)  
> \(C_3 \cdot 2.5 = 1\)  
> \(C_3 = \frac{2}{5}\)
---
### Variation 3 (Moderate)  
**Exercise (5 points)**  
Let \(X\) be a discrete random variable with support \(\{1, 2, 3, 4\}\). The probability mass function is \(P(X = k) = C_4 \cdot \max(k, 5 - k)\). Find \(C_4\).
> **Solution**  
> Values:  
> \(k=1: \max(1,4)=4\)  
> \(k=2: \max(2,3)=3\)  
> \(k=3: \max(3,2)=3\)  
> \(k=4: \max(4,1)=4\)  
> Sum: \(4+3+3+4=14\)  
> \(C_4 \cdot 14 = 1\)  
> \(C_4 = \frac{1}{14}\)
---
### Variation 4 (Challenging)  
**Exercise (7 points)**  
Let \(X\) be a discrete random variable with support \(\{1, \dots, N\}\), where \(N \geq 2\) is even. The probability mass function is \(P(X = k) = C_N \cdot \left| k - \frac{N}{2} \right|\). Find \(C_N\).
> **Solution**  
> Let \(m = N/2\)  
> Sum splits:  
> \(\sum_{k=1}^{m} (m - k) + \sum_{k=m+1}^{N} (k - m)\)  
> First sum: \(\sum_{j=0}^{m-1} j = \frac{(m-1)m}{2}\)  
> Second sum: \(\sum_{j=1}^{m} j = \frac{m(m+1)}{2}\)  
> Total: \(\frac{(m-1)m}{2} + \frac{m(m+1)}{2} = m^2\)  
> Substitute \(m = N/2\): Sum = \(N^2/4\)  
> \(C_N \cdot \frac{N^2}{4} = 1\)  
> \(C_N = \frac{4}{N^2}\)
---
### Variation 5 (Hardest)  
**Exercise (9 points)**  
Let \(X\) be a discrete random variable with support \(\{1, \dots, N\}\), where \(N \geq 4\) is even. The probability mass function is:  
\[
P(X = k) = C_N \cdot \left( \left| k - \frac{N}{2} \right| + 1 \right)
\]  
Find \(C_N\) and compute \(E[X]\).
> **Solution**  
> Let \(m = N/2\)  
> **Part 1: Find \(C_N\)**  
> Sum: \(\sum_{k=1}^{m} (m - k + 1) + \sum_{k=m+1}^{N} (k - m + 1)\)  
> First sum: \(\sum_{i=1}^{m} i = \frac{m(m+1)}{2}\)  
> Second sum: \(\sum_{j=1}^{m} (j + 1) = \frac{m(m+1)}{2} + m\)  
> Total: \(\frac{m(m+1)}{2} + \frac{m(m+1)}{2} + m = m^2 + 2m\)  
> Substitute \(m = N/2\): Sum = \(\frac{N^2}{4} + N\)  
> \(C_N \cdot \left( \frac{N^2}{4} + N \right) = 1\)  
> \(C_N = \frac{4}{N(N+4)}\)  
>  
> **Part 2: Compute \(E[X\)]**  
> \(E[X] = C_N \left[ \sum_{k=1}^{m} k(m - k + 1) + \sum_{k=m+1}^{N} k(k - m + 1) \right]\)  
> First sum: \((m+1)\sum k - \sum k^2 = \frac{m(m+1)^2}{2} - \frac{m(m+1)(2m+1)}{6} = \frac{m(m+1)(m+2)}{6}\)  
> Second sum: \(\sum (j+m)(j+1) = \frac{m(5m^2+15m+4)}{6}\) (after substitution \(j = k-m\))  
> Total inner sum: \(\frac{m(m+1)(m+2)}{6} + \frac{m(5m^2+15m+4)}{6} = m(m^2+3m+1)\)  
> \(E[X] = \frac{4}{N(N+4)} \cdot \frac{N}{2} \left( \frac{N^2}{4} + \frac{3N}{2} + 1 \right) = \frac{N^2 + 6N + 4}{2(N+4)}\)
---
### Variation 6 (Min Function on Small Support)
**Exercise (4 points)**  
Let \(X\) be a discrete random variable with support \(\{1, 2, 3, 4\}\). Its probability mass function is given by \(P(X = k) = C \cdot \min(k, 3)\) for \(k \in \{1, 2, 3, 4\}\). Find the constant \(C\).
> **Solution**  
> The normalization condition is \(\sum_{k=1}^{4} P(X=k) = 1\).  
> We evaluate \(P(X=k)\) for each \(k\) in the support:  
> \(P(X=1) = C \cdot \min(1, 3) = C \cdot 1 = C\)  
> \(P(X=2) = C \cdot \min(2, 3) = C \cdot 2 = 2C\)  
> \(P(X=3) = C \cdot \min(3, 3) = C \cdot 3 = 3C\)  
> \(P(X=4) = C \cdot \min(4, 3) = C \cdot 3 = 3C\)  
> Summing these probabilities:  
> \(C + 2C + 3C + 3C = 1\)  
> \(9C = 1\)  
> \(C = \frac{1}{9}\)
---
### Variation 7 (Simple Linear PDF)
**Exercise (3 points)**  
Let \(X\) be a continuous random variable with support on the interval \([0, 2]\). Its probability density function is \(f(x) = C \cdot x\) for \(x \in [0, 2]\). Find the constant \(C\).
> **Solution**  
> For a PDF, the normalization condition is \(\int_{-\infty}^{\infty} f(x) dx = 1\).  
> Given the support is \([0, 2]\), this becomes \(\int_0^2 C \cdot x \, dx = 1\).  
> \(C \int_0^2 x \, dx = 1\)  
> \(C \left[ \frac{x^2}{2} \right]_0^2 = 1\)  
> \(C \left( \frac{2^2}{2} - \frac{0^2}{2} \right) = 1\)  
> \(C \left( \frac{4}{2} - 0 \right) = 1\)  
> \(2C = 1\)  
> \(C = \frac{1}{2}\)
---
### Variation 8 (Symmetric Quadratic PMF)
**Exercise (4 points)**  
Let \(X\) be a discrete random variable with support \(\{-2, -1, 0, 1, 2\}\). The probability mass function is \(P(X=k) = C \cdot (k^2 + 1)\) for \(k \in \{-2, -1, 0, 1, 2\}\). Find \(C\).
> **Solution**  
> The normalization condition is \(\sum_{k=-2}^{2} P(X=k) = 1\).  
> We evaluate \(P(X=k)\) for each \(k\):  
> \(P(X=-2) = C \cdot ((-2)^2 + 1) = C \cdot (4 + 1) = 5C\)  
> \(P(X=-1) = C \cdot ((-1)^2 + 1) = C \cdot (1 + 1) = 2C\)  
> \(P(X=0) = C \cdot (0^2 + 1) = C \cdot (0 + 1) = C\)  
> \(P(X=1) = C \cdot (1^2 + 1) = C \cdot (1 + 1) = 2C\)  
> \(P(X=2) = C \cdot (2^2 + 1) = C \cdot (4 + 1) = 5C\)  
> Summing these probabilities:  
> \(5C + 2C + C + 2C + 5C = 1\)  
> \(15C = 1\)  
> \(C = \frac{1}{15}\)
---
### Variation 9 (Finite Geometric Series PMF)
**Exercise (6 points)**  
Let \(X\) be a discrete random variable with support \(\{0, 1, \dots, N-1\}\) for some integer \(N \geq 1\). The probability mass function is \(P(X=k) = C \cdot \left(\frac{1}{2}\right)^k\). Find \(C\).
> **Solution**  
> The normalization condition is \(\sum_{k=0}^{N-1} P(X=k) = 1\).  
> So, \(\sum_{k=0}^{N-1} C \cdot \left(\frac{1}{2}\right)^k = 1\).  
> \(C \sum_{k=0}^{N-1} \left(\frac{1}{2}\right)^k = 1\).  
> The sum is a finite geometric series \(\sum_{k=0}^{n-1} r^k = \frac{1-r^n}{1-r}\). Here, \(n=N\) and \(r=1/2\).  
> \(\sum_{k=0}^{N-1} \left(\frac{1}{2}\right)^k = \frac{1 - (1/2)^N}{1 - 1/2} = \frac{1 - 2^{-N}}{1/2} = 2(1 - 2^{-N})\).  
> So, \(C \cdot 2(1 - 2^{-N}) = 1\).  
> \(C = \frac{1}{2(1 - 2^{-N})} = \frac{1}{2 - 2^{1-N}}\).  
> This can also be written as \(C = \frac{2^{N-1}}{2^N - 1}\).
---
### Variation 10 (Continuous PDF with Max Function)
**Exercise (7 points)**  
Let \(X\) be a continuous random variable with support on the interval \([0, 1]\). Its probability density function is \(f(x) = C \cdot \max(x, 1-x)\) for \(x \in [0, 1]\). Find \(C\).
> **Solution**  
> The normalization condition is \(\int_0^1 f(x) \, dx = 1\).  
> We need to understand the function \(\max(x, 1-x)\) on \([0, 1]\).  
> The term \(1-x\) is greater than or equal to \(x\) when \(1-x \geq x \implies 1 \geq 2x \implies x \leq 1/2\).  
> The term \(x\) is greater than \(1-x\) when \(x > 1-x \implies 2x > 1 \implies x > 1/2\).  
> So, \(\max(x, 1-x) = \begin{cases} 1-x & \text{if } 0 \leq x \leq 1/2 \\ x & \text{if } 1/2 < x \leq 1 \end{cases}\).  
> We split the integral based on this:  
> \(\int_0^1 C \cdot \max(x, 1-x) \, dx = C \left( \int_0^{1/2} (1-x) \, dx + \int_{1/2}^1 x \, dx \right) = 1\).  
> Calculate the first integral:  
> \(\int_0^{1/2} (1-x) \, dx = \left[ x - \frac{x^2}{2} \right]_0^{1/2} = \left( \frac{1}{2} - \frac{(1/2)^2}{2} \right) - 0 = \frac{1}{2} - \frac{1/8} = \frac{4-1}{8} = \frac{3}{8}\).  
> Calculate the second integral:  
> \(\int_{1/2}^1 x \, dx = \left[ \frac{x^2}{2} \right]_{1/2}^1 = \frac{1^2}{2} - \frac{(1/2)^2}{2} = \frac{1}{2} - \frac{1/8} = \frac{3}{8}\).  
> So, \(C \left( \frac{3}{8} + \frac{3}{8} \right) = 1\).  
> \(C \left( \frac{6}{8} \right) = 1\).  
> \(C \left( \frac{3}{4} \right) = 1\).  
> \(C = \frac{4}{3}\).
---