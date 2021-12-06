**What and Why?**
The company is launching promotion programs to boost the sales of products that people would purchase during the visit to threatre.
The promotion has 2 parts 
1. send discount/coupon to customers who probably purchase a specific product -> this can improve the customer loytaly and attract people to go to the threatre.
2. send promotions to customers who is not likely to purchase the product so they will purchase something.


**How?**
The company tries to predicts whether customer will purcahse a specific product based on their user profile (demographc information), transactions histories that reveal what products and their visit information that reveals the movie they are watching.



**Frame the problem**

We are doing a binary classification problem that has target feature as Purcahse / No purchase to predict the customer behavior. 
The independet features / data are 1. user profile, 2. transaction history  and 3. ticket information

**Data Collection:**
1. User profile - customer survey
2. keep track of transaction. Without profile, we can use transaction per visit.   With profile, can track transaction histories of each customer
3. Ticket information - track via Box Office, or online ticketing system.

**Model Deployment:**
1. We can send the promotion on the fly - based on people's purchse, send them promotion at cashier.
This requires low latency because the real-time transaction is expected to be short for most people.

2. Send promotinos offline - analyze / make prediction and send promotions via offline method (email, mail)





