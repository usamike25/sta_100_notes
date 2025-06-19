
### Variation 1: Asymmetric Binary Support  
**Exercise:** Let \(X\) be a discrete random variable with support \(\{-1, 1\}\) and law:  
\[
P(X = -1) = \frac{1}{3}, \quad P(X = 1) = \frac{2}{3}.
\]  
Let \(X_1, X_2, \dots, X_n\) be \(n\) independent copies of \(X\), and define the random vector \(Y = (X_1, X_2, \dots, X_n)\).

(a) \(\mathbb{P}(X = -1)\) and \(\mathbb{P}(X = 1)\)?  
**Solution:**  
>\(\mathbb{P}(X = -1) = \frac{1}{3}\), \(\mathbb{P}(X = 1) = \frac{2}{3}\).  

(b) Calculate \(E[|X|^2]\).  
**Solution:**  
>\(|X|^2 = X^2\).  
>\(X^2 = 1\) (since \((-1)^2 = 1, 1^2 = 1\)).  
>\(E[X^2] = 1 \cdot P(X^2 = 1) = 1\).  

(c) Find \(E[X]\) and \(\text{Var}(X)\).  
**Solution:**  
>\(E[X] = (-1) \cdot \frac{1}{3} + 1 \cdot \frac{2}{3} = \frac{1}{3}\).  
\(\text{Var}(X) = E[X^2] - (E[X])^2 = 1 - \left(\frac{1}{3}\right)^2 = 1 - \frac{1}{9} = \frac{8}{9}\).  

(d) Law of \(\frac{X+1}{2}\)?  
**Solution:**  
>Let \(T = \frac{X+1}{2}\).  
>- If \(X = -1\), \(T = 0\) with \(P = \frac{1}{3}\).  
>- If \(X = 1\), \(T = 1\) with \(P = \frac{2}{3}\).  
Support: \(\{0, 1\}\), law: \(P(T = 0) = \frac{1}{3}\), \(P(T = 1) = \frac{2}{3}\).  

(e) Law of \(Y\)? Calculate \(P(Y \in \{1\}^n)\).  
**Solution:**  
>Law of \(Y\): product measure on \(\{-1,1\}^n\) with \(P(Y = (y_1,\dots,y_n)) = \prod_{i=1}^n P(X_i = y_i)\).  
\(P(Y \in \{1\}^n) = P(X_1 = 1, \dots, X_n = 1) = \left(\frac{2}{3}\right)^n\).  

(f) Show \(\|Y\|_2^2\) is constant \(\mathbb{P}\)-a.s.  
**Solution:**  
>\(\|Y\|_2^2 = \sum_{i=1}^n X_i^2\). Since \(X_i^2 = 1\) for all \(i\), \(\|Y\|_2^2 = n\). Constant everywhere.  

(g) Law of \(Z = X_1 + X_2\)?  
**Solution:**  
>- \(Z = -2\) if \(X_1 = -1, X_2 = -1\): \(P = \frac{1}{3} \cdot \frac{1}{3} = \frac{1}{9}\).  
>- \(Z = 0\) if mixed: \(P = P(X_1 = -1, X_2 = 1) + P(X_1 = 1, X_2 = -1) = \frac{1}{3} \cdot \frac{2}{3} + \frac{2}{3} \cdot \frac{1}{3} = \frac{4}{9}\).  
>- \(Z = 2\) if both 1: \(P = \frac{2}{3} \cdot \frac{2}{3} = \frac{4}{9}\).  
Law: \(P(Z = -2) = \frac{1}{9}\), \(P(Z = 0) = \frac{4}{9}\), \(P(Z = 2) = \frac{4}{9}\).  

---

### Variation 2: Three-Valued Symmetric Support  
**Exercise:** Let \(X\) be a discrete random variable with support \(\{-1, 0, 1\}\) and law:  
\[
P(X = -1) = \frac{1}{4}, \quad P(X = 0) = \frac{1}{2}, \quad P(X = 1) = \frac{1}{4}.
\]  
Let \(X_1, X_2, \dots, X_n\) be \(n\) independent copies of \(X\), and define \(Y = (X_1, X_2, \dots, X_n)\).

(a) \(\mathbb{P}(X = -1)\), \(\mathbb{P}(X = 0)\), \(\mathbb{P}(X = 1)\)?  
**Solution:**  
>\(\mathbb{P}(X = -1) = \frac{1}{4}\), \(\mathbb{P}(X = 0) = \frac{1}{2}\), \(\mathbb{P}(X = 1) = \frac{1}{4}\).  

(b) Calculate \(E[|X|^2]\).  
**Solution:**  
>\(|X|^2 = X^2\).  
\(E[X^2] = (-1)^2 \cdot \frac{1}{4} + 0^2 \cdot \frac{1}{2} + 1^2 \cdot \frac{1}{4} = \frac{1}{4} + 0 + \frac{1}{4} = \frac{1}{2}\).  

(c) Find \(E[X]\) and \(\text{Var}(X)\).  
**Solution:**  
\(E[X] = (-1) \cdot \frac{1}{4} + 0 \cdot \frac{1}{2} + 1 \cdot \frac{1}{4} = 0\).  
\(\text{Var}(X) = E[X^2] - (E[X])^2 = \frac{1}{2} - 0 = \frac{1}{2}\).  

(d) Law of \(\frac{X+1}{2}\)?  
**Solution:**  
>Let \(T = \frac{X+1}{2}\).  
>- \(X = -1\): \(T = 0\), \(P = \frac{1}{4}\).  
>- \(X = 0\): \(T = 0.5\), \(P = \frac{1}{2}\).  
>- \(X = 1\): \(T = 1\), \(P = \frac{1}{4}\).  
Support: \(\{0, 0.5, 1\}\), law: \(P(T = 0) = \frac{1}{4}\), \(P(T = 0.5) = \frac{1}{2}\), \(P(T = 1) = \frac{1}{4}\).  

(e) Law of \(Y\)? Calculate \(P(Y \in \{1\}^n)\).  
**Solution:**  
>Law of \(Y\): product measure on \(\{-1,0,1\}^n\) with \(P(Y = (y_1,\dots,y_n)) = \prod_{i=1}^n P(X_i = y_i)\).  
\(P(Y \in \{1\}^n) = P(X_1 = 1, \dots, X_n = 1) = \left(\frac{1}{4}\right)^n\).  

(f) Show \(\|Y\|_2^2\) is **not** constant \(\mathbb{P}\)-a.s. and find \(P(\|Y\|_2^2 = 0)\) and \(P(\|Y\|_2^2 = n)\).  
**Solution:**  
>\(\|Y\|_2^2 = \sum_{i=1}^n X_i^2\). Since \(X_i^2 = 0\) if \(X_i = 0\) and 1 otherwise:  
>- \(P(\|Y\|_2^2 = 0) = P(\text{all } X_i = 0) = \left(\frac{1}{2}\right)^n\).  
>- \(P(\|Y\|_2^2 = n) = P(\text{no } X_i = 0) = \left(\frac{1}{2}\right)^n\) (as \(P(X_i \neq 0) = \frac{1}{2}\)).  
Since \(0 < \left(\frac{1}{2}\right)^n < 1\) for \(n \geq 1\), \(\|Y\|_2^2\) is not constant.  

(g) Law of \(Z = X_1 + X_2\)?  
**Solution:**  
>Support: \(\{-2, -1, 0, 1, 2\}\). Calculations:  
>- \(Z = -2\): \(X_1 = -1, X_2 = -1\), \(P = \frac{1}{4} \cdot \frac{1}{4} = \frac{1}{16}\).  
>- \(Z = -1\): mixed \((-1,0)\) or \((0,-1)\), \(P = \frac{1}{4} \cdot \frac{1}{2} + \frac{1}{2} \cdot \frac{1}{4} = \frac{1}{4}\).  
>- \(Z = 0\): could be \((-1,1)\), \((1,-1)\), or \((0,0)\), \(P = \frac{1}{4} \cdot \frac{1}{4} + \frac{1}{4} \cdot \frac{1}{4} + \frac{1}{2} \cdot \frac{1}{2} = \frac{3}{8}\).  
>- \(Z = 1\): mixed \((1,0)\) or \((0,1)\), \(P = \frac{1}{4} \cdot \frac{1}{2} + \frac{1}{2} \cdot \frac{1}{4} = \frac{1}{4}\).  
>- \(Z = 2\): \((1,1)\), \(P = \frac{1}{4} \cdot \frac{1}{4} = \frac{1}{16}\).  
Law: \(P(Z = -2) = \frac{1}{16}\), \(P(Z = -1) = \frac{4}{16}\), \(P(Z = 0) = \frac{6}{16}\), \(P(Z = 1) = \frac{4}{16}\), \(P(Z = 2) = \frac{1}{16}\).  

---

### Variation 3: Asymmetric Binary Support in \(\{0,1\}\)  
**Exercise:** Let \(X\) be a discrete random variable with support \(\{0, 1\}\) and law:  
\[
P(X = 0) = \frac{1}{3}, \quad P(X = 1) = \frac{2}{3}.
\]  
Let \(X_1, X_2, \dots, X_n\) be \(n\) independent copies of \(X\), and define \(Y = (X_1, X_2, \dots, X_n)\).

(a) \(\mathbb{P}(X = 0)\) and \(\mathbb{P}(X = 1)\)?  
**Solution:**  
>\(\mathbb{P}(X = 0) = \frac{1}{3}\), \(\mathbb{P}(X = 1) = \frac{2}{3}\).  

(b) Calculate \(E[|X|^2]\).  
**Solution:**  
>\(|X|^2 = X^2 = X\) (since \(0^2=0, 1^2=1\))  
\(E[|X|^2] = E[X] = 0 \cdot \frac{1}{3} + 1 \cdot \frac{2}{3} = \frac{2}{3}\).  

(c) Find \(E[X]\) and \(\text{Var}(X)\).  
**Solution:**  
>\(E[X] = 0 \cdot \frac{1}{3} + 1 \cdot \frac{2}{3} = \frac{2}{3}\).  
\(\text{Var}(X) = E[X^2] - (E[X])^2 = \frac{2}{3} - \left(\frac{2}{3}\right)^2 = \frac{2}{3} - \frac{4}{9} = \frac{2}{9}\).  

(d) Law of \(\frac{X+1}{2}\)?  
**Solution:**  
>Let \(T = \frac{X+1}{2}\).  
>- \(X = 0\): \(T = 0.5\), \(P = \frac{1}{3}\).  
>- \(X = 1\): \(T = 1\), \(P = \frac{2}{3}\).  
Support: \(\{0.5, 1\}\), law: \(P(T = 0.5) = \frac{1}{3}\), \(P(T = 1) = \frac{2}{3}\).  

(e) Law of \(Y\)? Calculate \(P(Y \in \{1\}^n)\).  
**Solution:**  
>Law of \(Y\): product measure on \(\{0,1\}^n\) with \(P(Y = (y_1,\dots,y_n)) = \prod_{i=1}^n P(X_i = y_i)\).  
\(P(Y \in \{1\}^n) = P(X_1 = 1, \dots, X_n = 1) = \left(\frac{2}{3}\right)^n\).  

(f) Is \(\|Y\|_2^2\) constant? If not, find its law.  
**Solution:**  
>\(\|Y\|_2^2 = \sum_{i=1}^n X_i^2 = \sum_{i=1}^n X_i\) (since \(X_i^2 = X_i\)).  
\(\sum_{i=1}^n X_i \sim \text{Binomial}(n, p=\frac{2}{3})\) (number of 1's).  
Thus, for \(k = 0,1,\dots,n\):  
\(P\left(\|Y\|_2^2 = k\right) = \binom{n}{k} \left(\frac{2}{3}\right)^k \left(\frac{1}{3}\right)^{n-k}\).  
Not constant (e.g., for \(n=1\), takes 0 and 1).  

(g) Law of \(Z = X_1 + X_2\)?  
**Solution:**  
>Support: \(\{0, 1, 2\}\).  
>- \(Z = 0\): \(X_1 = 0, X_2 = 0\), \(P = \frac{1}{3} \cdot \frac{1}{3} = \frac{1}{9}\).  
>- \(Z = 1\): mixed, \(P = P(0,1) + P(1,0) = \frac{1}{3} \cdot \frac{2}{3} + \frac{2}{3} \cdot \frac{1}{3} = \frac{4}{9}\).  
>- \(Z = 2\): \(X_1 = 1, X_2 = 1\), \(P = \frac{2}{3} \cdot \frac{2}{3} = \frac{4}{9}\).  
Law: \(P(Z = 0) = \frac{1}{9}\), \(P(Z = 1) = \frac{4}{9}\), \(P(Z = 2) = \frac{4}{9}\).  

---

### Variation 4: Non-Integer Support  
**Exercise:** Let \(X\) be a discrete random variable with support \(\{3, 5\}\) and law:  
\[
P(X = 3) = \frac{2}{5}, \quad P(X = 5) = \frac{3}{5}.
\]  
Let \(X_1, X_2, \dots, X_n\) be \(n\) independent copies of \(X\), and define \(Y = (X_1, X_2, \dots, X_n)\).

(a) \(\mathbb{P}(X = 3)\) and \(\mathbb{P}(X = 5)\)?  
**Solution:**  
>\(\mathbb{P}(X = 3) = \frac{2}{5}\), \(\mathbb{P}(X = 5) = \frac{3}{5}\).  

(b) Calculate \(E[|X|^2]\).  
**Solution:**  
>\(|X|^2 = X^2\).  
\(E[X^2] = 3^2 \cdot \frac{2}{5} + 5^2 \cdot \frac{3}{5} = 9 \cdot \frac{2}{5} + 25 \cdot \frac{3}{5} = 18/5 + 75/5 = 93/5 = 18.6\).  

(c) Find \(E[X]\) and \(\text{Var}(X)\).  
**Solution:**  
>\(E[X] = 3 \cdot \frac{2}{5} + 5 \cdot \frac{3}{5} = 6/5 + 15/5 = 21/5 = 4.2\).  
\(\text{Var}(X) = E[X^2] - (E[X])^2 = \frac{93}{5} - \left(\frac{21}{5}\right)^2 = \frac{93}{5} - \frac{441}{25} = \frac{465}{25} - \frac{441}{25} = \frac{24}{25} = 0.96\).  

(d) Law of \(\frac{X+1}{2}\)?  
**Solution:**  
>Let \(T = \frac{X+1}{2}\).  
>- \(X = 3\): \(T = \frac{4}{2} = 2\), \(P = \frac{2}{5}\).  
>- \(X = 5\): \(T = \frac{6}{2} = 3\), \(P = \frac{3}{5}\).  
Support: \(\{2, 3\}\), law: \(P(T = 2) = \frac{2}{5}\), \(P(T = 3) = \frac{3}{5}\).  

(e) Law of \(Y\)? Calculate \(P(Y \in \{5\}^n)\).  
**Solution:**  
>Law of \(Y\): product measure on \(\{3,5\}^n\) with \(P(Y = (y_1,\dots,y_n)) = \prod_{i=1}^n P(X_i = y_i)\).  
\(P(Y \in \{5\}^n) = P(X_1 = 5, \dots, X_n = 5) = \left(\frac{3}{5}\right)^n\).  

(f) Is \(\|Y\|_2^2\) constant? Justify and find its range.  
**Solution:**  
>\(\|Y\|_2^2 = \sum_{i=1}^n X_i^2\), where \(X_i^2 \in \{9, 25\}\) (since \(3^2 = 9, 5^2 = 25\)).  
Range: from \(9n\) (all 3) to \(25n\) (all 5).  
Since \(n \geq 1\) and \(9 < 25\), unless \(n = 0\), it takes at least two values if \(n \geq 1\). Thus, not constant (e.g., for \(n=1\), is 9 or 25).  

(g) Law of \(Z = X_1 + X_2\)?  
**Solution:**  
>Support: \(\{6, 8, 10\}\) (since \(3+3=6, 3+5=8, 5+3=8, 5+5=10\)).  
>- \(Z = 6\): \(X_1 = 3, X_2 = 3\), \(P = \frac{2}{5} \cdot \frac{2}{5} = \frac{4}{25}\).  
>- \(Z = 8\): mixed \((3,5)\) or \((5,3)\), \(P = \frac{2}{5} \cdot \frac{3}{5} + \frac{3}{5} \cdot \frac2{5} = \frac{12}{25}\).  
>- \(Z = 10\): \(X_1 = 5, X_2 = 5\), \(P = \frac{3}{5} \cdot \frac{3}{5} = \frac{9}{25}\).  
Law: \(P(Z = 6) = \frac{4}{25}\), \(P(Z = 8) = \frac{12}{25}\), \(P(Z = 10) = \frac{9}{25}\).  

---

### Variation 5: Asymmetric Three-Valued Support  
**Exercise:** Let \(X\) be a discrete random variable with support \(\{-1, 0, 1\}\) and law:  
\[
P(X = -1) = \frac{1}{2}, \quad P(X = 0) = \frac{1}{3}, \quad P(X = 1) = \frac{1}{6}.
\]  
Let \(X_1, X_2, \dots, X_n\) be \(n\) independent copies of \(X\), and define \(Y = (X_1, X_2, \dots, X_n)\).

(a) \(\mathbb{P}(X = -1)\), \(\mathbb{P}(X = 0)\), \(\mathbb{P}(X = 1)\)?  
**Solution:**  
>\(\mathbb{P}(X = -1) = \frac{1}{2}\), \(\mathbb{P}(X = 0) = \frac{1}{3}\), \(\mathbb{P}(X = 1) = \frac{1}{6}\).  

(b) Calculate \(E[|X|^2]\).  
**Solution:**  
\(E[X^2] = (-1)^2 \cdot \frac{1}{2} + 0^2 \cdot \frac{1}{3} + 1^2 \cdot \frac{1}{6} = 1 \cdot \frac{1}{2} + 0 + \frac{1}{6} = \frac{3}{6} + \frac{1}{6} = \frac{4}{6} = \frac{2}{3}\).  

(c) Find \(E[X]\) and \(\text{Var}(X)\).  
**Solution:**  
>\(E[X] = (-1) \cdot \frac{1}{2} + 0 \cdot \frac{1}{3} + 1 \cdot \frac{1}{6} = -\frac{1}{2} + \frac{1}{6} = -\frac{1}{3}\).  
\(\text{Var}(X) = E[X^2] - (E[X])^2 = \frac{2}{3} - \left(-\frac{1}{3}\right)^2 = \frac{2}{3} - \frac{1}{9} = \frac{5}{9}\).  

(d) Law of \(\frac{X+1}{2}\)?  
**Solution:**  
>Let \(T = \frac{X+1}{2}\).  
>- \(X = -1\): \(T = 0\), \(P = \frac{1}{2}\).  
>- \(X = 0\): \(T = 0.5\), \(P = \frac{1}{3}\).  
>- \(X = 1\): \(T = 1\), \(P = \frac{1}{6}\).  
Support: \(\{0, 0.5, 1\}\), law: \(P(T = 0) = \frac{1}{2}\), \(P(T = 0.5) = \frac{1}{3}\), \(P(T = 1) = \frac{1}{6}\).  

(e) Law of \(Y\)? Calculate \(P(Y \in \{1\}^n)\).  
**Solution:**  
Law of \(Y\): product measure on \(\{-1,0,1\}^n\).  
\(P(Y \in \{1\}^n) = P(X_1 = 1, \dots, X_n = 1) = \left(\frac{1}{6}\right)^n\).  

(f) Find \(E[\|Y\|_2^2]\) and \(\text{Var}(\|Y\|_2^2)\).  
**Solution:**  
>\(\|Y\|_2^2 = \sum_{i=1}^n X_i^2\).  
Let \(W_i = X_i^2\), so \(\|Y\|_2^2 = \sum_{i=1}^n W_i\).  
\(W_i\) is discrete:  
>- \(P(W_i = 0) = P(X_i = 0) = \frac{1}{3}\).  
>- \(P(W_i = 1) = P(X_i = -1 \text{ or } 1) = \frac{1}{2} + \frac{1}{6} = \frac{2}{3}\).  
Thus, \(E[W_i] = 0 \cdot \frac{1}{3} + 1 \cdot \frac{2}{3} = \frac{2}{3}\).  
\(\text{Var}(W_i) = E[W_i^2] - (E[W_i])^2 = \frac{2}{3} - \left(\frac{2}{3}\right)^2 = \frac{2}{3} - \frac{4}{9} = \frac{2}{9}\) (since \(W_i^2 = W_i\)).  
By independence:  
\(E[\|Y\|_2^2] = n \cdot E[W_i] = n \cdot \frac{2}{3}\).  
\(\text{Var}(\|Y\|_2^2) = n \cdot \text{Var}(W_i) = n \cdot \frac{2}{9}\).  

(g) Law of \(Z = X_1 + X_2\)?  
**Solution:**  
>Support: \(\{-2,-1,0,1,2\}\) (all combinations).  
Calculations:  
>- \(Z = -2\): \((-1,-1)\), \(P = \frac{1}{2} \cdot \frac{1}{2} = \frac{1}{4}\).  
>- \(Z = -1\): \((-1,0)\), \((0,-1)\), \(P = \frac{1}{2} \cdot \frac{1}{3} + \frac{1}{3} \cdot \frac{1}{2} = \frac{1}{3}\).  
>- \(Z = 0\): \((-1,1)\), \((0,0)\), \((1,-1)\), \(P = \frac{1}{2} \cdot \frac{1}{6} + \frac{1}{3} \cdot \frac{1}{3} + \frac{1}{6} \cdot \frac{1}{2} = \frac{1}{12} + \frac{1}{9} + \frac{1}{12} = \frac{1}{4} + \frac{1}{9} \ \text{(scaling via 36!)} = \frac{9}{36} + \frac{4}{36} = \frac{13}{36}\)? Let's calculate accurately:  
  \((-1,1)\): \(P = \frac{1}{2} \cdot \frac{1}{6} = \frac{1}{12}\),  
  \((0,0)\): \(P = \frac{1}{3} \cdot \frac{1}{3} = \frac{1}{9} = \frac{4}{36}\),  
  \((1,-1)\): \(P = \frac{1}{6} \cdot \frac{1}{2} = \frac{1}{12} = \frac{3}{36}\),  
  Total \(= \frac{1}{12} + \frac{1}{9} + \frac{1}{12} = \frac{3}{36} + \frac{4}{36} + \frac{3}{36} = \frac{10}{36} = \frac{5}{18}\).  
>- \(Z = 1\): \((0,1)\), \((1,0)\), \(P = \frac{1}{3} \cdot \frac{1}{6} + \frac{1}{6} \cdot \frac{1}{3} = \frac{1}{18} + \frac{1}{18} = \frac{1}{9}\).  
>- \(Z = 2\): \((1,1)\), \(P = \frac{1}{6} \cdot \frac{1}{6} = \frac{1}{36}\).  
Law:  
\(P(Z = -2) = \frac{9}{36}\),  
\(P(Z = -1) = \frac{12}{36}\),  
\(P(Z = 0) = \frac{10}{36}\),  
\(P(Z = 1) = \frac{4}{36}\),  
\(P(Z = 2) = \frac{1}{36}\).  
Simplify: \(\frac{9}{36} = \frac{1}{4}\), but better reduced:  
Sum: \(9 + 12 + 10 + 4 + 1 = 36/36\), so:  
\[
P(Z = -2) = \frac{9}{36}, \quad P(Z = -1) = \frac{12}{36}, \quad P(Z = 0) = \frac{10}{36}, \quad P(Z = 1) = \frac{4}{36}, \quad P(Z = 2) = \frac{1}{36}.
\]  
Simplify fractions: \(\frac{3}{12}\), \(\frac{1}{3}\), \(\frac{5}{18}\), \(\frac{1}{9}\), \(\frac{1}{36}\)? Or leave as is.  

--- 

**Progression:**  
- Variation 1: Basic asymmetric binary with clear constant norm.  
- Variation 2: Triple-valued symmetric, introduces more calculations.  
- Variation 3: \(\{\text{0,1}\}\) support, requires handling sums as binomials.  
- Variation 4: Non-integer support, expands to multiplicative values.  
- Variation 5: Asymmetric triple-valued, most complex distributions and variances.