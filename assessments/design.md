<link rel="stylesheet" href="../styles/styles.css" type="text/css">

> *[This template can be adapted as necessary (i.e., with good reason) to suit the project specifics.]*

<!-- TOC ignore:true -->
# Robot Vision System For A Pick And Place Task
<!--
	Co-Author: @dau501
	Editor(s):
	Year: 2023
-->

`Detailed System Design and Implementation Report`

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

<div class="page"/><!-- page break -->

# Introduction
> *[In this opening, briefly*
> * *Discuss the **software/system** that will be developed;*
> * *Define the purpose of this **Detailed Design and Implementation Report** and identify its target reader or audience.]*

## Overview
> *[Provide an overview (or executive summary) of this document]*

## Definitions, Acronyms and Abbreviations
> *[Provide the definition of all terms, acronyms, and abbreviations used in this document.]*

## Assumptions and Simplifications
> *[List and discuss the assumptions and simplifications you have made in developing the detailed system design (as presented in this document).]*

<div class="page"/><!-- page break -->

# System Architecture Overview
> *[Provide a high-level overview of the system architecture as defined in the System Architecture Design and Research Report.*\
> *This is to provide a context for the discussions in the remainder of this document.]*

# Detailed System Design: Using OO or Alternative
> *[Develop and present a detailed design, following a specific approach (e.g., responsibility-driven object-oriented design).*
>
> *Note that an alternative design approach to OO can also be used (instead),*
> *but a justification needs to be provided as to why the chosen approach is more suitable to the target system.*\
> *In any case, the design, its justification and verification need to be presented.*
>
> *Also note that depending on the SDLC chosen (eg, agile development), this part of the detailed design may be developed in a number of stages of the project;*
> *but, they need to be considered before the implementation of the relevant part of the system.]*

## The Detailed Design and Justification
> *[For example, if using OO design, the design should include one or more class diagrams and possibly other UML diagrams,*
> *the necessary description and justifications of them (including design patterns and heuristics used if any).*
>
> *An alternative approach can also be adopted, In any case, the design decisions need to be justified.]*

## Design Verification
> *[Present and discuss the verification of your design in this section.*\
> *A usual approach for design verification is to demonstrate that the use scenarios (from the SRS) can be supported by your design.*\
> *Well accepted alternative approaches can also be used instead.]*

<div class="page"/><!-- page break -->

# Implementation
Due to the project requiring the group to learn an entirely new set of skills,
the start of the project has exclusively involved completing background research in the relevant fields.
This includes research into ROS2, Machine Learning, and Computer Vision.

## ROS2
ROS 2 consists of multiple software libraries for developing robotics software.
It allows for structuring the different components of the robot system into a graph containing nodes, topics, services, and actions.
Commands can be used within a terminal to control different aspects of ROS and it supports programming in C++ and Python.

### Nodes and Topics
Nodes represent a single, modular purpose.
For example; publishing information from a camera, moving grasping claw, moving arm motors, rotating claw, etc.
Nodes have parameters that can be set or changed via CLI or in code.

Topics are used to connect nodes. Nodes can subscribe to topics and receive data or publish to them by sending data.
For example a vision camera publishes object positions to a topic, relevant nodes subscribe to receive the position data and
then use it to move the arm to that position

### Services
Services are another way to connect nodes.
A client node can send a request message containing some data to a server node.
The server node then sends a response message containing some data back to the client node.
Services can be used to confirm data is correct or for other nodes to modify data for the client node to use.

### Actions
Actions are a way to connect nodes to allow for the robot to perform an action.
Actions can be cancelled unlike topics and services and they consist of three parts:
1. Goal service
	* Client sends the goal required
	* Server sends acknowledgment
2. Result service
	* Client sends request for result
	* Server sends feedback until goal is reached
	* Server sends result
3. Feedback topic
	* Server sends gradually changing data
	* Feedback stops once goal is reached

### Bags
Bags are used for recording and playing back data published to topics.
Once data is recorded in a bag, it can be used to perform actions again in the exact same way which is useful for debugging and troubleshooting.

### Proposed Implementation
Each distinct part of the robot system that moves will need to be represented as a node.
This includes but is not limited to the grasping claw, robot arm motors, vision camera and nodes for performing actions or invoking services.
Any movements or tasks will be performed via an action, this will include;
closing grasping claw, picking up distinct objects, placing objects, resetting position, etc.
Simulations will be used to test tasks before running them on the physical robot and to allow for better development remotely.

### Integration
All code written to control the robot will use ROS 2 libraries.
Code created in C++ and Python will use the rclcpp and rclpy libraries respectively.
The modularity of ROS allows for much easier integration with the object detection software that will be created.
Nodes related to the vision camera can utilise the object detection program to allow the robot to move to the correct positions and
perform actions efficiently and accurately.

## Machine Learning
When tackling ML, a key pillar is the training of models, which of course requires data.

### Structured Data
* Typically quantitative data.
* Highly organised and easily decipherable.
* SQL can and usually is used to manage structured data.

Examples:\
Dates, names, addresses, credit card numbers.

### Unstructured Data
* Typically qualitative data.
* Needs special tools to be processed and analysed.
* Best stored in non-relational databases.

### Semi-Structured Data
* A bridge between the two.
* Has metadata to have better organisation.

The project will use either semi-structured or unstructured as they support images.

### ML Methods
* Supervised
* Unsupervised
* Semi-Supervised

## Computer Vision
The perception system will be able to identify objects and their locations with a great deal of accuracy thanks to the Depth Cameras use of binocular vision,
which works similarly to human eyes depth perception.
Its 120-degree field of view and depth range of 0.2 to 20 metres give it a large detection area and enables better tracking of object positions.

The Depth Camera can record video at a variety of frame rates and resolutions,
including 2.2K at 15 fps, 1080p at 30 fps or 15 fps, and 720p at 60, 30 or 15 fps.
Higher frame rates would enable better position tracking, while higher resolutions would improve object detection.

With this in mind he project will require a system that is composed of the following items:

### Input Data Validator
The Depth Camera will likely output complex and possibly unprocessable visual data.
Data must be passed to this sub-component to check for proper formatting in order to maintain high accuracy.

### Perception Data Logger
The perception system must keep track of metadata pertaining to the data it retrieved, its results, confidence level, and other attributes.
This information is helpful for telemetry, bug fixing, and training computer vision models.

### Computer Vision Network
This is the central component of the image processing system, which uses validated input data to identify the presence of components that need to be assembled.
The machine-learning network that has been trained to find objects at their designated locations is represented by this sub-component.

### Position Data Formatter
The Computer Vision Network's raw output is not accessible to other components because it is improbable that they will find it useful.
Only boolean data indicating an item's presence or absence should be included in the data prediction model's output.
The robot's motion control is then updated with the position data.

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
