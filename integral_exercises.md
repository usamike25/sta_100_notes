### Exercises 1
1. \(\int_{[-1,1]} x \, \lambda(dx)\), where \(\lambda\) is Lebesgue measure on \(\mathbb{R}\).
> \(\int_{-1}^1 x\, dx = 0\) (odd function over symmetric interval).
2. \(\int x^2 \, P(dx)\), where \(P(A) = (1-p)\delta_0(A) + p\delta_1(A)\), \(p \in (0,1)\).
> \((1-p)(0-p)^2 + p(1-p)^2 = p(1-p)\).
3. \(\int_1^e \log(x) \, \lambda(dx)\), where \(\lambda\) is Lebesgue measure.
> \(\int_1^e \log x \, dx = [x \log x - x]_1^e = (e \cdot 1 - e) - (1\cdot0 - 1) = 1\).
4. \(\int_{\{1,2,3\}} x \, \mu(dx)\), where \(\mu\) is counting measure on \(\mathcal{P}(\mathbb{N})\).
> \(\sum_{x=1}^3 x = 6\).
5. \(\int_{\mathbb{N} \times \mathbb{N}} 3^{-(x+y)} \, m(d(x,y))\), where \(m\) is counting measure on \(\mathcal{P}(\mathbb{N} \times \mathbb{N})\) and \(\mathbb{N} = \{0,1,2,\dots\}\).
> \(\sum_{x=0}^\infty \sum_{y=0}^\infty 3^{-(x+y)} = \left(\sum_{x=0}^\infty 3^{-x}\right)^2 = \left(\frac{1}{1 - \frac{1}{3}}\right)^2 = \left(\frac{3}{2}\right)^2 = \frac{9}{4}\).
6. \(\int_{\mathbb{R}} x \, \mu(dx)\), where \(\mu(A) = \sum_{x=0}^\infty \frac{e^{-2} 2^x}{x!} \delta_x(A)\).
> Expectation of \(\text{Poisson}(2)\): \(2\).
7. \(\int_{[0,2]} x^3 \, \lambda(dx)\).
> \(\int_0^2 x^3 dx = \frac{2^4}{4} = 4\).
8. \(\int (x-p)^3 \, P(dx)\), same \(P\) as exercise 2.
> \((1-p)(0-p)^3 + p(1-p)^3 = p(1-p)(1-2p)\).
9. \(\int_0^1 \frac{1}{1+x^2} \, \lambda(dx)\).
> \(\int_0^1 \frac{1}{1+x^2} dx = \arctan(1) - \arctan(0) = \frac{\pi}{4}\).
10. \(\sum_{k=1}^\infty \frac{k}{2^k}\), interpreting as \(\int f(k) m(dk)\), \(m\) counting measure on \(\mathbb{N}=\{1,2,...\}\).
> \(\sum_{k=1}^\infty \frac{k}{2^k} = 2\).
11. \(\int_{\mathbb{N}} (x!)^{-1} e^{-1} \, \mu(dx)\), \(\mu\) as in exercise 6 with parameter 1 (i.e., \(\mu(A) = \sum_{x=0}^\infty \frac{e^{-1} 1^x}{x!} \delta_x(A)\)), \(\mathbb{N}=\{0,1,2,...\}\).
> \(\sum_{x=0}^\infty \frac{e^{-1} 1^x}{x!} = 1\) (total probability of Poisson(1)). Note: the integral is \(\int_{\mathbb{N}} \frac{1}{x!} e^{-1} \mu(dx)\). The question appears to imply the integrand term \(\frac{e^{-1} \lambda^x}{x!}\) is part of the measure. Re-reading exercise 6, \(\mu(A)\) is the measure \(P(X \in A)\) for Poisson. So here we integrate \(g(x) = (x!)^{-1}e^{-1}\) against \(dP(x)\), where \(P\) is Poisson(1). This would be \(\sum_{x=0}^\infty (x!)^{-1}e^{-1} \frac{e^{-1}1^x}{x!} = e^{-2} \sum_{x=0}^\infty \frac{1}{(x!)^2}\), which is \(e^{-2} I_0(2)\) where \(I_0\) is modified Bessel func.
> The likely intended question is \(\int_{\mathbb{N}} 1 \, \mu(dx)\) where \(\mu\) is Poisson(1) measure, which sums to 1. OR \(\int_{\mathbb{N}} x \cdot \frac{e^{-1}}{x!} \mu_c(dx)\) where \(\mu_c\) is counting measure, and this would be \(E[X]=1\).
> Assuming the question means: given Poisson measure \(P_\lambda(A) = \sum_{x \in A \cap \mathbb{N}_0} \frac{e^{-\lambda}\lambda^x}{x!}\), calculate \(\int_{\mathbb{N}_0} g(x) P_1(dx)\) with \(g(x)=1\).
> **Solution:** The sum of probabilities for a Poisson(1) distribution is \(\sum_{x=0}^\infty \frac{e^{-1}1^x}{x!} = e^{-1}\sum_{x=0}^\infty \frac{1}{x!} = e^{-1}e = 1\). If the question meant \(\int_{\mathbb{N}_0} \frac{(x!)^{-1}e^{-1}}{\text{term from measure}} (\text{term from measure } dP(x))\), this is likely asking for \(\sum_{x=0}^\infty (x!)^{-1}e^{-1} P(x)\) where \(P(x)\) is Poisson probability for \(x\). This would be \(e^{-1} \sum ((x!)^{-2} e^{-1}) = e^{-2} \sum (x!)^{-2}\). The phrasing is a bit ambiguous but often \(\mu\) as in ex 6 implies \(\mu\) IS the Poisson measure. If \(\mu(dx) = \frac{e^{-1}1^x}{x!} \delta_x(dx)\) then \(\int (x!)^{-1}e^{-1} \mu(dx) = \sum_{x=0}^{\infty} (x!)^{-1}e^{-1} \frac{e^{-1}1^x}{x!} = e^{-2} \sum_{x=0}^{\infty} \frac{1}{(x!)^2}\).
> If it means $$\int_{\mathbb{N}_0} \frac{e^{-1}}{x!} \, \text{counting\_measure}(dx)$$this is \(e^{-1}\sum (x!)^{-1} = e^{-1} e = 1\). Given the solution in the original is `1`, this last interpretation is most likely, where \(\mu\) is counting measure.
> **Original Solution Interpretation:** \(\sum_{x=0}^\infty \frac{e^{-1} 1^x}{x!} = 1\) (total probability of Poisson(1)). This implies the integrand is \(1\) and the measure is Poisson(1).

12. \(\int_{\mathbb{N} \times \{0,1\}} 4^{-(x+y)} \, m(d(x,y))\), \(m\) counting measure, \(\mathbb{N}=\{0,1,2,...\}\).
> \(\sum_{x=0}^\infty \sum_{y=0}^1 4^{-(x+y)} = \left(\sum_{x=0}^\infty 4^{-x}\right) \left(\sum_{y=0}^1 4^{-y}\right) = \frac{1}{1-1/4} \times (4^0 + 4^{-1}) = \frac{4}{3} \times (1 + \frac{1}{4}) = \frac{4}{3} \times \frac{5}{4} = \frac{5}{3}\).
13. \(\int_0^\infty x e^{-x} \, \lambda(dx)\).
> \(\int_0^\infty x e^{-x} dx = 1\) (Gamma(2) distribution mean, or \(\Gamma(2)\) function).
14. \(\int_{\{0,1\}^n} \sum_{i=1}^n x_i \, \mu(dx)\), \(\mu\) counting measure on \(\{0,1\}^n\).
> \(\sum_{x \in \{0,1\}^n} \sum_{i=1}^n x_i = n \cdot 2^{n-1}\). For a fixed \(i\), \(x_i=1\) in half of the \(2^n\) configurations, so \(2^{n-1}\) times. Summing over \(n\) coordinates gives \(n 2^{n-1}\).
15. \(\int_{\mathbb{R}} e^{-x^2} \, \lambda(dx)\) over \(\mathbb{R}\).
> No elementary closed form for the antiderivative, but the definite integral is known as \(\sqrt{\pi}\) (Gaussian integral).
16. \(\int_{\mathbb{N}_0} x^2 P_\lambda(dx)\), where \(P_\lambda(dx)\) denotes integrating against the Poisson measure with parameter \(\lambda\), i.e. \(P_\lambda(A) = \sum_{x \in A \cap \mathbb{N}_0} \frac{e^{-\lambda}\lambda^x}{x!}\). (The original text says \(\delta_x(dx)\) which is confusing).
> This is \(E[X^2]\) for \(X \sim \text{Poisson}(\lambda)\). \(E[X^2] = \text{Var}(X) + (E[X])^2 = \lambda + \lambda^2\).
17. \(\int_0^1 x \log(x) \, \lambda(dx)\).
> \(\int_0^1 x \log x dx = [\frac{x^2}{2}\log x - \frac{x^2}{4}]_0^1 = (0 - \frac{1}{4}) - \lim_{x\to 0}(\frac{x^2}{2}\log x - \frac{x^2}{4}) = -\frac{1}{4}\).
18. \(\int_{[0,1]^2} (x^2 + y^2) \, \lambda(dxdy)\).
> \(\int_0^1 \int_0^1 (x^2 + y^2) dy dx = \int_0^1 [x^2y + \frac{y^3}{3}]_0^1 dx = \int_0^1 (x^2 + \frac{1}{3}) dx = [\frac{x^3}{3} + \frac{x}{3}]_0^1 = \frac{1}{3} + \frac{1}{3} = \frac{2}{3}\).
19. \(\int_{\mathbb{N} \times \mathbb{N}} (xy)^{-1} 2^{-(x+y)} \, m(d(x,y))\), where \(\mathbb{N}=\{1,2,...\}\) and \(m\) is counting measure.
> \(\sum_{x=1}^\infty \sum_{y=1}^\infty \frac{2^{-x}}{x} \frac{2^{-y}}{y} = \left(\sum_{k=1}^\infty \frac{(1/2)^k}{k}\right)^2 = (-\log(1-1/2))^2 = (\log 2)^2\).
20. \(\int_0^\infty \frac{\sin x}{x} \, \lambda(dx)\).
> \(\int_0^\infty \frac{\sin x}{x} dx = \frac{\pi}{2}\) (Dirichlet integral).
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
> **Solution:** \(\sum_{x=0}^{\infty} e^{-x} = \sum_{x=0}^{\infty} (1/e)^x = \frac{1}{1-1/e} = \frac{e}{e-1}\)  
*(Geometric series under counting measure.)*
8. **\(\int_{[0,1]\times[0,1]} (x+y)(\lambda\times\lambda)(d(x,y))\)**, where \(\lambda\times\lambda\) is the product measure.
> **Solution:** \(\int_0^1\int_0^1 (x+y) dx dy = \int_0^1 (\frac{1}{2}+y) dy = \frac{1}{2} + \frac{1}{2} = 1\)  
*(Double integral with linear function.)*
9. **\(\int_{\mathbb{R}} x \mu(dx)\)**, where \(\mu = \sum_{k=0}^\infty \frac{1}{2^{k+1}}\delta_k\).
> **Solution:** \(\sum_{k=0}^\infty k \frac{1}{2^{k+1}} = \frac{1}{2} \sum_{k=0}^\infty k (\frac{1}{2})^k = \frac{1}{2} \frac{1/2}{(1-1/2)^2} = \frac{1}{2} \frac{1/2}{1/4} = 1\)  
*(Expected value of a discrete distribution (a geometric distribution variant starting at 0, \(P(X=k) = (1/2)^{k+1}\)).)*
10. **\(\int_{\mathbb{N}\times\mathbb{N}} e^{-(x+y)}(\mu\times\mu)(d(x,y))\)**, where \(\mu\) is the counting measure on \(\mathbb{N}=\{0,1,2,\dots\}\).
> **Solution:** \(\left(\sum_{x=0}^\infty e^{-x}\right) \left(\sum_{y=0}^\infty e^{-y}\right) = \left(\frac{e}{e-1}\right)^2\)  
*(Product measure and separable function, using result from ex. 7.)*
11. **\(\int_{\mathbb{R}} x \nu(dx)\)**, where \(d\nu = \frac{1}{\sqrt{2\pi}} e^{-x^2/2} dx\) (standard Gaussian measure).
> **Solution:** \(0\)  
*(Symmetry of Gaussian measure; expected value of N(0,1).)*
12. **\(\int_{[0,\infty)} x^2 \mu(dx)\)**, where \(d\mu = 2e^{-2x} dx\). (This is an Exponential distribution with rate 2).
> **Solution:** \(\int_0^\infty x^2 2e^{-2x} dx\). For \(\text{Exp}(\beta)\) with density \(\beta e^{-\beta x}\), \(E[X^2] = 2/\beta^2\). Here \(\beta=2\), so \(E[X^2] = 2/2^2 = 1/2\).  
*(Exponential distribution second moment.)*
13. **\(\int_{[-2,2]} |x| \lambda(dx)\)**, where \(\lambda\) is Lebesgue measure.
> **Solution:** \(2 \int_0^2 x dx = 2 [\frac{x^2}{2}]_0^2 = 2 \cdot \frac{4}{2} = 4\)  
*(Integral of absolute value over symmetric interval.)*
14. **\(\int_{[-1,1]} 1 \mu(dx)\)**, where \(d\mu = |x| dx\).
> **Solution:** \(\int_{-1}^1 |x| dx = 2 \int_0^1 x dx = 2 \cdot \frac{1}{2} = 1\)  
*(Integration against a weighted Lebesgue measure.)*
15. **\(\int_{\mathbb{R}} e^{-|x|} \lambda(dx)\)**.
> **Solution:** \(2 \int_0^\infty e^{-x} dx = 2 [-e^{-x}]_0^\infty = 2(0 - (-1)) = 2\)  
*(Double-sided exponential integral.)*
16. **\(\int_{\mathbb{N}_0} (x-1)^2 P(dx)\)**, where \(P\) is Poisson measure with mean 1: \(P(\{k\}) = \frac{e^{-1}}{k!}\) for \(k \in \mathbb{N}_0 = \{0,1,2,\dots\}\).
> **Solution:** This is \(E[(X-1)^2]\) for \(X \sim \text{Poisson}(1)\). Mean \(E[X]=\lambda=1\). So \(E[(X-E[X])^2] = \text{Var}(X) = \lambda = 1\).  
*(Variance of Poisson distribution.)*
17. **\(\int_{[0,1]} x \nu(dx)\)**, where \(\nu = g_*\lambda\) is the pushforward of Lebesgue measure \(\lambda\) on \([0,1]\) under \(g(x) = x^2\).
> **Solution:** By change of variables, \(\int_{[0,1]} g(x) \lambda(dx) = \int_0^1 x^2 dx = \frac{1}{3}\).  
*(Pushforward measure and change of variables. The integral becomes \(\int_S y d\nu(y)\). If \(Y=g(X)\), then \(E[Y] = \int x d\nu(x)\) means we are finding \(E[X]\) where \(X\) has measure \(\nu\). The wording here is \(\int x \nu(dx)\) where \(\nu\) is defined on range of \(g\). So we integrate \(\int_{[0,1]} y d\nu(y)\). Using transformation: if \(y=x^2\), then pdf of \(Y\) is \(f_Y(y) = f_X(\sqrt{y}) |\frac{d}{dy}\sqrt{y}| = 1 \cdot \frac{1}{2\sqrt{y}}\) for \(y \in [0,1]\). So \(\int_0^1 y \frac{1}{2\sqrt{y}} dy = \int_0^1 \frac{\sqrt{y}}{2} dy = [\frac{1}{2} \frac{y^{3/2}}{3/2}]_0^1 = \frac{1}{3}\).
Original interpretation: \(\int x \nu(dx)\). If \(\nu\) is on the target space of \(g\), then the variable should be \(y\), not \(x\). If it means \(\int x d(g_*\lambda)(x)\), then it's \(\int x^2 d\lambda(x)\). This means \(x\) is a dummy variable representing values in range of \(g\). So \(\int_0^1 y f_Y(y) dy\). This is what was computed.
Alternatively \(\int_{g([0,1])} id(y) d\nu(y) = \int_{[0,1]} id(g(x)) d\lambda(x) = \int_0^1 x^2 dx = 1/3\). This is standard notation. The \(x\) in \(\int x \nu(dx)\) is the variable of integration over the space where \(\nu\) is defined.
*(Pushforward measure and change of variables.)*
18. **\(\int_{\mathbb{Z}} |x| e^{-|x|} \mu(dx)\)**, where \(\mu\) is the counting measure on \(\mathbb{Z}\).
> **Solution:** \(\sum_{x \in \mathbb{Z}} |x|e^{-|x|} = 0 \cdot e^0 + 2 \sum_{x=1}^\infty x e^{-x} = 2 \sum_{x=1}^\infty x (1/e)^x = 2 \frac{1/e}{(1-1/e)^2} = 2 \frac{e^{-1}}{(1-e^{-1})^2} = 2 \frac{e^{-1}}{( (e-1)/e )^2} = 2 \frac{e^{-1}}{(e-1)^2/e^2} = \frac{2e}{(e-1)^2}\).  
*(Series involving absolute values and exponential decay.)*
19. **\(\int_{\mathbb{R}} x \mu(dx)\)**, where \(\mu = \delta_0 + \lambda|_{[1,2]}\) (Lebesgue measure restricted to \([1,2]\)).
> **Solution:** \(\int_{\mathbb{R}} x \delta_0(dx) + \int_{\mathbb{R}} x \lambda|_{[1,2]}(dx) = 0 \cdot 1 + \int_1^2 x dx = 0 + [\frac{x^2}{2}]_1^2 = \frac{4}{2} - \frac{1}{2} = \frac{3}{2}\).  
*(Mixed discrete-continuous measure.)*
20. **\(\int_{[0,\infty)\times[0,\infty)} |x-y| e^{-x} e^{-y} (\lambda\times\lambda)(d(x,y))\)**.
> **Solution:** \(\int_0^\infty \int_0^\infty |x-y| e^{-x}e^{-y} dx dy\). This is \(E[|X-Y|]\) for i.i.d \(X,Y \sim \text{Exp}(1)\). The probability \(P(X>Y) = 1/2\).
> \(2 \int_0^\infty \int_y^\infty (x-y) e^{-x}e^{-y} dx dy = 2 \int_0^\infty e^{-y} \left( \int_y^\infty x e^{-x} dx - y \int_y^\infty e^{-x} dx \right) dy\).
> \(\int_y^\infty e^{-x} dx = [-e^{-x}]_y^\infty = e^{-y}\).
> \(\int_y^\infty x e^{-x} dx = [-xe^{-x} - e^{-x}]_y^\infty = (0-0) - (-ye^{-y} - e^{-y}) = ye^{-y} + e^{-y}\).
> So integral becomes \(2 \int_0^\infty e^{-y} (ye^{-y} + e^{-y} - y e^{-y}) dy = 2 \int_0^\infty e^{-2y} dy = 2 [-\frac{1}{2} e^{-2y}]_0^\infty = 2 (0 - (-\frac{1}{2})) = 1\).  
*(Integral involving absolute difference of exponentials.)*
---
### Exercises 3
1.  **\(\int_{\mathbb{R}} \mathbf{1}_{[0,1]}(x) \cos(\pi x) \, d\lambda(x)\)**, where \(\lambda\) is Lebesgue measure.
> **Solution:** \(\int_0^1 \cos(\pi x) dx = \left[\frac{1}{\pi}\sin(\pi x)\right]_0^1 = \frac{1}{\pi}(\sin(\pi) - \sin(0)) = 0\).  
*(Standard definite integral of a trigonometric function.)*
2.  **\(\int_{\mathbb{R}^2} \mathbf{1}_{B(0,1)}(x,y) \, d(\lambda \times \lambda)(x,y)\)**, where \(B(0,1) = \{(x,y) : x^2+y^2 \le 1\}\) is the unit disk and \(\lambda\) is Lebesgue measure.
> **Solution:** This is the Lebesgue measure of the unit disk, which is its area: \(\pi(1)^2 = \pi\).  
*(Lebesgue measure of a geometric shape in \(\mathbb{R}^2\).)*
3.  **\(\int_{\{0,1,2\}} (x^2 - 1) \, d\mu(x)\)**, where \(\mu = \delta_0 + 2\delta_1 + \delta_2\).
> **Solution:** \((0^2-1)\cdot 1 + (1^2-1)\cdot 2 + (2^2-1)\cdot 1 = (-1) + (0)\cdot 2 + (3)\cdot 1 = -1 + 0 + 3 = 2\).  
*(Linearity of integral for a sum of Dirac measures.)*
4.  **\(\int_{[0, \pi/2]} \sin(x) \, d\nu(x)\)**, where \(\nu(A) = \lambda(A \cap [0, \pi/4]) + \delta_{\pi/2}(A)\), and \(\lambda\) is Lebesgue measure.
> **Solution:** \(\int_0^{\pi/4} \sin(x) dx + \sin(\pi/2) \cdot 1 = [-\cos(x)]_0^{\pi/4} + 1 = (-\cos(\pi/4) - (-\cos(0))) + 1 = (-\frac{\sqrt{2}}{2} + 1) + 1 = 2 - \frac{\sqrt{2}}{2}\).  
*(Integral with respect to a mixed measure: part Lebesgue, part Dirac.)*
5.  **\(\int_{\mathbb{N}_0} x \, dP(x)\)** where \(\mathbb{N}_0 = \{0,1,2,\dots\}\) and \(P\) is the Geometric distribution measure \(P(\{k\}) = (1-p)^k p\) for \(k \in \mathbb{N}_0\), \(p \in (0,1)\).
> **Solution:** This is the expected value of a geometric random variable starting at 0. \(E[X] = \sum_{k=0}^\infty k p(1-p)^k = \frac{1-p}{p}\).  
*(Expected value of a geometric distribution.)*
6.  **\(\int_{(0,1)} x^{-1/2} \, d\lambda(x)\)**, where \(\lambda\) is Lebesgue measure.
> **Solution:** \(\int_0^1 x^{-1/2} dx = [2x^{1/2}]_0^1 = 2(1)^{1/2} - \lim_{a\to 0} 2a^{1/2} = 2 - 0 = 2\).  
*(Integral of a function with an integrable singularity at the boundary.)*
7.  **\(\int_{\mathbb{R}} \mathbf{1}_{\mathbb{Q}}(x) \, d\lambda(x)\)**, where \(\mathbb{Q}\) is the set of rational numbers and \(\lambda\) is Lebesgue measure.
> **Solution:** Since \(\mathbb{Q}\) is a set of Lebesgue measure zero, \(\lambda(\mathbb{Q})=0\). The integral of the indicator function is \(\int \mathbf{1}_{\mathbb{Q}} d\lambda = \lambda(\mathbb{Q}) = 0\).  
*(Integral of an indicator function of a null set.)*
8.  **\(\int_{[0,1]} x \, d\mu_C(x)\)**, where \(\mu_C\) is the standard Cantor measure on \([0,1]\) (normalized so \(\mu_C([0,1])=1\)).
> **Solution:** By symmetry of the Cantor set and the Cantor measure construction around \(1/2\), the expected value \(\int_{[0,1]} x \, d\mu_C(x)\) is \(\frac{1}{2}\).  
*(Integral with respect to the Cantor measure.)*
9.  **\(\int_{[0,1]^2} \min(x,y) \, d(\lambda \times \lambda)(x,y)\)**, where \(\lambda\) is Lebesgue measure.
> **Solution:** \(\int_0^1 \left( \int_0^x y \, dy + \int_x^1 x \, dy \right) dx = \int_0^1 \left( \frac{x^2}{2} + x(1-x) \right) dx = \int_0^1 \left( \frac{x^2}{2} + x - x^2 \right) dx = \int_0^1 \left( x - \frac{x^2}{2} \right) dx = \left[\frac{x^2}{2} - \frac{x^3}{6}\right]_0^1 = \frac{1}{2} - \frac{1}{6} = \frac{3-1}{6} = \frac{1}{3}\).  
*(Double integral involving the min function, solved using Fubini's theorem.)*
10. **\(\int_{\mathbb{N}} \frac{1}{x(x+1)} \, d\mu(x)\)**, where \(\mu\) is the counting measure on \(\mathbb{N}=\{1,2,...\}\).
> **Solution:** \(\sum_{x=1}^\infty \frac{1}{x(x+1)} = \sum_{x=1}^\infty \left(\frac{1}{x} - \frac{1}{x+1}\right) = \left(1-\frac{1}{2}\right) + \left(\frac{1}{2}-\frac{1}{3}\right) + \dots = 1\). (Telescoping series).  
*(Summation as an integral with counting measure; telescoping series.)*
11. **\(\int_{[0,1]} x^2 \, d(g_*\lambda)(x)\)**, where \(g_*\lambda\) is the pushforward of Lebesgue measure \(\lambda\) on \([0,1]\) by \(g(t) = t^3\). (The integration variable \(x\) lives in the target space of \(g\), which is also \([0,1]\)).
> **Solution:** Using the change of variables formula for pushforward measures: \(\int_{[0,1]} x^2 \, d(g_*\lambda)(x) = \int_{[0,1]} (g(t))^2 \, d\lambda(t) = \int_0^1 (t^3)^2 \, dt = \int_0^1 t^6 \, dt = \left[\frac{t^7}{7}\right]_0^1 = \frac{1}{7}\).  
*(Pushforward measure and change of variables theorem.)*
12. **\(\int_{[0,\infty)} x e^{-x^2} \, d\lambda(x)\)**, where \(\lambda\) is Lebesgue measure.
> **Solution:** Let \(u=x^2\), then \(du=2xdx\), so \(xdx = \frac{1}{2}du\). The limits \(x=0 \Rightarrow u=0\) and \(x\to\infty \Rightarrow u\to\infty\).
> \(\int_0^\infty e^{-u} \frac{1}{2}du = \frac{1}{2} [-e^{-u}]_0^\infty = \frac{1}{2} (0 - (-1)) = \frac{1}{2}\).  
*(Gaussian-related integral, solvable with u-substitution.)*
13. **\(\int_{\mathbb{R}} \cos(x) \, d\mu(x)\)**, where \(d\mu(x) = \frac{1}{\pi(1+x^2)}dx\) (Standard Cauchy distribution measure).
> **Solution:** This is the real part of the characteristic function \(\phi(t) = E[e^{itX}]\) of the standard Cauchy distribution, evaluated at \(t=1\). The characteristic function is \(\phi(t) = e^{-|t|}\). So, \(\int_{\mathbb{R}} \cos(x) \frac{1}{\pi(1+x^2)}dx = \text{Re}(e^{-|1|}) = e^{-1}\). (Since \(\sin(x)\) is odd, its integral against the even measure is 0).  
*(Integral related to the characteristic function of the Cauchy distribution.)*
14. **\(\int_{\{ (x,y) \in \mathbb{N}_0^2 : x+y=N \}} 1 \, d\mu(x,y)\)**, where \(N \in \mathbb{N}_0 = \{0,1,2,\dots\}\) and \(\mu\) is the counting measure on \(\mathbb{N}_0^2\).
> **Solution:** This counts the number of pairs of non-negative integers \((x,y)\) such that \(x+y=N\). The possible values for \(x\) are \(0, 1, \ldots, N\), each determining a unique \(y\). Thus there are \(N+1\) such pairs.  
*(Counting measure on a specific discrete set, a diagonal slice of \(\mathbb{N}_0^2\).)*
15. **\(\int_{[0,1]} x \, dF(x)\)**, where \(F(x)\) is the cumulative distribution function (CDF) of a uniform \(U(0,1)\) random variable.
> **Solution:** For \(X \sim U(0,1)\), \(F(x)=x\) for \(x \in [0,1]\), and \(dF(x) = f(x)dx = 1 \cdot dx\) for \(x \in (0,1)\). The integral is interpreted as \(\int_{[0,1]} x \lambda(dx)\), where \(\lambda\) is Lebesgue measure.
> \(\int_0^1 x \, dx = \left[\frac{x^2}{2}\right]_0^1 = \frac{1}{2}\).  
*(Connection to probability theory (expected value) and Riemann-Stieltjes integrals for absolutely continuous CDFs.)*
16. **\(\int_{\mathbb{R}^2} e^{-(x^2+y^2)} \, d(\lambda \times \lambda)(x,y)\)**, where \(\lambda\) is Lebesgue measure.
> **Solution:** Convert to polar coordinates: \(x=r\cos\theta, y=r\sin\theta\), \(dxdy = r dr d\theta\). \(x^2+y^2=r^2\).
> \(\int_0^{2\pi} \int_0^\infty e^{-r^2} r \, dr d\theta = 2\pi \int_0^\infty e^{-r^2} r \, dr\). From problem #12, \(\int_0^\infty e^{-r^2} r \, dr = 1/2\).
> So the integral is \(2\pi \cdot \frac{1}{2} = \pi\).  
*(Double integral evaluated using polar coordinates, related to Gaussian integrals.)*
17. **\(\int_{[0,1]} x \, d\mu(x)\)**, where \(\mu = \frac{1}{2}\delta_{1/4} + \frac{1}{2}\lambda|_{[0,1]}\) (a mixture of a Dirac measure at \(1/4\) and scaled Lebesgue measure on \([0,1]\)). The integration variable \(x\) lives on \([0,1]\).
> **Solution:** \(\int_{[0,1]} x \, d\left(\frac{1}{2}\delta_{1/4}\right)(x) + \int_{[0,1]} x \, d\left(\frac{1}{2}\lambda|_{[0,1]}\right)(x) = \frac{1}{2} \cdot \frac{1}{4} + \frac{1}{2} \int_0^1 x \, dx = \frac{1}{8} + \frac{1}{2} \left[\frac{x^2}{2}\right]_0^1 = \frac{1}{8} + \frac{1}{2} \cdot \frac{1}{2} = \frac{1}{8} + \frac{1}{4} = \frac{3}{8}\).  
*(Integral with respect to a linear combination of measures (mixed measure).)*
18. **\(\int_0^\infty \frac{\sin^2(x)}{x^2} \, d\lambda(x)\)**, where \(\lambda\) is Lebesgue measure.
> **Solution:** This is a known definite integral. \(\int_0^\infty \left(\frac{\sin x}{x}\right)^2 dx = \frac{\pi}{2}\). It can be solved using Parseval's theorem with the Fourier transform of \(\mathbf{1}_{[-1,1]}(t)\), or complex integration.  
*(Known definite integral related to the sinc function.)*
19. **\(\int_{T_2} (x+y) \, d(\lambda\times\lambda)(x,y)\)** where \(T_2 = \{(x,y) \in [0,1]^2 : x+y \le 1\}\) (a triangle) and \(\lambda\) is Lebesgue measure.
> **Solution:** \(\int_0^1 \int_0^{1-x} (x+y) \, dy dx = \int_0^1 \left[xy + \frac{y^2}{2}\right]_0^{1-x} dx = \int_0^1 \left(x(1-x) + \frac{(1-x)^2}{2}\right) dx\)
> \(= \int_0^1 \left(x-x^2 + \frac{1-2x+x^2}{2}\right) dx = \int_0^1 \left(x-x^2 + \frac{1}{2} - x + \frac{x^2}{2}\right) dx\)
> \(= \int_0^1 \left(\frac{1}{2} - \frac{x^2}{2}\right) dx = \left[\frac{x}{2} - \frac{x^3}{6}\right]_0^1 = \frac{1}{2} - \frac{1}{6} = \frac{3-1}{6} = \frac{1}{3}\).  
*(Double integral over a triangular region.)*
20. **\(\int_{\mathbb{R}} \frac{1}{(x-a)^2+b^2} \, d\lambda(x)\)**, for \(b>0\), \(\lambda\) Lebesgue measure.
> **Solution:** Let \(u = \frac{x-a}{b}\), so \(x = bu+a\) and \(dx = b \, du\).
> \(\int_{-\infty}^\infty \frac{1}{b^2 u^2 + b^2} b \, du = \int_{-\infty}^\infty \frac{b}{b^2(u^2+1)} \, du = \frac{1}{b} \int_{-\infty}^\infty \frac{1}{u^2+1} \, du\)
> \(= \frac{1}{b} [\arctan(u)]_{-\infty}^\infty = \frac{1}{b} \left(\frac{\pi}{2} - \left(-\frac{\pi}{2}\right)\right) = \frac{1}{b} (\pi) = \frac{\pi}{b}\).  
*(Integral of a Lorentzian/Cauchy profile.)*
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