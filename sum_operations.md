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
  \[\sum_{k=1}^{n} k  = \frac{n(n+1)}{2}\]
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

### Quick Reference Table

| Sum                          | Closed Form                                  | Conditions                     |
|------------------------------|----------------------------------------------|--------------------------------|
| \(\sum\limits_{k=1}^{n} k\)     | \(\dfrac{n(n+1)}{2}\)                       | \(n \geq 1\)                  |
| \(\sum\limits_{k=1}^{n} k^2\)   | \(\dfrac{n(n+1)(2n+1)}{6}\)                 | \(n \geq 1\)                  |
| \(\sum\limits_{k=1}^{n} k^3\)   | \(\left[\dfrac{n(n+1)}{2}\right]^2\)          | \(n \geq 1\)                  |
| \(\sum\limits_{k=0}^{n} r^k\)   | \(\dfrac{1-r^{n+1}}{1-r}\)                  | \(r \neq 1\)                  |
| \(\sum\limits_{k=0}^{n} k r^k\) | \(r \dfrac{1 - (n+1)r^n + n r^{n+1}}{(1-r)^2}\) | \(r \neq 1\)           |
| \(\sum\limits_{k=0}^{n} \binom{n}{k}\)     | \(2^n\)                                    | \(n \geq 0\)                  |
| \(\sum\limits_{k=0}^{n} k \binom{n}{k}\)   | \(n \cdot 2^{n-1}\)                         | \(n \geq 1\)                  |
| \(\sum\limits_{k=0}^{n} k^2 \binom{n}{k}\) | \(n(n+1) \cdot 2^{n-2}\)                    | \(n \geq 2\)                  |
| \(\sum\limits_{k=0}^{m} \binom{n}{k}\)     | No closed form; use approximations          | \(0 \leq m \leq n\)           |

| **Series Type**              | **Sum/Result**                                | **Key Trick/Approach**                                         | **Conditions/Comments**                |
|-----------------------------|---------------------------------------------|---------------------------------------------------------------|----------------------------------------|
| Geometric                   | \(\sum_{n=0}^\infty r^n = \frac{1}{1-r}\)  | Identify pattern \(1 + r + r^2 + \cdots\)                     | \(\|r\| < 1\)                          |
| Geometric (negative exponent, n≥0)    | \(\sum_{n=0}^\infty r^{-n} = \frac{r}{r - 1}\)  | Pattern: \(1 + r^{-1} + r^{-2} + \cdots\)  | \(r \in (-\infty, -1) \cup (1, \infty)\)  |
| Geometric (shifted)                   | \(\sum_{n=1}^\infty r^n = \frac{r}{1-r}\)  | Identify pattern \( r + r^2 + \cdots\)                     | a∈(0,1)                          |
| Geometric (shifted, neg)  | \(\sum_{n=1}^\infty r^{-n} = \frac{1}{r - 1}\)  | Pattern: \(r^{-1} + r^{-2} + \cdots\)  | \(r \in (-\infty, -1) \cup (1, \infty)\)  |
| Geometric (general)                   | \(\sum_{n=0}^\infty ar^n = \frac{a}{1-r}\)  | First term is a. Common ratio is r.                    | \(\|r\| < 1\)                          |
| Arith.-Geometric Series       | \(\sum_{n=1}^\infty nr^n = \frac{r}{(1-r)^2}\)  | -                    | $\$                          |
| Arith.-Geometric Series       | \(\sum_{n=1}^\infty n^2r^n = \frac{r(1+r)}{(1-r)^3}\)  | -                    | $\$                          |
| Telescoping                 | \(\sum_{n=1}^\infty \left(\frac{1}{n} - \frac{1}{n+1}\right) = 1\) | Partial fractions \(\frac{1}{n(n+1)} = \frac{1}{n} - \frac{1}{n+1}\) | Cancellation leaves first/last terms   |
| \(p\)-series                | \(\sum_{n=1}^\infty \frac{1}{n^p}\) converges if \(p > 1\) | Compare to integral \(\int_1^\infty x^{-p}dx\)               | Diverges if \(p \leq 1\)               |
| Alternating Series          | \(\sum_{n=1}^\infty (-1)^{n+1}\frac{1}{n} = \ln 2\) | Leibniz test: terms \(\downarrow\) to 0                       | Error \(\leq \|a_{n+1}\|\)             |
| Basel Problem (\(\zeta(2)\))| \(\sum_{n=1}^\infty \frac{1}{n^2} = \frac{\pi^2}{6}\) | Fourier series of \(f(x)=x^2\) or Parseval's theorem         | Generalizes to \(\zeta(2k)\)           |
| Exponential                 | \(\sum_{n=0}^\infty \frac{x^n}{n!} = e^x\)  | Taylor series expansion at \(x=0\)                            | 
| Exponential (Reciprocal Factorial) | \(\sum_{n=0}^\infty \frac{1}{n!} = e\) | Taylor series of \(e^x\) evaluated at \(x=1\) | Core definition of \(e\); converges absolutely |Converges \(\forall x \in \mathbb{C}\) |
| Harmonic Variant            | \(\sum_{n=1}^\infty \frac{1}{n(n+1)} = 1\)  | Partial fractions \(\frac{1}{n} - \frac{1}{n+1}\)             | Telescopes completely                  |
| Generating Function         | \(\sum_{n=0}^\infty \binom{2n}{n}x^n = \frac{1}{\sqrt{1-4x}}\) | Binomial theorem or hypergeometric identities              | \(\|x\| < \frac{1}{4}\)                |
| Leibniz (Arctangent)        | \(\sum_{n=0}^\infty \frac{(-1)^n}{2n+1} = \frac{\pi}{4}\) | Integrate \(\sum (-1)^n x^{2n} = \frac{1}{1+x^2}\)            | \(\tan^{-1}(1)\) special case          |
| Logarithmic                 | \(\sum_{n=1}^\infty \frac{x^n}{n} = -\ln(1-x)\) | Integrate geometric series term-by-term                       | \(-1 \leq x < 1\)                      |
| Zeta at Even Integers       | \(\zeta(2k) = (-1)^{k+1}\frac{B_{2k}(2\pi)^{2k}}{2(2k)!}\) | Bernoulli numbers \(B_n\) (e.g., \(B_2=\frac{1}{6}\))       | \(\zeta(4)=\frac{\pi^4}{90}\)          |
| Gaussian-like Sums          | \(\sum_{n=-\infty}^\infty e^{-an^2} = \sqrt{\frac{\pi}{a}}\) | Poisson summation or completing the square                   | Relates to theta functions             |
| Euler-Maclaurin            | \(\sum_{k=1}^n f(k) \approx \int f + \frac{f(1)+f(n)}{2} + \frac{B_2}{2!}(f'(n)-f'(1)) + \cdots\) | Approximate sums via integrals + corrections | Useful for asymptotic analysis        |

</body>
</html>
