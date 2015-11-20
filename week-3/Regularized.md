#Regularization

to many features
=> overfitting

=> Regularization will make it less prone to overfitting

but how to?

by add a new regularization parameter at the end

`J(θ) = 1/(2*m)*Σ ((h_θ(χ) - Υ)^2 + λ* Σ (Θ_j)^2)`
regularize only θ1~n, excluding θ_0

#Regularized Linear Regression

min `J(θ) = 1/(2*m)*Σ(h_θ(χ) - Υ)^2 + λ* Σ (Θ_j)^2`

#Regularized Logistic Regression

- extract the θ_0's gradient when we're working on regularized linear regression4

- So the gradient descent update of θ0 is still the same

- but the other has to add `(λ/m)* θ_i`  (i=1:n)