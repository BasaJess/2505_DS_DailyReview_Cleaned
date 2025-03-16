# Daily Review | Designing Data Products
<span style="color:grey">
Friday, 07.03.2025
</span>

---
## <span style="color:black"> __Basic Overview__ </span>
 

* <span style="color:grey"> Exploratory analysis - understand what happened in the past
* <span style="color:grey"> Predictive analyis - predict what will happen
* <span style="color:grey"> Predict what, for whom and for what purpose?

---
##  __Schedule__
<span style="color:grey">

|Time|Content|
|---|---|
|09:00 - 10:00|Daily Review|
|10:00 - 12:30|Working on Team Project|
|12:30 - 13:30|Lunch Break| 
|13:30 - 16:00|Working on Team Project|
|16:00 - 16:20|Stand-up|
|16:20 - 18:00|Working on Team Project|

## <span style="color:black"> __Product = Customer x Business x Technology__ </span>

<span style="color:grey">

* Usability
* Business viability
* Feasibility
  
Value = product of the three
  
</span>

## <span style="color:black"> Measuring Success </span>

* The first model should be the simplest model that could address the product needs.
* Business performance: measured usually by one KPI (key performance indicator)
* Model performance: an offline metric that captures how well the model will fit the business need


## <span style="color:black"> _Note: The business metric is independent from the model metric... It is a measure of the product success._ </span>

---
## <span style="color:black"> __Examples of Measuring Business Performance__ </span>

<span style="color:grey">

Business metrics:
* Click through rate (CTR) - for recommenders
* Usage - model that generates html from hand drawn diagrams
* Adoption by finance team - internal revenue forecasting

</span>

## <span style="color:black"> Measuring Success </span>

Regression:
* RMSE, RMSLE
* MAPE ( mean absolute percentage error) - accuracy as a ratio

Classification:
* Accuracy
* Precision
* Recall


<span style="color:grey">

---
## <span style="color:black"> __Business Performance vs. Model Performance__ </span>

<span style="color:grey">

![alt text](Business_vs_Model_Performance_4.png)

<span style="color:grey">

---
## <span style="color:black"> __Relationship Between Business Performance & Model Performance__ </span>

<span style="color:grey">

* Thinking of the business value of your model and the cost of being wrong can help you choose the right model metric.
* Always start from the value!
  
<span style="color:grey">

---
## <span style="color:black"> __Going Beyond Aggregated Metrics__ </span>

<span style="color:grey">

* Most model performance metrics we’ve seen are aggregated metrics
* They help determine whether a model has learned well from a dataset or needs improvement
* Next step: examine results and errors to understand why and how is the model failing or succeeding
* Validation and Iteration
* Note: Performance metrics can be deceptive, on highly imbalanced datasets a classifier can reach very high accuracy without any predictive power

<span style="color:grey">

---
## <span style="color:black"> __Types of supervised learning__ </span>

<span style="color:grey">

![alt text](img_p15.png)

<span style="color:grey">

---
## <span style="color:black"> Validate The Model | Inspect How It Is Performing </span>

<span style="color:grey">

* Regression: looking at residuals, for example doing EDA on residuals and inspecting the outliers
* Classification: one can start with a confusion matrix, breaking results in true class and predictions

<span style="color:grey">

---

## <span style="color:black"> __Confusion Matrix for Classification__ </span>

<span style="color:grey">

Counts how often the model predicted correctly and how often it got confused.
* False Positive: false alarm / type I error
* False Negative: missed detection / type II error

![alt text](Screenshot.png) 

<span style="color:grey">

---
## <span style="color:black"> __Residual Analysis for Regression__ </span>

<span style="color:grey">

* This is like EDA again but on residuals (predicted - observed)
* Plot residuals /and standardized residuals vs predicted
* We want our residuals to have no patterns, to be symmetrically distributed, centered in the middle of the plot

![alt text](img_p18_1.png) 

* IF NOT.. then there is room for improvement in the model.

![alt text](img_p18_2.png) 

<span style="color:grey">

---
## <span style="color:black"> __Objectives & Key Results__ </span>

<span style="color:grey">

* OKRs drive strategic change, innovation, or significant improvement.
* Use OKRs to measure and maintain performance over time.
* Main performance evaluation tools at tech companies  
* OKRs (Objectives and Key Results) are a goal-setting framework used to align teams and individuals with business objectives. They focus on setting ambitious, outcome-driven goals and measuring success through specific key results.
* Objective (O) – A clear, inspiring, and time-bound goal.
* Key Results (KRs) – Measurable outcomes that indicate progress toward the objective.

---
<span style="color:grey">

## <span style="color:black"> __Characteristics of OKRs:__ </span>

<span style="color:grey">

* Ambitious – OKRs encourage stretch goals beyond just maintaining performance.
* Time-Bound – Typically reviewed quarterly or annually.
* Transparent – Shared across the organization for alignment.
* Outcome-Oriented – Focuses on results, not just effort.
* Challenging - Success rate should be around 67%

---
## <span style="color:black"> __Example of an OKR for a Data Scientist:__ </span>

<span style="color:grey"> 

* Objective A: Improve the efficiency and accuracy of the fraud detection model
    * KR1: Increase model precision from 85% to 90% within six months.
    * KR2: Reduce false positives by 20% to avoid unnecessary account blocks.
    * KR3: Automate real-time fraud alerts, reducing response time from 10 minutes to 4 minutes. 

* Objective B: Improve the ...
    * KR1: Increase ...
    * KR2: Reduce ...
    * KR3: Enhance ...
![alt text](OKR.png) 

<span style="color:grey">

---
---
## Helpful References

- [OKRs: the ultimate guide to objectives and key results](https://www.atlassian.com/agile/agile-at-scale/okr)
- [OKR Examples for Data Science](https://okrstudio.com/okr-examples/data-science)






