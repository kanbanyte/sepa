<link rel="stylesheet" href="../styles/styles.css" type="text/css">

> *[This template can be adapted as necessary (i.e., with good reason) to suit the project specifics.]*

<!-- TOC ignore:true -->
# Robot Vision System For A Pick And Place Task
<!--
	Co-Author: @dau501
	Editor(s):
	Year: 2023
-->

`System Architecture Design and Research Report`

<!-- TOC ignore:true -->
## Industry Project 24
List of your Names:

|Name|Position|Email|
|:-|:-|:-|
|@Slothman1|Team Leader/Client Liaison|id@swin.student.edu.au|
|@dau501|Development Manager/Planning Manager|id@swin.student.edu.au|
|@finnmcgearey|Support Manager/Developer|id@swin.student.edu.au|
|@vkach|Quality Manager/Developer|id@swin.student.edu.au|
|@NickMcK14|Support Manager/Developer|id@swin.student.edu.au|
|@Huy-GV|Quality Manager/Developer|id@swin.student.edu.au|

<!-- SUBJECT CODE, NAME, SEMESTER AND DATE -->

```gherkin
@Note:
Please read carefully.
Throughout this document, all text in RED ITALICS should be replaced with data relevant to your project.
Delete all the explanatory text in RED, including this box before submission.
```

<div class="page"/><!-- page break -->

# DOCUMENT SIGN OFF
|Name|Position|Signature|Date|
|:-|:-|:-|:-|
|@Slothman1|Team Leader/Client Liaison|student_signature(&emsp;)|DD/MM/2023|
|@dau501|Development Manager/Planning Manager|student_signature(&emsp;)|DD/MM/2023|
|@finnmcgearey|Support Manager/Developer|student_signature(&emsp;)|DD/MM/2023|
|@vkach|Quality Manager/Developer|student_signature(&emsp;)|DD/MM/2023|
|@NickMcK14|Support Manager/Developer|student_signature(&emsp;)|DD/MM/2023|
|@Huy-GV|Quality Manager/Developer|student_signature(&emsp;)|DD/MM/2023|

> *[When document is finalised for submission, all team members must affix their signature in the Document Sign Off table]*\
> ***[No-one should sign unless they have read the report and agree with it.]***

# CLIENT SIGN OFF
|Name|Position|Signature|Date|
|:-|:-|:-|:-|
|@FelipMarti|Research Fellow|<br/>|&emsp;/&emsp;/2023|

|Organisation|
|:-|
|Swinburne's Factory of the Future<br/><br/><br/><br/>|

> *[Client to sign off on the Software Design to signify they agree with the design]*

<div class="page"/><!-- page break -->

# Introduction
> *[In this opening, briefly*
> * *Discuss the **software/system** that will be developed;*
> * *Define the purpose of this **Software Design and Research Report** and identify its target reader or audience.]*

## Overview
> *[Provide an overview (or executive summary) of this document]*

## Definitions, Acronyms and Abbreviations
> *[Provide the definition of all terms, acronyms, and abbreviations used in this document.]*

# Problem Analysis
> *[This section provides a high-level analysis of the SRS of the target software system from the viewpoint of developing a design solution for it.]*

## System Goals and Objectives
> *[Summarise the high-level system goals and objectives, and refer to the SRS document.]*

## Assumptions
> *[List and discuss the assumptions you have made in developing the system design (as presented in this document).]*

## Simplifications (if any)
> *[List and discuss the simplifications that have been made in developing the system design.]*

<div class="page"/><!-- page break -->

# High-Level System Architecture and Alternatives
> *[Describe, using appropriate models and notations, the chosen **high-level** architecture of the software system that will be developed.*\
> *Also discuss two additional architecture alternatives that have been explored but not chosen.*\
> *This is a refinement of the high-level architecture discussed in the SRS.]*
>
> *Note that this section is about the high-level architecture design (rather than a lower-level detailed design in the next section).*

## System Architecture
> *[Present the system architecture in this section.*\
> *A Component-and-Connector view and a Deployment Allocation view (or some alternatives of similar nature) with the necessary descriptions and*
> *justifications are expected as the minimum.]*

## Other Alternative Architectures Explored
> *[Present and discuss two additional architecture alternatives that have been explored and*
> *provide the rationale as to why they are considered inferior to the chosen architecture.]*

<div class="page"/><!-- page break -->

# Research and Investigations
HeeHooVision conducted several research efforts to ensure the success of the project.\
These research efforts were classified into three categories:
1. Understanding The System's Business/Application Domain.
2. Exploring Similar Existing Systems.
3. Researching Technological Platforms and Programming Languages.

### Understanding The System's Business/Application Domain
HeeHooVision conducted research on the pick and place task, the FOF, and the robotics industry.\
This research aimed to provide insights into the problem at hand and the requirements for the solution.
HeeHooVision also looked into the client's needs and expectations to ensure the solution aligned with their goals.

### Exploring Similar Existing Systems
HeeHooVision conducted a thorough review of current technologies related to providing robots with vision systems to pick and place tasks.\
This research aimed to identify potential solutions and best practices that could be adopted or adapted for this project.
HeeHooVision also explored existing robotic vision systems and analysed their architecture and implementation to inform the design of the proposed system.

### Researching Technological Platforms and Programming Languages
HeeHooVision explored various software development methodologies and frameworks to find the best fit for the project.\
This research aimed to ensure that the system would be compatible with the required platforms and
that HeeHooVision had the necessary skills and resources to implement the system successfully.
HeeHooVision also researched the required hardware and software tools,
such as the Universal Robots UR5e robotic arm, ZED 2 Depth Camera, ROS2, C/C++, Python, OpenCV, and PyTorch.

### Additional Investigations and Research Efforts
HeeHooVision further covered many topics to assist with achieving the project, the topics involve other conducted research on:
* OpenCV to understand its capabilities and how it could be used for image processing in the project.
* Data collection, tagging, and organisation to ensure that the collected data was usable and accurate.
* ROS2 to understand its capabilities and how it could be used for robot programming.
* Python and C++ coding principles and best practices to ensure that the code was clean, efficient, and maintainable.
* Potential mounting options for the sensors to ensure that they were positioned correctly for accurate data collection.

HeeHooVision also conducted research into GitHub to ensure that the project was well-organised and easily accessible to team members.\
They explored different organisational strategies and established guidelines for version control and collaboration to ensure that the project ran smoothly.

## Research into Application Domain
> *[Research into the application domain goes here.]*

## Research into System Design
> *[Research into the system design goes here.]*

## Research into Technical Platforms, Languages and Tools
> *[Research into the technical platforms, programming languages and tools goes here.]*

## Other Research
> *[Research into other aspects  of the project/system goes here.]*

<div class="page"/><!-- page break -->

# References
> *[If you have used information from published sources, show where it came from here (and cite them in the relevant places of this report).*\
> *Use the Harvard system of citation (or another system, but be consistent).*\
> *For instance, they may be books, journal articles, or websites.]*

> ***[Your reference list entry must be in the form of***\
> &emsp; **Author, Initial(s) Year, *Title of Document/Webpage/Website*, Organisation/Host, viewed Day Month Year, &lt;URL>.**
>
> &emsp; example
>
> &emsp; Yates, J 2009, Tax expenditures and housing, Australian Housing and Urban Research Institute, viewed 12 November 2013,\
> &emsp; <http://www.ahuri.edu.au/publications/download/ahuri_judith_yates_research_paper>.]
>
> ***[Your in-text may be in the form of***
> * **Direct quote**\
> "Most official estimates ..." (Yates 2009).
> * **Paraphrase**\
> Yates (2009) looked at the equity implications of tax ...]
>
> ***[For more information on the Harvard style guide, refer to***\
> &emsp; <http://www.swinburne.edu.au/lib/studyhelp/harvard_style.html>]
