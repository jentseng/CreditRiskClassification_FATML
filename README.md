# Accountable AI for Credit Default Risk Modeling
### Authors: Catherine Miao, Karan Palsani, Michael Sparkman, Jenny Tseng, Tony (Junhong) Xu
### FATML project focused on fairness and explainability of credit default risk modeling

This repository contains our work in building fair and explainable models that predict credit default risks. The original dataset was obtained from Kaggle's [Home Credit Default Risk competition](https://www.kaggle.com/c/home-credit-default-risk/overview). For the purpose of running the code, all csv's generated for modeling were stored in a folder named cleaned_tables. CSV's generated for exploratory data analysis (EDA) were stored in a folder named EDA-helpers.

The Jupyter notebooks are numbered in the sequence we approached the problem and described below:

0. EDA of the main table containing applicant info; e.g., detecting outliers, treating null values
1. EDA of five supplemental tables that contain additional information for some of the applicants; e.g., summarizing key information for an applicant
2. Preparing datasets for modeling; e.g., checking bias of the three protected attributes in the dataset (age, gender, marital status), merging all tables, setting up training and testing sets, preparing a SMOTED dataset
3. Building a BRCG and a GLRM models (both in IBM's AIX 360 toolkit) based on the SMOTED top 20 features found from a Random Forest (RF) model
4. Building a RF and an XGBoosting models based on the SMOTED top 20 features found from the RF model found from #3 above; explaining the models with SHAP
5. Building various Decision Tree, Logistic Regression, and Random Forest models to compare with the models built in #3 and #4.

For more detailed descsription of the project, see [here](https://medium.com/@tonyxu_71807/ensuring-fairness-and-explainability-in-credit-default-risk-modeling-shap-ibm-tool-kit-aix-360-bfc519c191bf?).
