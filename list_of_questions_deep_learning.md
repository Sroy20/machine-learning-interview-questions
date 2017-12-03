# Deep Learning - List of questions

## Table of Contents

- [General questions](#general-questions)
- [Machine Learning basics](#machine-learning-basics)
- [Optimization procedures](#optimization-procedures)
- [Parameter initialization](#parameter-initialization)
- [Sequence Modeling](#sequence-modeling)
- [Autoencoders](#autoencoders)
- [Representation Learning](#representation-learning)
- [Adversarial Networks](#adversarial-networks)

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
1. Compare and contrast L1-loss vs. L2-loss and L1-regularization vs. L2-regularization.

## Machine Learning basics

1. Can you state Tom Mitchell's definition of learning and discuss T, P and E?
1. What can be different types of tasks encountered in Machine Learning?
1. What are supervised, unsupervised, semi-supervised, self-supervised, multi-instance learning, and reinforcement learning?
1. Loosely how can supervised learning be converted into unsupervised learning and vice-versa?
1. Consider linear regression. What are T, P and E?
1. Derive the normal equation for linear regression.
1. What do you mean by affine transformation? Discuss affine vs. linear transformation.
1. Discuss training error, test error, generalization error, overfitting, and underfitting.
1. Compare representational capacity vs. effective capacity of a model.
1. Discuss VC dimension.
1. What are nonparametric models? What is nonparametric learning?
1. What is an ideal model? What is Bayes error? What is/are the source(s) of Bayes error occur?
1. What is the no free lunch theorem in connection to Machine Learning?
1. What is regularization? Intuitively, what does regularization do during the optimization procedure? (expresses preferences to certain solutions, implicitly and explicitly)
1. What is weight decay? What is it added?
1. What is a hyperparameter? How do you choose which settings are going to be hyperparameters and which are going to be learnt? (either difficult to optimize or not appropriate to learn - learning model capacity by learning the degree of a polynomial or coefficient of the weight decay term always results in choosing the largest capacity until it overfits on the training set)
1. Why is a validation set necessary?
1. What are the different types of cross-validation? When do you use which one?
1. What are point estimation and function estimation in the context of Machine Learning? What is the relation between them?
1. What is the maximal likelihood of a parameter vector $theta$? Where does the log come from?
1. Prove that for linear regression MSE can be derived from maximal likelihood by proper assumptions.
1. Why is maximal likelihood the preferred estimator in ML? (consistency and efficiency)
1. Under what conditions do the maximal likelihood estimator guarantee consistency?
1. What is cross-entropy of loss? (trick question) 


## Optimization procedures

1. What is the difference between an optimization problem and a Machine Learning problem?
1. How can a learning problem be converted into an optimization problem?
1. What is empirical risk minimization? Why the term empirical? Why do we rarely use it in the context of deep learning?
1. Name some typical loss functions used for regression. Compare and contrast. (L2-loss, L1-loss, and Huber loss)
1. What is the 0-1 loss function? Why can't the 0-1 loss function or classification error be used as a loss function for optimizing a deep neural network? (Non-convex, gradient is either 0 or undefined. https://davidrosenberg.github.io/ml2015/docs/3a.loss-functions.pdf)
1. 


## Parameter initialization

1.  

## Sequence Modeling

1. Write the equation describing a dynamical system. Can you unfold it? Now, can you use this to describe a RNN? (include hidden, input, output, etc.) 
1. What determines the size of an unfolded graph?
1. What are the advantages of an unfolded graph? (arbitrary sequence length, parameter sharing, and illustrate information flow during forward and backward pass)
1. What does the output of the hidden layer of a RNN at any arbitrary time _t_ represent?
1. Are the output of hidden layers of RNNs lossless? If not, why?
1. RNNs are used for various tasks. From a RNNs point of view, what tasks are more demanding than others? 
1. Discuss some examples of important design patterns of classical RNNs.
1. Write the equations for a classical RNN where hidden layer has recurrence. How would you define the loss in this case? What problems you might face while training it? (Discuss runtime)
1. What is backpropagation through time? (BPTT)
1. Consider a RNN that has only output to hidden layer recurrence. What are its advantages or disadvantages compared to a RNNhaving only hidden to hidden recurrence? 
1. What is Teacher forcing? Compare and contrast with BPTT.
1. What is the disadvantage of using a strict teacher forcing technique? How to solve this?
1. 
1. Explain the vanishing/exploding gradient phenomenon for recurrent neural networks. (use scalar and vector input scenarios)
1. Why don't we see the vanishing/exploding gradient phenomenon in feedforward networks? (weights are different in different layers - Random block intialization paper)
1. What is the key difference in architecture of LSTMs/GRUs compared to traditional RNNs? (Additive update instead of multiplicative)
1. What is the difference between LSTM and GRU?
1. Explain Gradient Clipping. 
1. Adam and RMSProp adjust the size of gradients based on previously seen gradients. Do they inherently perform gradient clipping? If no, why?
1. Discuss RNNs in the context of Bayesian Machine Learning.
1. Can we do Batch Normalization in RNNs? If not, what is the alternative? (BNorm would need future data; Layer Norm)

## Autoencoders

1. Describe an Autoencoder? What does it "auto-encode"?
1. What were Autoencoders traditionally used for? Why there has been a resurgence of Autoencoders for generative modeling?
1. What is recirculation?
1. What loss functions are used for Autoencoders?
1. What is a linear autoencoder? Can it be optimal (lowest training reconstruction error)? If yes, under what conditions?
1. What is the difference between Autoencoders and PCA (can also be used for reconstruction - https://stats.stackexchange.com/questions/229092/how-to-reverse-pca-and-reconstruct-original-variables-from-several-principal-com).
1. What is the impact of the size of the hidden layer in Autoencoders?
1. What is an undercomplete Autoencoder? Why is it typically used for? 
1. What is a linear Autoencoder? Discuss it's equivalence with PCA. (only valid for undercomplete) Which one is better in reconstruction?
1. What problems might a nonlinear undercomplete Autoencoder face?
1. What are overcomplete Autoencoders? What problems might they face? Does the scenario change for linear overcomplete autoencoders? (identity function)
1. Discuss the importance of regularization in the context of Autoencoders.
1. Why does generative autoencoders not require regularization?
1. What are sparse autoencoders?
1. What is a denoising autoencoder? What are its advantages? How does it solve the overcomplete problem?
1. What is score matching? Discuss it's connections to DAEs.
1. Are there any connections between Autoencoders and RBMs?
1. What is manifold learning? How are denoising and contractive autoencoders equipped to do manifold learning? 
1. What is a contractive autoencoder? Discuss its advantages. How does it solve the overcomplete problem?
1. Why is a contractive autoencoder named so? (intuitive and mathematical)
1. What are the practical issues with CAEs? How to tackle them?
1. What is a stacked autoencoder? What is a deep autoencoder? Compare and contrast.
1. Compare the reconstruction quality of a deep autoencoder vs. PCA.
1. What is predictive sparse decomposition?
1. Discuss some applications of Autoencoders.

## Representation Learning

1. What is representation learning? Why is it useful? (for a particular architecture, for other tasks, etc.)
1. What is one-shot and zero-shot learning (Google's NMT)? Give examples.
1. What trade offs does representation learning have to consider?
1. What is greedy layer-wise unsupervised pretraining? Why greedy? Why layer-wise? Why unsupervised? Why pretraining?
1. What were/are the purposes of the above technique? (deep learning problem and initialization)
1. 

## Adversarial Networks

1. Discuss state-of-the-art attack and defense techniques for adversarial models.
1.  

