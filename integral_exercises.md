### Exercises 1

1. \(\int_{[-1,1]} x \, \lambda(dx)\), where \(\lambda\) is Lebesgue measure on \(\mathbb{R}\).

> \(\int_{-1}^1 x\, dx = 0\) (odd function over symmetric interval).

2. \(\int x^2 \, P(dx)\), where \(P(A) = (1-p)\delta_0(A) + p\delta_1(A)\), \(p \in (0,1)\).

> \((1-p)(0-p)^2 + p(1-p)^2 = p(1-p)\).

3. \(\int_1^e \log(x) \, \lambda(dx)\), where \(\lambda\) is Lebesgue measure.

> \(\int_1^e \log x \, dx = [x \log x - x]_1^e = (e \cdot 1 - e) - (1\cdot0 - 1) = 1\).

4. \(\int_{\{1,2,3\}} x \, \mu(dx)\), where \(\mu\) is counting measure on \(\mathcal{P}(\mathbb{N})\).

> \(\sum_{x=1}^3 x = 6\).

5. \(\int_{\mathbb{N} \times \mathbb{N}} 3^{-(x+y)} \, m(d(x,y))\), where \(m\) is counting measure on \(\mathcal{P}(\mathbb{N} \times \mathbb{N})\).

> \(\sum_{x=0}^\infty \sum_{y=0}^\infty 3^{-(x+y)} = \left(\sum_{x=0}^\infty 3^{-x}\right)^2 = \left(\frac{1}{1 - \frac{1}{3}}\right)^2 = \left(\frac{3}{2}\right)^2 = \frac{9}{4}\).

6. \(\int_{\mathbb{R}} x \, \mu(dx)\), where \(\mu(A) = \sum_{x=0}^\infty \frac{e^{-2} 2^x}{x!} \delta_x(A)\).

> Expectation of \(\text{Poisson}(2)\): \(2\).

7. \(\int_{[0,2]} x^3 \, \lambda(dx)\).

> \(\int_0^2 x^3 dx = \frac{2^4}{4} = 4\).

8. \(\int (x-p)^3 \, P(dx)\), same \(P\) as exercise 2.

> \((1-p)(0-p)^3 + p(1-p)^3 = p(1-p)(1-2p)\).

9. \(\int_0^1 \frac{1}{1+x^2} \, \lambda(dx)\).

> \(\int_0^1 \frac{1}{1+x^2} dx = \arctan(1) - \arctan(0) = \frac{\pi}{4}\).

10. \(\sum_{k=1}^\infty \frac{k}{2^k}\), interpreting as \(\int f(k) m(dk)\), \(m\) counting measure on \(\mathbb{N}\).

> \(\sum_{k=1}^\infty \frac{k}{2^k} = 2\).

11. \(\int_{\mathbb{N}} (x!)^{-1} e^{-1} \, \mu(dx)\), \(\mu\) as in exercise 6 with parameter 1.

> \(\sum_{x=0}^\infty \frac{e^{-1} 1^x}{x!} = 1\) (total probability of Poisson(1)).

12. \(\int_{\mathbb{N} \times \{0,1\}} 4^{-(x+y)} \, m(d(x,y))\), \(m\) counting measure.

> \(\sum_{x=0}^\infty \sum_{y=0}^1 4^{-(x+y)} = \left(\sum_{x=0}^\infty 4^{-x}\right) \left(\sum_{y=0}^1 4^{-y}\right) = \frac{4}{3} \times \frac{1 + \frac{1}{4}}{1} = \frac{4}{3} \times \frac{5}{4} = \frac{5}{3}\).

13. \(\int_0^\infty x e^{-x} \, \lambda(dx)\).

> \(\int_0^\infty x e^{-x} dx = 1\) (Gamma(2) moment).

14. \(\int_{\{0,1\}^n} \sum_{i=1}^n x_i \, \mu(dx)\), \(\mu\) counting measure on \(\{0,1\}^n\).

> \(\sum_{x \in \{0,1\}^n} \sum_{i=1}^n x_i = n \cdot 2^{n-1}\) (each coordinate is 1 half the time).

15. \(\int_{\mathbb{R}} e^{-x^2} \, \lambda(dx)\) over \(\mathbb{R}\).

> No elementary closed form, integral known as \(\sqrt{\pi}\).

16. \(\int_{\mathbb{N}} x^2 \frac{\lambda^x e^{-\lambda}}{x!} \delta_x(dx)\), Poisson weight with parameter \(\lambda\).

> \(\lambda + \lambda^2\) (variance plus squared mean of Poisson).

17. \(\int_0^1 x \log(x) \, \lambda(dx)\).

> \(\int_0^1 x \log x dx = -\frac{1}{4}\).

18. \(\int_{[0,1]^2} (x^2 + y^2) \, \lambda(dxdy)\).

> \(\int_0^1 \int_0^1 (x^2 + y^2) dy dx = 2 \times \frac{1}{3} = \frac{2}{3}\).

19. \(\int_{\mathbb{N} \times \mathbb{N}} (xy)^{-1} 2^{-(x+y)} \, m(d(x,y))\), \(x,y \ge 1\).

> \(\left(\sum_{x=1}^\infty \frac{2^{-x}}{x}\right)^2\) (square of the polylog \(Li_1(1/2) = -\log(1 - 1/2) = \log 2\)), approx \((\log 2)^2\).

20. \(\int_0^\infty \frac{\sin x}{x} \, \lambda(dx)\).

> \(\int_0^\infty \frac{\sin x}{x} dx = \frac{\pi}{2}\).

---
### Exercises 2

1. **\(\int_{[0,1]} d\lambda(x)\)**, where \(\lambda\) is Lebesgue measure on \(\mathcal{B}(\mathbb{R})\).

> **Solution:** \(1\)  
*(Simple Lebesgue measure of an interval.)*

2. **\(\int_{\mathbb{R}} |x| \delta_0(dx)\)**, where \(\delta_0\) is the Dirac measure at 0.

> **Solution:** \(0\)  
*(Dirac measure evaluation at a point.)*

3. **\(\int_A d\mu(x)\)**, where \(A = \{1,2,3\}\) and \(\mu\) is the counting measure on \(\mathcal{B}(\mathbb{Z})\).

> **Solution:** \(3\)  
*(Counting measure on a finite set.)*

4. **\(\int_{\mathbb{R}} x^2 (\delta_2 + \delta_3)(dx)\)**.

> **Solution:** \(13\) (since \(2^2 + 3^2 = 4 + 9\))  
*(Sum of Dirac measures.)*

5. **\(\int_{[0,\infty)} e^{-x} \lambda(dx)\)**, where \(\lambda\) is Lebesgue measure.

> **Solution:** \(1\)  
*(Exponential integral over Lebesgue measure.)*

6. **\(\int_{\mathbb{R}} (x-p)^2 P(dx)\)**, where \(P = (1-p)\delta_0 + p\delta_1\) for \(p \in (0,1)\).

> **Solution:** \(p(1-p)\)  
*(Variance of a Bernoulli distribution.)*

7. **\(\int_{\mathbb{N}} e^{-x} \mu(dx)\)**, where \(\mu\) is the counting measure on \(\mathbb{N} = \{0,1,2,\ldots\}\).

> **Solution:** \(\frac{e}{e-1}\)  
*(Geometric series under counting measure.)*

8. **\(\int_{[0,1]\times[0,1]} (x+y)(\lambda\times\lambda)(d(x,y))\)**, where \(\lambda\times\lambda\) is the product measure.

> **Solution:** \(1\)  
*(Double integral with linear function.)*

9. **\(\int_{\mathbb{R}} x \mu(dx)\)**, where \(\mu = \sum_{k=0}^\infty \frac{1}{2^{k+1}}\delta_k\).

> **Solution:** \(1\)  
*(Expected value of a discrete distribution.)*

10. **\(\int_{\mathbb{N}\times\mathbb{N}} e^{-(x+y)}(\mu\times\mu)(d(x,y))\)**, where \(\mu\) is the counting measure on \(\mathbb{N}\).

> **Solution:** \(\left(\frac{e}{e-1}\right)^2\)  
*(Product measure and separable function.)*

11. **\(\int_{\mathbb{R}} x \nu(dx)\)**, where \(d\nu = \frac{1}{\sqrt{2\pi}} e^{-x^2/2} dx\) (standard Gaussian measure).

> **Solution:** \(0\)  
*(Symmetry of Gaussian measure.)*

12. **\(\int_{[0,\infty)} x^2 \mu(dx)\)**, where \(d\mu = 2e^{-2x} dx\).

> **Solution:** \(\frac{1}{2}\)  
*(Exponential distribution second moment.)*

13. **\(\int_{[-2,2]} |x| \lambda(dx)\)**, where \(\lambda\) is Lebesgue measure.

> **Solution:** \(4\)  
*(Integral of absolute value over symmetric interval.)*

14. **\(\int_{[-1,1]} 1 \mu(dx)\)**, where \(d\mu = |x| dx\).

> **Solution:** \(1\)  
*(Integration against a weighted Lebesgue measure.)*

15. **\(\int_{\mathbb{R}} e^{-|x|} \lambda(dx)\)**.

> **Solution:** \(2\)  
*(Double-sided exponential integral.)*

16. **\(\int_{\mathbb{N}} (x-1)^2 P(dx)\)**, where \(P\) is Poisson measure with mean 1: \(P(\{k\}) = \frac{e^{-1}}{k!}\) for \(k \in \mathbb{N}_0\).

> **Solution:** \(1\)  
*(Variance of Poisson distribution.)*

17. **\(\int_{[0,1]} x \nu(dx)\)**, where \(\nu = g_*\lambda\) is the pushforward of Lebesgue measure \(\lambda\) on \([0,1]\) under \(g(x) = x^2\).

> **Solution:** \(\frac{1}{3}\)  
*(Pushforward measure and change of variables.)*

18. **\(\int_{\mathbb{Z}} |x| e^{-|x|} \mu(dx)\)**, where \(\mu\) is the counting measure on \(\mathbb{Z}\).

> **Solution:** \(\frac{2e}{(e-1)^2}\)  
*(Series involving absolute values and exponential decay.)*

19. **\(\int_{\mathbb{R}} x \mu(dx)\)**, where \(\mu = \delta_0 + \lambda|_{[1,2]}\) (Lebesgue measure restricted to \([1,2]\)).

> **Solution:** \(\frac{3}{2}\)  
*(Mixed discrete-continuous measure.)*

20. **\(\int_{[0,\infty)\times[0,\infty)} |x-y| e^{-x} e^{-y} (\lambda\times\lambda)(d(x,y))\)**.

> **Solution:** \(1\)  
*(Expected absolute difference of two i.i.d. exponential variables.)*
## Measure-Theoretic Integral Patterns Cheat Sheet

### Basic Measure Integrals
| Measure Type          | Domain             | Integrand    | Result     | Notes                                  |
|-----------------------|--------------------|--------------|------------|----------------------------------------|
| **Lebesgue (λ)**      | [-a, a]          | Odd f(x)     | 0          | f(-x) = -f(x) symmetry                 |
|                       | [a, b]          | 1            | b - a      | Interval length                        |
|                       | [0, ∞)          | e⁻ˣ          | 1          | Exponential decay                     |
|                       | ℝ               | e⁻ˣ²         | √π         | Gaussian integral                     |
|                       | [0, 1]          | 1/(1+x²)     | π/4        | Arctangent primitive                  |
|                       | [1, e]          | ln x         | 1          | Integration by parts                  |
|                       | [0, 1]          | x ln x       | -1/4       | Gamma function relation               |
|                       | [0, ∞)          | x e⁻ˣ        | 1          | Γ(2) = 1!                             |
|                       | [0, ∞)          | sin(x)/x     | π/2        | Dirichlet integral                    |
|                       | [-a, a]         | \|x\|        | a²         |                                        |
|                       | [0,1]×[0,1]     | x² + y²      | 2/3        | Fubini's theorem                      |
 **Dirac (δ)**         | Any             | f(x)         | f(a)       | Point evaluation at a                |
|                       | ℝ               | \|x\|        | \|a\|       |                                      |
|                       | ℝ               | x² (cδₐ + dδ_b) | ca² + db²   | Linear combination                  |
| **Counting (μ)**      | {a₁..aₙ}       | 1            | n          | Cardinality                           |
|                       | ℕ              | rˣ           | (1-r)⁻¹     | Geometric series (∣r∣<1)            |
|                       | ℕ              | x·rˣ         | r(1-r)⁻²    | Differentiated series               |
|                       | {0,1}ⁿ         | Σxᵢ          | n·2ⁿ⁻¹      | Linear function sum                 |
|                       | {1,2,3}        | x            | 6          | Finite sum                           |
| **Bernoulli (P)**      | {0,1}         | x            | p          | Mean                                  |
|                        | {0,1}         | (x-p)²       | p(1-p)     | Variance                             |
|                        | {0,1}         | (x-p)³       | p(1-p)(1-2p)| Skewness                            |
| **Poisson (P)**        | ℕ₀            | 1            | 1          | Normalization                        |
|                        | ℕ₀            | x            | λ          | Mean                                 |
|                        | ℕ₀            | (x-λ)²       | λ          | Variance                             |
|                        | ℕ₀            | x²           | λ + λ²     | Second moment                       |

### Advanced Measures
| Measure Type          | Domain             | Integrand    | Result     | Notes                                  |
|-----------------------|--------------------|--------------|------------|----------------------------------------|
| **Product Measures**   | ℕ × ℕ         | f(x)g(y)     | [∑f][∑g]   | Separable functions                 |
|                        | [0,∞)²        | \|x-y\|e⁻ˣe⁻ʸ | 1          | Exp(1) i.i.d. absolute difference   |
|                        | [0,1]×[0,1]   | x + y        | 1          | Fubini's theorem                    |
|                        | ℕ × {0,1}     | 4⁻⁽ˣ⁺ʸ⁾      | 5/3        | Mixed geometric series             |

| Measure Type          | Domain             | Integrand    | Result     | Notes                                  |
|-----------------------|--------------------|--------------|------------|----------------------------------------|
| **Weighted Measures**  | ℝ             | e⁻\|ˣ\|       | 2          | Double-sided exponential            |
|                        | [-1,1]        | 1 (dμ = \|x\|dx) | 1         | Weighted Lebesgue                  |
|                        | [0,∞)         | x²(2e⁻²ˣ dx)  | 1/2        | Exponential distribution moment    |
|                        | ℤ             | \|x\|e⁻\|ˣ\|   | 2e(e-1)⁻²  | Discrete Laplace                  |
| **Pushforward**        | [0,1] g(x)=x² | x            | 1/3        | ∫x·d(g*λ) = ∫g(t)dλ(t)            |

### Key Properties
**Linearity**:  
∫(af + bg)dμ = a∫fdμ + b∫gdμ

**Product Measures**:  
∫_{X×Y} h(x,y)d(μ×ν) = ∫_X ∫_Y h(x,y)dν dμ

**Change of Variables**:  
For T measurable: ∫_{T(Ω)} f dν = ∫_Ω f∘T dμ

**Convergence Tools**:  
Monotone Convergence, Dominated Convergence, Fubini-Tonelli

**Series Relations**:  
∑_{k=1}^∞ k2⁻ᵏ = 2, ∑_{k=0}^∞ k!⁻¹e⁻¹ = 1