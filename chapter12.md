
# Cheat Sheet: Convergence of Random Vectors  
*(Based on Chapter 12 of Probability Theory Notes)*  


## Key Definitions  

### 2. **Modes of Convergence**  (strongest to weakest)
Let $(X_n)_{n \in \mathbb{N}}$ be random vectors on $(\Omega, \mathcal{F}, P)$, and $X$ a random vector.  

#### **Almost Sure (a.s.) Convergence**  
**Definition 12.1**:  
$$P\left(\lim_{n \to \infty} X_n = X\right) = 1.$$  
**Notation**: $X_n \xrightarrow{\text{a.s.}} X$.  

#### **$L_p$ Convergence**  
**Definition 12.1**:  
For $p = 1, 2$, assume $E[\|X_n\|^p], E[\|X\|^p] < \infty$. Then,  
$$\lim_{n \to \infty} E\left[\|X_n - X\|^p\right] = 0.$$  
**Notation**: $X_n \xrightarrow{L_p} X$.  

#### **Convergence in Probability**  
**Definition 12.1**:  
For every $\varepsilon > 0$,  
$$\lim_{n \to \infty} P\left(\|X_n - X\| > \varepsilon\right) = 0.$$  
**Notation**: $X_n \xrightarrow{P} X$.  

---

### 3. **Borel-Cantelli Lemma**  
**Proposition 12.1**:  
For events $\{A_n\}_{n \in \mathbb{N}}$:  
- **Part (i)**: If $\sum_{n=1}^\infty P(A_n) < \infty$, then $P\left(\limsup A_n\right) = 0$.  
- **Part (ii)**: If $\{A_n\}$ is independent and $\sum_{n=1}^\infty P(A_n) = \infty$, then $P\left(\limsup A_n\right) = 1$.  

**Intuition**:  
- $\limsup A_n$ = "infinitely many $A_n$ occur."  
- Finite sum ⇒ finitely many events occur almost surely.  
- Infinite sum + independence ⇒ infinitely many events occur almost surely.  

---

### 4. **Hierarchy of Convergence**  
1. **Strongest → Weakest**:  
   - $X_n \xrightarrow{\text{a.s.}} X$ ⟹ $X_n \xrightarrow{P} X$ (Prop 12.3).  
   - $X_n \xrightarrow{L_p} X$ ⟹ $X_n \xrightarrow{P} X$ (Prop 12.2).  
   -  $X_n \xrightarrow{P} X$ ⟹ $X_n \xrightarrow{d} X$ 
   - **No reverse implications hold** (see Remark 12.3).  

2. **Uniqueness of Limits** (Prop 12.4):  
   If $X_n \xrightarrow{P} X$ and $X_n \xrightarrow{P} Y$, then $X = Y$ almost surely.  

---

### 5. **Key Results**  
#### **Subsequence Extraction** (Prop 12.5)  
If $X_n \xrightarrow{P} X$, there exists a subsequence $(X_{s(n)})$ such that $X_{s(n)} \xrightarrow{\text{a.s.}} X$.  

#### **Dominated Convergence for $L_1$** (Prop 12.6)  
If $X_n \xrightarrow{P} X$ and $|X_n| \leq Y$ (with $E[|Y|] < \infty$), then $X_n \xrightarrow{L_1} X$.  

#### **Scheffé’s Lemma** (Prop 12.8)  
If $X_n \xrightarrow{P} X$, $E[|X_n|] \to E[|X|]$, and $E[|X|] < \infty$, then $X_n \xrightarrow{L_1} X$.  

---

### 6. **Law of Large Numbers (LLN)**  
**Strong LLN** (Prop 12.9):  
For i.i.d. $(X_n)_{n \in \mathbb{N}}$ with $E[|X_1|] < \infty$:  
$$\frac{1}{n} \sum_{i=1}^n X_i \xrightarrow{\text{a.s.}} E[X_1].$$  

**Example 12.4**:  
For i.i.d. $X_n$ with mean $\mu$ and variance $\sigma^2$:  
$$\frac{1}{n} \sum_{i=1}^n (X_i - \bar{X}_n)^2 \xrightarrow{\text{a.s.}} \sigma^2.$$  

---

### 7. **Convergence in Distribution**  
**Definition 12.2**:  
$X_n \xrightarrow{d} X$ if for every continuous bounded $\varphi$:  
$$E[\varphi(X_n)] \to E[\varphi(X)].$$  

**Properties** (Remark 12.7):  
1. Weakest form of convergence: $X_n \xrightarrow{P} X$ ⟹ $X_n \xrightarrow{d} X$ (Prop 12.10).  
2. **Lévy’s Theorem**: $X_n \xrightarrow{d} X$ iff $\Phi_{X_n}(v) \to \Phi_X(v)$ for all $v \in \mathbb{R}^k$.  
3. **Central Limit Theorem (CLT)**:  
   For i.i.d. $X_n$ with finite variance:  
   $$\frac{S_n - n\mu}{\sqrt{n}} \xrightarrow{d} \mathcal{N}(0, \sigma^2).$$  

---

## Additional Notes  
- **Continuous Mapping Theorem**: If $X_n \xrightarrow{\text{a.s./}P/d} X$ and $g$ is continuous, then $g(X_n) \xrightarrow{\text{a.s./}P/d} g(X)$ (Prop 12.7, 12.10).  
- **Edge Cases**: See Examples