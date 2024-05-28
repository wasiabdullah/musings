## Maths in markdown

## Simple Linear regression ( with one feature )
$y_{pred} = h_o(x) = \theta_0 + \theta_1*x_1 $  where $\theta $ present weight assocaited with each parameter $x$ ,$\theta_0 $ being bias term.

### The error/loss function uses 
$$ J(\theta) = \frac {\sum\limits_{x=0}^{n} {{(y_{pred} - y})^2}} {n} $$

$$\frac{\partial }{\partial t}$$

### Gradient descent update rule - ( to minimize loss function )

$$\frac{\partial j(\theta)}{\partial \theta_0} = $$

$$ \theta_0 = \theta_0 - { \eta \sum\limits_{i=1}^{m}{(y_{actual} - y_{predicted})^2}}$$

$$ \theta_1 = \theta_1 - { \eta \sum\limits_{i=1}^{m}{(y_{actual} - y_{predicted})^2}}x_1$$
for a particular theta j , where $\eta $ is learing parameter , m the number of observations

## Linear Regression with multiple features

$$y_{pred} = h_0(x) = \theta_0 + \theta_1X_1 + ..... + \theta_nX_N$$ 
where $\theta $ present weight assocaited with each parameter $X$ , $\theta_0 $ being bias term , n the number of parameters. Above can be written as   
$$y_{pred} = h_0(x) = \theta_0X_0 + \theta_1X_1 + ..... + \theta_nX_N$$
where 
$$X_0 = 1$$ 

### The error/loss function uses 
$$ J(\theta) = \frac {\sum\limits_{x=0}^{n} {{(y_{pred} - y})^2}} {n} $$

### Gradient descent update rule - ( to minimize loss function )

$$ \theta = \theta - {\eta \nabla J(\theta) }$$
on differentiation

$$ \theta_j = \theta_j - { \eta \sum\limits_{i=1}^{m}{(y_{actual} - y_{predicted})^2}}X_j$$
for a particular theta j , where $\eta $ is learing parameter , m the number of observations
 

### R squared square

It is also called as coefficient of determination. It tell us what percentage of variability in dependent variable is contributed by the independent variables
 $$R^2 = 1 - \frac{SS_{res}}{SS_{total}}$$
 
 where $$SS_{res} = \sum\limits_{i=1}^{m}{(y_{actual} - {y_{predicted}})^2} $$ is the residual sum of squares
 and  where $$SS_{total} = \sum\limits_{i=1}^{m}{(y_{actual} - {y_{mean}})^2} $$ is the total sum of squares 
, m is the number of observations 




### Adjusted R squared square

$$ R^2_{adjusted} = 1 - {\frac {(1 - R^2)(n-1)}{(n-k-1)}}$$
where $ R^2$ is R squared score n is the number of observations and k is the number of parameters   

---------

On the other side, we are not sure about the mean temperature and we want to infer it from the data. For doing that we can follow a *maximum likelihood* approach,

$$ \mu_{t} = \arg\max_\mu \ln p(s_1,\ldots,s_n|\mu) = \arg\max_\mu \prod_i \int_{t_i} p(s_i|t_i)p(t_i|\mu) dt_i $$
where $s_i$ denotes the sensor readings, $t_i$ is the real temperature at time $i$. 

However, with PPLs, we do not have to care about the underlying inference problem. We just define the model and let the PPL's engine make the work for us. So the model is defined as follows, using Pyro's parameters (defined as ``pyro.param``), which are free variables we can optimize.   

--------
