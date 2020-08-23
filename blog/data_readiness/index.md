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

As a member of an agile software engineering team, once every week I sit for a product backlog grooming session.
Let's assume our backlog items could look like below,
* Epic: Enabling synchronization between multiple referencedata systems.
  * Stroy 1: Skeleton implementation for multiple referencedata systems.
  * Story 2: Connection management for multiple referencedata systems.
  * Story 3: Implementation of FT mechanisms.
  * Story 4: Audit Trail implementation related to multiple referencedata systems.
  *  etc...
			
Most common questions we address in the discussion takes the form of,  
	*"How much effort would it take to complete story 1?." "Ans: about 10 Man days/ 20 story points"*  
	*"What is the confidence level of this effort estimate?"*  
	*"Work required for Story 4 is not clear enough for us to give an estimate with a 70% confidence level. We might only be able to give a very high-level estimate. We need an analysis task first."*  
	*"Effort for story 2 is too big for us to take into one sprint. We need to break it down."*  
	*"Who can do this task?"*  
	*"Can this task be parallelized by assigning multiple developers?"*  
	*"What is the Definition of Done(DoD) for this work item?"*  
		
Most of the questions above are valid and arises directly or indirectly irrespective of the development methodology(agile, waterfall, etc...) we use.

Let's assume a very high-level task breakdown of an ML project,
Assume we have already decomposed our current system and identified a subprocess that needs to be automated.
* Epic: Automating fraud detection system using Machine Learning.
  * Stroy 1: Bring data to C1 readiness.
  * Stroy 2: Bring data to B1 readiness.
  * Stroy 3: Bring data to A1 readiness.
  * Stroy 4: Modelling building and testing.
  * Stroy 5: Testing in pre-production.
  * Stroy 6: Deployment.
  * etc...

Now assume similar questions mentioned before arising in this discussion. What would make it easier to address those questions?. I suggest following refinements to the data readiness pipeline.

#### What we could do
1. Breaking data readiness bands to sub-bands or work items to enabling smaller goals.  
Already data readiness levels description consists of three bands and possible work items in each band. These work items can be considered as an initial breakdown for a start. However, we would need to check them for completeness.

2. Making smaller goals well defined to enable accurate time estimates and to increase accountability.   
All most all the time estimates are made from a gut feeling. But that requires experience which won't be readily available as data processing is often neglected. Therefore, a clear description of the task and defining what "done" means(Definition of Done) would be really helpful.  

3. Defining what skills would be most suitable at the task level to enabling effective resource allocation and team creation.  

After refinement it could look like,

|  Band | Work item  | Description | Skill Required  |  DoD |
|---|---|---|---|---|
|  C | Item 1  | Description  | Skill Required  | DoD  |
|  C | Investigate privacy, legal or ethical accessability contraints.  | Investigate all privacy, legal or ethical constraints associated with the data set.  | Data ethics/policy advisor  | Documentation on existing contraints, what actions(anonymization, approvals, .. ) needed to alleviate those constrains, etc..  |
|  C | Converting data into usable digital format  | Data could be on printed paper, PDF, or several web pages. This task aims to convert these data to a usable digital format.  | Depends on original and end formats. Eg, if data is extracted via web scrapping or if the convertion is from digital to digital, then programming skills are required. else ...  | List of checks : Conversion, Testing, QA verification, Documentation (original format, converted format, number of data points converted, total data points found, decisions taken, etc.), Documentation review, etc..|
|  C | Item 4  | Description  | Skill Required  | DoD  |
|  B | Item 1  | Description  | Skill Required  | DoD  |
|  B | Item 2  | Description  | Skill Required  | DoD  |
|  B | Item 3  | Description  | Skill Required  | DoD  |
|  B | Item 4  | Description  | Skill Required  | DoD  |
|  A | Item 1  | Description  | Skill Required  | DoD  |
|  A | Item 2  | Description  | Skill Required  | DoD  |
|  A | Item 3  | Description  | Skill Required  | DoD  |
|  A | Item 4  | Description  | Skill Required  | DoD  |

From this point onwards **we might see an opportunity to define sub-bands based on work item ordering and skills required**. Because then those sub-bands makes complete sense when it comes to planning. Also when creating teams, this guides on which combination of skills set is required.
		
Why solving this problem is important?  
* Enabling smaller well-defined goals contributes to higher accuracy in resource planning.
* This can be considered as "brownfield innovation". Therefore, first people will try to incorporate these readiness levels to their existing project management processes. Therefore, compatibility is important to decrease resistance to embrace innovation.
* What would happen if we leave this as it is?. Then each team will define there own fine-grained versions suitable for there specific needs which would make difficulties in collaboration, inefficient resource transfer across teams, etc. 

Things to remember  
* Should be generic enough for all teams to adopt this. For example, some companies shift to agile but practice a slightly modified version that is tailored to be more suitable for their needs and organisational structure. 
* Should be specific enough to build SMART goals around them.

### 2. Continuous adaptation 
Data readiness levels can also be seen as a grouping of work items required in the data preparation process. 
	
C4 -> *work item 1, work item 2, work item 3, work item 4, ..., work item n1* -> C1  
C1 -> Data becomes electronically available -> B4  
B4 -> *work item 1, work item 2, work item 3, work item 4, ..., work item n2* -> B1    
B1 -> Pose a question to the data. -> A4  
A4 -> *work item 1, work item 2, work item 3, work item 4, ..., work item n3* -> A1  
	
As the world changes, there will be new work items(new challenges) added to above work item sets. And some work items might not be needed anymore (ex: with standardized data collection practices, etc..). Hence it is important to update the data readiness pipeline (I would like to call it as a methodology for data processing) as we progress. 
If we could gain a broader consensus across the data science community for data readiness levels, data science community itself can contribute to updating the "Methodology" by using the experience. 

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
