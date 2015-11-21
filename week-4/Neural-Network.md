The model representation might be more high level.
You can check the `Application` part to see a concrete example
about how Neural network can be applied to ml.

# Model Representation I

## Neuron in the brain

- Nucleus 

- Dendrite(input wires)

- Axon (output wire)

## Neuron model: Logistic unit

`x1, x2, x3 -> O -> hΘ(x)`

(Sometimes we can add x0, it's called "bias unit". And x0 is always equal to 1.)

`hΘ(x) = 1/(1+e^(-Θ'X))`

Sigmoid(logistic) activation function

### Neural Network

Θj = matrix of weights controlling function mapping from layer j to layer j+1.


Θj's dimension = s_(j+1) * (s_j +1)

![Image of neuron_network_modal]('https://raw.githubusercontent.com/abalone0204/Machine-Learning-Note/master/image/neuron_network_modal.png')


# Model Representation II

- forward propagate: from input layer -> hidden layer -> output layer 

# Application


## 1. Simple

- AND

- OR

## 2. x1 XNOR x2

