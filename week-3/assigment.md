# `costFunction.m`

I think the most confusing part is : what is `gradient`

Seems the naming is kinda ambiguous.

But it's actually quite simple,

`gradient` means the theta after the gradient descent.

e.q: 
    the Θ is an n-vector, so we set
    from gradient(1)~ gradient(n)

Note that while this gradient looks identical to the linear regression gra- dient, the formula is actually different because linear and logistic regression have different definitions of hθ(x).

# `fminunc`

set the GradObj option to on
=> tells fminunc that our function returns both the cost and the gradient

Don't have to do anything, codes provided in the `ex2.m`.

Just read it XD

# `predict.m`

- return θ >= 0.5 => since the boolean is 0 or 1 in Octave

# Regularized logistic regression

- First, plot the data

- Found that we cant easily sperate it to two parts by a straight line

#Feature mapping

- One way to fit the data better is to create more features from each data point