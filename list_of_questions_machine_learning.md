# Machine Learning - List of questions

## Learning Theory

1. Describe bias and variance with examples. 
1. What is Empirical Risk Minimization? 
1. What is Union bound and Hoeffding's inequality? 
1. Write the formulae for training error and generalization error. Point out the differences.
1. State the uniform convergence theorem and derive it. 
1. What is sample complexity bound of uniform convergence theorem? 
1. What is error bound of uniform convergence theorem? 
1. What is the bias-variance trade-off theorem? 
1. From the bias-variance trade-off, can you derive the bound on training set size?
1. What is the VC dimension? 
1. What does the training set size depend on for a finite and infinite hypothesis set? Compare and contrast. 
1. What is the VC dimension for an n-dimensional linear classifier? 
1. How is the VC dimension of a SVM bounded although it is projected to an infinite dimension? 
1. Considering that Empirical Risk Minimization is a NP-hard problem, how does logistic regression and SVM loss work? 

## Model and feature selection
1. Why are model selection methods needed?
1. How do you do a trade-off between bias and variance?
1. What are the different attributes that can be selected by model selection methods?
1. Why is cross-validation required?
1. Describe different cross-validation techniques.
1. What is hold-out cross validation? What are its advantages and disadvantages?
1. What is k-fold cross validation? What are its advantages and disadvantages?
1. What is leave-one-out cross validation? What are its advantages and disadvantages?
1. Why is feature selection required?
1. Describe some feature selection methods.
1. What is forward feature selection method? What are its advantages and disadvantages?
1. What is backward feature selection method? What are its advantages and disadvantages?
1. What is filter feature selection method and describe two of them?
1. What is mutual information and KL divergence?
1. Describe KL divergence intuitively.

## Miscellaneous
1. What is the difference between loss function, cost function and objective function?

## Curse of dimensionality 
1. Describe the curse of dimensionality with examples.
1. What is local constancy or smoothness prior or regularization?

## Universal approximation of neural networks
1. State the universal approximation theorem? What is the technique used to prove that?
1. What is a Borel measurable function?
1. Given the universal approximation theorem, why can't a MLP still reach a arbitrarily small positive error?

## Deep Learning motivation
1. What is the mathematical motivation of Deep Learning as opposed to standard Machine Learning techniques?
1. In standard Machine Learning vs. Deep Learning, how is the order of number of samples related to the order of regions that can be recognized in the function space?
1. What are the reasons for choosing a deep model as opposed to shallow model? (1. Number of regions O(2^k) vs O(k) where k is the number of training examples 2. # linear regions carved out in the function space depends exponentially on the depth. )
1. How Deep Learning tackles the curse of dimensionality? 

## Support Vector Machine
1. How can the SVM optimization function be derived from the logistic regression optimization function?
1. What is a large margin classifier?
1. Why SVM is an example of a large margin classifier?
1. SVM being a large margin classifier, is it influenced by outliers? (Yes, if C is large, otherwise not)
1. What is the role of C in SVM?
1. In SVM, what is the angle between the decision boundary and theta?
1. What is the mathematical intuition of a large margin classifier?
1. What is a kernel in SVM? Why do we use kernels in SVM?
1. What is a similarity function in SVM? Why it is named so?
1. How are the landmarks initially chosen in an SVM? How many and where?
1. Can we apply the kernel trick to logistic regression? Why is it not used in practice then?
1. What is the difference between logistic regression and SVM without a kernel? (Only in implementation – one is much more efficient and has good optimization packages)
1. How does the SVM parameter C affect the bias/variance trade off? (Remember C = 1/lambda; lambda increases means variance decreases)
1. How does the SVM kernel parameter sigma^2 affect the bias/variance trade off?
1. Can any similarity function be used for SVM? (No, have to satisfy Mercer’s theorem)
1. Logistic regression vs. SVMs: When to use which one? 
( Let's say n and m are the number of features and training samples respectively. If n is large relative to m use log. Reg. or SVM with linear kernel, If n is small and m is intermediate, SVM with Gaussian kernel, If n is small and m is massive, Create or add more fetaures then use log. Reg. or SVM without a kernel)

## Bayesian Machine Learning
1. What are the differences between “Bayesian” and “Freqentist” approach for Machine Learning?
1. Compare and contrast maximum likelihood and maximum a posteriori estimation.
1. How does Bayesian methods do automatic feature selection?
1. What do you mean by Bayesian regularization?
1. When will you use Bayesian methods instead of Frequentist methods? (Small dataset, large feature set)

## Regularization
1. What is L1 regularization?
1. What is L2 regularization?
1. Compare L1 and L2 regularization.

## Evaluation of Machine Learning systems
1. What are accuracy, sensitivity, specificity, ROC?
1. What are precision and recall?
1. Describe t-test in the context of Machine Learning.

## k-means clustering
1. Describe the k-means algorithm.
1. What is distortion function? Is it convex or non-convex?
1. Tell me about the convergence of the distortion function.
1. Topic: EM algorithm
1. What is the Gaussian Mixture Model?
1. Describe the EM algorithm intuitively. 
1. What are the two steps of the EM algorithm
1. Compare GMM vs GDA.

## Dimensionality Reduction
1. Why do we need dimensionality reduction techniques? (data compression, speeds up learning algorithm and visualizing data)
1. What do we need PCA and what does it do? (PCA tries to find a lower dimensional surface such the sum of the squared projection error is minimized)
1. What is the difference between logistic regression and PCA?
1. What are the two pre-processing steps that should be applied before doing PCA? (mean normalization and feature scaling)

## Basics of Natural Language Processing
1. What is WORD2VEC?
1. What is t-SNE? Why do we use PCA instead of t-SNE?
1. What is sampled softmax?
1. Why is it difficult to train a RNN with SGD?
1. How do you tackle the problem of exploding gradients? (By gradient clipping)
1. What is the problem of vanishing gradients? (RNN doesn't tend to remember much things from the past)
1. How do you tackle the problem of vanishing gradients? (By using LSTM)
1. Explain the memory cell of a LSTM. (LSTM allows forgetting of data and using long memory when appropriate.)
1. What type of regularization do one use in LSTM?
1. What is Beam Search?
1. How to automatically caption an image? (CNN + LSTM)

