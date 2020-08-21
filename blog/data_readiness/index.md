---
layout: page
title: My take on "Data Readiness Levels" by Professor Neil D. Lawrence
tags: [about, Jekyll, theme, responsive]
modified: 2020-08-16T20:53:07.573882-04:00
comments: true
---

This is my take on "Data Readiness Levels" which is based on this wonderful [paper](https://arxiv.org/abs/1705.02245), [blog post](http://inverseprobability.com/2017/01/12/data-readiness-levels), [talk](http://inverseprobability.com/talks/notes/data-readiness-levels.html) and [webpage](http://data-readiness.org//) by Professor Neil D. Lawrence.


# Data Readiness Levels : An attempt to develop language around data quality.
	
## Background:
* Data-generating collaborators often only have a very basic understanding of the complications of collating, processing and curating data.
* Challenges include: poor data collection practices, missing values, inconvenient storage mechanisms, intellectual property, security and privacy.
* Therefore, preparing data is neccessary before eventual interpretation of data through machine learning or other approaches.
* Preparing data also involves numerous steps. With each step data becomes closer to "Ready for the task". We can think of it as data being carried along the readiness pipeline.

## Why this is done? (The Problem/Purpose of this paper):  
* Project overruns can occur due to failure to account for the amount of time required to curate and collate. Also many failings on large data projects are associated with a failure to provision resources for the challenges involved in preparing our data, rather than a failing in the algorithmics of the system. Therefore, In project reporting, a major challenge is in encapsulating problems and enabling goals to be built around the processing of data.
* Also when preparing data is considered, we need to increase the accountability of the process and allow the nature of the data to be manifest.
	
## What is done? (Proposed Solution/The Idea):
* This papaer contributes to build a common language for assessing the readiness of a particular data set by proposing the use of data readiness levels; It gives a rough outline of three stages of data preparedness. (a way to share the status of a particular data set)
* Speculates on how formalisation of these data readiness levels could facilitate project management.

## How it is done? (The implementaion of the Solution/Idea)
* The initial proposal is that data readiness should be split into three bands. Each band being represented by a letter, A, B and C. These bands reflect stages of data readiness which would each likely have some sub-levels, so the best data would be A1 and the worst data might be C4.
	
	
### Band C : Band C is about the accessibility of a data set.
***Is the data accessible? ; To be used data has to be accessible first.***
* The lowest sub-level of Band C (let’s label it as C4) : We belive that the data may exist, but its existence isn’t even verified yet. We might think of it as hearsay data. Possible problems that needs to be addressed to improve data accessibility.  
  * Whether it really is being recorded
  * The format in which it’s being recorded
  * Are there privacy or legal constraints on the accessibility of the recorded data, have ethical constraints been alleviated?
  * Limitations on access due to topology.  		
* For data to arrive at C1, then it would have all above considerations dealt with.
* C1 data readiness level : Data is ready to be loaded into analysis software, or it can be made available for others to access. It is machine readable and ethical procedures for data handling have been addressed.
* Band C contains data accessibility related challenges : “data munging” or “data wrangling”, ethical and legal challenges to be solved to move it to C1(Accessible Data).
	
### Band B : Band B is about the faithfulness and representation of the data. 
***Is this data valid ? What’s actually there in the data set?; To use a data set effectively experts should know what’s actually there in the data set.***
* Required investigations may include :
  * Is what is recorded matching what is purported to be recorded?
  * How are missing values handled, what is their encoding?
  * What is the noise characterization for sensors?
  * For manual data are there data entry errors?
  * Are any scientific units correctly formulated?
  * Characteristics of the collection process should also be verified,
    * Was data collection randomized?
    * Is it biased in any particular way?
	* If the data has been agglomerated at some point (for example, for privacy) how were missing values dealt with before agglomeration?
  * If the data has been through a spreadsheet software, can you confirm that no common spreadsheet analysis errors were made?
* B1 data readiness level : Expert(s) has carried out an investigation on data and a broad idea of limitations in the data is present in the expert’s mind. Here the analyst begin to have an intuition about what might really be possible with the data set.
* This work in band B is reusable across multiple teams.
	
### Band A : Band A is about data in context
***Is this data set usable in this context?, Can we solve this task/problem with this data set?***
* It is at Band A that we consider the appropriateness of a given data set to answer a particular question or to be subject to a particular analysis. A data set can only be considered in Band A once a task is defined.
* A1 data readiness level : Data has been considered alongside a task and any remedial steps have been taken.
* At A1 it is ready to be deployed in the context given and it can be used to make predictions with the data.
* Work that might be needed : 
  * Annotation of the data by human expert
  * There may be a realisation that new data needs to be actively collected to get the answers required	 
* It is possible for a data set to be A1 for one question but only B1 for a different question.
			 
## What can we do to improve this work?
<To do>
