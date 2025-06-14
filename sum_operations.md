<!DOCTYPE html>
<html>
<head>
    <script src='https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js'></script>
</head>
<body>
    
### Cheat Sheet: Key Sum Operations in Probability & Analysis

---

#### **1. Geometric Series**
- **Convergence Condition**: Infinite geometric series converge **only if** \(|r| < 1\).
- **Finite Geometric Series** (for \(|r| \neq 1\)):  
  \[\sum_{k=0}^{n} r^k = \frac{1 - r^{n+1}}{1 - r}\]
- **Infinite Geometric Series**:  
  \[\sum_{k=0}^{\infty} r^k = \frac{1}{1 - r}\]  
  (e.g., \(\sum_{n=1}^{\infty} \frac{1}{3^n} = \frac{\frac{1}{3}}{1 - \frac{1}{3}} = \frac{1}{2}\))
- **Variants**:
  - Start at \(k = m\): \(\sum_{k=m}^{\infty} r^k = \frac{r^m}{1 - r}\)
  - Constant in numerator: \(\sum_{n=1}^{\infty} a r^n = \frac{a r}{1 - r}\) (for \(|r|<1\))

---

#### **2. Arithmetic Series**
- **Sum of First \(n\) Integers**:  
  \[\sum_{k=1}^{n} k = 1 + 2 + \dots + n = \frac{n(n+1)}{2}\]
- **Sum of Squares**:  
  \[\sum_{k=1}^{n} k^2 = \frac{n(n+1)(2n+1)}{6}\]
- **Sum of Cubes**:  
  \[\sum_{k=1}^{n} k^3 = \left( \frac{n(n+1)}{2} \right)^2\]

---

#### **3. Special Infinite Series** (for \(|r| < 1\))
- **Linear multiplier**:  
  \[\sum_{k=1}^{\infty} k r^{k} = r \frac{d}{dr} \left( \sum_{k=0}^{\infty} r^k \right) = \frac{r}{(1-r)^2}\]
- **Squared multiplier**:  
  \[\sum_{k=1}^{\infty} k^2 r^{k} = \frac{r(1+r)}{(1-r)^3}\]
- **Exponential Series**:  
  \[\sum_{k=0}^{\infty} \frac{x^k}{k!} = e^x\]
- **Harmonic Series** (divergent):  
  \[\sum_{k=1}^{\infty} \frac{1}{k} = \infty\]

---

#### **4. \(p\)-Series & Convergence Tests**
- **\(p\)-Series Test**:  
  \(\sum_{n=1}^{\infty} \frac{1}{n^p}\) **converges** if \(p > 1\) (e.g., \(\sum \frac{1}{n^2} = \frac{\pi^2}{6}\)), **diverges** if \(p \leq 1\).  
- **Integral Test**:  
  If \(f(n) > 0\) and decreasing, \(\sum_{n=1}^{\infty} f(n)\) converges \(\iff \int_{1}^{\infty} f(x)  dx\) converges.

---

#### **5. Binomial & Taylor Series**
- **Binomial Expansion**:  
  \[(1 + x)^n = \sum_{k=0}^{n} \binom{n}{k} x^k\]  
  For \(|x| < 1\) and real \(\alpha\): \((1+x)^\alpha = \sum_{k=0}^{\infty} \binom{\alpha}{k} x^k\).  
- **Sum of Binomial Coefficients**:  
  \[\sum_{k=0}^{n} \binom{n}{k} = 2^n, \quad \sum_{k=0}^{n} \binom{n}{k} r^k = (1+r)^n\]

---

#### **6. Telescoping Series**
- **Key Trick**: Partial fraction decomposition to cancel terms.  
- **Example**:  
  \[\sum_{n=1}^{\infty} \frac{1}{n(n+1)} = \sum_{n=1}^{\infty} \left( \frac{1}{n} - \frac{1}{n+1} \right) = 1\]

---

### **Rules of Thumb**:
1. **Normalization Check**: For probability, always verify \(\sum_{\text{all } \omega} P(\omega) = 1\).
2. **Convergence**: For any series, confirm convergence before applying closed-form formulas.
3. **Shift Indices**: Adjust indices to match standard forms (e.g., shift \(n \to n+1\)).
4. **Differentiation/Integration**: Useful to derive sums (e.g., differentiate \(\sum r^k\) to get \(\sum k r^{k-1}\)).

---

**Usage Example**:  
To compute \(\sum_{n=1}^{\infty} n \left(\frac{1}{2}\right)^n\):  
- Recognize \(|r| = \frac{1}{2} < 1\) → series converges.  
- Apply \(\sum_{n=1}^{\infty} n r^n = \frac{r}{(1-r)^2}\) with \(r = \frac{1}{2}\):  
  \[
  \text{Sum} = \frac{\frac{1}{2}}{\left(1 - \frac{1}{2}\right)^2} = \frac{\frac{1}{2}}{\frac{1}{4}} = 2
  \]  

> **Keep this sheet handy for probability normalizations, expectation calculations, and series convergence checks!** 
</body>
</html>
