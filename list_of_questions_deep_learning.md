# Deep Learning - List of questions

## General questions

1. How will you implement dropout during forward and backward pass?
1. What do you do if Neural network training loss/testing loss stays constant? (ask if there could be an error in your code, going deeper, going simpler…)
1. Why do RNNs have a tendency to suffer from exploding/vanishing gradient? How to prevent this? (Talk about LSTM cell which helps the gradient from vanishing, but make sure you know why it does so. Talk about gradient clipping, and discuss whether to clip the gradient element wise, or clip the norm of the gradient.)
1. Do you know GAN, VAE, and memory augmented neural network? Can you talk about it?
1. Does using full batch means that the convergence is always better given unlimited power? (Beautiful explanation by Alex Seewald: https://www.quora.com/Is-full-batch-gradient-descent-with-unlimited-computer-power-always-better-than-mini-batch-gradient-descent)
1. What is the problem with sigmoid during backpropagation? (Very small, between 0.25 and zero.)
1. Given a black box machine learning algorithm that you can’t modify, how could you improve its error? (you can transform the input for example.)
1. How to find the best hyper parameters? (Random search, grid search, Bayesian search (and what it is?))
1. What is transfer learning?

