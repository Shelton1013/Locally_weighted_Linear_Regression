# Notebook

Code from Stanford cs229

# Locally_weighted_Linear_Regression

when using linear regression, naively,it might seem that the more features we add, the better. The choice of features is important to ensuring good performance of a learning algorithm.
(When we talk about model selection, we’ll also see algorithms for automatically choosing a good set of features.) 

The locally weighted linear regression (LWR) algorithm which, assuming there is sufficient training data, makes the choice of features less critical.

The algotithm:
1. Fit $\theta$ to minmize $$\sum_{i}^{m}w^{i}(y^{i}-\theta^{T}x^{i})^2$$
2. Output y_predict $(\theta^{T}x)$

A choice for the weights is 
$$w^{i} = exp(-\frac{(x^{i}-x)^2}{2\tau^{2}})$$
where,
- $x$ is the input for which you want to make a prediction.
- $x^{i}$ is the $i$ th training example


## Bandwidth Parameter
$\tau$ has an effect on overfitting and underfitting:

if $\tau$ is too broad, you end up over-smoothing the data leading to underfitting.

if $\tau$ is too thin, you end up fitting a very jagged fit to the data leading to overfitting.


## Conclusion
- Locally weighted linear regression is a supervised learning algorithm.
- It is a non-parametric algorithm.
- There exists No training phase. All the work is done during the testing phase/while making predictions.
- The dataset must always be available for predictions.
- Locally weighted regression methods are a generalization of k-Nearest Neighbour.
- In Locally weighted regression an explicit local approximation is constructed from the target function for each query instance.
- The local approximation is based on the target function of the form like constant, linear, or quadratic functions localized kernel functions.
  
