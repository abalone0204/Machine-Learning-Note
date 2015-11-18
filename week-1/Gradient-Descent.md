#Gradient Descent

# prerequisite

- already not abt Cost function and hypothesis function

```
#recap
## 1. Hypothesis function
h (theta) = theta * x
## 2. Cost function
Cost =J(theta)= (1/2*m)* sum ((h(theta)- y)^2)
```

# Goal 

- Find the `theta` which can minimize the `J(theta)`

# Implement

alpha = learning rate

```
do until (find min of J(theta)){
    theta_i = theat_i - alpha* d/d(theta) (J(theta))
}
```

Update theta simultaneously,
it will automatically move more smoothly while getting closer to the lowest point.
=> we don't need to decrease the learning rate while is closer to local solution, just keep it the same.


- this is called a "Batch Gradient Descent", it means we take every elements in dataset in each step.