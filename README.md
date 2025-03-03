# Simple-Linear-Regression-with-GradientDescent
This project implements the Simple Linear Regression algorithm with Gradient descent, using Purely Python Programming Language

## **1. Understanding Linear Regression**
Linear regression models the relationship between an **independent variable** \( X \) and a **dependent variable** \( y \) using a straight-line equation:

\[
y = mX + b
\]

where:
- \( m \) (**slope**) represents the rate of change of \( y \) with respect to \( X \).
- \( b \) (**intercept**) represents the value of \( y \) when \( X = 0 \).

The goal of training is to find the best values for \( m \) and \( b \) such that the predicted values \( \hat{y} \) are as close as possible to the actual \( y \).

---

## **2. The Cost Function (Mean Squared Error)**
To measure the error between predictions and actual values, we use the **Mean Squared Error (MSE)**:

\[
MSE = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2
\]

where:
- \( y_i \) is the actual value.
- \( \hat{y}_i = mX_i + b \) is the predicted value.
- \( n \) is the number of data points.

Our goal is to **minimize this error**.

---

## **3. Gradient Descent Optimization**
Since **MSE** is a function of \( m \) and \( b \), we use **gradient descent** to update them iteratively.

### **Computing Gradients**
We calculate the **partial derivatives** of the MSE with respect to \( m \) and \( b \):

\[
\frac{\partial MSE}{\partial m} = -\frac{2}{n} \sum X_i (y_i - \hat{y}_i)
\]

\[
\frac{\partial MSE}{\partial b} = -\frac{2}{n} \sum (y_i - \hat{y}_i)
\]

These gradients tell us the **direction** in which we should adjust \( m \) and \( b \) to **reduce the error**.

### **Updating Parameters**
Using the gradients, we update \( m \) and \( b \) iteratively:

\[
m = m - \alpha \frac{\partial MSE}{\partial m}
\]

\[
b = b - \alpha \frac{\partial MSE}{\partial b}
\]

where:
- \( \alpha \) (**learning rate**) controls how big the steps are in each update.
- This process repeats for a given number of **iterations**.

---

### **📌 Summary**
- We use **Gradient Descent** to iteratively adjust \( m \) and \( b \).
- The **Mean Squared Error (MSE)** helps measure how well the model fits.
- The **learning rate** \( \alpha \) determines how fast the model learns.
- The algorithm continues **until convergence** (or for a fixed number of iterations).
