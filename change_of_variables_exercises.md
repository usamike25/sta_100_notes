### **Original Exercise & Solution**  
**Exercise 4 (6 points).**  
Let \( X_1 \) and \( X_2 \) be two random variables that are independent with a common uniform distribution on \([0,1]\).  
**Question:** What is the PDF of the random vector \( Y = \left(\frac{1 + X_1}{2}, X_2\right) \)?  

**Solution:**  
- **Transformation:** \( Y_1 = \frac{1 + X_1}{2}, Y_2 = X_2 \).  
- **Inverse:** \( X_1 = 2Y_1 - 1, X_2 = Y_2 \).  
- **Jacobian:**  
  \[
  |J| = \det \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} = 2.
  \]  
- **Support for \( Y \):**  
  \( \frac{1}{2} \leq Y_1 \leq 1 \) (from \( 0 \leq 2Y_1 - 1 \leq 1 \)) and \( 0 \leq Y_2 \leq 1 \).  
- **PDF:**  
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

**Solution:**  
- **Inverse:** \( X_1 = Y_1/2, X_2 = Y_2/3 \).  
- **Jacobian:** \( |J| = \det \begin{pmatrix} 1/2 & 0 \\ 0 & 1/3 \end{pmatrix} = \frac{1}{6} \).  
- **Support:** \( Y \in [0, 2] \times [0, 3] \).  
- **PDF:**  
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

**Solution:**  
- **Inverse:** \( X_1 = \frac{Y_1 + Y_2}{2}, X_2 = \frac{Y_1 - Y_2}{2} \).  
- **Jacobian:** \( |J| = \det \begin{pmatrix} 1/2 & 1/2 \\ 1/2 & -1/2 \end{pmatrix} = \frac{1}{2} \).  
- **Support:** Parallelogram bounded by \( y_1 + y_2 = 0, 2 \) and \( y_1 - y_2 = 0, 2 \).  
- **PDF:**  
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

**Solution:**  
- **Inverse:** \( X_1 = \sqrt{Y_1}, X_2 = Y_2 \).  
- **Jacobian:** \( |J| = \det \begin{pmatrix} \frac{1}{2\sqrt{y_1}} & 0 \\ 0 & 1 \end{pmatrix} = \frac{1}{2\sqrt{y_1}} \).  
- **Support:** \( Y \in [0, 1] \times [0, 1] \).  
- **PDF:**  
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

**Solution:**  
- **Inverse/Jacobian:** Identical to Original (but \( f_X(x_1, x_2) = e^{-(x_1 + x_2)} \)).  
- **Support:** \( Y_1 \geq \frac{1}{2}, Y_2 \geq 0 \).  
- **PDF:**  
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

**Solution:**  
- **Inverse:** \( X_1 = Y_1 Y_2, X_2 = Y_2 \).  
- **Jacobian:** \( |J| = \det \begin{pmatrix} y_2 & y_1 \\ 0 & 1 \end{pmatrix} = y_2 \).  
- **Support:** \( 0 \leq Y_2 \leq 1, 0 \leq Y_1 \leq \frac{1}{Y_2} \).  
- **PDF:**  
  \[
  f_Y(y_1, y_2) = 
  \begin{cases} 
  y_2 & \text{in the support}, \\
  0 & \text{otherwise.}
  \end{cases}
  \]  