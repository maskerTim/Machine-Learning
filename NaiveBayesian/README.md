# Naive Bayesian Classifier
[![hackmd-github-sync-badge](https://hackmd.io/cC5XJhIOQy-2_upQMaw06Q/badge)](https://hackmd.io/cC5XJhIOQy-2_upQMaw06Q)
###### tags: `Machine Learning` `Naive Bayesian`

## Key Component :key: 
* Naive Bayesian classifier assumes that all attributes (also called features) in x are independent random variable (RV).
* Posteriori probability:
![Posteriori Probability](https://i.imgur.com/6bpwQBC.png)
P( C ) is prior probability of C, C is the class
P(x) is prior probability of x, the features
P(x|C) is posteriori probability, the probability of x given C
P(C|x) is posteriori probability, the probability of C given x


## Question :question: 
### Question 1 :question:
![Question 1](https://i.imgur.com/RIzHdSK.jpg)
![Question 1-1](https://i.imgur.com/9EuFQOl.png)

We want to know about the probability of P(C|red, circle).


## Solution :mag_right: 
In short, we need to know P(+|red,circle) and P(-|red,circle).
#### Solution 1 :mag_right: 
##### Components we require
![Probability we need](https://i.imgur.com/ms65cLx.png)

##### Calculate P(+|red,circle)
![P(+|red,circle)](https://i.imgur.com/35fgCip.png)
![Cal of P(+|red,circle)](https://i.imgur.com/N9sWCTB.png)

##### Calculate P(-|red,circle)
![P(-|red,circle)](https://i.imgur.com/VZA1xlt.png)
![Cal of P(-|red,circle)](https://i.imgur.com/ppuoc0S.png)

##### Comparison of P(+|red,circle) and P(-|red,circle)
![Comparison](https://i.imgur.com/k3a5cZl.png)
The final answer is P(+|red,circle).


