---
layout: page
title: Short Notes on ML Interpretability
tags: [about, Jekyll, theme, responsive]
modified: 2014-08-08T20:53:07.573882-04:00
comments: true
---

Disclaimer : following is an extracted gist on Interpretable machine learning from following sources.
* [https://christophm.github.io/interpretable-ml-book/intro.html](https://christophm.github.io/interpretable-ml-book/intro.html)
* [https://medium.com/analytics-vidhya/shap-part-2-kernel-shap-3c11e7a971b1](https://medium.com/analytics-vidhya/shap-part-2-kernel-shap-3c11e7a971b1)

* Surrogate models
    * Surrogate models are (generally simpler) models that are used to explain a more complex model

* Two ways to make machine learning interpretable
  * use interpretable models, such as linear models or decision trees
  * The other option is the use of model-agnostic interpretation tools that can be applied to any supervised machine learning model.

* All model-agnostic methods can be further differentiated on level of explanations
  * explain global model behavior across all data instances. Global explanations
  * explain individual predictions.Instance level explanations
 
* The following methods explain the overall behavior of the model:
  * Partial Dependence Plots, Accumulated Local Effects, Feature Interaction, Feature Importance, Global Surrogate Models and Prototypes and Criticisms.

* To explain individual predictions we have
  * Local Surrogate Models, Shapley Value Explanations, Counterfactual Explanations (and closely related: Adversarial Examples).

* Some methods can be used to explain both aspects of global model behavior and individual predictions:
  * Individual Conditional Expectation and Influential Instances.

* Machines surpass humans in many tasks, such as playing chess (or more recently Go) or predicting the weather. Even if the machine is as good as a human or a bit worse at a task, there remain great advantages in terms of speed, reproducibility and scaling. A major disadvantage of using machine learning is that insights about the data and the task the machine solves is hidden in increasingly complex models.

* The best performing models are often blends of several models (also called ensembles) that cannot be interpreted, even if each single model could be interpreted.

* The interpretability of the features is a big assumption. But if it is hard to understand the input features, it is even harder to understand what the model does. 

* Interpretability  non-mathematical definitions
  * Interpretability is the degree to which a human can understand the cause of a decision.
  * Interpretability is the degree to which a human can consistently predict the model’s result 
 
* Importance of Interpretability
  * Some models may not require explanations because they are used in a low-risk environment, meaning a mistake will not have serious consequences
  * The need for interpretability : for certain problems or tasks it is not enough to get the prediction (the what). The model must also explain how it came to the prediction (the why), because a correct prediction only partially solves your original problem. 
  * knowing the ‘why’ can help you learn more about the problem, the data and the reason why a model might fail.
  * The following reasons drive the demand for interpretability and explanations
    * Human curiosity and learning
	* The goal of science : The goal of science is to gain knowledge, but many problems are solved with big datasets and black box machine learning models. The model itself becomes the source of knowledge instead of the data. Interpretability makes it possible to extract this additional knowledge captured by the model.
	* safety measures : 
	* detecting bias : Interpretability is a useful debugging tool for detecting bias in machine learning models.
	* increase social acceptance : The process of integrating machines and algorithms into our daily lives requires interpretability to increase social acceptance. A machine or algorithm that explains its predictions will find more acceptance.
	* debugged and audited : Machine learning models can only be debugged and audited when they can be interpreted. Later, when a model is used in a product, things can go wrong. An interpretation for an erroneous prediction helps to understand the cause of the error. It delivers a direction for how to fix the system.
		
		
* When we do not need interpretability.
  * Interpretability is not required if the model has no significant impact.
  * Interpretability is not required when the problem is well studied.
  * Interpretability might enable people or programs to manipulate the system.

* Taxonomy of Interpretability Methods
  * Intrinsic or post hoc
  * Result of the interpretation method
    * Feature summary statistic:
    * Feature summary visualization:
    * Model internals (e.g. learned weights):
    * Data point:
    * Intrinsically interpretable model:
  * Model-specific or model-agnostic?
  * Local or global?

* Evaluation of Interpretability
  * Doshi-Velez and Kim (2017) propose three main levels for the evaluation of interpretability:
    * Application level evaluation (real task)
    * Human level evaluation (simple task)
    * Function level evaluation (proxy task)
		
		
* Properties of Explanations
  * An explanation usually relates the feature values of an instance to its model prediction in a humanly understandable way.
  * Properties of Explanation Methods
    * Expressive Power is the “language” or structure of the explanations the method is able to generate. 
    * Translucency describes how much the explanation method relies on looking into the machine learning model, like its parameters.
    * Portability describes the range of machine learning models with which the explanation method can be used.
    * Algorithmic Complexity describes the computational complexity of the method that generates the explanation.
  * Properties of Individual Explanations
    * Accuracy: How well does an explanation predict unseen data? High accuracy is especially important if the explanation is used for predictions in place of the machine learning model.
    * 
    * Comprehensibility: How well do humans understand the explanations?
    * Representativeness: How many instances does an explanation cover?
		
* Human-friendly Explanations
  * As an explanation for an event, humans prefer short explanations (only 1 or 2 causes) that contrast the current situation with a situation in which the event would not have occurred.
  * What Is an Explanation? : An explanation is the answer to a why-question
  * What Is a Good Explanation?
    * Explanations are contrastive (Lipton 19909). Humans usually do not ask why a certain prediction was made, but why this prediction was made instead of another prediction. What it means for interpretable machine learning: Humans do not want a complete explanation for a prediction, but want to compare what the differences were to another instance’s prediction
    * Explanations are selected. People do not expect explanations that cover the actual and complete list of causes of an event. We are used to selecting one or two causes from a variety of possible causes as THE explanation. What it means for interpretable machine learning: Make the explanation very short, give only 1 to 3 reasons, even if the world is more complex. 
    * Explanations are social. They are part of a conversation or interaction between the explainer and the receiver of the explanation.
    * Explanations focus on the abnormal.
		
* Chapter 4 Interpretable Models
  * The easiest way to achieve interpretability is to use only a subset of algorithms that create interpretable models.
  * 4.1 Linear Regression
    * A linear regression model predicts the target as a weighted sum of the feature inputs.
    * Whether the model is the “correct” model depends on whether the relationships in the data meet certain assumptions, which are linearity, normality, homoscedasticity, independence, fixed features, and absence of multicollinearity.
		
* Model-Agnostic Methods
  * Separating the explanations from the machine learning model (= model-agnostic interpretation methods) has some advantages
	
* it is also true that there is always a trade-off between accuracy of models & its interpretability. This situation has got to change – the trade-off between accuracy & interpretability is not acceptable.
	
* understandable and usable AI systems in order to address broader issues such as fairness, accountability, transparency and safety.

* The recipe for training local surrogate models:
  * Select your instance of interest for which you want to have an explanation of its black box prediction.
  * Perturb your dataset and get the black box predictions for these new points.
  * Weight the new samples according to their proximity to the instance of interest.
  * Train a weighted, interpretable model on the dataset with the variations.
  * Explain the prediction by interpreting the local model.	
	
* Shapley values method
  * The Shapley value is the average marginal contribution of a feature value across all possible coalitions.
  * The interpretation of the Shapley value is: Given the current set of feature values, the contribution of a feature value to the difference between the actual prediction and the mean prediction is the estimated Shapley value.
  * The Shapley value requires a lot of computing time. 
  * The Shapley value is the wrong explanation method if you seek sparse explanations (explanations that contain few features). Explanations created with the Shapley value method always use all the features.
  * The Shapley value returns a simple value per feature, but no prediction model like LIME. This means it cannot be used to make statements about changes in prediction for changes in the input
  * Another disadvantage is that you need access to the data

