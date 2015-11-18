# Logistic Regression

- Since linear regression isn't a very well algorithm for classification

# Hypothesis Representation

- Predict y =1 or y = 0

- g(h_theta) = classifier 
    
    - `0 < g(h_theta(x)) < 1`
    
    = g(theta' * x)
    
    = g(z) = 1/(1+e^(-z)) -> Sigmoid function | Logistic function

- g(h_theta) = estimate the probibility that y input on 1 

e.q:

    `h_theta(x) = 0.7 -> P(y=1 | x; theta)`
    the probability function is paramterized by theta,
    and put x into this function to predict `y=1`'s probability is 0.7

# Decision Boundary

if g(h_theta) > 0.5 
     -> predict  y = 1
else 
    -> predict y = 0


```
h_theta > 0 =>  y = 1 
h_theta < 0 =>  y = 0 
```

```
theta' * x > 0 =>  y = 1 
theta' * x < 0 =>  y = 0 
```

-> Assume `theta' * x =  theta_1 * x_1 + theta_0 * x_0

```
theta_1 * x_1 + theta_0 * x_0 > 0 => y = 1
theta_1 * x_1 + theta_0 * x_0 > 0 => y = 0
```

so `theta_1 * x_1 = theta_0` is the decision boundary.

(x_0 is 1)

# Cost Function



# Simplified Cost Function and Gradient Descent

