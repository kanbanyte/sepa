<link rel="stylesheet" href="../styles/styles.css" type="text/css">

<!-- TOC ignore:true -->
# Robot Vision System For A Pick And Place Task
<!--
	Co-Author: @dau501
	Editor(s):
	Year: 2023
-->

`Project Plan`

<!-- TOC ignore:true -->
## Industry Project 24
List of your Names:

|Name|Position|Email|Phone|
|:-|:-|:-|:-|
|@Slothman1|Team Leader/Client Liaison|id@swin.student.edu.au|1300 655 506|
|@vkach|Quality Manager/Developer|id@swin.student.edu.au|04xx xxx xxx|
|@dau501|Development Manager/Planning Manager|id@swin.student.edu.au|04xx xxx xxx|
|@finnmcgearey|Support Manager/Developer|id@swin.student.edu.au|04xx xxx xxx|
|@NickMcK14|Quality Manager/Developer|id@swin.student.edu.au|04xx xxx xxx|
|@Huy-GV|Quality Manager/Developer|id@swin.student.edu.au|04xx xxx xxx|

<!-- SUBJECT CODE, NAME, SEMESTER AND DATE -->

```gherkin
@Note:
Please read carefully.
Throughout this document, all text in RED ITALICS should be replaced with data relevant to your project.
Delete all the explanatory text in RED, including this box before submission.
```

<div class="page"/><!-- page break -->

# DOCUMENT CHANGE CONTROL
|Version|Date|Authors|Summary of Changes|
|:-|:-|:-|:-|
|||||
|||||
|||||
|||||
|||||
|||||
|||||
|||||
|||||
|||||

> *[Each time this document is revised, complete details of changes in Document Change Control table]*

# DOCUMENT SIGN OFF
|Name|Position|Signature|Date|
|:-|:-|:-|:-|
|@Slothman1|Lead|||
|@vkach|-|||
|@dau501|-|||
|@finnmcgearey|-|||
|@NickMcK14|-|||
|@Huy-GV|-|||

> *[When document is finalised for submission, all team members must affix their signature in the Document Sign Off table]*\
> ***[No-one should sign unless they have read the report and agree with it.]***

# CLIENT SIGN OFF
|Name|Position|Signature|Date|
|:-|:-|:-|:-|
|-|-|-|-|

|Organisation|
|:-|
||

> *[Client to sign off on the Project Plan to signify they agree with the plan]*

<div class="page"/><!-- page break -->

# CONTENTS
<!-- TOC -->

* [DOCUMENT CHANGE CONTROL](#document-change-control)
* [DOCUMENT SIGN OFF](#document-sign-off)
* [CLIENT SIGN OFF](#client-sign-off)
* [CONTENTS](#contents)
* [INTRODUCTION](#introduction)
    * [BACKGROUND](#background)
    * [KEY PROJECT PERSONNEL](#key-project-personnel)
        * [CLIENT](#client)
        * [OTHER STAKE HOLDERS](#other-stake-holders)
        * [PROJECT SUPERVISOR, TEAM LEADER AND KEY PROJECT MEMBERS](#project-supervisor-team-leader-and-key-project-members)
* [TERMS OF REFERENCE](#terms-of-reference)
    * [OBJECTIVES](#objectives)
    * [SCOPE](#scope)
    * [CRITICAL SUCCESS FACTORS](#critical-success-factors)
    * [ACCEPTANCE CRITERIA](#acceptance-criteria)
* [ESTABLISHMENT](#establishment)
    * [PROCESSES, PROCEDURES AND STANDARDS](#processes-procedures-and-standards)
    * [PROJECT ENVIRONMENT](#project-environment)
    * [PROJECT TEAM SKILL DEVELOPMENT REQUIREMENTS](#project-team-skill-development-requirements)
* [DELIVERABLES, ACTIVITIES AND CAPITAL RESOURCES](#deliverables-activities-and-capital-resources)
    * [DELIVERABLES](#deliverables)
    * [ACTIVITIES](#activities)
    * [RESOURCES](#resources)
* [ORGANISATION AND STRUCTURE](#organisation-and-structure)
* [RISKS](#risks)
* [SCHEDULE](#schedule)
    * [PROJECT TIME LINE](#project-time-line)
    * [EXTERNAL DEPENDENCIES](#external-dependencies)
    * [ASSUMPTIONS](#assumptions)
* [BUDGET](#budget)
* [REFERENCES](#references)
* [TABLES INDEX](#tables-index)

<!-- /TOC -->

<div class="page"/><!-- page break -->

# INTRODUCTION
This document is designed to serve as a guide to use in relation to the proposed plans and ideas for the project. 
This document is deigned to be easily accessible to the client to see the intentions with the project. 
This document will assist in defining future documents as this outlines expectations, proposed ideas and a rough plan for the project.

## BACKGROUND
The factory of the future focuses on developing technologies, 
the latest being a chip assembling robot which is in need of a vision system. 
The required pick and place tasks are currently unable to be completed in less than ideal conditions as well the system is far from autonomous. 
The factory of the future wants this project to be completed to 
both show how emerging technologies can be used to automate tasks as well as how robots can be incorporated into regular workflows.

## KEY PROJECT PERSONNEL
The key personnel involve in this project are as follows:

### CLIENT
@FelipMarti is a research fellow within the Factory of the Future. 
With a background in IoT he is now working with intelligent robots and computer vision systems.

### OTHER STAKE HOLDERS
S.W: a fellow worker in the factory of the future, responsible for a good degree of robot demonstrations.\
Swinburne clients: potential investors or researchers interested in the technology and wish to view it in progress.\
Swinburne developers: People responsible for the maintaining of the system. 

### PROJECT SUPERVISOR, TEAM LEADER AND KEY PROJECT MEMBERS
@Slothman1: Team leader and client liaison\
@vkach: Quality manager and developer\
@dau501: Development manager and planning manager\
@finnmcgearey: Support manager and developer\
@Huy-GV: Quality manager and developer\
@NickMcK14: Support manager and developer

D.R.: Project supervisor

<div class="page"/><!-- page break -->

# TERMS OF REFERENCE
The goal of this project is to be able to provide computer vision to a UR5 robot arm,
while using machine learning techniques to allow the robot to assess the situation and act accordingly.

## OBJECTIVES
The objectives of this project are to design and implement a vision system for a pick and place task using a robot located within the Factory of the Future.
To achieve this, the following must be achieved:
* Develop a vision system that will enable the robot to locate objects to pick and place, even if they are not in the predefined position.
* The vision system should be able to detect objects accurately and efficiently, and provide the necessary information to the robot's control system.
* The vision system should also be able to detect if objects are missing/out of place and pause until given a command that it is safe to continue.

## SCOPE
The scope of this project includes the development of a vision system that is compatible with the robot's hardware and software.

The vision system should be able to detect objects:
* in a variety of lighting conditions and at various distances from the robot.
* that are partially occluded or have complex shapes.

Future work may arise depending on the schedule and progress of the scoped out project.
One example of this, is ensuring the robot is able to pick up a fallen over/out of place object.

## CRITICAL SUCCESS FACTORS
The critical success factors for this project include:
* Developing a vision system that is accurate, efficient, and reliable.
* Ensuring that the vision system:
	* is compatible with the robot's hardware and software.
	* can detect objects in a variety of lighting conditions and at various distances from the robot.
	* can detect objects that are partially occluded or have complex shapes.

## ACCEPTANCE CRITERIA
The acceptance criteria for this project include:
* Successful implementation and testing of the vision system.
* The vision system should be integrated with the robot's control system and enable the robot to perform pick and place tasks with increased efficiency and accuracy.
* The system should be able to detect:
	* objects accurately and efficiently.
	* objects in a variety of lighting conditions and at various distances from the robot.
	* objects that are partially occluded or have complex shapes.
	* if objects are out of place or missing and halt the task until told to continue.

<div class="page"/><!-- page break -->

# ESTABLISHMENT
## PROCESSES, PROCEDURES AND STANDARDS
The project team will follow the Kanban methodology for this project as it is a system that easily allows us to monitor our current tasks and
allows for a more independent work style, thus increasing overall productivity.

The Kanban board will have 8 columns: `New`, `Reopened`, `Requested`, `Fix`, `Deploy`, `Merged`, `Closed`, and `Dropped`,
which will be automated by GitHub's (classic) Projects automation features.
The board will serve as the primary source of information for the team's progress,
with each task being represented by a card that will move across the board's columns as it progresses through the project's workflow.

The team will utilize GitHub as the source control system for this project.
All code changes will be submitted via pull requests, and
a team member other than the author will be responsible for reviewing the changes before they are merged into the `main` branch.

All code produced must follow good programming practice, in particular code must follow consistent conventions of naming variables, functions, classes, etc.
(for example camelCase or snake_case).
Clear, concise comments will also be included to help with readability and comprehensibility.

## PROJECT ENVIRONMENT
The project will require the use of various programming lanugages, frameworks, modules, and development environments to be successfully completed.
The following tools and technologies will be utilised throughout the project:
* C/C++
* Python
* OpenCV
* PyTorch
* Robot Operating System (ROS2)
* Markdown & CSS
* Ubuntu Linux OS
* Potential IDEs:
	* Visual Studio
	* Visual Studio Code
	* VIM
	* PyCharm

## PROJECT TEAM SKILL DEVELOPMENT REQUIREMENTS
The project will require knowledge in multiple fields of study to successful deliver the final product;
the team will be required to have expertise in the following areas:
* Computer Vision
* Sensors
* Robotics
	* Completed the tutorials for ROS
* AI
* Software Programming
	* Python (Particularly OpenCV & PyTorch)
	* C/C++

The team members will be encouraged to attend relevant training sessions and conferences to develop their skills in these areas.
Online tutorials will be helpful references and sources for honing programming capabilities.

<div class="page"/><!-- page break -->

# DELIVERABLES, ACTIVITIES AND CAPITAL RESOURCES
## DELIVERABLES
### Software systems
* Functioning computer vision system satisfying all requirements within scope.
* Functioning robotic control system satisfying all requirements within scope.

### Documentation
* Documents outlining design choices as specified in [System Documentation](#system-documentation).
* Documents detailing test plans as specified in [Testing](#testing).
    * Include simulation test plans and results.
    * Include integration tests and results.

### Hardware modifications
* Tool that mounts the depth camera such that all items of interest are within clear view.

## ACTIVITIES
### Research:
* Learn to use Robot OS within Ubuntu.
* Study concepts of machine learning, with a focus on computer vision. 
* Research ways to build an AI model based on project needs.

### Design and implementation:
* Model the problem into the software system.
* Train the machine learning model in simulation.

### Deployment:
* Deploy the machine learning model in production.
* Deploy the robotic control software into the robot arm.

### Testing:
* Test the computer vision system in simulation using a collection of photographs taken in various conditions.
* Test the robotic control system in simulation, covering all identified edge cases.
* Integration test on the robot arm with the control and computer system installed, covering all edge cases as identified in prior simulation tests.

### System Documentation:
* User flow documentation: robot behaviors given an input, including explanation for special cases.
* Software architecture documentation: software models, their relationship and interactions. 
* Design decision documentation: explanation for software tool/framework and various design choices.

## RESOURCES
> *[List and describe specific resources needed in order to complete the project]*
>
> *[Resources are things you need to do the project which may be provided by your client or university.*\
> *For example, equipment, room, software library]*

<div class="page"/><!-- page break -->

# ORGANISATION AND STRUCTURE
> *[List all the groups of people that will be involve or has a role in the project,*
> *Be sure to include every role (especially business users who will be interviewed during the requirements modelling and those involved in acceptance testing)]*
>
> *[This is not just your team.*\
> *It is anyone else who has direct interaction with the project.*\
> *This also includes people will be interacting with the software;*\
> *(e.g., people who test it or are interviewed about it, and other members of their organisation)]*
>
> *[Describe the organisational structure that will be used during the project.*\
> *For example, a matrix structure may be used in describing role of each group.*\
> *This enables the person responsible for the activity or deliverable to see the groups of people to me managed]*

#### Activities and Deliverables
<!-- This table is confusing and likely subject to change. -->
|Activities and Deliverables|Group involved as identified above|
|:-|:-|
|**From 4.2**||
|**From 4.1**||

**Table 1 Activities and Deliverables**

<div class="page"/><!-- page break -->

# RISKS
> *[Discuss any major risks that could affect your project plan]*
>
> *[This is not a full risk analysis but more of a look at the risks that affect the running of the project]*
>
> *[Take this seriously.*\
> *When things start to go wrong, you will be expected to follow the strategies outlined here.*\
> *Explain mitigation strategies in detail.*\
> *Number each strategy and place the number in the table above]*
>
> *[For each Risk record the following*
> * *Rank*
> * *Name*
> * *Description*
> * *Likelihood of occurrence*
> * *Severity*
> * *Strategy for mitigation (prevention)*
> * *Contingency or fall-back position should the risk manifest itself.*\
> *(plan B) - not an elaboration of the mitigation strategy]*

#### Risks Associated With This Project
|Rank|Name/Description|Occurrence Probability<br/>(H/M/L)|Severity<br/>(H/M/L)|Mitigation Strategy Number|Contingency|
|:-|:-|:-:|:-:|:-|:-|
|||||||
|||||||
|||||||
|||||||
|||||||
|||||||

**Table 2 Risks**

<div class="page"/><!-- page break -->

# SCHEDULE
## PROJECT TIME LINE
> *[Given the tasks (group as activities) in Section 4.2, schedule each tasks using a Gantt chart or some other type of time line.*\
> *You do not have to use Microsoft Project.*\
> *Acceptable Gantt charts can be created using Excel or various graphics programs or can be hand-drawn]*
>
> *[For each task, show the deadline, and who is allocated to each task (your team members).*\
> *Often it is better to allocate two people to each task in case one becomes unavailable (e.g., breaks a leg)]*

## EXTERNAL DEPENDENCIES
> *[Describe any inputs from external parties that are required to ensure that the schedule is met.*\
> *These dependencies, if any, must also be indicated in the time line (Section 7.1) as a critical point]*

## ASSUMPTIONS
> *[Describe any assumptions that have been made in arriving at the schedule.*\
> *These may be critical to the implementation of the software]*

<div class="page"/><!-- page break -->

# BUDGET
> *[Summarise in a table the rate per hour for each of the team member.*\
> *Look for an appropriate rate per work when doing such type of project.*\
> *Using the role listed in Section 1.2.3, complete the table below]*

#### Personnel Cost
|Name|Rate per Hour|
|:-|:-:|
|||
|||
|||

**Table 3 Personnel Cost**
> *[List all the tasks (grouped as activities) described in Section 4.2 in a table and estimate the number of hours needed to complete each task]*

#### Time Estimated to Complete Each Task
|Activity|Task|Estimated hours needed (hrs)|Total per activity (hrs)|
|:-:|:-|:-:|:-:|
|1|A|10||
||B|15||
||C|20||
||D|5|50|
|||||
||F|5|10|
|||Total||
|||||

**Table 4 Task Time Estimate**
> *[As a guide in estimating the time consider the following:]*
>
> *[Each team member should contribute equally, and time spent actually writing software should be about*
> *(200 hours x number of team members, ie, about 10 hours per week per member, excluding lectures) across the 2 semesters,*\
> *Total time allocation for each student should not exceed 10 hours per week,*\
> *The total hours per activity should be feasible within the schedule defined in Section 7.1]*
>
> *[Note that the schedule in Section 7.1 includes slack time]*

<div class="page"/><!-- page break -->

# REFERENCES
> *[If you have used information from published sources, show where it came from.*\
> *Use the Harvard system of citation.*\
> *For instance, if it is from a website]*

> ***Your reference list entry must be in the form of***\
> &emsp; **Author, Initial(s) Year, *Title of Document/Webpage/Website*, Organisation/Host, viewed Day Month Year, &lt;URL>.**
>
> &emsp; example
>
> &emsp; Yates, J 2009, Tax expenditures and housing, Australian Housing and Urban Research Institute, viewed 12 November 2013,\
> &emsp; <http://www.ahuri.edu.au/publications/download/ahuri_judith_yates_research_paper>.
>
> ***Your in-text may be in the form of***
> * **Direct quote**\
> "Most official estimates ..." (Yates 2009).
> * **Paraphrase**\
> Yates (2009) looked at the equity implications of tax ...
>
> ***For more information on the Harvard style guide, refer to***\
> &emsp; <http://www.swinburne.edu.au/lib/studyhelp/harvard_style.html>

# TABLES INDEX
Table 1 [Activities and Deliverables](#activities-and-deliverables)\
Table 2 [Risks](#risks-associated-with-this-project)\
Table 3 [Personnel Cost](#personnel-cost)\
Table 4 [Task Time Estimate](#time-estimated-to-complete-each-task)
