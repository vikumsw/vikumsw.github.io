---
layout: page
title: My take on "The 3Ds of Machine Learning Systems Design" by Professor Neil Lawrence
tags: [about, Jekyll, theme, responsive]
modified: 2014-08-08T20:53:07.573882-04:00
comments: true
---

This is my take on "The 3D's process" which is based on this wonderful [article](http://inverseprobability.com/2018/11/05/the-3ds-of-machine-learning-systems-design#fnref5) by [Professor Neil Lawrence]. I have changed the structure and compiled in a way I prefer. Everything you find here is explained clearly on the [original article](http://inverseprobability.com/2018/11/05/the-3ds-of-machine-learning-systems-design#fnref5) and I highly recommend reading it.

# The 3Ds of Machine Learning Systems Design
Purpose of the article is describing the challenges of deploying our innovation and consider what the solutions may be.

## The 3D's process
### The Decomposition Challenge: 
We have to put some careful thought into right sub-processes to automate with machine learning.  
#### Why?:  
* We cannot simply automate all decisions through data. We are constrained by our data and the models we use.
* The selection of which task to automate becomes critical and has downstream effects on our overall system design.
* We’d like to keep our models simple and interpretable. If we can convert a complex mapping to a linear mapping through clever selection of sub-tasks and features this is a big win.
		
#### How?:
* We would have to separate a complex task into separate entities that are capable of being partitioned and identify appropriate sub-task to be automated.
* Should consider automating feature and model selection, model improvement using AutoML.
* End-to-end training could be considered to embrace the characteristic of co-evolution of systems ; upstream errors can be compensated by downstream corrections.
 * Can lead to improvements in performance
 * But it could also damage our systems decomposability, its interpretability, and perhaps its adaptability.
 * The trade-off between interpretability and performance is a constant tension which we should always retain in our minds when performing our system design.
----
### The Data Challenge:
* What we need is cheap high-quality data. 
* “The Data Crisis” : Data access is cheap, but data quality is often poor. This could be due to , the lack of attention paid to data, high cost and data cleaning is perceived as tedious. Also data cleaning is highly complex ; it requires a deep understanding of how machine learning systems operate and good intuitions about the data it self.As a consequence, data cleaning seems difficult to formulate into a readily teachable set of principles.
		
#### Why?:
* It is difficult to overstate the importance of data. It is half of the equation for machine learning but is often utterly neglected.
		
#### How?:
* We need to develop processes(that are efficient) for improving and verifying data quality.
* To improve efficiency of processes, Firstly, we should not duplicate work. Secondly, where possible we should automate work.
* Value of data cleaning should be correctly recognised in management decision making processes to avoid duplication of work.
* Automation of work is increasingly possible through techniques in "AI". Ex: AIDA project
* Three principal changes need to occur in response:
  1. The Data First Paradigm : we need to move from a software first paradigm to a data first paradigm.  
  This first change is a cultural change in which our teams think about their outputs in terms of data.  
  Software and its quality standards must be maintained, but not at the expense of the data we are producing.  
  Data cleaning and maintenance need to be prized as highly as software debugging and maintenance.  
  Instead of decomposing our systems around the software components, we need to decompose them around the data generating and consuming components.  
  Instead of software as a service, we should refocus around data as a service.  
  Move from software orientated architecture to a data orientated architecture.  
  1. We need to improve our language around data quality.
  1. Thirdly, we need to improve our mental model of the separation of data science from applied science.
  Avoid thinking that data science as a sub-set of the software engineer’s or applied scientist’s skill set.
  Need to recruit and deploy the correct type of resources.
----
### The Deployment Challenge:
Need continuous monitoring systems to ensure their existing functionality has not been broken as the world evolves around them
		
#### Why?:
* As we move forward the conditions under which we trained our model will be changed. We need to ensure the assumptions of design have not been invalidated.
* When we are consuming data from others, we cannot assume that it has been produced in alignment with our goals for our own systems.
			
#### How?:
* We need to establish best practice around model deployment.
* We need to shift our culture from software as a service to data as a service.
* Create 'hypervisor' systems that understand the context in which models are deployed and recognize when circumstance has changed and models need retraining or restructuring.
* Consider a major re-architecting of systems around our services.
* Should scope the use of a streaming architecture (such as Apache Kafka) that ensures data persistence and enables asynchronous operation of our systems. This would enable the provision of QC streams, and real time dash boards as well as hypervisors.
