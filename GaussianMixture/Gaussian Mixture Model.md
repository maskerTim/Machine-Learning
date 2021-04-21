# Gaussian Mixture Model
###### tags: `Machine Learning` `GMM`

## Key Component :key: 
* A Gaussian mixture model is a weighted sum of Gaussian densities:
![Gaussian mixture model](https://i.imgur.com/5VjMIkX.png)
* Assume data are generated as follow:
    * Pick generator function g_j randomly with a probability P(g_j chosen) = alpha_j.
    * Multidimensional Gaussian data point is generated from g_j.
* Parameter Estimation (How to estimate Gaussain parameters from data points?): Expectation-Maximization (EM)
    * Expectation step: Assume that Gaussian parameters are known, want to estimate alpha_j
    * Maximization step: Given alpha_j, update Gaussain parameters
* EM Example:
    1. Assume we use three (univariate) Gaussian as mixture model:
![EM_1](https://i.imgur.com/H1Gd4WJ.png)
Suppose we have n observation x_i, i=1,2,...,n
Use maximum likelihood (ML) estimation to find:
![EM_2](https://i.imgur.com/yguBgDy.png)
Let likelihood function be:
![EM_3](https://i.imgur.com/N6OLpAR.png)
    2. EM algorithm--M Step
    To find optimal value for \theta, we use derivatives:
    ![EM_4](https://i.imgur.com/33dDuTi.png)
    With some computations, we have (M step):
    ![EM_5](https://i.imgur.com/RBEMKp6.png)
    3. EM algorithm--E step
    We also need to estimate \alpha_j by letting (E step):
    ![EM_6](https://i.imgur.com/ALWex1d.png)
    However, we have one constraint:
    ![EM_7](https://i.imgur.com/LyQYTwA.png)
    This can be solved with **Lagrange multipiliers**
    Solving it, we have:
    ![EM_8](https://i.imgur.com/YBEMtJu.png)


## Question :question: 
#### Question 1: EM algorithm--numerical example
* The following one-dimensional data points are known from two clusters:[0.9, 0.7, 1.2, 2.4, 1.8].
* Suppose that the initial conditions are:
![Q_1](https://i.imgur.com/aBaTkE8.png)
* Update the parameters by completing the E and M steps in one epoch.


## Solution :mag_right: 
* Recall the general form of univariate Guassian:
![S_1](https://i.imgur.com/32M59c9.png)
* In our case,
![S_2](https://i.imgur.com/bZvfjwv.png)
```
g1: [0.398, 0.390, 0.395, 0.244, 0.340]
g2: [0.295, 0.261, 0.340, 0.383, 0.395]
```
* To compute: \alpha_1=\alpha_2=0.5
![S_3](https://i.imgur.com/jhuCHFH.png)
Therefore,
![S_4](https://i.imgur.com/Hehf2PE.png)
* With the given g_1(x) and g_2(x), we have:
```
beta 1: [0.574, 0.599, 0.537, 0.389, 0.463]
beta 2: [0.426, 0.401, 0.463, 0.611, 0.537]
```
* M-Step: update parameter
![M-Step](https://i.imgur.com/b3RQLEl.png)
```
new mu1, new sigma1: 1.3065753725700628 0.3510142879511143
new mu2, new sigma2: 1.4982149218892322 0.408060269961259
```
* E-Step: updata probability
![E-Step](https://i.imgur.com/E9t8AMg.png)
```
new alpha 1: 0.5124981885949778
new alpha 2: 0.48750181140502213
```







