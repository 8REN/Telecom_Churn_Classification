# Telecom Service Termination 


  
  ## Binary Classification on Churn Dataset
  
  
 Author: Brennan Mathis
 
 The contents of this repository contains an analysis of telecommunications 
 data regarding phone usage and customer retention.
 
data includes the following info:
       'state', 'account length', 'area code', 'phone number',
       'international plan', 'voice mail plan', 'number vmail messages',
       'total day minutes', 'total day calls', 'total day charge',
       'total eve minutes', 'total eve calls', 'total eve charge',
       'total night minutes', 'total night calls', 'total night charge',
       'total intl minutes', 'total intl calls', 'total intl charge',
       'customer service calls', 'churn'. (telecomchurndataset.csv)
 
 ### Problem:
 
What features are involved in customer retention?
Can customer churn be predicted with data provided?
Are false positives preferred to false negatives?
 
### Libraries
from geopy.distance import geodesic
from geopy import Point
import numpy as np 
import pandas as pd 
import seaborn as sns 
import matplotlib.pyplot as plt
import scipy.stats as stats
import statsmodels.api as sm
import statsmodels.formula.api as smf
import statsmodels.stats.api as sms
from statsmodels.formula.api import ols
from statsmodels.stats import diagnostic
from sklearn.feature_selection import RFE
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error
from sklearn.model_selection import cross_val_score
from sklearn import svm
from sklearn.model_selection import train_test_split
from sklearn.metrics import r2_score
from sklearn.model_selection import KFold

## perform gridsearch of multiple algorithms to find
## best fit for the job

columns not factored into assessment include: 
'area code', 
'number vmail messages', 
'total day minutes',
'total eve minutes',
'total night minutes',
'total intl minutes',
this is due to high correlation with other features, or irrelevance to assessment


 ![corrheatmap](https://github.com/br3nnan8/mod3_classificationproject/blob/master/visualizations/corrheatmap.png)

 ![age/pricescatter](https://github.com/br3nnan8/mod2_kc_housing_regression/blob/master/visualizations/kc_ageprice_scatter.png)
 
 ![violinplot1](https://github.com/br3nnan8/mod2_kc_housing_regression/blob/master/visualizations/kc_bedvsprice_violin.png)
 
 ![violinplot2](https://github.com/br3nnan8/mod2_kc_housing_regression/blob/master/visualizations/kc_gradevsprice_violin.png)
 
 ![lot/pricekde](https://github.com/br3nnan8/mod2_kc_housing_regression/blob/master/visualizations/kc_lotsizeprice_kde.png)
 
![lot/pricekde](https://github.com/br3nnan8/mod2_kc_housing_regression/blob/master/visualizations/kc_renovatedvsnonrenovated_kde.png)
 
 To expand on this project, I would like to assess scaling the continuous data and providing more weight to certain variables in the model. Additional regressions with polynomials as well.
 
 
