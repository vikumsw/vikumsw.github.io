---
layout: page
title: A Short Note on AutoML
tags: [about, Jekyll, theme, responsive]
modified: 2014-08-08T20:53:07.573882-04:00
comments: true
---

This is an short note on AutoML which is heavily based on this wonderful [article](https://www.vanderschaar-lab.com/automl-powering-the-new-human-machine-learning-ecosystem/#what-is-automl) by [The van der Schaar Lab](https://www.vanderschaar-lab.com/). I might have added things slightly here and there. But almost everything you find here is explained clearly on the [original article](https://www.vanderschaar-lab.com/automl-powering-the-new-human-machine-learning-ecosystem/#what-is-automl) and I highly recommend reading it.

## What is AutoML?
Coming up with automatic methodologies that can create effective machine learning models.

## Why we need AutoML? (Purpose)
The conventional way to make machine learning models is to hand-craft them. But there exists fundamental issues and limitations in this method.  
Crafting a machine learning model involves completing several painstaking stages. There is no universally applicable “best” algorithm for all problems exists.  
There are numerous algorithms and hyperparameters to choose from and these options are growing everyday making the selection more difficult. Moreover, deciding whether certain steps are necessary or not is not straight forward.  

	
Due to above reasons hand-crafting a machine learning models is,  

* Often extremely time-consuming. 
* Can generally only be done efficiently by experts
* Dependent on assumptions, and therefore may yield poor results.
* Required to repeat these tedious time consuming stages for every new problem or dataset.
		
As a consequence of above problems machine learning is out of reach for non-expert end users and smaller organizations without access to expert users.

*Therefore, AutoML could be a potential solution that could allow non-expert users to create flexible high-quality models to tackle new problems.*
	
### Advantages
* Free data scientists from manual model tuning, allowing them to focus on more important areas.
* Enabling faster iteration and delivery of results.
* Democratizing machine learning:Help to enable the widespread adoption of machine learning by specialists without machine learning expertise.
* Create better flexible high-quality effective machine learning models.
	
## What stages can be automated by AutoML? 
In the early days it was primarily on automation of parameter optimization. But now is covers practically the entire model construction process, including 

* Feature engineering
* Algorithm selection	and hyperparameter optimization
* Model training
* Evaluation
	
## Importance of interpretability
In AutoML the pipelines are not hand-crafted. They may be complex, and they may also need additional “debugging” and integration of interpretability techniques to ensure fairness and its alignment with our goals.
	
## Roadblocks hindering its wide adoption
* Data Cleaning, Preparation, and Standardization :
Data cleaning and preparing the datasets is painstaking.This applies to both hand-crafted ML and AutoML. In almost every case, a data scientist in collaboration with a domain professional will need to review, clean, and prepare data so that it can be understood by an AutoML framework. 
 * Solution : Common protocols or methods for formatting and preparing data will need to be developed and adhered to.
* The need to build layers of abstraction that permit various users to interact with an AutoML framework at their own knowledge level, and with their intended usage in mind.
* Commonization of Components: The need for user-friendly AutoML frameworks to be constructible from modular “blocks” that can be selected depending on the purpose of the model.
	
	
## What is left to do in this area of machine learning?
Quoting an expert, Professor Mihaela van der Schaar : 
>"AutoML is a broad, nebulous, and often misunderstood area that is still in development, and its potential isn’t even close to being fully realized yet".
>

In the context of healthcare , She furthermore adds
> "Our view, as a machine learning lab that works extensively alongside clinicians, medical researchers, hospital managers, and patients, is that AutoML is essential to ensuring that machine learning can be applied effectively and consistently throughout healthcare, and that its impact can be felt and appreciated by communities outside our own."
>
	

---

**Hand-crafted machine learning models**: *ONE* answer to *ONE* question  
**AutoML**: *ONE* answer to *MANY* questions

---

