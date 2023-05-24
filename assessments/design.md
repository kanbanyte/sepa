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
The following sequence diagram offers a visual representation of how the proposed system complies with the project requirements by showing the interactions between components and the continuous flow of operations.
It depicts the real-time object detection and communication of object positions which enables autonomous operation and ongoing learning and adaptation.

``` mermaid
sequenceDiagram
    participant G as GUI
    participant D as DepthCamera
    participant N as NeuralNetwork
    participant R as RobotOperatingSoftware
    participant A as RoboticArm

    G->>D: Capture image

    loop Continuous Operation
        D->>N: Image data
        alt Object Detection Successful
            N->>N: Process image data
            N-->>R: Detected object positions
            R->>A: Move arm to object positions
            A->>R: Component retrieval status
            R->>G: Update Status
        else Object Detection Failed
            N-->>G: No object positions
        end
    end
```

### Real-time Object Detection, Processing, and Analysis
The depth camera continuously captures images, and the neural network processes the image data in real-time.
The object positions detected by the neural network are sent to the robot operating software promptly.
This verifies that the system enables real-time object detection, processing, and analysis, ensuring accuracy and speed.

### Object Location Data Communication
The object positions detected by the neural network are communicated from the depth camera to the robot operating software.
The robot operating software then uses this data to control the robotic arm's movements.
This verifies that the system successfully communicates the object location data to the robot operating software, facilitating the pick and place task.

### Continuous Learning and Adaptation
It is not explicitly depicted in the sequence diagram but, the neural network module is designed to continuously learn and adapt to new configurations of the chips in their stands once implemented.
Through training and updating the neural network with new data, it can improve its object recognition and location detection capabilities over time.
This verifies that the system has the potential to continuously learn and adapt to different chip layouts, without the need for user input.

### Autonomous Systems
The sequence diagram shows the continuous operation of the system without the need for human intervention.
The robotic arm moves to the detected object positions automatically based on the commands from the robot operating software.
The system operates independently, minimizing human involvement and fulfilling the requirement of an autonomous system.

<div class="page"/><!-- page break -->

# Implementation
> *[In this part of the report, provide an overview of the state of the system implementation (relative to the SRS, architecture design and detailed design), and*
> *document the key implementation decisions.]*

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
