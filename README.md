# Tabular_Multiple-Dependent-Variables_Rossmann

#from fast.ai -> fastbook -> 09_tabular
#and  Practical-Deep-Learning-for-Coders-2.0 -> Tabular Notebooks -> 02_Regression_and_Permutation_Importance
#Kaggle's Rossmann competition for data
#Cleaned data source: fastai -> course-v3 -> nbs -> dl1 -> rossmann_data_clean.ipynb




The goal is to transform the Rossmann Data set to multiple dependent varibles. That will be one for each store's sales.

Mini-rossmann, only stores 1 and 3 were chosen because the entire csv is too large to upload to github.
  Also, keep things simple.
  
Why try multiple dependent variables? Because I haven't seen it done before.
  
Challenges:

1. Cannot get rmse and oob to work with multiple dependent variables.
m_rmse(m, xs, ys)

---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-30-1b4545f11396> in <module>
----> 1 m_rmse(m, xs, ys)

<ipython-input-29-51c1e6f73377> in m_rmse(m, xs, ys)
      1 def r_mse(pred,ys): return round(math.sqrt(((pred-ys)**2).mean()), 6)
----> 2 def m_rmse(m, xs, ys): return r_mse(m.predict(xs), ys)

<ipython-input-29-51c1e6f73377> in r_mse(pred, ys)
----> 1 def r_mse(pred,ys): return round(math.sqrt(((pred-ys)**2).mean()), 6)
      2 def m_rmse(m, xs, ys): return r_mse(m.predict(xs), ys)

~/anaconda3/lib/python3.7/site-packages/pandas/core/series.py in wrapper(self)
    110         if len(self) == 1:
    111             return converter(self.iloc[0])
--> 112         raise TypeError(f"cannot convert the series to {converter}")
    113 
    114     wrapper.__name__ = f"__{converter.__name__}__"

TypeError: cannot convert the series to <class 'float'>

