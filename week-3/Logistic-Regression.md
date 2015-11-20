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

Now we take new hypothesis function to `g(theta' * x)`

```
h_theta = g(theta' *x)

```

Just a quick recap:

Cost function in linear regression is :

`J(theta) = 1/(2 *m) * sum((h_theta(x) - y)^2) `

and we extract out the h_theta part 

-> `Cost (h_theta(x), y) = 1/2(h_theta(x)-y)^2`

and since the `Cost` is too complex (it has 1/1+e^-z),

so it will make the `J(theta)` non-convex.

We must get `J(theta)` convex to find the global minimum.

## Logistic regression cost function

`Cost (h_theta(x), y)`

```
=> { 
    -log(h_theta) if y = 1,
    -log(1-h_theta) if y = 0
    }
```

> Why log? 
> Thinking in the log(z) and log(1-z) which z is a real number.


# Simplified Cost Function and Gradient Descent

So now we got a cost function:

```
J(theta) =  (1/m)*(sum(Cost(h_theta(x) - y)))
```

and `Cost (h_theta(x), y)` =>

```
{ 
  -log(h_theta(x)) if y = 1,
  -log(1-h_theta) if y = 0
}
```

Simplify => `-y*log(h_theta)+ -(1-y)*(1-h_theta)`

```
J(theta) = (1/m)*sum((-y*log(h_theta)+ -(1-y)*(1-h_theta)))
```

Then how to min(J(theta))

Gradient Descent !
(it's very similar to the way we do in linear regression)


#Advanced Optimization

- Conjugate gradient

- BFGS

- L-BFGS

=> Advantages: fast, don't need to find alpha 

Disadvatanges: more complex


We don't need to know too much, 
just use the `fminunc` offered by Octave

```matlab
options = optimset('GradObj', 'on', 'MaxIter', '100');
initialTheta = zeros(2,1);
[optTheta, functionVal, exitFlag] ...
    = fminunc(@costFunction, initialTheta, options)
```
# Multiclass Classification: One-vs-all

set y = 1, 2, 3, 4

gotta have h_1, h_2, h_3, h_4

max h_i(x)