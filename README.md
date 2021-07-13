# News Recommendation  
The project is to predict 5 articles for each user according to the user click history and user features. Analyzed on user-news interaction data from a news App released by Alibaba Cloud TIANCHI Competition and built an algorithm in Python to predict five articles with ranking a user would click.   

The project includes parts:  
1. Recall article candidates from item-based cf  
2. Extracting user features for feature engineering  
3. Build, train and test model  

# 1. Recall article candidates from item-based cf
(1) Getting item-based recommendation according to content similarity, item created time, user click time and topk items.   

# 2. Extracting user features
(1) Getting user activity according to the number of clicks and time difference between consecutive clicks, user device feature, user time preferrence feature, category perferrence feature as new features.   

# 3. Build, train and test model  
(1) Prepare train, validate and test dataset. Label the articles and produce neg samples.   
(2) Get article candidates from item-based recommendation.  
(3) Adding user features as new features.   
(4) Train and test data on LightGBM  ranking and LightGBM  classfier models with 200,000 training and 50,000 test datasets, tuned hyper parameters, trained Logistic Regression Model on two models to predict five articles with ranking.  

# Results
Mean Reciprocal Rank was 0.2341 (Top1 is 0.3073). The reciprocal rank was 1/n if actual clicked article was at rank n among five articles.  
