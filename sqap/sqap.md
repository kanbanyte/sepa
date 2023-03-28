<link rel="stylesheet" href="../styles/styles.css" type="text/css">

> *[Note: This is a sample/template document for the Software/System Quality Assurance Plan (SQAP), from a number of years ago.*\
> *Please adapt and adjust to your project needs and add details.]*

<!-- TOC ignore:true -->
# Robot Vision System For A Pick And Place Task
<!--
	Co-Author: @dau501
	Editor(s):
	Year: 2023
-->

`System Quality Assurance Plan (SQAP)`

<!-- TOC ignore:true -->
## Industry Project 24
List of your Names:

|Name|Position|Email|Phone|
|:-|:-|:-|:-|
|@Slothman1|Team Leader/Client Liaison|id@swin.student.edu.au|04xx xxx xxx|
|@vkach|Quality Manager/Developer|id@swin.student.edu.au|04xx xxx xxx|
|@dau501|Development Manager/Planning Manager|id@swin.student.edu.au|04xx xxx xxx|
|@finnmcgearey|Support Manager/Developer|id@swin.student.edu.au|04xx xxx xxx|
|@|-|id@swin.student.edu.au|04xx xxx xxx|
|@Huy-GV|Quality Manager/Developer|id@swin.student.edu.au|04xx xxx xxx|

<!-- SUBJECT CODE, NAME, SEMESTER AND DATE -->

<div class="page"/><!-- page break -->

<!-- TOC ignore:true -->
## Review history
|Version|Date|Author|Comments|
|:-|:-|:-|:-|
|1.00||All Authors|Created initial draft document.|
|1.10||All Authors|Updated based on feedback from external reviews.|
|1.20||S. Smith|Updated based on internal review and Supervisor feedback.|
|1.30||S. Smith & T. Le|Updated based on internal review and Supervisor feedback.|
|1.40||All|Final Submission.|

<!-- TOC ignore:true -->
## Acronyms/Abbreviations
**ASAP** &emsp; As Soon as Possible\
**COB** &emsp; Close of Business (5:00 PM)\
**DMO** &emsp; Defence Materiel Organisation\
**DMS** &emsp; Data Management System\
**GUI** &emsp; Graphical User Interface\
**IEEE** &emsp; Institute of Electrical and Electronics Engineers\
**JDK** &emsp; Java Development Kit\
**JRE** &emsp; Java Runtime Environment\
**Ver.** &emsp; Version\
**SQAP** &emsp; SoftwareQuality Assurance Plan \
**SRS** &emsp; SoftwareRequirements Specification \
**SVN** &emsp; Subversion \
**SVVP** &emsp; SoftwareVerification and Validation Plan

<div class="page"/><!-- page break -->

<!-- TOC ignore:true -->
# Contents
<!-- TOC -->

* [Introduction](#introduction)
	* [Author List/Roles](#author-listroles)
	* [Purpose](#purpose)
* [Reference Documents](#reference-documents)
* [Management](#management)
	* [Organisation/Roles](#organisationroles)
		* [Meeting Roles](#meeting-roles)
		* [Formal Review Meeting Roles](#formal-review-meeting-roles)
		* [Champion Roles](#champion-roles)
		* [Communication Roles](#communication-roles)
	* [Tasks and Responsibilities](#tasks-and-responsibilities)
		* [General Team Member Responsibilities](#general-team-member-responsibilities)
		* [Champions](#champions)
* [Documentation](#documentation)
	* [Software Documents](#software-documents)
		* [SQAP](#sqap)
		* [SRS](#srs)
		* [Project Plan](#project-plan)
		* [Module Plan](#module-plan)
		* [Self-assessment reports](#self-assessment-reports)
		* [Audit Report](#audit-report)
	* [Management Documents](#management-documents)
		* [Meeting Agendas](#meeting-agendas)
		* [Meeting Minutes](#meeting-minutes)
* [Standards, practices, conventions and metrics](#standards-practices-conventions-and-metrics)
	* [Purpose](#purpose)
	* [Standards](#standards)
		* [Coding Standard](#coding-standard)
		* [Documentation Formatting Standard](#documentation-formatting-standard)
		* [Filename/Location standards](#filenamelocation-standards)
		* [SVN standards](#svn-standards)
		* [Document Releases](#document-releases)
	* [Practices](#practices)
		* [Communication Practices](#communication-practices)
		* [Meetings](#meetings)
		* [Worklogs](#worklogs)
		* [SVN](#svn)
		* [Coding practices](#coding-practices)
* [Reviews and Audits](#reviews-and-audits)
	* [Purpose](#purpose)
	* [Review/Audit list](#reviewaudit-list)
		* [Reviews](#reviews)
		* [Audits](#audits)
* [Testing](#testing)
	* [Requirement](#requirement)
	* [Use case generation](#use-case-generation)
	* [Installation and User Documentation Generation](#installation-and-user-documentation-generation)
* [Problem reporting and corrective action](#problem-reporting-and-corrective-action)
	* [Personnel](#personnel)
	* [Work](#work)
		* [Project major time line](#project-major-time-line)
		* [Stage-dependent tasks](#stage-dependent-tasks)
		* [Crossed-states tasks](#crossed-states-tasks)
		* [Task creation](#task-creation)
		* [Task assignment](#task-assignment)
		* [Task life](#task-life)
		* [Issue Categories](#issue-categories)
* [Tools and methodologies](#tools-and-methodologies)
	* [Tools](#tools)
		* [LaTeX](#latex)
		* [Issues tracking](#issues-tracking)
		* [SVN](#svn)
		* [Visual Studio](#visual-studio)
		* [Virtual Machine](#virtual-machine)
		* [Skype](#skype)
	* [Agile Methodology: Kanban](#agile-methodology-kanban)
* [Records collection, maintenance and retention](#records-collection-maintenance-and-retention)
* [Risk Management](#risk-management)
	* [Purpose](#purpose)
	* [Categorization](#categorization)
	* [Risks with respect to the work to be done](#risks-with-respect-to-the-work-to-be-done)
	* [Risks with respect to the management](#risks-with-respect-to-the-management)
	* [Risks with respect to the client](#risks-with-respect-to-the-client)

<!-- /TOC -->

<div class="page"/><!-- page break -->

<!-- TOC ignore:true -->
# Chapter 1

# Introduction
## Author List/Roles
|Author|Student ID|Role Semester 1|Role Semester 2|
|:-|:-|:-|:-|
|||Team Leader / Supervisor Liaison|Testing/Usability Champion|
|||SVN / Mantis Champion|Documentation / Quality Champion|
|||Client Liaison|N.A (No longer part of Team)|
|||Usability/Quality Champion|SVN / Mantis Champion|
|||Documentation Champion|Team Leader / Supervisor Liaison|
|||Coding Champion / Sargent At Arms|Coding Champion / Client Liaison|

## Purpose
This document outlines the policies and procedures that members of Team 02 will follow to achieve an overall high standard of quality for Project Eagle,
a Data Management System (DMS) for the Defence Materiel Organisation(DMO).\
All team members are expected to adhere to the processes outlined in this document.

<!-- TOC ignore:true -->
# Chapter 2

# Reference Documents
* Institute of Electrical and Electronics Engineers (IEEE) Std 730-1998, IEEE Standard for Software Quality Assurance Plans
* IEEE Std 830-1998, IEEE Recommended Practice forSoftware Requirements Specifications
* SPINGRID Software Quality Assurance Plan, Version0.1.3 14 June 2006
* OMP Quality Assurance Plan, Version1.1 May15, 2006
* Swinburne Java Coding Standard - SwinBrain
* Swinburne .NET Coding Standard - SwinBrain
* SVN Best Practices: <http://svn.apache.org/repos/asf/subversion/trunk/doc/user/svn-best-practices.html>

<div class="page"/><!-- page break -->

<!-- TOC ignore:true -->
# Chapter 3

# Management
## Organisation/Roles
The following list contains currently identified Roles:

### Meeting Roles
#### Chair
Performed by the Team Leader and is responsible for running/controlling the meeting as well as deter-mining and distributing the agenda for the meeting.\
Apologies and items to be added to the agenda from other team members are to be sent to the Chair prior to meeting.

#### Sargent at Arms
Keeps an eye on proceedings and time spent on each item.\
Responsible for keeping the meeting on topic and on time.\
Their conduct must ensure that team members still have the ability to voice their opinions and ideas.\
Additional time can be utilized for discussion outside of the arranged meeting time.

#### Scribe
Records the meeting minutes and is responsible for circulation of meeting minutes.\
This role will be rotated through team members on a monthly basis as follows: Justin, Ben, Ha, Alex, Jason and Simon.\
The Chair is not expected to take minutes.

<div class="page"/><!-- page break -->

### Formal Review Meeting Roles
#### Moderator
Plans the review and coordinates the review process

#### Scribe
Documents any issues or problems found during the review

#### Inspector
Examines the document/product for defects

#### Author
The creator of the work being reviewed

#### Reader
Reads out documents for the inspectors.

<div class="page"/><!-- page break -->

### Champion Roles
Champion is a role that directly responsible for ensuring the quality of a particular area assigned to them,
as well as the compliance of standards and procedures of their section's of the project.\
They are not however responsible for completing majority of the works.\
They are to delegate work, assist where appropriate and are the single point of contact for issues.

Team Leader is responsible ensuring the team works effectively together to achieve successful completion of the project.\
The Team Leader typically chairs team meetings and is the supervisor liaison.\
They should be notified of any political issues within the team.\
The team leader is also responsible for monitoring the completion of work logs to ensure members are recording time spend, and contributing.\
They are also responsible for writing status reports where applicable and attending team leader meetings.

Documentation Champion in in charge of making sure all documentation is consistent, complete and to a high standard.\
This includes Latex formatting and filenames.

SVN Champion is responsible for ensuring that the repository is used to its full potential and enforcing the SVN standards.\
They are also responsible for maintaining directory structure and resolving any issues with the repository.

Mantis Champion is responsible for maintaining the Mantis bug tracker and ensuring tasks are closed out once completed.\
They should encourage members to complete their allocated tasks.

Usability Champion needs to ensure the product meets usability related non-functional requirements.\
They should understand the Client Requirements and ensure that any products are built with the client use in mind.\
They should assist with testing to ensure the GUIs are usable and intuitive.

The Code Champion is responsible for quality and on schedule delivery of code.\
They are to ensure other members are building and uploading code that compiles and is up to standard.\
They are responsible for ensuring delegated works are completed in a timely manner.

Testing Champion is responsible for running and reporting on test results.\
This includes Unit and functional testing.\
They should work with the Usability Champion to ensure that exceptions and errors are understandable and informative.\
They are to ensure tests carried out by other members are captured and recorded.

### Communication Roles
#### Client
The Client Liaison acts as the single point of contact between the team and the client.\
This allows coordination of all incoming and outgoing correspondence with the client and distribution to all team members.\
They are also responsible for setting up regular Client Meetings

#### Supervisor
The Supervisor Liaison allows the University and Supervisor to have a single point of contact for the team.\
However, other team members may contact the Supervisor for issues themselves.\
The role is typically filled by the Team Leader.

<div class="page"/><!-- page break -->

## Tasks and Responsibilities
### General Team Member Responsibilities
* If a team member is selected for a task they will complete the task by the allocated time.\
If unable to complete task in time, member is to raise an issue prior to deadline with the team leader.
* Meeting Actions are binding unless changed at a later meeting.
* Team members are responsible for the logging of their own time sheets.
* Members are to conduct themselves in an appropriate manner facilitating a healthy work environment.
* Members are required to maintain communication with team.
* Members are required to follow all processes as described in the SQAP.
* Members must make their best effort attend all allocated meetings/workshops and are to submit an apology if they are unable to attend.
* Members are to follow all directives from champions.
* Members are to actively partake in group discussion and provide input to the product and the process.

### Champions
#### Team Leader
* Responsible for the running of weekly team meetings.
* Responsible for the booking of weekly meeting room.
* Responsible for maintaining administrative documentation.
* Responsible for motivating and tracking team progress.
* Responsible for monitoring work logs and time spent on project.
* Responsible for being a point of contact for issues/resolution.
* Responsible for liaising with supervisor

#### Client Liaison
* This champion is directly responsible for all communications with the client.
* Correspondence from team members must be relayed to/from client in a timely manner via client liaison.
* Minor/non-urgent communications are to be collated to avoid bombarding client.
* Any compiled versions that need to be tested will be sent via the liaison.
* Liaison is responsible for ensuring client receives all relevant information for a test,
as well as distribution of the test results supplied by the client to the team (bidirectional communication).

#### Usability and Graphical User Interface (GUI)
* Responsible for ensuring team members take usability into account during development.
* Responsible for ensuring consistency of GUI
* Responsible for ensuring that performance does not negatively impact usability.

#### Documentation
* Responsible for creating and maintaining document templates.
* Maintaining quality and standards of documents.
* Responsible for providing assistance with documentation issues.
* Responsible for maintaining documentation tools.

#### Code
* Responsible for quality control of code artifacts.
* Responsible for tracking code progress
* In charge of organising developer meetings to discuss progress and address any difficulties or concerns.
* In charge of ensuring appropriate workload is assigned for each developer.
* In charge of ensuring standards and best practices are met and followed, respectively, during the development process.

#### SVN
* Creating and maintaining repository.
* Monitoring commit messages.
* Maintaining file structure and location standards.
* Providing assistance with branching and merging.

#### Mantis
* Creating and maintaining Mantis
* Closing out resolved issue
* Monitoring progress of members with issues/tasks

#### Testing
* Completing or delegating running of tests
* Reporting results of tests to team and on SVN
* Building test documents
* Encouraging testing within the team and compile results

<div class="page"/><!-- page break -->

<!-- TOC ignore:true -->
# Chapter 4

# Documentation
## Software Documents
### SQAP
TheSQAP is a plan written before any development that outlines all standard practices and
procedures to ensure a quality process therefore help produce a high quality product.

### SRS
A Software Requirements Specification will be developed to describe the behaviour of the proposed DMS as derived from client requirements.\
The SRS will be based on the IEEE 830 standard, but will be modified to make it appropriate for our project.\
A general outline of the document is as follows:
1. Introduction
	1. Purpose - Outline of the SRS
	2. Scope - What the DMS is, what it will do and its application
	3. Definitions, acronyms, and abbreviations
	4. References
	5. Overview
2. Overall description
	1. Product perspective - How the product works with other tools, i.e., dataflow
	2. Product functions
	3. User characteristics - Who will use the product, what training will they get
	4. Constraints
	5. Assumptions and dependencies
3. Specific requirements

### Project Plan
A document to guide the building of the product.\
It will include a brief description of the project and why it should be built,
what needs to be done to build the software and a timeline for when modules should be complete.

As more modules are mapped and more details are known about each item, the project plan is to be updated.\
It should also contain milestones where applicable and deliverable dates.

### Module Plan
Module plan is to be developed following requirement analysis phase of each iteration of the software life-cycle.

Module plan contains:
* Module scope
* Design solution for module
* Work division
* Timeline of artifacts and testing

### Self-assessment reports
A self-assessment report is to be completed by each team member each as per the unit outline that will provide evidence of work completed and self reflection.\
It will document knowledge and experience that has been gained during the process.

This document should contain the following sections:
* Summary
* Work completed
* Mistakes made
* Knowledge gained
* Evidence

### Audit Report
When ever an audit is carried out a document must be produced that indicates the outcome;
anything that does not follow the processes outlined in this document SQAP, whether the process is followed and corrective actions.

Audits can be carried out internally and externally.

## Management Documents
### Meeting Agendas
* This document will be of Latex type and will be prepared by the Team Leader (Or Meeting Chair)prior to each meeting.
* All team members are expected to contribute to the agenda by requesting topics of their choice be added to the agenda.
* Topics shall be owned by the team member who submitted them, unless otherwise stated.
* Owners shall attend the meeting prepared to introduce and discuss their topic.
* Submissions will be accepted by Close of Business (5:00PM)(COB) the day prior to the meeting.
* The author of the agenda will upload to the SVN by COB the day before the meeting.\
A reminder email will also be sent to the required attendees with a PDF attachment of the agenda.

### Meeting Minutes
* Will be collected at every meeting.
* Must follow the minutes template as outlined on the SVN.
* Will be collected as either a raw .txt file or LaTeX file and then converted to latex format.
* Formatted minutes will be released on the SVN no later than the following day's COB.
* APDF copy of the minute scan also be emailed if requested, however, members are expected to find the minutes on the SVN and complete their actions independently.

<div class="page"/><!-- page break -->

<!-- TOC ignore:true -->
# Chapter 5

# Standards, practices, conventions and metrics
## Purpose
Standards are essential for measuring and thus ensuring software quality.\
This section covers technical, documentation as well as process standards which guide the project's development and management.\
These standards mainly govern the output quality of each project's deliverable: libraries, applications, documents.\
In addition, they also serve as the development guidelines throughout the projects.

This section also includes practices that the development team shall adhere to, and will be assessed against.

These standards and practices are the basis to ensure and measure quality of the project's deliverables.\
The detailed procedure for assessment against the standards and practices can be found in the Reviews and Audits section.

All documentation (including the full SVN repository) will be available for the client a pon completion of the project for any future usage.

## Standards
The following standards will be used as the basis for quality control in this project.\
They shall be adhered to closely throughout the software lifecycle.\
Standards will be reviewed to ensure that they are being met.

### Coding Standard
The following language-specific standards are used
* Swinburne C# and .NET Standard
* Swinburne Java Standards (Spikes only, N/A for final coding as C# is the chosen language.)

<div class="page"/><!-- page break -->

### Documentation Formatting Standard
Where possible, all text documents will be written in LaTeX to ensure they are easily merge-able.
* No non-standard LaTeX package should be used.
* The hyper ref package should be used in all documents; so that all links function correctly.
* The line `\setlength{\parskip}{1}` can be added to the document header to remove paragraph indents, and use vertical space to separate paragraphs instead.
* All documents should use the `fullpage` package so that the margins are a reasonable and consistent size.
* No references should be hard-coded but rather use the `\label-\ref` standard.
* Only the document classes article, report and beamer should be used.
* No customizing of the fonts; everything should be left at the default.
* Tabs should be converted to spaces with a width of 4.
* Indenting of the mark-up should be done to improve readability.
* Figures:
	* All figures need to be in directory called "figures" where the TEX file is located.
	* All figures need to be wrapped in a `\begin{figure}[H]` command and labelled with an appropriate caption under the figure.
		```latex
		\begin{figure}[H]
			\centering
			\includegraphics{imagefile.png}
			\caption{This is the caption}
		\end{figure}
		```
* Tables
	* All tables need to be wrapped in a `\begin{table}[H]`.
	* All tables should be labelled with an appropriate caption under the table.
	* All tables should have borders like in the example below
	* The use of long tables is accepted to allow tables to span multiple pages.
		```latex
		\begin{table}[H]
			\centering
			\begin{tabular}{l|l|l}
				\hline
				col1 & col2 & col3 \\ \hline \hline
				1 & 2 & 3 \\\hline
			\end{tabular}
			\caption{This is the caption}
		\end{table}
		```
* Acronyms should be added to an acronyms table created with the code example below, and used with the `\ac{}` command
	```latex
	\section*{Acronyms}
	\begin{acronym}[TDMA]
		\acro{COB}{Close of Business}
		\acro{IEEE}{Institute of Electrical and Electronics Engineers}
	\end{acronym}
	```
* Presentations should be done using the LaTeX beamer package.\
The Warsaw theme should also be used to ensure visual consistency.

### Filename/Location standards
* All file and folder names will be lowercase.\
With the exception of the code folder where uppercase characters are allowed for the purposes of integrating with MicrosoftVisualStudio's standards.
* There shall be no whitespace (spaces) in filenames.
* " " will be used to delimit the file and folder names in the event that the name is multiple words.
* Management/Administration files will be named as follows "filename yyyymmdd".
* Coding files shall be organised in folders in this structure \trunk\code\eagle\subproject\, \subproject is the programming unit (Java or .NET projects)
* Coding file shall be named inform at of subproject abbr namespace `filename.extension`, where namespace represents the subcomponents of a sub project.
* Management/Administration related files are to kept within the docs folder.
* Multiple related files with similar content such as the meeting minutes are to be stored within an appropriately named encapsulating folder.

#### Document Tree
The following document tree describes the SVN structure.\
Additional folders may be added at the discretion of team members after consulting with the SVN champion.
```brainfuck
repos
	+---trunk
		+---docs
			+---meetings minutes
				\---agendas
			+---presentations
				+---project presentation 1
				\---figures
			+---sqap
				+---figures
				+---references
				\---release
			+---project plan
				+---figures
				\---release
			+---self assessment reports
			+---srs
				+---figures
				+---release
				\---mockup
			+---standards
			\---worklogs
		+---code
			+---eagle
				\---subproject
	+---tags
	\---branches
```

<div class="page"/><!-- page break -->

### SVN standards
* All Commits to the SVN are required to have a corresponding message, which follows the following standard:\
[Mantis Issue ID] file .ext - Sect ion/Module - List of Changes (brief and concise).

In the event that sections are not relevant the fields are still included but left blank.\
i.e., [] file.ext\
--committed the new file
* Ensure files to be committed are not currently open in their respective editors.

#### Branching Standard
This SVN will utilise the Branch-When-Needed system.\
Users commit their day-to-day work on `/trunk`.
1. `/trunk` must compile and pass regression tests at all times.
2. A single commit (change-set) must not be so large so as to discourage peer-review.
3. If rules 1 and 2 come into conflict (i.e., it's impossible to make a series of small commits without disrupting the trunk),
then the user should create a branch and commit a series of smaller change-sets there.\
This allows peer-review without disrupting the stability of `/trunk`.

Pros: `/trunk` is guaranteed to be stable at all times.\
The hassle of branching/merging is somewhat rare.

Cons: Adds a bit of burden to users' daily work: they must compile and test before every commit.

### Document Releases
In the event that a document is released to an outside party; be it submission to the university or the client it must be:
* Converted into a static format such as a pdf
* Appropriately renamed with a revision number
* Moved to a release folder within its current folder

Each release will be named as follows: filename rxxx, where xxx is a number.\
The first release will be 100 and each additional release will be incremented by 10 i.e., filename r100 will be followed by filename r110.

<div class="page"/><!-- page break -->

## Practices
The following practices will be used as the basis for quality control in this project.\
They shall be adhered to closely throughout the software life cycle.\
Practices will be audited to ensure that they are being followed appropriately.

### Communication Practices
#### Client
* All contact will be made to the client through the client liaison champion.
* In the event that the champion is absent or on leave, alternative arrangements will be made (In advance if possible).
* Contact will be primarily made through email.
* Phone calls maybe used in the event that emails cannot provide enough detailed information.
* Meetings with the client shall be regular, taking place approximately every three weeks.\
However correspondence via phone or email should be more regular
* Meetings will always have a minimum of two team members present.

#### Team
* Email will be the primary method of communication, when face to face communication can not be conducted.
* Student email addresses are to be used in all email communications.
* Emailing of documents will not occur if the item can or is held in the SVN with the exception of finalised meeting agendas and meeting minutes in PDF format only.
* Emails need to be checked daily.
* If a request for reply or acknowledgement of email receipt, members are to respond upon reading for the first time.
* Email communication will be kept to a professional standard.
* Emails can be used to confirm verbal contracts.
* Skype meetings are permitted if face-to-face meetings are unable to be arranged, but should be kept to a minimum.

#### Supervisor
* Formal contact with the supervisor will conducted by the Team Leader.
* Supervisor will be present atone meeting per fortnight, at the request of the team leader (typically the Weekly Team Meeting).
* Contact will primarily be through email.
* Agreements with supervisor will be confirmed via email.
* All emails to the supervisor should CC the entire team unless they are of a personal nature.
* If the team meeting is held out of business hours, then a separate meeting should be arranged with the supervisor.\
If this cannot be achieved, then at the very least a status report should be emailed to the supervisor to ensure they remain up to date with the progress.

<div class="page"/><!-- page break -->

### Meetings
* Team meetings will be held on a weekly basis and will have a standard length30to 60minutes.
* All team members are required to be present.
* If a team member can not be present, an apology needs to be communicated directly to the team leader As Soon as Possible (ASAP).
* All meetings require minutes to be taken.
* A meeting outside of the weekly team meeting does not need all members present; notes are required.
* Any meeting with the client requires at least two members present, again notes will be taken.\
Notes will distributed to client for confirmation.
* notes will be stored on the SVN

### Worklogs
* Weekly update of Worklogs on the SVN
* Team Leader to monitor Worklogs.
* Team Leader to monitor and maintain the project hours summary sheet

### SVN
* Temporary/intermediate files are not to be committed

### Coding practices
General guidelines
* Strictly follow C# and .NET standards as outlined in 5.2.1
* Keep the code simple, avoid using unnecessary "clever" code.
* All source files must use the standard header template
* All methods, fields and properties must have comments that follows the official standard in 5.2.1,
inherited class only requires comment if behaviors differ greatly from that outlines by its parent classes
* Public properties are acceptable, however default setters are discouraged, and guards should be used in writing setters.
* Development must be in-line with architectural design, in order to ensure transparency in code.
* Once a week meetings (15 minutes) to report progress/difficulties in development, could be con-ducted after weekly team meeting.\
The aim is to ensure problems are known early and progress are understood by the whole team.

<div class="page"/><!-- page break -->

#### Guidelines on project structure
There shall be only one Windows Form Application project for a particular module, it shall be the only User Interface project.

All major components (ReportGenerator,DatabaseIOetc.) are to be implemented byC# libraries.

User interface is to be implemented by native .NET form creator to ease future development, XML-based interface design is discouraged.

There shall be a library project called `EagleStaticCommon` which contains helper or data components that are used by all other components.\
To avoid breaking the layered architecture, `EagleStaticCommon` shall only contain static functions and properties.\
However the decision of putting a component in `EagleStaticCommon` must be considered carefully to avoid overcrowding, which lead to confusion.

#### Guideline on components design
Each component design must be justified by thorough analysis into quality requirements of the component, applied design patterns or tactics.

It is recommended that to the very least, a component design should incorporate and separate the following component into directories in the library:
* Interface: include all abstract classes and interfaces
* Enumeration: all enumerations
* EventArgs: all subclasses of EventArgs if any
* Structures: all data structures if any
* Contracts: contract classes if any

#### Guideline on naming and namespaces
Appropriate namespaces will be automatically created by Visual Studio if folder structure is set up in the project.

<div class="page"/><!-- page break -->

<!-- TOC ignore:true -->
# Chapter 6

# Reviews and Audits
## Purpose
This section of the SQAP defines a set of procedures used to validate project deliverables and
to verify team processes with respect to defined requirements and standards.

The purpose of validation is to ensure that the correct deliverables are being produced with respect to the client requirements and team standards.\
This is done through internal and external reviews.

The purpose of verification is the ensure that processes outlined in the SQAP are followed to ensure product quality.\
This is done through internal and external audits.

The standards, procedures and practices can be found in chapter 5, Standards and Practices.

## Review/Audit list
### Reviews
Reviews are held during all phases of the project's life-cycle.

#### Formal Review Process
All formal review meetings must use the following process,a formal review is to be declared ona case by case basis:
1. Are view committee is selected and the specified roles are filled.
2. The Moderator identifies and/or confirms the review's objectives.
3. The Moderator ensures that all members of the committee understand the objectives and the review process.
4. &nbsp;
	1. Individual: the review committee will prepare to review the work by examining it carefully for potential defects.
	2. Team: there view committee meets at a planned time to pool the results of their preparation activity and
	arrive at a consensus regarding the status of the document or standard being reviewed
5. Author of the work makes the required changes as specified by the review committee.
6. Moderator verifies that the actions required by the Author have taken place.

<div class="page"/><!-- page break -->

#### Informal Review Processes
#### Code
Code quality is to be ensured through regular reviews as listed below.\
In the event that code is found to be unsatisfactory the results will be communicated to the relevant team member and raised as an Issue.
1. Peer review: Code commits shall be reviewed by a peer developer, assigned in the team meeting, as recommended by the Code champion, for the following aspects.\
Weekly inspection will be carried out on all commits by the assigned peer prior to the next meeting.
	* Coding Standard
	* Task Completion
	* Verified against initial specifications, from each stage's detail design.
	* Agreement upon any changes to specifications
2. Client review: Every 2 weeks, all working branches are merged and sent to client for testing and review against the following:
(The method of transfer will not require meeting with the client face to face and is distinctly different from client meetings.)
	* Deliverable time line
	* Verified against specifications
	* Validate task completion

#### Meeting
Meeting quality will primarily be maintained through audits of the correct process but all meeting related documents will also be reviewed for quality.

Meeting minutes will be reviewed following the first meeting of each secretary against the standards.\
This is done alongside the formal acceptance of minutes at the conclusion of each meeting.

Agenda will be accepted prior to each meeting and formally reviewed prior to the following meeting.

Any documents found to be unsatisfactory will have results communicated to the secretary and raised as an Issue.

<div class="page"/><!-- page break -->

#### Management Document
Management documents will be reviewed against document standards prior to being finalised and released.\
In the event that the document is found to be unsatisfactory, a list of improvements will be generated and raised as an issue.\
One example of this is the feed back sheets provided by the supervisor.

### Audits
Audits should be held regularly during all phases of the project's life-cycle to ensure processes put in place are being adhered to.

#### Coding Practices Audit
Coding practices will be audited by code champion on a case by case basis (normally as a result of consecutive unsatisfactory peer reviews).\
Failure to meet defined coding processes will result in a list of improvements being generated and communicated to responsible team member(s).

#### Communication Audit
Communications will be audited on a monthly basis by Team Leader.\
Failure to meet defined communication processes will result in a list of improvements being generated and communicated to responsible team member(s).

#### SVN Practices Audit
SVN Practices will be audited as part of the routine maintenance by the SVN champion.\
Failure to meet the prescribed practices will be communicated to relevant team members with recommendations for improvement.

<div class="page"/><!-- page break -->

<!-- TOC ignore:true -->
# Chapter 7

# Testing
Testing will be predominately in the form of field testing with the assistance of the client.\
This is the accepted method due the domain knowledge requirement of the user, and the restrictive nature of the project.\
The team are to perform as many tests on the releases before handing over to the client.\
Unit tests can be utilised, but will not make up a large part of the testing.\
The can be used for confirming numerical data generated by the program has been manipulated correctly.

The team will also perform some usability/function testing on the prototype prior to release.\
This will most likely be involve trying to break/crash the program.\
As the project is heavily reliant on import and export of data, there are numerous times when IO Exceptions could be thrown.\
As part of this testing, the tester is to document all error, messages and general comments relating to usability of the GUI.\
The tester should also be provided with a list of performance metrics to be tested and monitored during the testing process.\
Some examples are: CPU usage, memory usage, processing time, closing opened files and termination of processes correctly.

Once the team has made their best effort to break the program, handled all exceptions, provided usable error messages and
are satisfied with the release, it is to be given to the client for feedback.

The release should be accompanied with feedback sheets for the client to complete and return to the team so that issues can be repeated, and ultimately, resolved.\
The client will also be expected to provide an acceptable performance level for the metrics used.\
For example what is the acceptable processing time; 1 minute or 1 hour?

<div class="page"/><!-- page break -->

## Requirement
The overall goal of the team is to satisfy the clients needs when building the software.\
Therefore, strong consultation with them will result in a product that works, is usable and maintainable.\
The requirements outlined in SRS shall be verified and validated by the client to ensure the product is suitable for deployment and use.

## Use case generation
Use cases shall be validated and verified by the client with the assistance of the testing team.\
Sample outputs from the client will allow a basic understanding for the team,
but ultimately the client will be responsible for communication specific uses of the software to ensure the team can adapt it to suit.

## Installation and User Documentation Generation
The releases will be an in the form of an executable and a set of .dll files that will be provided to the client.\
There is no installation as such,the user simply runs the executable.\
All input and output files will be located as part of the GUI.

The client will also be supplied with a comprehensive user document that details the GUI and should have some examples of how to use it.\
The client will also be supplied documentation of the code and the design documents.\
This is to assist with maintainability and use for future projects.

Once code has been finalised, and testing is completed, they will be supplied with all of the source code and a final build of the software.
* Tailored for a particular module, tests will be outlined within the module plans.
* Modules will be tested against a set of defined use-cases as agreed by client.
* Testing will consist of both black and white box testing.

<div class="page"/><!-- page break -->

<!-- TOC ignore:true -->
# Chapter 8

# Problem reporting and corrective action
## Personnel
If an issue arises with personnel the Team Leader is to be notified.\
The Team Leader will follow up on the issue to gather all the facts.\
Once known the Team Leader will suggest a corrective action.\
Corrective Action can include but is not limited to: counselling, team reorganization, protocol changes.

## Work
### Project major time line
There is one parent project, which is ProjectEagle.\
ProjectEagle shall contain multiple sub-projects, which are the major modules that will be developed: Module 1-2, Module 3, and Module 4.

ProjectEagle will have multiple Versions (Manage\Project \Version), each shall be a major milestone for development.

Each sub-project will also have multiple version, with each major version is one iteration.

To implement spiral process model,the following postfix is included into each sub-project version to indicate the stage
* "dsg" indicating the design stage.
* "dev" indicating the development stage.
* "tst" indicating the testing stage.

Release date of each version is the due date, scope is to be planned according to this due date.

Progress of the current stage can be viewed by visiting "Road map" page.

### Stage-dependent tasks
Stage-dependent issues and tasks must indicate which sub-project they belong to, as well as which version\
(e.g., [Module 1-2] v1.0 dsg indicating this issue belong to design phase of Module 1-2 first release).

### Crossed-states tasks
Crossed-states tasks and issues must indicate parent's version.\
For example, documentation tasks may fall under ProjectEagle v1.0.

### Task creation
Minute taker is to convert meeting's actions to task and assign to appropriate developer.\
Developer is responsible to divide the task logically into smaller tasks if necessary.\
Team member would also create task as appropriate: for bug reporting or planning.\
Task creator must check for existing issue prior to creating task.

<div class="page"/><!-- page break -->

### Task assignment
When a task cannot be assigned upon creation, the respective champion of the task must perform assignment within 24h of task creation.

### Task life
Assignee (who is assigned to the task), must response within 12h if the assignment is deemed in appropriate.

Resolver is responsible to ensure solutions are checked against the appropriate standards and practices prior to marking the issue as "Resolved".

It is stressed that the resolver must entered the time spent on the task into the time-spent box before confirming as 'resolved'.

After an issue is marked "Resolved",
respective champion is responsible to formally/informally review the task (exception for trivial tasks), then mark the issue as "closed"

### Issue Categories
Categories can be updated to adapt to the project's development, the following are most up to date:
* Administration
* Audit - External
* Audit - Internal
* Client Liaison
* Coding - Prototype
* Documentation - AD
* Documentation - General
* Documentation - PP
* Documentation - SAR
* Documentation - SD
* Documentation - SQAP
* Documentation - SRS
* Lecture
* Meeting - Client
* Meeting - Other
* Meeting - Weekly
* Presentation Preparation
* Research - Coding
* Research - Documentation
* Review - External
* Review - Internal
* SVN Management
* Requirements - Module 1
* Design - Module 1
* Coding - Module 1
* Testing - Module 1
* Requirements - Module 3
* Design - Module 3
* Coding - Module 3
* Testing - Module 3

<div class="page"/><!-- page break -->

<!-- TOC ignore:true -->
# Chapter 9

# Tools and methodologies
## Tools
### LaTeX
To compile the documentation TEX files, pdflatex should be used, on Windows the MiKTeX 2.9 package provides this.\
The recommended editor for LaTeX files is the Texmaker editor, version3.3.1 has been recommended.

### Issues tracking
Issue tracking tool is Mantis.\
The tool can be access by SIMS username and password at:\
<https://mercury.it.swin.edu.au/hit3158/hit3158_02/mantis/Mantis>\
provides a simple to use and feature-rich platform to track issues,progress and effort by the team.

### SVN
All commit and updates by team members shall be done through TortoiseSVN or SmartSVN client to avoid potential problems.\
Both programs have been tested to work, so it is up to the individual to choose which program they prefer.

### Visual Studio
VisualStudio2010 (available via MSDNAcademicAlliance in association with Swinburne FICT faculty) is selected as the standard C# development environment.\
It provides state-of-the-art development tool as well as supporting client's .NET 2.0 standard environment.

### Virtual Machine
All development will be done on a virtual machine with a Windows XP 32bit image provided by the client.\
The recommended Virtual Machine software is VirtualBox version 4.1.8.

### Skype
If Skype meetings are deemed to be necessary, then all team members will need to download and install Skype and have access to a microphone and speakers.

<div class="page"/><!-- page break -->

## Agile Methodology: Kanban

![kanban](https://www.nimblework.com/wp-content/uploads/2022/12/Simple-Kanban-Board-5-1024x628.webp)

<sup>Figure Source: <https://www.nimblework.com/kanban/what-is-kanban/></sup>

The Kanban Agile Methodology approach will prioritize collaboration, flexibility, and continuous improvement.
The Kanban board will be used to visualize the workflow and identify bottlenecks, enabling the team to respond quickly to changes and adapt the design accordingly.
Regular communication and meetings will ensure that the design is meeting the project requirements, and
the team will focus on delivering small, incremental changes to the design, allowing for feedback and iteration throughout the project lifecycle.

Some key points for utilizing Kanban for software architecture and design in this project are:
* Breaking down the overall design into smaller, more manageable components, and creating a backlog of tasks that need to be accomplished.
* Prioritizing the backlog based on importance and complexity, and assigning each task to a specific team member or group.
* Utilizing Kanban boards to visualize the workflow, track progress, and ensure visibility and collaboration among team members.

Kanban is an iterative software development process that emphasizes flexibility, continuous improvement, and customer collaboration.
This approach can help ensure that the software architecture and design process is efficient, effective, and customer-centric.
By delivering small, incremental changes and seeking continuous feedback, the team can ensure that the final product meets the needs of its users.

<div class="page"/><!-- page break -->

<!-- TOC ignore:true -->
# Chapter 10

# Records collection, maintenance and retention
Minutes, Agendas and Notes from meetings are added to project team's SVN Repository as described in SVN Procedures.\
Minutes and Notes will be added following approval by meeting participants.

All documentation will be retained in repository for the duration of the project.

<!-- TOC ignore:true -->
# Chapter 11

# Risk Management
## Purpose
Risk management is undertaken to facilitate the creation of a product that is high quality, on time and delivers the scope specified by the client.
## Categorization
For this project three major categories of risks have been identified:
1. Risks with respect to the work to be done.
2. Risks with respect to the management.
3. Risks with respect to the client.

In the following sections each of these categories have their major risks identified.\
For each risk, a description, a probability to occur, its impact and the preventative/(reductive) action associated are given.

Both the probability of a risk occurring and the impact of a risk if it does occur have been quantified as being low, moderate or high.\
Actions have been categorized as preventative and reductive;
preventative actions aim to reduce the likelihood of risks occurring and reductive actions reduce the impact of risks if they do occur.

<div class="page"/><!-- page break -->

## Risks with respect to the work to be done
* Corruption of repository
	* Probability: Low.
	* Impact: High resulting in loss of work.
	* Reductive Action: Weekly backups plus local checkouts reduce impact significantly.
* Design Errors
	* Probability: High.
	* Impact: High, design errors would potentially increase production time and/or produce a deliverable not valid to client requirements.
	* Preventative Action: Rigorous design methodology prior to development.
* Time Shortage
	* Probability: High.
	* Impact: High, resulting in a loss of product quality, loss of functionality or delivered past deadline.
	* Preventative Action: Rigorous design methodology prior to development including work distribution and conservative timelines.
* Illness or absence of team members
	* Probability: High.
	* Impact: Variable impact dependant on time in schedule.
	* Reductive Action: Shared understanding of work allows load to be distributed.
* Software non deployable
	* Probability: Moderate.
	* Impact: High,will be unable to provide client with the DMS.
	* Preventative Action: Regular contact with client with minor releases to ensure that they can be deployed on the system.

## Risks with respect to the management
* Illness or sudden absence of team leader
	* Probability: Moderate.
	* Impact: Variable impact dependent on time in schedule.
	* Reductive Action: Emergency meeting to be organised by Team Leader to elect temporary team leader.
* SQAP not suitable for our purposes
	* Probability: Low.
	* Impact: High, failure to follow SQAP would reduce product quality.
	* Preventative Action: SQAP to be produced with full team input and cleared with team supervisor.
* Team member leaves the team
	* Probability: Low.
	* Impact: High, their roles and responsibilities are no longer being fulfilled, and the amount of man hours the team can provide in a given time is diminished.
	* Preventative Action: None.\
	However, roles and responsibilities will need to be redistributed to the remaining team members.

<div class="page"/><!-- page break -->

## Risks with respect to the client
* Changing client requirements
	* Probability: Moderate.
	* Impact: Moderate, increased workload and timeline issues.
	* PreventativeAction: Rigorous discussion of requirements plus official SRS document early in project timeline.
* Client unavailable
	* Probability: Moderate.
	* Impact: Low, unavailability for questions and software releases
	* ReductiveAction: Vital questions for client to be communicated before they become critical.
* Client abandons project
	* Probability: Low.
	* Impact: High, No more work modules for the project to complete.
	* Reductive Action: Get as many modules and requirements off the client as possible.
