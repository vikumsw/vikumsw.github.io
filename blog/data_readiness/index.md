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
### 1. Problem 1: 
Now project management team have an idea about the data preparation work required in terms of three levels of data graduation. I see this useful at project milestone level planning (bringing data from C4 to C1 can be thought of as a milestone).  
But when creating teams, managers would also need more clear insight on which combination of skill set is required.
Also in team level planning, can the development team create tasks that fit their development methodology and allocate time and resource persons to tackle the tasks effectively?.
The product management team should be able to track the progress via well defined smaller goals/work items. These smaller goals/work items enable effective resource allocation: We should be able to estimate time/efforts with adequate confidence levels and allocate people with required skills to those tasks.
This might not be easy as the work in a band seems too broad for a single work item and might require different skill sets.  
To elaborate this more lets first consider below project planning scenario from a software engineering context,

### 2. Continuous adaptation 
### 3. Standardize documentation for work items done in each band.
Assume a scenario that we have to build a machine learning application and we are also aware that the required data set is available off the shelf in B1 readiness level. We have to be extra careful at Band A investigations because decisions on data preparation taken outside the context of the application (band C, band B) have dangerous downstream consequences.
Therefore with the dataset, I would also like to receive two reports.
1. **C1 Report:** This report contains all the documentation done in Band C work.  
2. **B1 Report:** This report contains all the documentation done in Band B work.   

If done correctly, experts might be able to do most work in band A, only with C1 & B1 reports. Only the POC will require opening the data set.
However, this will be most effective only if the documentation in the bands B and C are done according to a common simple standard.
	
* How to come up with a standard?: *It's difficult to come up with best practices by simulating the process mentally without much experience. If I have to come up with a standard, I  would start with a C4 data set, will bring it to A1 while creating a list of best practices and defining a standard with the feedback of different stakeholders. Few iterations of the whole process might be needed with different data sets until we got a standard with adequate quality. (An easier and quicker way could be arranging a meeting series with experts to get it done using their experience).*

### Other Thoughts...
* For all of this to work, we should ensure we get broader consensus across data sciences. What can we do to make the idea spread faster among decision-makers and practitioners?
  * **Courses on data processing which speak the proposed data readiness language:** The author also mentions that processes involved in Grade C and B are often badly taught in courses on data science. I see this as a gap which can be converted to an opportunity. *What if we offer courses on data processing which speak the proposed data readiness language to fill this gap?*. This way the idea of data readiness levels can be spread first to practitioners and then to managers through practitioners. However, this idea is based on the assumption that there would be considerable demand for a free course on data processing (which can be assessed by market research).		
  * **Promoting shift to Data-Oriented Architectures** which will demand huge attention to the quality of the data would also increase the need for a language around data quality.
* A language around a process enables helps to identify possible improvements by enabling analysis in much greater depth. As a result, this could lead to the rise of more roles specialized for certain work items in data readiness pipeline. (Eg: There was no scrum master role before agile.)

#### Terminology
* Epic: Collection of stories.
* Story: A development task involved in adding functionality to a system.
* backlog: Place holder for the work items that need to be done.
* sprint: A short, time-boxed period when a team works to complete a set amount of work.
