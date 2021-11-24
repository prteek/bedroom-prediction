# bedroom-prediction
Modelling for number of bedroom predictions on data from Homesearch


### Limitations:
1. Not much analysis of individual variables relationship with target variable. This could highlight some clear non linearities and open the opportunities to use Linear models with spline transformations, or heirarchical modelling on some categorical variables
2. Do not treat high value (more bedroom) houses specially but some weighting based on floor area of postcode could help practically
3. Perhaps a better metric could be chosen as compared to accuracy. Better for multiclass classification like Cohen's Kappa or Matthew's coeff or something that takes into account class imbalance if needed 
4. At the moment all features have been considered but Recursive feature elimination can help reduce noise from the model, there are several correlated features some of which are possibly redundant
5. Did not handle null values gracefully
6. Computationally expensive option (GB) has been chosen


### Future work:
1. Explore random forests in a little more detail since they fit the training data better even on high regularisation so they may be on to some pattern perhaps but they do not handle missing values
2. Use Feature importance and try to link it with subject matter understanding
3. Understand misclassified predictions and see if new features could be engineered or if any issues start popping up i.e. for a particular postcode or particular house type we're under estimating more than others
4. Use subject matter expertise since the nature of problem is more human driven than physics driven. Use heirarchical models and encode some priors around particular house type or postcode. Also have an estimate of uncertainity around predictions to chose a tradeoff of underprediction or over prediction
5. Take a look at literature 
