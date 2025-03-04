# **Multiple Linear Regression using Gradient Descent**

This project implements **Multiple Linear Regression using Gradient Descent** in **pure Python** (without external libraries like NumPy or Scikit-learn).  
The goal is to train a model that predicts an output variable based on multiple input features.

---

## **1. Understanding Multiple Linear Regression**
Multiple Linear Regression models the relationship between a **dependent variable** $y$ and multiple **independent variables** $X_1, X_2, \dots, X_n$ using the equation:

$$
y = b_0 + b_1X_1 + b_2X_2 + \dots + b_nX_n
$$

where:

- $b_0$ is the **intercept** (bias term).
- $b_1, b_2, \dots, b_n$ are the **coefficients** (weights) for each independent variable.

The goal is to determine the best values for $b_0, b_1, \dots, b_n$ that **minimize the prediction error**.

---

## **2. Cost Function (Mean Squared Error)**
To measure how well the model fits the data, we use the **Mean Squared Error (MSE)**:

$$
MSE = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2
$$

where:

- $y_i$ is the **actual value**.
- $\hat{y}_i = b_0 + b_1 X_{i1} + b_2 X_{i2} + \dots + b_n X_{in}$ is the **predicted value**.
- $n$ is the **total number of data points**.

Our goal is to **minimize this error**.

---

## **3. Gradient Descent Optimization**
Since **MSE** depends on $b_0, b_1, \dots, b_n$, we use **Gradient Descent** to update them iteratively.

### **Computing Gradients**
To minimize **MSE**, we compute the **partial derivatives** of the cost function with respect to each coefficient:

$$
\frac{\partial MSE}{\partial b_j} = -\frac{2}{n} \sum_{i=1}^{n} X_{ij} (y_i - \hat{y}_i)
$$

for each $j = 0, 1, 2, \dots, n$.

- When $j = 0$, we set $X_{ij} = 1$ (for the **bias term**).
- These gradients tell us **how to adjust the coefficients** to reduce the error.

### **Updating Coefficients**
Using the gradients, we update the coefficients iteratively:

$$
b_j = b_j - \alpha \frac{\partial MSE}{\partial b_j}
$$

where:

- $\alpha$ (**learning rate**) controls how big the steps are in each update.

This process repeats **until the model converges** (or for a fixed number of iterations).

---

## **📌 Summary**
✅ **Multiple Linear Regression** extends simple linear regression to multiple features.  
✅ We minimize **Mean Squared Error (MSE)** to find the best coefficients.  
✅ **Gradient Descent** iteratively updates the coefficients until convergence.  
✅ The **learning rate** $\alpha$ determines how fast the model learns.  

🚀 **Happy Coding!**
