# OTTO--recommendation system

Introdction:

Goal of the Competition
The goal of this competition is to predict e-commerce clicks, cart additions, and orders. I build a multi-objective recommender system based on previous events in a user session.

My work will help improve the shopping experience for everyone involved. Customers will receive more tailored recommendations while online retailers may increase their sales.

In this model, I considered and compared different models such as XGboost, Recall system, Item collabration. 
Every session includes clicks, carts, orders, and time stampes. 
Actually, from data cleaning step , we shall consider on transform time into normal time stamps as 2018-07-10
Current trend for recommendating predition , many scientist like to use Xgboost, However, Xgboost also has some shortcomes that we need to reduce these errors to enhance accuracy. 

Explaination:

Collaborated with a team of 3 to predict e-commerce clicks, cart additions, and orders based on 2 billion+
train data and 6 million test data from OTTO, the largest Germany online shop
Iteratively enhanced model performance: issue discovery, quantifying the issue, creating a solution
Evaluated different multi-model combinations to find high prediction accuracy as an Ensemble
model,XGboost, LGBM, Catboost, Recall, Rerank, adjusted exponential weights, biases, and optimized
fits,achieving a score of 0.577 using the ensemble model

