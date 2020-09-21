---
layout: page
title: ML notes
tags: [ML]
modified: 2014-08-08T20:53:07.573882-04:00
comments: true
---

* AI, ML, Robotics... What's our end goal/purpose? : Its increasing Productivity.  
All these technologies bring Automation -> Automation makes us Efficient -> Being more Efficient makes us more Productive

* What is Machine Learning? : data+model→prediction
	
* A learning algorithm consists of : prediction function + objective function + optimation algorithm
  * Prediction function :A function which is used to make the predictions. It includes our assumptions about how the world works.  e.g. smoothness, ...
  * Objective function 	:A function which defines the cost of misprediction. To put it in another way, it specifies the quality of the match between the prediction function and the training data

* Much of the acdemic field of machine learning is the quest for new learning algorithms that allow us to bring different types of models and data together.

* Artificial Intelligence, Data Science and Classical statistics
  * Artificial intelligence technologies typically focus on emulating some form of human behaviour.
  * Data Science technologies focus on drawing inferences from data which is collected by happenstance, rather than by experimental design.
  * Classical statistics is the science of drawing conclusions from data. Here the question is formed first, and data is collected to answer the question.
	
* Robotics -> Emulation of a human’s motor skills to automate processes.  
Machine learning is aiming to replicate processes which require emulation of our cognitive skills through the direct use of data.
A key idea in machine learning is to emulate the process as a mathematical function. Each function has a set of parameters which control its behavior. Learning is the process of changing these parameters to change the shape of the function to make it more representative of the data. Our choice of which class of mathematical functions we use is a vital component of our model.

* A beautiful perspective on ML : http://inverseprobability.com/2017/07/17/what-is-machine-learning

* “Symbolic AI” = “Classical AI” = “Rule-based AI” = “Good old-fashioned AI” : explicitly represent human knowledge in a declarative form (i.e. facts and rules).
	
* Classical three subdivisions of the field: supervised learning, unsupervised learning and reinforcement learning

* Supervised Learning
  * In supervised learning the inputs, x, are mapped to a label, y, through a function f (prediction function) that is dependent on a set of parameters, w. y=f(x,y)
  Challenges:
    * choosing which features, x, are relevant in the prediction
	  * Feature selection is a critical stage in the algorithm design process. The features we select should be ones we expect to correlate with the prediction. Feature selection algorithms: algorithms that automate the process of finding the features that we need.
	  * choosing the appropriate class of function, f, to use.
	    * smooth?, linear, with periodic components?
		* Encoding invariance in the prediction function is like encoding knowledge in the model. If we don’t specify these invariances then the model must learn them. This will require a lot more data to achieve the same performance, making the model less data efficient.
	  * selecting the right parameters, w.

  * The ability of a machine learning system to predict well on production systems given only its training data is known as its generalization ability. The choice of the class of prediction functions is critical in ensuring that the model generalizes well.
	  
* Labels : A label is the thing we're predicting  
Features: A feature is an input variable.
	
* Regression vs. classification  
A regression model predicts continuous values.   
A classification model predicts discrete values. 
	
* L2 Loss : squared error

* Linear Regression: Prediction function takes the form -> y = w0 + w1*x1 + w2*x2 + ... + wn*xn

* In supervised learning, a machine learning algorithm builds a model by examining many examples and attempting to find a model that minimizes loss; this process is called empirical risk minimization.

* Mean square error (MSE) : The average squared loss per example over the whole dataset.

* A Machine Learning model is trained by starting with an initial guess for the weights and bias and iteratively adjusting those guesses until learning the weights and bias with the lowest possible loss.

* Reducing Loss: Gradient Descent, BFGS

* Adagrad and Adam : separate effective learning rate per feature.

* Learning rate(step size):  
A Hyperparameter.  
Too small -> Learning will take too long  
Too large -> The next point will perpetually bounce haphazardly

* Gradient Descent (full-batch) : uses all examples in one iteration  
Stochastic gradient descent (SGD) : uses only a single example in one iteration (a batch size of 1)  
Mini-batch stochastic gradient descent (mini-batch SGD) :

* One epoch spans sufficient iterations to process every example in the dataset.

* Generalization refers to your model's ability to adapt properly to new, previously unseen data, drawn from the same distribution as the one used to create the model.

* Partitioning Data (If we are not using cross validation)
  * Train set (to train), Validation set(to test our hyperparameters), Test set (hold out set) (to test)
  * Why Validation set? : The more often we evaluate(hyperparameters) on a given test set, the more we are at risk for implicitly overfitting to that one test set.
  * A better workflow: Pick the model that does best on the validation set(we can do many rounds here) -> Double-check that model against the test set.

* Cross-Validation : allows us to utilize our data better.
  * No need to split data, training & hyperparameter tuning can be done using the single data set.
  * types : Simple K-Folds, Leave One Out (handy on small datasets), Stratified Cross Validation
  * If we have a small dataset -> cross validation is a good choice

* Type I error  = False positive.  
Type II error = False negative.

* Feature engineering means transforming raw data into a feature vector.

* Categorical features : features which have a discrete set of possible values
  * One-hot encoding when a single value is 1
  * Multi-hot encoding when multiple values are 1.
  * When you have a big cardinality -> sparse representation : in which only nonzero values are stored
  * Encodings : One Hot Encoding, Label Encoding (normally used on ordinal features)
  
* Qualities of Good Features
  * Avoid rarely used discrete feature values.
  * Prefer clear and obvious meanings: Good -> house_age_years: 27, Bad -> house_age: 851472000
  * Don't mix "magic" values with actual data: ex: quality_rating: -1 (do not do this)
  * Account for upstream instability: The definition of a feature shouldn't change over time, good->city_id: "br/sao_paulo", bad->inferred_city_cluster: "219"


* Implementing a ML Solution Steps : 
  1. Define a ML Problem and propose a solution.
  2. Construct the data set
  3. Transform Data
  4. Train a model
  5. Use the model to make predictions.  
  

* Data Preparation and Feature Engineering in ML
  * Direct vs. Derived Labels
  * Transforming Numeric Data :
    * Normalizing/Scaling: making all same scale
	  * Why?:
	    * Helps gradient descent converge more quickly.
	    * Helps avoid the "NaN trap,"
	    * Helps the model learn appropriate weights for each feature.
	  * Techniques:
        * Linear Scaling: When the feature is more-or-less uniformly distributed across a fixed range.
	    * Clipping: When the feature contains some extreme outliers.
	    * Log Scaling: When the feature conforms to the power law.
	    * Z-score: When the feature distribution does not contain extreme outliers.
    * Bucketing(binning): numeric->categorical
      * Buckets with equally spaced boundaries
	  * Quantile Bucketing: creating buckets that each have the same number of points
  * Transforming Categorical Data
	* Sparse representation: [4] is equivalent to [0, 0, 0, 0, 1, 0, 0].
    * Out of Vocab (OOV): to deal with outliers in categorical data 

* Handling extreme outliers -> clipping

* Scrubbing : deal with Omitted values, Duplicate examples, Bad labels, Bad feature values

* Feature Crosses : A feature cross is a synthetic feature formed by multiplying (crossing) two or more features. Might provide enhanced predictive abilities. We can Encode Nonlinearity
 
* Crossing One-Hot Vectors: learn this , can test with housing data as well

* Generalization curve : shows the loss for both the training set and validation set against the number of training iterations.
	
* Complete: https://colab.research.google.com/github/google/eng-edu/blob/master/ml/fe/exercises/intro_to_modeling.ipynb?utm_source=ss-data-prep&utm_campaign=colab-external&utm_medium=referral&utm_content=intro_to_modeling
	
* Handling class Imbalance
  * Up-sample the minority class
  * Down-sample the majority class
  * Change your performance metric
  * Use tree-based algorithms
  * Reframe as Anomaly Detection
  * Create Synthetic Samples

* Training/serving skew :  different results are computed for your metrics at training time vs. serving time.
  * Solution : During training, use only the features that you'll have available in serving, and make sure your training set is representative of your serving traffic.

* Overcrossing? or model if the model is too complex we give it the opportunity to fit to the noise in the training data.  This is overfitting: Solution : regularization
  
* Regularization Strategies
  * Early stopping
  * Penalizing Model Complexity
    * L2 regularization (a.k.a. ridge): complexity(model) = sum of the squares of the weights
	  * lambda (also called the regularization rate):If your lambda value is too high, your model will be simple, but you run the risk of underfitting your data
	*  L1 Regularization: Penalize sum of abs(weights)
	  * Advantages:
		* Incorporates variable selection to the modeling problem.
		* You can have a lot of computational savings since (no computation for features whose coefficient is 0) 

* Classification threshold = Decision threshold  
  
* Metrics
  * Accuracy : (tp+tn)/ (all examples)
    * not good with class imbalance
  * Precison : if model says true, how much can we trust the model. tp/(tp+fp)
    * use when the cost of a false positive is high
    * increase Precison means-> say yes only when we are absolutely sure. -> this is like increasing our classification threshold.
  * Recall : how good the model is recalling true scenarios?. tp/(tp+fn)
	* use when the cost of a false negative is high
	* increase recall -> this is like lowering our classification threshold.
  * Precision,  Recall did not say how good our model is differentiating postives from negatives. here comes AUC: Area Under the ROC Curve.
    *  One way of interpreting AUC is as the probability that the model ranks a random positive example more highly than a random negative example.
  * Prediction Bias
   * Prediction Bias = "average of predictions" - "average of observations" 
  * F1 Score: ((precision*recall)/(precision+recall))
    * F1 score conveys the balance between the precision and the recall. 1 being the best, and those tending to 0 being the worst
	* Use when true negatives don’t matter.


* Ensemble Learning : Combine weak models to form a powerful model
  * Simple Ensemble Techniques
    * Max Voting(generally used for classification): Train multiple models on the data set->get predictions for each data point-> take the mode of all the predictions
	* Averaging: Train multiple models on the data set->get predictions for each data point-> take the average of all the predictions
	* Weighted Average: Train multiple models on the data set->get predictions for each data point-> take the weighted average of all the predictions
  * Advanced Ensemble techniques
    * Stacking:  TODO
	* Bagging :
	  * Reduce the variance of our predictions.(solution to overfitting)
	  * Combines results of multiple classifiers modeled on different sub-samples of the same data set.
	  * Data set-> create multiple data sets(bootstrap sampling, can have a fraction of the columns as well as rows(hyperparameter of the ensemble))->create multiple classifiers->combine classifier results (mean, median or mode value).
	  * Example : Random forest
	* Boosting:
	  * Got n number of base learners -> Each learner is trained sequencially, based on previous run targeting higher weights for the mis-classified data points -> combine results.
	  * Exmaples : GBM and XGBoost(got regularization) (both tree based)

* Desicion Tree Algorithm
  * can handle both classification and regression
  * In this technique, we keep spliting the population into more homogeneous sub-populations based on most significant splitter in input variables.
  * aim is to make more homogeneous child nodes.
  * split algorithms : classification-> gini, chi square, information gain. regression: reduction in variance
  * splitting continues until a stopping condition is reached.
  * stopping criterias: Minimum samples for a node split, Minimum samples for a terminal node (leaf),Maximum depth of tree (vertical depth),Maximum number of terminal nodes Maximum features to consider for split
  * How to avoid over-fitting ?: set stopping criterias, prunning
  * Predictions : regression -> mean value of obsevations in the leaf node where the data falls. classification -> mode of obsevations in the leaf node where the data falls.
  * Regression decision trees cannot extrapolate!. (because it takes the mean)
  * Advantages: Simple,Easy to identify most significant variables,It is not influenced by outliers and missing values to a fair degree.
  * Prunning
    * Bottom-up pruning, Top-Down Pruning
	* Pruning Algorithms :
	  * Reduced error pruning : Starting at the leaves, each node is replaced with its most popular class. If the prediction accuracy is not affected then the change is kept.

* Random Forest Algorithm
  * Ensemble technique: Bagging multiple decision trees
  * classification-> majority voting, regression-> mean
  * Disadvantages : black box

* K Nearest Neighbor (KNN) 
  * both classification(widely used) and regression.
  * K: # of neighbors considered in prediction. The choice of the parameter K is very crucial in this algorithm.
  * small K -> might overfit, Large K -> might underfit, Use elbow method on validation error curve to choose K.

* Logistic Regression
  * Calculates a Probability
  * Log Loss is the loss function for logistic regression.
  
* Naive Bayes Classifiers
  * Assumption : Every pair of features is independent of each other. This is why we call it naive.
  * For a observation X(feature vector), compute P(L1/X),...,P(Ln/X) (n labels) and choose the corresponding label in the largest.
  * P(y/X) is calculated using bayes theorem. P(y/X) = P(y) P(X/y) / P(X)
  * All P(xi/yi) can be precalculated using the data set. 
  * Read: https://www.geeksforgeeks.org/naive-bayes-classifiers/
  * Gaussian Naive Bayes, continuous values associated with each feature are assumed to be distributed according to a Gaussian distribution.
  * easy to train, fast, easy to update with new data(in the case of a decision tree we have to build the tree from scratch).
  * “ensembling, boosting, bagging” won’t help. Naive Bayes has no variance to minimize.
 
* Kernel methods 
  * a class of algorithms
  * example : support vector machine
 
* Bayes Theorem
  * Finds the probability of an event occurring given the probability of another event that has already occurred.P(A/B)
  * P(A)=priori of A = the prior probability.
  * P(A/B) is a posteriori probability of A.
  * P(A/B) = P(A) P(B/A) / P(B)

* SVM?? TODO
 
* Supervised learning is broadly divided into classification and regression.  
Unsupervised learning can be broadly split into methods that cluster the data (i.e. provide a discrete label) and methods that represent the data as a continuous value.

* Unsupervised Learning
  * The aim in unsupervised learning is to extract structure from data.
  * The type of structure? depends on context of the task.
  * Clustering
	* notion of a similarity function exists. (ex: squared distance)
	* Example algorithms : k-Means Clustering, Hierarchical Clustering
  * Dimensionality Reduction
    * compress the data by replacing with a reduced number of continuous variables.
    * It assumes that the data we observe is generated from some lower dimensional underlying process.
	* Example algorithms : Principal Component Analysis
	
* k-Means Clustering
  * k-means clustering is a distance-based algorithm.
  * simple, quick to implement, but it is an initialization sensitive algorithm.
  * https://www.analyticsvidhya.com/blog/2019/10/gaussian-mixture-models-clustering/
  * Algorithm : 1. centroid initialitation-> 2. centroid assingment-> 3.centroid update -> repeat 2 & 3 until centroids does not change
  * Applications : Customer Segmentation
  * Drawbacks : Clusters created have a circular shape,
  * cluster centroids inititialitation: random, random data points, random assingment and calculate centroids, kmeans++
  * Right Number of Clusters: elbow curve

* Gaussian Mixture Models
  * a powerful distribution-based clustering algorithm
  * GMMs use the soft clustering technique for assigning data points to Gaussian distributions.
  * initializes k Gaussian distributions in the feature space. 
  * use Expectation-Maximization (EM) to find model parameters
  * initially we randomly assign the values for the mean(μ), covariance(Σ), and density(Π) for each cluster.
  * For each point xi, calculate the probability that it belongs to cluster/distribution c1, c2, … ck.
  * we go back and update the Π, μ and Σ values.
  
* Hierarchical Clustering <todo>
  * https://www.youtube.com/watch?v=6R16reLVl3I
  * https://www.youtube.com/watch?v=OcoE7JlbXvY
  
* Principal Component Analysis
  * a dimensionality reduction technique.
  * A principal component is a normalized linear combination of the original predictors in a data set.
  * First principal component is a linear combination of original predictor variables which captures the maximum variance in the data set.
  * normalization of variables necessary in PCA
  
* Bias and Variance trade off
  * Bias : ‘how much on an average are the predicted values different from the actual value.’
  * Varience : ‘how different will the predictions of the model be at the same point if different samples are taken from the same population’
  * Low model complexity  -> high bias (underfitting)
  * High model complexity -> high variance (overfitting)
  * The optimal model complexity -> balanced bias and varience

* Reinforcement Learning
  * model free approach known as Q-learning
  * model based reinforcement learning  
  
* ANN = Artificial neural network

* Regularization Techniques for Neural Network
  * Dropout :  removes some nodes in that layer based on a proability.
  * DropConnect : removes some connections in that layer based on a proability.
 
* EDA
  * Univariate Analysis
    * Numerical feature
	  * Types: Discrete, Continuous
	  * Things to watch : Mean, Standard Deviation, Max, Min,Interquartile range (IQR),Histograms,Skewness and Kurtosis
	  * how?: Descriptive statistics summary, Distribution plot
	* Categorical feature
	  * Types: Nominal Data & Ordinal Data
	  * Things to watch : Cardinality(How many categories are there), What are the diffrent categories?, What is the most common category?,Values counts for each category, Values percentages for each category.
	  * how?: Descriptive statistics summary, Value count plots, Pie Graph for precentages of each category.
  * Bivariate analysis
    * numerical-numerical
	  * scatter plot
	* Numerical-Categorical
	  * Box Plot
  * Correlation Analysis
  
* Hyperparamter Tuning
  * Grid search,Manual search, Random search, Bayesian Optimization and More..

* MLE (Maximum Likelihood Estimation)
  * We fit a distribution to data that maximizes the likelihood that you observed the things you observed.	 
  * needs to find distibution parameters

* Backpropagation
	* algorithm for computing the negative gradient of a cost function in a neural network. 
	* result is a gradient vector, giving weights for each connection indicating how it affects the cost function.

* Generative VS Discriminative Models <Todo> : https://medium.com/@mlengineer/generative-and-discriminative-models-af5637a66a3
  * A Generative Model ‌learns the joint probability distribution p(x,y). It predicts the conditional probability with the help of Bayes Theorem.
    * Naïve Bayes
  * A Discriminative model ‌learns the conditional probability distribution p(y|x).
    * ‌Logistic regression, Scalar Vector Machine, Traditional neural networks

* Cross-validation for time series dataset
  * time series is not randomly distributed data—it is ordered by chronological order. K-fold wont work.
  * A technique : Forward chaining,
	fold 1 : training [1], test [2]
	fold 2 : training [1 2], test [3]
	fold 3 : training [1 2 3], test [4]
	fold 4 : training [1 2 3 4], test [5]
	fold 5 : training [1 2 3 4 5], test [6]
	
* What’s a Fourier transform?
  * A method to decompose functions into a superposition of symmetric functions.	
	
* Time Series Analysis: TODO
  
* Questions:  
Which form of regularization should we use?
	
* Sources :
  * http://inverseprobability.com/2017/07/17/what-is-machine-learning


* Do again:  
Feature Crosses  
https://developers.google.com/machine-learning/guides/rules-of-ml#ml_phase_ii_feature_engineering  
Classification: Prediction Bias  
Binary Classification: Programming Exercise