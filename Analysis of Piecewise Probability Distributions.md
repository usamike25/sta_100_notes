### **Variation 1** (Difficulty: ★☆☆☆☆)
Let  
$$
\phi(x) = 
\begin{cases} 
0 & x < -2 \\
\frac{1}{8}x + \frac{1}{4} & -2 \leq x < 0 \\
\frac{1}{4} - \frac{1}{16}x & 0 \leq x < 4 \\
0 & x \geq 4 
\end{cases}
$$

**(a)** Verify that $\int_{-\infty}^{\infty} \phi(x) \, dx = 1$. [2]  
**(b)** Find the distribution function $F_X$ of $X$. [4]  
**(c)** Calculate $\mathbb{E}[X]$ and $\text{Var}(X)$. [5]  
**(d)** Show $F_X|_{(-2,4)} : (-2,4) \to (0,1)$ is a bijection. [3]  
**(e)** Verify $F_X|_{[-2,4]} : [-2,4] \to [0,1]$ is a bijection. [1]  
**(f)** Find $F_X^{-1}|_{[-2,4]}$. [3]

---

### **Variation 2** (Difficulty: ★★☆☆☆)
Let  
$$
\phi(x) = 
\begin{cases} 
0 & x < -4 \\
\frac{1}{36}x + \frac{1}{12} & -4 \leq x < -1 \\
\frac{1}{6} & -1 \leq x < 1 \\
\frac{1}{12} - \frac{1}{72}(x-3) & 1 \leq x < 4 \\
0 & x \geq 4 
\end{cases}
$$

**(a)** Verify $\int \phi(x) \, dx = 1$. [2]  
**(b)** Derive $F_X$. [5]  
**(c)** Compute $\mathbb{E}[X]$ and $\text{Var}(X)$. [5]  
**(d)** Prove $F_X|_{(-4,4)} : (-4,4) \to (0,1)$ is bijective. [3]  
**(e)** Explain why $F_X|_{[-4,4]} : [-4,4] \to [0,1]$ is bijective. [1]  
**(f)** Find $F_X^{-1}|_{[-4,4]}$. [4]

---

### **Variation 3** (Difficulty: ★★★☆☆)
Let  
$$
\phi(x) = 
\begin{cases} 
0 & x < 0 \\
\frac{1}{8}x & 0 \leq x < 2 \\
\frac{1}{4}e^{2-x} & 2 \leq x < 4 \\
0 & x \geq 4 
\end{cases}
$$

**(a)** Show $\int \phi(x) \, dx = 1$. [3] *(Requires integration by parts)*  
**(b)** Find $F_X$. [5]  
**(c)** Compute $\mathbb{E}[X]$ and $\text{Var}(X)$. [6]  
**(d)** Prove bijectivity for $F_X|_{(0,4)} : (0,4) \to (0,1)$. [3]  
**(e)** Show $F_X|_{[0,4]} : [0,4] \to [0,1]$ is bijective. [1]  
**(f)** Derive $F_X^{-1}|_{[0,4]}$. [4] *(Inverse involves logarithms)*  

---

### **Variation 4** (Difficulty: ★★★★☆)
Let  
$$
\phi(x) = 
\begin{cases} 
0 & x < -\pi \\
\frac{1}{8}\cos\left(\frac{x}{2}\right) & -\pi \leq x < 0 \\
\frac{1}{8}(1 + \sin x) & 0 \leq x < \frac{\pi}{2} \\
0 & x \geq \frac{\pi}{2} 
\end{cases}
$$

**(a)** Verify $\int \phi(x) \, dx = 1$. [4] *(Trigonometric integrals)*  
**(b)** Find $F_X$. [6] *(Multi-part integration)*  
**(c)** Calculate $\mathbb{E}[X]$ and $\text{Var}(X)$. [7]  
**(d)** Prove $F_X|_{(-\pi, \pi/2)} : (-\pi, \pi/2) \to (0,1)$ is bijective. [3]  
**(e)** Is $F_X|_{[-\pi, \pi/2]} : [-\pi, \pi/2] \to [0,1]$ bijective? Justify. [2]  
**(f)** Find $F_X^{-1}|_{[-\pi, \pi/2]}$. [5] *(Requires solving transcendental equations)*  

---

### **Variation 5** (Difficulty: ★★★★★)
Let  
$$
\phi(x) = 
\begin{cases} 
0 & x < -3 \\
\frac{1}{20}(x+5) & -3 \leq x < -1 \\
\frac{1}{10\sqrt{4-x^2}} & -1 \leq x < 1 \\
\frac{1}{20}(5-x) & 1 \leq x < 5 \\
0 & x \geq 5 
\end{cases}
$$

**(a)** Prove $\int \phi(x) \, dx = 1$. [5] *(Uses geometry and trig substitution)*  
**(b)** Derive $F_X$ explicitly. [7] *(Requires elliptic integral for $\sqrt{4-x^2}$)*  
**(c)** Compute $\mathbb{E}[X]$ and $\text{Var}(X)$. [8] *(High-symmetry simplifies variance)*  
**(d)** Show $F_X|_{(-3,5)} : (-3,5) \to (0,1)$ is bijective. [4]  
**(e)** Verify $F_X|_{[-3,5]} : [-3,5] \to [0,1]$ is bijective. [2]  
**(f)** Find $F_X^{-1}|_{[-3,5]}$ symbolically. [6] *(Inverse for $\sqrt{4-x^2}$ is non-algebraic)*  

---

### **Progression Rationale**  
1. **Variation 1**: Asymmetric intervals, basic linear pieces.  
2. **Variation 2**: Four segments with discontinuities and shifted intervals.  
3. **Variation 3**: Exponential decay segment requiring advanced integration.  
4. **Variation 4**: Trigonometric functions and transcendental inverse.  
5. **Variation 5**: Elliptic integral in CDF, non-algebraic inverse, and asymmetric support.  