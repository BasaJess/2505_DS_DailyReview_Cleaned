# Day 27, 25.02.2025
<span style="color:grey">

</span>

---
## <span style="color:black"> __Basic Overview__ </span>
 

* <span style="color:grey"> Lecture logistic regression
* <span style="color:grey"> Time for exercise

---
##  <span style="color:black">__Schedule__
<span style="color:grey">

|Time|Content|
|---|---|
|09:00 - 10:00|Daily review|
|10:00 - 12:30|Lecture|
|12:30 - 13:30|Lunch Break| 
|13:30 - 16:00|Practical exercises|
|16:00 - 17:00|Stand-up|

---
## <span style="color:black"> __First Notes__ </span>
<span style="color:grey">
Logistic regression is a classification algorithm used for predicting the probability of a binary outcome (e.g., success/failure, yes/no, 1/0) based on one or more independent variables. While logistic regression is primarily used for binary categorical data (i.e., predicting outcomes that have two possible classes, like 0 or 1), the features used to train the model can be both categorical and numerical. This flexibility allows logistic regression to handle a wide range of problems.


</span>

---
## <span style="color:black"> Basics</span>

<span style="color:grey">

In logistic regression, the model calculates the probability of a data point belonging to the positive class (1) using the **sigmoid function**. The sigmoid function is a mathematical function that maps any real-valued number to a value between 0 and 1, which is interpreted as a probability.

​$$\hat{p}=\frac{1}{1+e^{z}}$$
 z is the linear combination of the input features and their corresponding coefficients: 
$$z= \beta_0 + \beta_1 \cdot x_1 + \beta_2 \cdot x_2 + ... +\beta_n \cdot x_n $$
The output of the sigmoid function $σ(z)$ is interpreted as the predicted probability that the target variable y equals 1 (i.e., the event occurs).

The predicted probability is compared to a **threshold** (typically 0.5) to classify the output as 0 or 1:
$$\begin{split} \begin{array}{c}{{\hat{p}\:=\:\sigma\bigl(b^{T}\,x\bigr)\:\ge\:0.5}}\\ {{b^{T}\:x\geq0}}\end{array}\end{split}$$

The cost function used in logistic regression is binary cross-entropy (also known as log loss). This function measures how well the predicted probabilities match the actual labels (0 or 1).

The **binary cross-entropy cost function** for a single data point is defined as:
$$Loss(\hat{p},y)= \underbrace{y\cdot\big(-\ln{(\hat{p})}\big)}_{\color{grey}{\text{“disabled” for }}y=0}+\underbrace{(1-y)\cdot\big(-\ln{(1-\hat{p})}\big)}_{\color{grey}{\text{“disabled” for }}y=1}$$

As y is always either 0 or 1, the formula can be summarized:
$$Loss(\hat{p},y) = -\big[y\ln{(\hat{p})} + (1-y)\ln{(1-\hat{p})}\big]$$ 

For all observations minimize the cost function by adjusting b:
$$J(b) = -\frac{1}{n}\sum_{i=1}^n[y_i\ln\left(\hat{p}_i\right)\ +\ (1-y_i)\ln\left(1-\hat{p}_i\right)\big]$$

This is typically done using **gradient descent**, an iterative optimization algorithm that updates the parameters in the direction of the steepest decrease in the cost function. By repeatedly updating the parameters, gradient descent minimizes the cost function, leading to better predictions.

But before starting, we get the partial derivatives because there is no closed-form analytical solution!
$$\frac{\partial}{\partial b_{j}}J(b)=\frac{1}{n}\sum_{i=1}^{n}\Bigl(\sigma\Bigl(b^{T}x_{i}\Bigr)-y_{i}\Bigr)x_{i,j}$$

At the end you get the shape of the decision boundary. 

**Why Different Cost Functions?**
The cost functions are different because logistic regression is dealing with a classification problem (predicting discrete classes) while linear regression is dealing with a regression problem (predicting continuous values).

Linear regression directly predicts a continuous value, so the cost function penalizes large errors with the squared difference between the true and predicted values (Mean Squared Error).

Logistic regression, on the other hand, predicts a probability (using the sigmoid function), and the cost function needs to measure how well the predicted probabilities align with the actual binary outcomes. The binary cross-entropy (log loss) cost function does this by penalizing incorrect confident predictions more severely and encourages probabilistic outputs close to the true labels.

---
## <span style="color:black"> Multiclass Classification </span>
* While logistic regression is typically used for binary classification, it can be extended to multiclass classification using techniques like one-vs-rest or softmax regression.
* In one-vs-rest (also known as one-vs-all), you train a separate binary classifier for each class, and for a given input, you select the class with the highest predicted probability.

---
## <span style="color:black"> What else? </span>

<span style="color:grey">

* Principles of assumptions, regularization and feature engineering are the same as we have already learned
* Class Imbalance: Logistic regression can struggle with imbalanced classes. In this case, techniques like resampling (either oversampling the minority class or undersampling the majority class) or adjusting the class weights can help improve performance.
* Cross-Validation: Always use cross-validation to assess the generalizability of the model. This will help ensure that your model is not overfitting to a particular training set.
</span> 

---