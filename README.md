# Analyze-A-B-Test-Results

This project will assure you have mastered the subjects covered in the statistics lessons. The hope is to have this project be as comprehensive of these topics as possible. 

To get the source go to file Analyze_ab_test_results_notebook.html or use Jupyter Notebook (Analyze_ab_test_results_notebook.ipynb)

## Table of Contents
- [Introduction](#intro)
- [Part I - Probability](#probability)
- [Part II - A/B Test](#ab_test)
- [Part III - Regression](#regression)

<a id='intro'></a>
### Introduction

A/B tests are very commonly performed by data analysts and data scientists.  It is important that you get some practice working with the difficulties of these 

For this project, you will be working to understand the results of an A/B test run by an e-commerce website.  The goal is to work through this notebook to help the company understand if they should implement the new page, keep the old page, or perhaps run the experiment longer to make their decision.

<a id='probability'></a>
#### Conclutions of Part I - Probability

As you can see in the table below, the probability to convert in Control group (0.1204) is slightly higher than Treatment group (0.1188). In addition, the probability to an individual be part of a group Control and Treatment is almost 50%. Therefore, there is no enough evidence to afirm that new treatment page leads to more conversions and more study neets to be done to determine if really new treatment page leads to more conversions. 

| Group |Probability | Conversion | Probability |
| --- | --- | --- | --- |
| Control | **0.4999** |Converted | **0.1204** |
| --- | --- | No Converted | 0.8712 |
| Treatment | **0.5001** | Converted | **0.1188** |
| --- | --- | No Converted | 0.8812 |

<a id='ab_test'></a>
#### Conclutions of Part II - A/B Test

In scientific studies, the $P_{value}$ is the level of marginal significance and represent the probability of observing and statistics.  Considering a **P_value = 0.9026** and **alpha = 0.05**. In this analysis we obtain a P_value greater than **alpha**, so we fail to reject H_0 and there isn't a significant difference betweeen the convertion proportion of new pages in relation with old pages.  


<a id='regression'></a>
#### Conclutions of Part III - Regression

Now, you are considering other things that might influence whether or not an individual converts.  Discuss why it is a good idea to consider other factors to add into your regression model.  Are there any disadvantages to adding additional terms into your regression model?

- Could be a good idea to use timestamp column, could be interesting if exist a correlation of the time with make a conversion. Also the time spendend in the page before make a convertion or maybe CTR (Click Though rate). 
- Is good idea to consider other factors to the regression model because we could find out other explanatory variables that influence a convertion. 
- One disadvantage to add new factor to the regression model is multicollinearity problem. This occur when is present two explanatory variables that are strong are related, but we could delete this variables if can't pass the Variance Inflation Factor (VIIF). 
- There are another problems that can affect the model as: correlation of errors, non constant variables of erros and outliers. 
