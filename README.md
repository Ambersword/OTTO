# OTTO

Goal of the Competition
The goal of this competition is to predict e-commerce clicks, cart additions, and orders. You'll build a multi-objective recommender system based on previous events in a user session.

Your work will help improve the shopping experience for everyone involved. Customers will receive more tailored recommendations while online retailers may increase their sales.

Submissions are evaluated on Recall@20 for each action type, and the three recall values are weight-averaged:

𝑠𝑐𝑜𝑟𝑒=0.10⋅𝑅𝑐𝑙𝑖𝑐𝑘𝑠+0.30⋅𝑅𝑐𝑎𝑟𝑡𝑠+0.60⋅𝑅𝑜𝑟𝑑𝑒𝑟𝑠
where 𝑅
 is defined as

𝑅𝑡𝑦𝑝𝑒=∑𝑁𝑖|{predicted aids}𝑖,𝑡𝑦𝑝𝑒∩{ground truth aids}𝑖,𝑡𝑦𝑝𝑒|∑𝑁𝑖min(20,|{ground truth aids}𝑖,𝑡𝑦𝑝𝑒|)
and 𝑁
 is the total number of sessions in the test set, and predicted aids
 are the predictions for each session-type (e.g., each row in the submission file) truncated after the first 20 predictions.

For each session in the test data, your task it to predict the aid values for each type that occur after the last timestamp ts the test session. In other words, the test data contains sessions truncated by timestamp, and you are to predict what occurs after the point of truncation.

For clicks there is only a single ground truth value for each session, which is the next aid clicked during the session (although you can still predict up to 20 aid values). The ground truth for carts and orders contains all aid values that were added to a cart and ordered respectively during the session.
