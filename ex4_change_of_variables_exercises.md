### **Original Exercise & Solution**  
**Exercise 4 (6 points).**  
Let \( X_1 \) and \( X_2 \) be two random variables that are independent with a common uniform distribution on \([0,1]\).  
**Question:** What is the PDF of the random vector \( Y = \left(\frac{1 + X_1}{2}, X_2\right) \)?  

>**Solution:**  
>- **Transformation:** \( Y_1 = \frac{1 + X_1}{2}, Y_2 = X_2 \).  
>- **Inverse:** \( X_1 = 2Y_1 - 1, X_2 = Y_2 \).  
>- **Jacobian:**  
  \[
  |J| = \det \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} = 2.
  \]  
>- **Support for \( Y \):**  
  \( \frac{1}{2} \leq Y_1 \leq 1 \) (from \( 0 \leq 2Y_1 - 1 \leq 1 \)) and \( 0 \leq Y_2 \leq 1 \).  
>- **PDF:**  
  \[
  f_Y(y_1, y_2) = 
  \begin{cases} 
  2 & \text{if } (y_1, y_2) \in [\frac{1}{2}, 1] \times [0, 1], \\
  0 & \text{otherwise.}
  \end{cases}
  \]  

---

### **Variation 1: Simple Linear Transformation**  
**Exercise:**  
Let \( X_1, X_2 \sim \text{Uniform}(0,1) \) be independent. Find the PDF of \( Y = (2X_1, 3X_2) \).  

>**Solution:**  
>- **Inverse:** \( X_1 = Y_1/2, X_2 = Y_2/3 \).  
>- **Jacobian:** \( |J| = \det \begin{pmatrix} 1/2 & 0 \\ 0 & 1/3 \end{pmatrix} = \frac{1}{6} \).  
>- **Support:** \( Y \in [0, 2] \times [0, 3] \).  
>- **PDF:**  
  \[
  f_Y(y_1, y_2) = 
  \begin{cases} 
  \frac{1}{6} & \text{if } (y_1, y_2) \in [0, 2] \times [0, 3], \\
  0 & \text{otherwise.}
  \end{cases}
  \]  

---

### **Variation 2: Coupled Linear Transformation**  
**Exercise:**  
For \( X_1, X_2 \sim \text{Uniform}(0,1) \), find the PDF of \( Y = (X_1 + X_2, X_1 - X_2) \).  

>**Solution:**  
>- **Inverse:** \( X_1 = \frac{Y_1 + Y_2}{2}, X_2 = \frac{Y_1 - Y_2}{2} \).  
>- **Jacobian:** \( |J| = \det \begin{pmatrix} 1/2 & 1/2 \\ 1/2 & -1/2 \end{pmatrix} = \frac{1}{2} \).  
>- **Support:** Parallelogram bounded by \( y_1 + y_2 = 0, 2 \) and \( y_1 - y_2 = 0, 2 \).  
>- **PDF:**  
  \[
  f_Y(y_1, y_2) = 
  \begin{cases} 
  \frac{1}{2} & \text{in the support}, \\
  0 & \text{otherwise.}
  \end{cases}
  \]  

---

### **Variation 3: Non-Linear Transformation**  
**Exercise:**  
For \( X_1, X_2 \sim \text{Uniform}(0,1) \), find the PDF of \( Y = (X_1^2, X_2) \).  

>**Solution:**  
>- **Inverse:** \( X_1 = \sqrt{Y_1}, X_2 = Y_2 \).  
>- **Jacobian:** \( |J| = \det \begin{pmatrix} \frac{1}{2\sqrt{y_1}} & 0 \\ 0 & 1 \end{pmatrix} = \frac{1}{2\sqrt{y_1}} \).  
>- **Support:** \( Y \in [0, 1] \times [0, 1] \).  
>- **PDF:**  
  \[
  f_Y(y_1, y_2) = 
  \begin{cases} 
  \frac{1}{2\sqrt{y_1}} & \text{if } (y_1, y_2) \in (0, 1] \times [0, 1], \\
  0 & \text{otherwise.}
  \end{cases}
  \]  

---

### **Variation 4: Exponential Distribution**  
**Exercise:**  
Let \( X_1, X_2 \sim \text{Exp}(1) \). Find the PDF of \( Y = \left(\frac{1 + X_1}{2}, X_2\right) \).  

>**Solution:**  
>- **Inverse/Jacobian:** Identical to Original (but \( f_X(x_1, x_2) = e^{-(x_1 + x_2)} \)).  
>- **Support:** \( Y_1 \geq \frac{1}{2}, Y_2 \geq 0 \).  
>- **PDF:**  
  \[
  f_Y(y_1, y_2) = 
  \begin{cases} 
  2e^{1 - 2y_1 - y_2} & \text{if } y_1 \geq \frac{1}{2}, y_2 \geq 0, \\
  0 & \text{otherwise.}
  \end{cases}
  \]  

---

### **Variation 5: Ratio Transformation**  
**Exercise:**  
For \( X_1, X_2 \sim \text{Uniform}(0,1) \), find the PDF of \( Y = (X_1 / X_2, X_2) \).  

>**Solution:**  
>- **Inverse:** \( X_1 = Y_1 Y_2, X_2 = Y_2 \).  
>- **Jacobian:** \( |J| = \det \begin{pmatrix} y_2 & y_1 \\ 0 & 1 \end{pmatrix} = y_2 \).  
>- **Support:** \( 0 \leq Y_2 \leq 1, 0 \leq Y_1 \leq \frac{1}{Y_2} \).  
>- **PDF:**  
  \[
  f_Y(y_1, y_2) = 
  \begin{cases} 
  y_2 & \text{in the support}, \\
  0 & \text{otherwise.}
  \end{cases}
  \]  

  ### **Variation 6: Order Statistics**
**Exercise:**
Let \( X_1, X_2 \sim \text{Uniform}(0,1) \) be independent. Find the PDF of \( Y = (Y_1, Y_2) \) where \( Y_1 = \min(X_1, X_2) \) and \( Y_2 = \max(X_1, X_2) \).
> **Solution:**
> - **Note:** This transformation is not one-to-one. For any pair \( (y_1, y_2) \) in the support of Y, there are two points in the support of X, namely \( (y_1, y_2) \) and \( (y_2, y_1) \), that map to it. We must sum their contributions.
> - **Inverse Mappings:**
>   1. \( X_1 = Y_1, X_2 = Y_2 \)
>   2. \( X_1 = Y_2, X_2 = Y_1 \)
> - **Jacobians:**
>   1. \( |J_1| = \det \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = 1 \)
>   2. \( |J_2| = \det \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} = |-1| = 1 \)
> - **Support for \( Y \):** Since \( 0 \leq X_1, X_2 \leq 1 \), the support for Y is the triangle defined by \( 0 \leq Y_1 \leq Y_2 \leq 1 \).
> - **PDF:**
>   The PDF is given by \( f_Y(y_1, y_2) = f_X(y_1, y_2)|J_1| + f_X(y_2, y_1)|J_2| \). Since \( f_X(x_1, x_2)=1 \) on its support.
>   \[
>   f_Y(y_1, y_2) =
>   \begin{cases}
>   1 \cdot 1 + 1 \cdot 1 = 2 & \text{if } 0 \leq y_1 \leq y_2 \leq 1, \\
>   0 & \text{otherwise.}
>   \end{cases}
>   \]
---
### **Variation 7: Polar Coordinates Transformation**
**Exercise:**
Let \( X_1, X_2 \sim N(0,1) \) be independent. Find the PDF of \( (R, \Theta) \) where \( X_1 = R \cos\Theta \) and \( X_2 = R \sin\Theta \).
> **Solution:**
> - **Original PDF:** \( f_X(x_1, x_2) = \frac{1}{2\pi} e^{-(x_1^2 + x_2^2)/2} \).
> - **Inverse:** The transformation is given, so the inverse maps from \( (x_1, x_2) \) to \( (r, \theta) \). We need the Jacobian of the forward transformation \( (r, \theta) \to (x_1, x_2) \).
> - **Jacobian:**
>   \[
>   |J| = \det \begin{pmatrix} \frac{\partial x_1}{\partial r} & \frac{\partial x_1}{\partial \theta} \\ \frac{\partial x_2}{\partial r} & \frac{\partial x_2}{\partial \theta} \end{pmatrix} = \det \begin{pmatrix} \cos\theta & -r\sin\theta \\ \sin\theta & r\cos\theta \end{pmatrix} = r\cos^2\theta + r\sin^2\theta = r.
>   \]
> - **Support for \( (R, \Theta) \):** \( x_1, x_2 \in (-\infty, \infty) \) implies \( R \ge 0 \) and \( \Theta \in [0, 2\pi) \).
> - **PDF:** Note that \( x_1^2 + x_2^2 = r^2 \).
>   \[
>   f_{R,\Theta}(r, \theta) = f_X(r\cos\theta, r\sin\theta) |J| = \frac{1}{2\pi} e^{-r^2/2} \cdot r.
>   \]
>   \[
>   f_{R,\Theta}(r, \theta) =
>   \begin{cases}
>   \frac{r}{2\pi} e^{-r^2/2} & \text{if } r \geq 0, \theta \in [0, 2\pi), \\
>   0 & \text{otherwise.}
>   \end{cases}
>   \]
---
### **Variation 8: Sum and One Variable (Exponential)**
**Exercise:**
Let \( X_1, X_2 \sim \text{Exp}(1) \) be independent. Find the PDF of \( Y = (X_1, X_1 + X_2) \).
> **Solution:**
> - **Original PDF:** \( f_X(x_1, x_2) = e^{-(x_1+x_2)} \) for \( x_1, x_2 > 0 \).
> - **Inverse:** \( X_1 = Y_1, X_2 = Y_2 - Y_1 \).
> - **Jacobian:**
>   \[
>   |J| = \det \begin{pmatrix} 1 & 0 \\ -1 & 1 \end{pmatrix} = 1.
>   \]
> - **Support for \( Y \):** \( X_1 > 0 \Rightarrow Y_1 > 0 \). \( X_2 > 0 \Rightarrow Y_2 - Y_1 > 0 \Rightarrow Y_2 > Y_1 \). So the support is \( 0 < y_1 < y_2 \).
> - **PDF:**
>   \[
>   f_Y(y_1, y_2) = f_X(y_1, y_2-y_1)|J| = e^{-(y_1 + (y_2 - y_1))} \cdot 1 = e^{-y_2}.
>   \]
>   \[
>   f_Y(y_1, y_2) =
>   \begin{cases}
>   e^{-y_2} & \text{if } 0 < y_1 < y_2, \\
>   0 & \text{otherwise.}
>   \end{cases}
>   \]
---
### **Variation 9: Logarithmic Transformation**
**Exercise:**
Let \( X_1, X_2 \sim \text{Uniform}(0,1) \) be independent. Find the PDF of \( Y = (-\ln X_1, -\ln X_2) \).
> **Solution:**
> - **Inverse:** \( X_1 = e^{-Y_1}, X_2 = e^{-Y_2} \).
> - **Jacobian:**
>   \[
>   |J| = \det \begin{pmatrix} -e^{-y_1} & 0 \\ 0 & -e^{-y_2} \end{pmatrix} = e^{-y_1}e^{-y_2} = e^{-(y_1+y_2)}.
>   \]
> - **Support for \( Y \):** \( X_1, X_2 \in (0,1) \implies -\ln X_1, -\ln X_2 \in (0, \infty) \). So \( y_1 > 0, y_2 > 0 \).
> - **PDF:** \( f_X(x_1, x_2) = 1 \) on \( (0,1)^2 \).
>   \[
>   f_Y(y_1, y_2) = 1 \cdot |e^{-(y_1+y_2)}| = e^{-y_1}e^{-y_2}.
>   \]
>   \[
>   f_Y(y_1, y_2) =
>   \begin{cases}
>   e^{-y_1}e^{-y_2} & \text{if } y_1 > 0, y_2 > 0, \\
>   0 & \text{otherwise.}
>   \end{cases}
>   \]
>   This shows that \( Y_1 \) and \( Y_2 \) are independent Exp(1) random variables.
---
### **Variation 10: Box-Muller Transformation**
**Exercise:**
For \( X_1, X_2 \sim \text{Uniform}(0,1) \), find the PDF of \( Y = (Y_1, Y_2) \) where \( Y_1 = \sqrt{-2\ln X_1} \cos(2\pi X_2) \) and \( Y_2 = \sqrt{-2\ln X_1} \sin(2\pi X_2) \).
> **Solution:**
> - **Inverse:**
>   \( Y_1^2 + Y_2^2 = -2\ln X_1 \implies X_1 = e^{-(Y_1^2 + Y_2^2)/2} \).
>   \( Y_2/Y_1 = \tan(2\pi X_2) \implies X_2 = \frac{1}{2\pi}\arctan(Y_2/Y_1) \).
> - **Jacobian:** The Jacobian of the inverse transformation \( (Y_1, Y_2) \to (X_1, X_2) \) is:
>   \[
>   |J| = \left| \det \begin{pmatrix} \frac{\partial x_1}{\partial y_1} & \frac{\partial x_1}{\partial y_2} \\ \frac{\partial x_2}{\partial y_1} & \frac{\partial x_2}{\partial y_2} \end{pmatrix} \right| = \left| -\frac{1}{2\pi}e^{-(y_1^2+y_2^2)/2} \right| = \frac{1}{2\pi}e^{-(y_1^2+y_2^2)/2}.
>   \]
> - **Support for \( Y \):** \( X_1, X_2 \in (0,1) \) maps to \( (Y_1, Y_2) \in \mathbb{R}^2 \).
> - **PDF:**
>   \[
>   f_Y(y_1, y_2) = f_X(x_1(y), x_2(y))|J| = 1 \cdot \frac{1}{2\pi}e^{-(y_1^2+y_2^2)/2}.
>   \]
>   This is the PDF of two independent standard normal random variables.
---
### **Variation 11: Ratio of Normal Variables**
**Exercise:**
Let \( X_1, X_2 \sim N(0,1) \) be independent. Find the joint PDF of \( Y = (X_1/X_2, X_2) \).
> **Solution:**
> - **Original PDF:** \( f_X(x_1, x_2) = \frac{1}{2\pi} e^{-(x_1^2 + x_2^2)/2} \).
> - **Inverse:** \( X_1 = Y_1 Y_2, X_2 = Y_2 \).
> - **Jacobian:**
>   \[
>   |J| = \det \begin{pmatrix} y_2 & y_1 \\ 0 & 1 \end{pmatrix} = |y_2|.
>   \]
> - **Support for \( Y \):** \( X_1, X_2 \in (-\infty, \infty) \implies Y_1, Y_2 \in (-\infty, \infty) \).
> - **PDF:**
>   \[
>   f_Y(y_1, y_2) = f_X(y_1 y_2, y_2)|J| = \frac{1}{2\pi} e^{-((y_1y_2)^2 + y_2^2)/2} |y_2|.
>   \]
>   \[
>   f_Y(y_1, y_2) =
>   \begin{cases}
>   \frac{|y_2|}{2\pi} e^{-y_2^2(1+y_1^2)/2} & \text{for } (y_1, y_2) \in \mathbb{R}^2, \\
>   0 & \text{otherwise.}
>   \end{cases}
>   \]
---
### **Variation 12: Sum and Ratio of Exponentials**
**Exercise:**
Let \( X_1, X_2 \sim \text{Exp}(1) \) be independent. Find the PDF of \( Y = (X_1+X_2, \frac{X_1}{X_1+X_2}) \).
> **Solution:**
> - **Inverse:** \( X_1 = Y_1 Y_2, X_2 = Y_1(1-Y_2) \).
> - **Jacobian:**
>   \[
>   |J| = \det \begin{pmatrix} y_2 & y_1 \\ 1-y_2 & -y_1 \end{pmatrix} = |-y_1y_2 - y_1(1-y_2)| = |-y_1| = y_1 \quad (\text{since } Y_1>0).
>   \]
> - **Support for \( Y \):** \( X_1, X_2 > 0 \) implies \( Y_1 = X_1+X_2 > 0 \) and \( Y_2 = \frac{X_1}{X_1+X_2} \in (0,1) \).
> - **PDF:** \( f_X(x_1, x_2) = e^{-(x_1+x_2)} \). Note \( x_1+x_2 = y_1 \).
>   \[
>   f_Y(y_1, y_2) = f_X(y_1y_2, y_1(1-y_2))|J| = e^{-y_1} \cdot y_1.
>   \]
>   \[
>   f_Y(y_1, y_2) =
>   \begin{cases}
>   y_1 e^{-y_1} & \text{if } y_1>0, y_2 \in (0,1), \\
>   0 & \text{otherwise.}
>   \end{cases}
>   \]
>   This shows \( Y_1 \sim \text{Gamma}(2,1) \) is independent of \( Y_2 \sim \text{Uniform}(0,1) \).
---
### **Variation 13: Transformation on a Triangular Support**
**Exercise:**
Let \( (X_1, X_2) \) be uniform on the triangle \( S = \{(x_1, x_2) : x_1>0, x_2>0, x_1+x_2 < 1\} \). Find the PDF of \( Y = (X_1+X_2, X_1-X_2) \).
> **Solution:**
> - **Original PDF:** The area of S is \( 1/2 \), so \( f_X(x_1, x_2) = 2 \) on S, and 0 otherwise.
> - **Inverse:** \( X_1 = \frac{Y_1+Y_2}{2}, X_2 = \frac{Y_1-Y_2}{2} \).
> - **Jacobian:** \( |J| = \det \begin{pmatrix} 1/2 & 1/2 \\ 1/2 & -1/2 \end{pmatrix} = | -1/4 - 1/4 | = 1/2 \).
> - **Support for \( Y \):** The vertices (0,0), (1,0), (0,1) of S map to (0,0), (1,1), (1,-1) in the Y-plane. The support is the triangle bounded by \( y_1 > |y_2| \) and \( y_1 < 1 \).
> - **PDF:**
>   \[
>   f_Y(y_1, y_2) = f_X(\dots)|J| = 2 \cdot \frac{1}{2} = 1.
>   \]
>   \[
>   f_Y(y_1, y_2) =
>   \begin{cases}
>   1 & \text{in the triangular region with vertices (0,0), (1,1), (1,-1)}, \\
>   0 & \text{otherwise.}
>   \end{cases}
>   \]
---
### **Variation 14: Product and Ratio Transformation**
**Exercise:**
For \( X_1, X_2 \sim \text{Uniform}(0,1) \), find the PDF of \( Y = (X_1 X_2, X_1/X_2) \).
> **Solution:**
> - **Inverse:** \( X_1 = \sqrt{Y_1 Y_2}, X_2 = \sqrt{Y_1/Y_2} \).
> - **Jacobian:**
>   \[
>   |J| = \det \begin{pmatrix} \frac{\sqrt{y_2}}{2\sqrt{y_1}} & \frac{\sqrt{y_1}}{2\sqrt{y_2}} \\ \frac{1}{2\sqrt{y_1y_2}} & \frac{-\sqrt{y_1}}{2y_2\sqrt{y_2}} \end{pmatrix} = |-\frac{1}{4y_2} - \frac{1}{4y_2}| = \frac{1}{2y_2}.
>   \]
> - **Support for \( Y \):** \( 0 < X_1, X_2 < 1 \) implies \( 0 < Y_1 < Y_2 \) and \( Y_1 Y_2 < 1 \).
> - **PDF:**
>  \[
>   f_Y(y_1, y_2) = f_X(\dots)|J| = 1 \cdot \frac{1}{2y_2}.
>   \]
>   \[
>   f_Y(y_1, y_2) =
>   \begin{cases}
>   \frac{1}{2y_2} & \text{if } 0 < y_1 < y_2 \text{ and } y_1 y_2 < 1, \\
>   0 & \text{otherwise.}
>   \end{cases}
>   \]
---
### **Variation 15: Beta Distribution from Gamma Variables**
**Exercise:**
Let \( X_1 \sim \text{Gamma}(2,1) \) and \( X_2 \sim \text{Gamma}(3,1) \) be independent. Find the PDF of \( Y = (X_1+X_2, \frac{X_1}{X_1+X_2}) \).
> **Solution:**
> - **Original PDF:** \( f_X(x_1, x_2) = \frac{1}{\Gamma(2)\Gamma(3)}x_1^{2-1}e^{-x_1} x_2^{3-1}e^{-x_2} = \frac{1}{2}x_1 x_2^2 e^{-(x_1+x_2)} \).
> - **Inverse:** \( X_1 = Y_1 Y_2, X_2 = Y_1(1-Y_2) \).
> - **Jacobian:** \(|J|=y_1\) (as in Var 12).
> - **Support for \( Y \):** \( X_1, X_2 > 0 \) implies \( Y_1 > 0 \) and \( Y_2 \in (0,1) \).
> - **PDF:**
>   \[
>   f_Y(y_1, y_2) = \frac{1}{2}(y_1y_2)(y_1(1-y_2))^2 e^{-y_1} \cdot y_1 = \frac{1}{2}y_1^4 y_2(1-y_2)^2 e^{-y_1}.
>   \]
>   \[
>   f_Y(y_1, y_2) =
>   \begin{cases}
>    \frac{1}{2}y_1^4 y_2(1-y_2)^2 e^{-y_1} & \text{if } y_1>0, y_2 \in (0,1), \\
>   0 & \text{otherwise.}
>   \end{cases}
>   \]
>   This can be factored to show \( Y_1 \sim \text{Gamma}(5,1) \) is independent of \( Y_2 \sim \text{Beta}(2,3) \).
>
# Bous 
### Variation 6: Coupled Linear Transformation with Different Coefficients  
**Exercise:**  
Let \( X_1, X_2 \sim \text{Uniform}(0,1) \) be independent. Find the PDF of  
\[
Y = \Bigl(2X_1 + X_2,\; X_1 - X_2\Bigr).
\]

>**Solution:**  
>- **Inverse:**  
  Write  
  \[
  \begin{cases}
  y_1 = 2x_1 + x_2,\\[1mm]
  y_2 = x_1 - x_2.
  \end{cases}
  \]
  Solve for \(x_1\) and \(x_2\). From the second equation,  
  \[
  x_1 = y_2 + x_2.
  \]
  Substitute into the first equation:  
  \[
  y_1 = 2(y_2+x_2) + x_2 = 2y_2 + 3x_2 \quad \Longrightarrow \quad x_2 = \frac{y_1 - 2y_2}{3}.
  \]
  Then,  
  \[
  x_1 = y_2 + \frac{y_1-2y_2}{3} = \frac{y_1+y_2}{3}.
  \]
>- **Jacobian:**  
  Compute the partial derivatives:
  \[
  \frac{\partial x_1}{\partial y_1}=\frac{1}{3},\quad \frac{\partial x_1}{\partial y_2}=\frac{1}{3},\quad \frac{\partial x_2}{\partial y_1}=\frac{1}{3},\quad \frac{\partial x_2}{\partial y_2}=-\frac{2}{3}.
  \]
  Hence,
  \[
  |J| = \left|\det \begin{pmatrix} 1/3 & 1/3 \\[0.5mm] 1/3 & -2/3 \end{pmatrix}\right| = \left|\frac{1}{3}\cdot\left(-\frac{2}{3}\right) - \frac{1}{3}\cdot\frac{1}{3}\right| = \left|\frac{-2-1}{9}\right| = \frac{1}{3}.
  \]
>- **Support:**  
  Since \(x_1,x_2\in[0,1]\), we require
  \[
  0\le \frac{y_1+y_2}{3}\le 1 \quad \Longrightarrow \quad 0\le y_1+y_2\le 3,
  \]
  \[
  0\le \frac{y_1-2y_2}{3}\le 1 \quad \Longrightarrow \quad 0\le y_1-2y_2\le 3.
  \]
>- **PDF:**  
  \[
  f_Y(y_1,y_2)=
  \begin{cases}
  \frac{1}{3}, & \text{if } (y_1,y_2) \text{ satisfy } 0\le y_1+y_2\le 3 \text{ and } 0\le y_1-2y_2\le 3,\\[1mm]
  0, & \text{otherwise.}
  \end{cases}
  \]

---

### Variation 7: Non-Linear Transformation with Cube and Square Root  
**Exercise:**  
Let \( X_1, X_2 \sim \text{Uniform}(0,1) \). Find the PDF of  
\[
Y = \Bigl(X_1^3,\; \sqrt{X_2}\Bigr).
\]

>**Solution:**  
>- **Inverse:**  
  \[
  x_1 = \sqrt[3]{y_1},\quad x_2 = y_2^2.
  \]
>- **Jacobian:**  
  Compute the derivatives:
  \[
  \frac{d x_1}{dy_1} = \frac{1}{3} y_1^{-2/3},\quad \frac{d x_2}{dy_2} = 2y_2.
  \]
  Hence,
  \[
  |J| = \frac{1}{3} y_1^{-2/3}\cdot 2y_2 = \frac{2y_2}{3y_1^{2/3}}.
  \]
>- **Support:**  
  Since \(x_1,x_2\in[0,1]\):
  \[
  y_1\in [0,1] \quad (\text{with } y_1>0 \text{ for the derivative to be defined}),\quad y_2\in [0,1].
  \]
>- **PDF:**  
  \[
  f_Y(y_1,y_2)=
  \begin{cases}
  \dfrac{2y_2}{3y_1^{2/3}}, & \text{if } y_1\in (0,1] \text{ and } y_2\in [0,1],\\[1mm]
  0, & \text{otherwise.}
  \end{cases}
  \]

---

### Variation 8: Logarithm and Square Root Transformation for Exponential Variables  
**Exercise:**  
Let \( X_1, X_2 \sim \text{Exp}(1) \). Find the PDF of  
\[
Y = \Bigl(\ln(1+X_1),\; \sqrt{X_2}\Bigr).
\]

>**Solution:**  
>- **Inverse:**  
  \[
  x_1 = e^{y_1} - 1,\quad x_2 = y_2^2.
  \]
>- **Jacobian:**  
  \[
  \frac{dx_1}{dy_1} = e^{y_1},\quad \frac{dx_2}{dy_2} = 2y_2 \quad \Longrightarrow \quad |J| = 2y_2\, e^{y_1}.
  \]
>- **Original PDF:**  
  Since \( f_X(x_1,x_2)= e^{-(x_1+x_2)} \), substituting the inverses gives
  \[
  f_X\bigl(e^{y_1}-1,y_2^2\bigr)= e^{-((e^{y_1}-1)+y_2^2)} = e^{\,1 - e^{y_1} - y_2^2}.
  \]
>- **PDF:**  
  \[
  f_Y(y_1,y_2)= 2y_2\, e^{y_1}\, e^{\,1 - e^{y_1} - y_2^2} = 2y_2\, e^{\,1+y_1 - e^{y_1} - y_2^2}.
  \]
>- **Support:**  
  \( y_1 \ge 0 \) and \( y_2 \ge 0 \).

---

### Variation 9: Ratio and Product Transformation  
**Exercise:**  
Let \( X_1, X_2 \sim \text{Uniform}(0,1) \). Find the PDF of  
\[
Y = \Bigl(\frac{X_1}{X_2},\; X_1X_2\Bigr).
\]

>**Solution:**  
>- **Inverse:**  
  From \( y_1=\frac{x_1}{x_2} \) we get \( x_1 = y_1 x_2 \). Then, since  
  \[
  y_2 = x_1x_2 = y_1x_2^2,\quad \text{it follows that} \quad x_2 = \sqrt{\frac{y_2}{y_1}},
  \]
  and so  
  \[
  x_1 = \sqrt{y_1y_2}.
  \]
>- **Jacobian:**  
  A careful computation (omitting intermediate algebra) shows that  
  \[
  |J| = \frac{1}{2y_1}.
  \]
>- **Support:**  
  For \(x_1,x_2\in[0,1]\) we require  
  \[
  \sqrt{y_1y_2}\le 1 \quad \Longrightarrow \quad y_1y_2 \le 1,
  \]
  and
  \[
  \sqrt{\frac{y_2}{y_1}} \le 1 \quad \Longrightarrow \quad y_2 \le y_1.
  \]
  Thus, the support is  
  \[
  y_1>0,\quad 0\le y_2 \le \min\Bigl(y_1,\, \frac{1}{y_1}\Bigr).
  \]
>- **PDF:**  
  \[
  f_Y(y_1,y_2)=
  \begin{cases}
  \dfrac{1}{2y_1}, & \text{if } y_1>0,\; 0\le y_2\le \min\left(y_1,\, \frac{1}{y_1}\right),\\[1mm]
  0, & \text{otherwise.}
  \end{cases}
  \]

---

### Variation 10: Multiplicative Transformation  
**Exercise:**  
Let \( X_1, X_2 \sim \text{Uniform}(0,1) \). Find the PDF of  
\[
Y = \Bigl(X_1,\; X_1X_2\Bigr).
\]

>**Solution:**  
>- **Inverse:**  
  Clearly,  
  \[
  x_1 = y_1,\quad x_2 = \frac{y_2}{y_1} \quad \text{(with } y_1>0 \text{)}.
  \]
>- **Jacobian:**  
  The Jacobian matrix is
  \[
  J = \begin{pmatrix}
  \frac{\partial x_1}{\partial y_1} & \frac{\partial x_1}{\partial y_2}\\[1mm]
  \frac{\partial x_2}{\partial y_1} & \frac{\partial x_2}{\partial y_2}
  \end{pmatrix} =
  \begin{pmatrix}
  1 & 0\\[1mm]
  -\frac{y_2}{y_1^2} & \frac{1}{y_1}
  \end{pmatrix}.
  \]
  Hence,  
  \[
  |J| = 1\cdot \frac{1}{y_1} - 0 = \frac{1}{y_1}.
  \]
>- **Support:**  
  \( x_1\in[0,1] \) implies \( y_1\in (0,1] \) and \( x_2\in[0,1] \) requires  
  \[
  0\le \frac{y_2}{y_1}\le 1 \quad \Longrightarrow \quad 0\le y_2 \le y_1.
  \]
>- **PDF:**  
  \[
  f_Y(y_1,y_2)=
  \begin{cases}
  \dfrac{1}{y_1}, & \text{if } y_1\in (0,1] \text{ and } 0\le y_2\le y_1,\\[1mm]
  0, & \text{otherwise.}
  \end{cases}
  \]

---

### Variation 11: Logarithmic Transformation for Exponential Variables  
**Exercise:**  
Let \( X_1, X_2 \sim \text{Exp}(1) \). Find the PDF of  
\[
Y = \Bigl(\ln(1+X_1),\; \ln(1+X_2)\Bigr).
\]

>**Solution:**  
>- **Inverse:**  
  \[
  x_1 = e^{y_1} - 1,\quad x_2 = e^{y_2} - 1.
  \]
>- **Jacobian:**  
  \[
  \frac{dx_1}{dy_1} = e^{y_1},\quad \frac{dx_2}{dy_2} = e^{y_2} \quad \Longrightarrow \quad |J| = e^{y_1+y_2}.
  \]
>- **Original PDF:**  
  \[
  f_X(x_1,x_2)= e^{-(x_1+x_2)} = e^{-\bigl[(e^{y_1}-1)+(e^{y_2}-1)\bigr]} = e^{\,2-e^{y_1}-e^{y_2}}.
  \]
>- **PDF:**  
  \[
  f_Y(y_1,y_2)= e^{y_1+y_2}\, e^{\,2-e^{y_1}-e^{y_2}} = e^{\,2+y_1+y_2-e^{y_1}-e^{y_2}}.
  \]
>- **Support:**  
  \( y_1,y_2\ge 0 \).

---

### Variation 12: Sum and Component Transformation  
**Exercise:**  
Let \( X_1, X_2 \sim \text{Uniform}(0,1) \). Find the PDF of  
\[
Y = \Bigl(X_1+X_2,\; X_1\Bigr).
\]

>**Solution:**  
>- **Inverse:**  
  \[
  x_1 = y_2,\quad x_2 = y_1 - y_2.
  \] 
>- **Jacobian:**  
  The transformation is linear with  
  \[
  |J| = \Bigl|\det \begin{pmatrix} 0 & 1 \\[1mm] 1 & -1 \end{pmatrix}\Bigr| = 1.
  \] 
>- **Support:**  
  \( x_1\in[0,1] \) gives \( y_2\in[0,1] \). Also, \( x_2\in[0,1] \) implies  
  \[
  0\le y_1-y_2\le 1 \quad \Longrightarrow \quad y_2 \le y_1 \le y_2+1.
  \] 
>- **PDF:**  
  \[
  f_Y(y_1,y_2)=
  \begin{cases}
  1, & \text{if } y_2\in[0,1] \text{ and } y_2\le y_1\le y_2+1,\\[1mm]
  0, & \text{otherwise.}
  \end{cases}
  \]

---

### Variation 13: Quadratic Addition Transformation  
**Exercise:**  
Let \( X_1, X_2 \sim \text{Uniform}(0,1) \). Find the PDF of  
\[
Y = \Bigl(X_1,\; X_1^2 + X_2\Bigr).
\]

>**Solution:**  
>- **Inverse:**  
  \[
  x_1 = y_1,\quad x_2 = y_2 - y_1^2.
  \]
>- **Jacobian:**  
  The Jacobian is
  \[
  J = \begin{pmatrix} 1 & 0 \\[0.5mm] -2y_1 & 1 \end{pmatrix} \quad \Longrightarrow \quad |J| = 1.
  \]
>- **Support:**  
  Since \( x_1\in[0,1] \) implies \( y_1\in[0,1] \), and \( x_2\in[0,1] \) gives  
  \[
  0\le y_2-y_1^2\le 1 \quad \Longrightarrow \quad y_2\in [y_1^2,\, y_1^2+1].
  \]
>- **PDF:**  
  \[
  f_Y(y_1,y_2)=
  \begin{cases}
  1, & \text{if } y_1\in[0,1] \text{ and } y_2\in [y_1^2,\, y_1^2+1],\\[1mm]
  0, & \text{otherwise.}
  \end{cases}
  \]

---

### Variation 14: Absolute Difference and Sum Transformation  
**Exercise:**  
Let \( X_1, X_2 \sim \text{Uniform}(0,1) \). Find the PDF of  
\[
Y = \Bigl(|X_1 - X_2|,\; X_1+X_2\Bigr).
\]

>**Solution:**  
This transformation has two branches. For the branch where \( X_1 \ge X_2 \):
>- **Inverse (Branch 1):**  
  \[
  x_1 = \frac{y_2+y_1}{2},\quad x_2 = \frac{y_2-y_1}{2}.
  \]
  The Jacobian is
  \[
  \left|\det \begin{pmatrix} 1/2 & 1/2 \\[1mm] -1/2 & 1/2 \end{pmatrix}\right| = \frac{1}{2}.
  \]
>For the branch \( X_2 > X_1 \), a similar computation yields the same absolute Jacobian. Summing the contributions from both branches gives an overall factor of 1.
>- **Support:**  
  The conditions \( x_1,x_2\in[0,1] \) imply
  \[
  y_1\in [0,1] \quad \text{and} \quad y_2\in [y_1,\, 2-y_1].
  \]
>- **PDF:**  
  \[
  f_Y(y_1,y_2)=
  \begin{cases}
  1, & \text{if } y_1\in[0,1] \text{ and } y_2\in [y_1,\, 2-y_1],\\[1mm]
  0, & \text{otherwise.}
  \end{cases}
  \]

---

### Variation 15: Mixed Transformation with Uniform and Exponential Variables  
**Exercise:**  
Let \( X_1 \sim \text{Uniform}(0,1) \) and \( X_2 \sim \text{Exp}(1) \) be independent. Find the PDF of  
\[
Y = \Bigl(e^{X_1}-1,\; 2X_2\Bigr).
\]

>**Solution:**  
>- **Inverse:**  
  \[
  x_1 = \ln(1+y_1),\quad x_2 = \frac{y_2}{2}.
  \]
>- **Jacobian:**  
  \[
  \frac{dx_1}{dy_1} = \frac{1}{1+y_1},\quad \frac{dx_2}{dy_2} = \frac{1}{2} \quad \Longrightarrow \quad |J| = \frac{1}{2(1+y_1)}.
  \]
>- **Support:**  
  Since \( x_1\in[0,1] \) we have  
  \[
  y_1\in \Bigl[ e^0-1,\, e^1-1 \Bigr] = [0, e-1],
  \]
  and \( x_2\ge 0 \) implies \( y_2\ge 0 \).
>- **Original PDF:**  
  \( f_{X_1}(x_1)=1 \) for \( x_1\in[0,1] \) and \( f_{X_2}(x_2)= e^{-x_2} \) for \( x_2\ge 0 \). Substituting \( x_2 = \frac{y_2}{2} \) yields  
  \[
  f_{X_2}\Bigl(\frac{y_2}{2}\Bigr)= e^{-y_2/2}.
  \]
>- **PDF:**  
  \[
  f_Y(y_1,y_2)= \frac{1}{2(1+y_1)}\, e^{-y_2/2},
  \]
  for \( y_1\in [0,e-1] \) and \( y_2\ge 0 \); zero otherwise.