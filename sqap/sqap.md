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
		* [Project Plan](#project-plan)
		* [Software Quality Assurance Plan SQAP](#software-quality-assurance-plan-sqap)
		* [Code Documentation](#code-documentation)
		* [Self-Assessment Reports](#self-assessment-reports)
		* [Software/System Requirements Specification SRS](#softwaresystem-requirements-specification-srs)
		* [System Architecture Design and Research Report SADRR](#system-architecture-design-and-research-report-sadrr)
		* [Audit Report](#audit-report)
	* [Management Documents](#management-documents)
		* [Meeting Agendas](#meeting-agendas)
		* [Meeting Minutes](#meeting-minutes)
* [Standards, Practices, Conventions and Metrics](#standards-practices-conventions-and-metrics)
	* [Purpose](#purpose-1)
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
	* [Purpose](#purpose-2)
	* [Review/Audit list](#reviewaudit-list)
		* [Reviews](#reviews)
		* [Audits](#audits)
* [Testing](#testing)
	* [Requirement](#requirement)
	* [Use case generation](#use-case-generation)
	* [Installation and User Documentation Generation](#installation-and-user-documentation-generation)
* [Problem Reporting and Corrective Action](#problem-reporting-and-corrective-action)
	* [Personnel](#personnel)
	* [Work](#work)
		* [Project major time line](#project-major-time-line)
		* [Stage-dependent tasks](#stage-dependent-tasks)
		* [Crossed-states tasks](#crossed-states-tasks)
		* [Task creation](#task-creation)
		* [Task assignment](#task-assignment)
		* [Task Life](#task-life)
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
	* [Purpose](#purpose-3)
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
The robot vision system for a pick and place task will be tackled by group 24 and following this document; the software quality assurance plan (SQAP),
it will be ensured that the projects requirements and quality standards are met.
The plan will outline the development process and testing procedures, including but not limited too reviewing, testing and integration.
In addition, the plan will describe several tools and methodologies that will be implemented and used to guarantee the solution's reliability,
maintainability and performance.
Finally, the plan will identify the team; `team_name`, responsible for the development and testing of the software as well as their roles and responsibilities.
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
The following section will detail the various roles within the team for various scenarios.

### Meeting Roles
These roles will be for regular meetings to discuss the current progress of the project and
will help ensure successful completion of the project and cohesion between team members.\
The meeting roles will consist of:

#### Meeting Manager
Coordinates meetings and ensure effective communication between meeting members.
Summarises the meeting, describing and allocating any future tasks to the relevant members.

#### Scribe
Records any important information and meeting minutes during the meeting for future reference and records.

#### Moderator
Ensures meeting remains within time and each member is able to state and discuss their relevant item.
Keeps track of meeting minutes for the scribe to record.
Makes sure that only nobody talks over another to keep the discussion understandable and time efficient.

<div class="page"/><!-- page break -->

### Formal Review Meeting Roles
Formal review meetings will be conducted to thoroughly check finished work in order to maximise the quality of the software architecture and design.
During the meeting, team members should provide constructive feedback and
ensure that the software architecture and design aligns with the project's objectives and adheres to quality standards.

The roles for such meetings will be similar to the meeting roles described in the previous section.
The formal review meetings roles will be as follows:
* The lead software architect and designer, along with other software architects and designers involved in the project
* Subject matter experts in computer vision, sensors, robotics, and AI to ensure the quality of the software design.
* The project manager to facilitate the review meeting and ensure effective communication between team members.
* Team members to review the software architecture and design documentation in advance and
provide constructive feedback during the meeting to ensure that the software design aligns with the project's objectives and adheres to quality standards.

<div class="page"/><!-- page break -->

### Champion Roles
A champion in a role is considered the primary person responsible for the quality of the work associated with that role.
While multiple team members could take on the same role, the champion of that role is essentially the leader of the role.
Champion roles are crucial for ensuring that the software is designed and developed according to best practices, meets the requirements of the project,
and is maintainable and scalable over time.\
The following will be the champion roles for the project:

#### Software Architect
Responsible for creating the overall architecture of the system, defining its components and interactions.

#### Software Designer
Designs specific modules and subsystems utilising the architectural plans.

#### Software Developer
Responsible for writing the code that implements the design, working closely with the designer to ensure that the code meets the design specifications and requirements.

#### Cobot/Hardware Champion
Will be primarily responsible for working with the cobot and ensuring all code is compatible and functional.

#### OS Integration Champion
Ensures that all code functions on Ubuntu as there may be compatibility issues between Windows and Ubuntu.

#### API Champion
Should have extra understanding regarding the APIs used such as ROS to ensure no unnecessary development of functions occurs.
They will also ensure the functions used are the most appropriate for the situation.

#### Documentation Champion
Ensures all code documentation is descriptive and explains the relevant functions and modules sufficiently.
Additionally, they will make sure all developers write concise and informative comments in their code to facilitate documentation creation.

#### GitHub Management Champion
Has expertise in managing GitHub repositories that will allow for better collaboration and efficiency.
They will be able to answer questions regarding GitHub tools and techniques that will make creating and editing work and software much easier.

#### Kanban Methodology Champion
Expertly understands the Kanban methodology which provides the team with an efficient and more individualistic working approach.
This champion role will help the team meet goals by providing them with a better understand of the Kanban methodology.

### Communication Roles
The communication roles are those necessary for effective communication between team members and between the client and stakeholders.
These roles will take on the responsibility of understanding the relevant information they need to communicate and
be able to clearly provide such information to the group they need to communicate with.

The communication roles to be established will be:

#### Software Architects and Designers:
Software architects and designers are responsible for developing the software architecture and design and ensuring that it aligns with the project's objectives and
adheres to quality standards.
They should also collaborate with subject matter experts to ensure that the system design meets the project's objectives.

#### Project Team Members with Expertise in Computer Vision, Sensors, Robotics, and AI:
Team members with expertise in these fields are responsible for providing input and review of the software architecture and
design to ensure that it aligns with the project's objectives.

#### Project Superviser
The project superviser will be consulted regarding information about the project and will provide feedback on work when necessary.
They will also communicate with the team leader should they need to contact the team regarding any work or updates on project progress.

#### Client
The client will communicate with team members should they require updates on progress.
Team members, particularly those working with the cobot, can correspond with the client to seek clarification on specific requirements.

#### Team Leader:
Responsible for facilitating communication between team members and ensuring that communication is effective and efficient.
They should also ensure that the project's software design documentation is complete, accurate, and
up-to-date to facilitate communication with the development team and stakeholders.

#### Quality Manager
Quality managers ensure quality is maximised throughout the project,
and therefore will be responsible for communicating quality requirements to the relevant team members.
They will also provide the project superviser and client with updates regarding the quality of the deliverables currently being worked on.

#### Support Manager
The support managers are responsible for providing support to other team members, the project superviser, or the client with regards to the project.
They will communicate with other team members to help them with work, research, or testing if necessary.
Should the superviser or client require assistance with understanding the deliverables or software,
the support managers should relay information to them regarding these aspects.

#### Development Manager
Development managers coordinate with the software developers to keep progress steady and ensure code functions correctly.
They will be able to provide the superviser, client, and team leader with updates regarding the development and testing process.

#### Planning Manager
The planning manager plans for the future documents, software components, etc.
to be delivered by potentially allocating work to the relevant members.
The will coordinate other managers to be able to meet requirements and deadlines to keep the project progressing efficiently and consistently.

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
This section will provide an overview of the various software documents that will be created to ensure that the software architecture and
design are thoroughly documented and therefore highly intelligible.

### Project Plan
This document will give a general outline of the project direction, including:
* Overview of the project description and background information.
* Details about the client, stakeholders, and other involved individuals.
* Objectives of the project.
* Acceptable standards and required skills necessary for completion.
* Project deliverables.
* Required research.
* Design, implementation, and testing.
* Risks associated with the project.
* Schedule and time line.

### Software Quality Assurance Plan (SQAP)
The SQAP is a document that describes the measures to be taken to ensure the maximisation of the quality of the project deliverables.\
This document will contain:
* The purpose of the document.
* The various roles required to successfully complete the project.
* Tasks and responsibilities of each member and role.
* Outline of the documentation that will be produced.
* Standards and practices that will be followed.
* Information about reviews and audits.
* Testing information.
* How problem reporting and corrective action will be taken.
* Tools and methodologies that will be used.
* Record collection and maintenance.
* Risk management.

### Code Documentation
Code documentation will contain the following:
* Description of the various created modules.
* Description of functions and classes and how to utilise them in code.
* Interdependency of each module or dependencies on external modules.

### Self-Assessment Reports
These reports will be introspective documents reporting on how each member thought each other performed, which will contain:
* A review of the client.
* Categories regarding metrics such as quantity and quality of work, communication, etc.

### Software/System Requirements Specification (SRS)
The SRS will describe the requirements of the software/system that will be developed.
It will include:
* Purpose of the document.
* Overall description of the system that is to be developed.
* Features of the software.
* System requirements such as hardware requirements.
* Acceptance Criteria for the software.
* Documentation to be delivered.
* Functional requirements of the software.
* Quality requirements.
* Interface requirements such as user interfaces, and hardware/software interfaces.

### System Architecture Design and Research Report (SADRR)
This document will give information about the overall system architecture and design, as well as additional research into the project.
Contained within this document will be:
* Overview of the document.
* Problem analysis which will outline the goals of the software systen and any assumptions and simplifications.
* High-level system architecture and alternatives
* Additional research
	* Research into the application domain
	* Research into the system design
	* Research into platforms, languages, and tools

### Audit Report
Audits, whether carried out internally or externally, must produce a document.\
Anything that is found that doesn't follow the processes outlined in the SQAP will result in corrective actions.
Audit reports should assess the projects scalability, maintainability and suitability.
Additionally an evaluation of the design documents should be carried out during an audit.

## Management Documents
### Meeting Agendas
* This document will be of a markdown type (`.md`) and will be prepared by the team leader prior to each meeting.
* Team members are expected to contribute to the agenda, upon request their topic will be added.
* Requested topics are expected to be presented by the team member that requested them, they are expected to attend the meeting ready to present.
* Owners are expected to attend the meeting and topics accepted before the end of day prior to the meeting.

### Meeting Minutes
* Will be collected at every meeting.
* Must follow the minutes template as outlined on the SVN.
* Will be collected as either a raw .txt file or LaTeX file and then converted to latex format.
* Formatted minutes will be released on the SVN no later than the following day's COB.
* APDF copy of the minute scan also be emailed if requested, however, members are expected to find the minutes on the SVN and complete their actions independently.

<div class="page"/><!-- page break -->

<!-- TOC ignore:true -->
# Chapter 5

# Standards, Practices, Conventions and Metrics
## Purpose
Ensuing good quality work is produced standards are essential;
this section will cover many standards of varying parts of the programming process.\
These standards aim to provide a structured approach to software design and development,
these primarily being in regards to scalability, maintainability and integrability.\
These standards also provide a basis for testing and validation, ensuing that the system performs as expected and meets the expectations of the client.
By adhering to these standards the development team can mitigate potential risks and ensure the successful and satisfactory delivery of the project.

## Standards
The proposed software development process will adhere to a number of industry standards including:
* [ISO/IEC/IEEE 12207](https://www.iso.org/standard/63712.html) for software development life cycle processes.
* [ISO/IEC/IEEE 15288](https://www.iso.org/standard/63711.html) for system life cycle processes.
* [ISO/IEC 25010](https://www.iso.org/standard/35733.html) for software product quality.

These standards will ensure that the project is developed in a systematic and controlled manner, meets quality requirements, and is maintainable in the long term.
To ensure compliance with standards, the project team will identify and adopt additional guidelines relevant to the project's domain and requirements.

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

### Software Versioning Strategy: SemVer
Versioning is a critical aspect of software development that helps developers and users manage changes to a project.
Semantic Versioning, or SemVer for short,
is a widely-adopted standard for versioning software projects that provides clear guidelines for how to version software releases and manage dependencies between them.

The SemVer standard uses a three-part version number in the format "MAJOR.MINOR.PATCH" to convey information about changes to the software.
The MAJOR version number indicates significant changes that may introduce incompatibilities with earlier versions,
the MINOR version number indicates new functionality added in a backwards-compatible manner, and
the PATCH version number indicates bug fixes or minor changes that are backwards-compatible.

In order to use SemVer effectively, it's important to follow these guidelines:
* Increase the MAJOR version when making incompatible changes
* Increase the MINOR version when adding new functionality in a backwards-compatible manner
* Increase the PATCH version when making backwards-compatible bug fixes or other minor changes
* Use pre-release version numbers (such as 1.0.0-alpha) to indicate that a version is not yet stable or complete
* Use build metadata (such as 1.0.0+build.1) to indicate additional build information without changing the version semantics

Adherence to SemVer ensures that version numbers convey meaningful information about the state of the software and the nature of changes between releases.
This enables developers and users to make informed decisions about which versions of a project to use and when to upgrade, and
helps prevent compatibility issues between different versions of the same project.

By following the guidelines provided by the SemVer standard,
teams can ensure that their software projects are versioned in a consistent and predictable way,
making it easier to manage dependencies and collaborate with other teams or individuals.

#### Semantic Versioning Specifications
Software using Semantic Versioning must declare a public API.
This API can exist strictly in documentation or be declared in the code itself.

A normal version number will be written as X.Y.Z where X, Y, and Z are non-negative integers
and do not contain leading zeroes. X is the major version, Y is the minor version, and Z is the patch version.
Each element must increase numerically. Example: 1.4.0 -> 1.5.0 -> 1.6.0.

Version 1.0.0 defines the public API.
The way in which the version number is incremented after this is dependent on the defined public API and
how it changes.

Once a versioned package has been released, the specific contents of that version can never be modified.
Any changes must be released as a new version.

Major version zero (0.y.z) is for initial development.
Anything in this version may change at any time.

Patch version Z (x.y.Z | x > 0) \
It must be incremented if:
* Only backwards compatible bug fixes are introduced
A bug fix is defined as an internal change that fixes incorrect behaviour.

Minor version Y (x.Y.z | x > 0)\
It must be incremented if:
* New, backwards compatible functionality is introduced to the public API
* Any public API functionality is marked as deprecated
It may also be incremented if:
* Substantial new functionality or improvements are introduced within the private code
* It includes patch level changes
Patch version must be reset to 0 when minor version is incremented.

Major version X (X.y.z | X > 0) \
It must be incremented if:
* Any backwards incompatible changes are introduced to the public API.]
It may also be incremented if:
* It includes minor and patch level changes
Patch and minor versions must be reset to 0 when the major version is incremented.

A pre-release version may be denoted by adding a hyphen and 
a series of dot separated identifiers immediately following the patch version.

Identifiers must:
* Comprise of only ASCII alphanumerics and hyphens [0-9A-Za-z-]

Identifiers can not:
* Be empty
* Include leading zeroes

A pre-release version indicates that the version is unstable and
might not satisfy the intended compatibility requirements as denoted by its associated normal version.
Examples: 1.0.0-alpha, 1.0.0-alpha.5, 1.0.0-x.9.z.14.

Build metadata may be denoted by appending a plus sign and
a series of dot separated identifiers immediately following the patch or pre-release version.
These are identifiers share the same properties as the identifiers used in pre-release versions.
Examples: 1.0.0-alpha+001, 1.0.0+111222333, 1.0.0-beta+exp.jpg.ff3355cc.

Precedence refers to how versions are compared to each other when ordered.
Precedence is calculated by separating the version into major, minor, patch and pre-release identifiers.
Two versions that differ only by the build metadata, have the same precedence.
Therefore, build metadata identifiers are ignored when determining precedence.

To determine precedence, compare each of the identifiers by the first difference.
Example: 1.0.0 < 2.0.0 < 2.1.0 < 2.1.1.

When major, minor, and patch are equal, a pre-release version has lower precedence than a normal version:
Example: 1.0.0-alpha < 1.0.0.

Precedence for two pre-release versions with the same major, minor, and
patch version must be determined by comparing each dot separated identifier from left to righ,
until a difference is found as follows:
* Identifiers consisting of only digits are compared numerically.
* Identifiers with letters or hyphens are compared lexically in ASCII sort order.
* Numeric identifiers always have lower precedence than non-numeric identifiers.
* A larger set of pre-release fields has a higher precedence than a smaller set, if all of the preceding identifiers are equal

### Document Releases
In the event that a document is released to an outside party; be it submission to the university or the client it must be:
* Converted into a static format such as a pdf
* Appropriately renamed with a revision number
* Moved to a release folder within its current folder

Each release will be named as follows: filename rxxx, where xxx is a number.\
The first release will be 100 and each additional release will be incremented by 10 i.e., filename r100 will be followed by filename r110.

<div class="page"/><!-- page break -->

## Practices
This section will cover several practises that will be employed as a basis for quality control wtihin the project.\
These practises will be followed closely throughout development, frequent audits will ensure that this is the case.\
Through rigorous upholding of the outlined practises the quality of the project will be maintained and ensured the deliverables be of high quality.

### Communication Practices
Effective communication between all parties associated with this project will use the practices laid out in this section to ensure quality control and
that the project progresses smoothly.
Communication with the following parties will use the respective practices:

#### Client
* Communication will occur primarily through Group Leader.
* Regular updates as to progress of research/development.
* Communication to primarily occur through email, face-to-face meetings can be arranged on an as needed basis.
* Communication is to be of a formal and respectful manner.
* All team members will be appraised of communication with the client, unless urgency requires otherwise.

#### Team
* Communication within group will primarily occur through Discord.
* Regular team meetings to discuss progress, issues, and feedback.
* Meetings will be arranged on Discord, unless a face-to-face meeting is required.
* Attendance to meetings is expected, except when absence has been discussed and understood by other team members.
* Collaborative work will be fostered by using Github features such as Discussions and Pull Requests for development.
* A Kanban Board will be used as a project management tool to track issues and pull requests, and to keep all team members up-to-date.

#### Supervisor
* Communication will occur primarily through Group Leader.
* Weekly meetings on Microsoft Teams to be held between team members and supervisor to discuss current progress and challenges being tackled.
* Communication to primarily occur through email, in-person meetings can be arranged on an as needed basis.
* Communication is to be of a formal and respectful manner.
* Inter-personal issues will be reported to supervisor to discuss possible actions and/or solutions for resolution.
* All team members will be appraised of communication with the client, unless urgency or personal issues require otherwise.

<div class="page"/><!-- page break -->

### Meetings
Regular meetings with all team members present will be held. The following goals and tasks should be completed for each week:
* All members are to attend each meeting.
* If a member cannot attend a particular meeting, all other members are to be notified ahead of time.
* All members are to provide updates on progress of current tasking, challenges that were completed and are currently being tackled.
* Members can use this time to ask for help from other members if required.
* A meeting agenda will be constructed for each regularly scheduled meeting to ensure all topics requiring discussion are covered.
* A meeting minutes document will be constructed for each meeting to ensure that all topics covered in the meeting are recorded accurately.
* A member of the team must be assigned the responsibility of both documents for each week.
Or different member can be delegated the task each week on agreement of all team members.

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
Outlined in this section will be a set of procedures used to validate project deliverables and
to verify team processes in regards to the defined requirements and standards.\
With regards to validation, it will be checked through internal and external reviews, and verification through audits.
These reviews and audits will help ensure that deliverables are up to scratch and product quality is maintained.
The information on these reviews and Audits are found earlier in the document under chapter 5.

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
For the testing phase of the project, a comprehensive approach will be used to ensure that the Robot Vision System is functioning optimally.

Unit testing will be performed on individual software components to verify their correct functionality.
This will likely make up most of the intial testing as the team has a lack of experience with computer vision and
robotic control so we will need to validate that our solutions are on the right track as we learn new skills.
This will largely be assisted by feedback from the client and other team members.

Integration testing will be conducted to ensure that the various components of the system are working together effectively.

Additionally, system-level testing will be carried out to validate that the entire Robot Vision System meets the project's requirements.
The testing process will be automated where possible, and any issues that arise will be documented and addressed promptly.
The team will also perform some usability/function testing to test edge cases where the placement of parts and
robot arm are in incorrect positions to test the robustness of the software solution and see what exceptions are thrown.
These tests will allow the team to design user friendly error messages.

We will work with the client to creatic metrics we can use to measure the success of the solution.

<div class="page"/><!-- page break -->

## Requirement
Our testing will aim to validate that our solution meets all the requirments outlined in thhe SRS above.\
This will require them team to have clear communication with the client to ensure their needs are met by our software.\
This will allow the team to create effective tests, specifically tailored to the requirments of the client.

## Use case generation
For the use case generation, we need to identify the various scenarios in which the robot will operate and the interactions with the system.

The use cases will:
* include details about the inputs, outputs, and actions of the system.
* be generated based on the requirements and will help in validating the system's functionality.
* also help in identifying any potential issues or edge cases that need to be addressed during the development process.

We will need to define our input domain in order to generate valid test cases.
For our software solution, this is all possible positions of chips, covers, batteries and trays.

Our system would be considered as an untestable program because the output cannot be verified, meaning it doesn't have a test oracle.
A test oracle is a procedure in which the outputs of a system can be verified against.
This means we will have to use metamorphic testing.

Metamorphic testing is defined by the following process:
* Defining an initial test case
* Identifying properties of the problem and metamorphic relations (MR)
* Creating follow-up test cases from the initial test case using previously developed MRs
* Verifying the MRs using the systems outputs

For this software solution,
an example of a MR is that the position of a chip placed in the holding bracket is the same regardless of the number of chips placed in adjacent slots.
Therefore, the theoretical output of the system should be that it can identify a specified chip irrespective of any arrangement of surrounding chips.


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

# Problem Reporting and Corrective Action
## Personnel
If an issue arises with personnel, the Team Leader is to be notified immediately, and
they will propose corrective action, which can include team reorganization, or protocol changes.
In the event of issues arising amongst team personnel, they should first be brought to the attention of the project manager or team leader for resolution.
Corrective action may include training, reallocation of tasks, or a discussion of expectations to ensure that team members are able to perform their roles effectively.
It is the responsibility of all team members to report any issues promptly to ensure that they are addressed in a timely manner.

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

### Task Life
Tasks would be created as **issues** on GitHub, and then moved across the Kanban board's columns as they progress through the workflow.
Each task would have an assignee responsible for working on it, and
a resolver responsible for ensuring that solutions are checked against appropriate standards and practices before **approving** the changes via *review*.

The task life would also include testing and maintenance stages, in which the task is verified and validated for functionality and
then maintained to ensure its continued operation and improvement over time.
Finally, the task would be *closed* via a **pull request** after it has been formally *reviewed* by the respective champion and *merged* into the **main** branch.

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
Unforeseen events can and will happen during the course of this project.
To ensure that a functional and high quality product is delivered on schedule, it is vital that risks are identified, analyzed and accounted for.
This section involves risk categorization and listing corresponding countermeasures.

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
|Rank|Name/Description|Occurrence Probability<br/>(H/M/L)|Severity<br/>(H/M/L)|Mitigation Strategy|Contingency|
|:-:|:-|:-:|:-:|:-|:-|
|1|Team leader absence.|L|M-H|Co-leader selected in advance.|Emergency vote.|
|2|Team member leaves.|L|H|Distribute work between at least 2 members.|Organize work handover to another member.|
|3|Inability to hold regular team meetings.|L-M|M-H|Members communicate their schedules|Members who cannot attend meetings provide updates to the team asynchronously.|
|4|Supervisor absence.|L|L|None|Asynchronous updates and catch-up meeting if needed.|
|5|Conflicts within the team.|M|H|Regular communication.|Irregular meetings to resolve disputes.|

* Temporary absence of team leader.\
The team leader can be temporarily absent due to illness or personal matters, and its impact varies depending on when it happens.\
To ensure smooth operation at all times, the team can preemptively allocate a second leader who automatically assumes control when the primary leader is away.
If both leaders are absent, an emergency team meeting is held to select another temporary leader.
* Team member leaves.\
This is a relatively low risk due to the importance of the capstone project.
However, its impact is high because the team's total productivity is reduced and prior planning might no longer be appropriate.\
There is no way to prevent this from occurring, but to minimize its impact,
all tasks should be broken up and allocated to as many members as possible to avoid dependence on a single person.
* Inability to hold regular meetings with all members present.\
This is a moderate-low risk.
The project requires frequent communication between team members and ideally the team should hold regular meetings to keep all members up to date.
Since each member has work and academic commitments it is possible that there may not be free time for a meeting where all members can attend.\
The risk can be mitigated by members communicating their schedules with others.
In the worst case scenario, members who cannot attend regular meetings need to write separate report and update themselves with the team progress on their own.
* Temporary absence of Supervisor.\
The supervisor can be temporarily absent due to illness or scheduling conflict.
This is a low risk and depending on the stages of the project, will not have a significant impact on the project.\
When this event occurs, the team will continue as usual and the team leader will draft an email detailing the progress of the project,
questions for the supervisor and potentially organize a replacement meeting if necessary.
* Conflicts within the team.\
Conflicts among the team are common in projects of any scale.
This risk has a significant impact as it directly harms the team's productivity and causes delays to planned work.\
The keys to keep the problem from happening and to remedy it if it occurs are frequent communication between team members and a democratically-run leadership.
To prevent disputes from spiralling out of control, team members should voice their opinions as soon as possible, either in team meetings or mails/messages.

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
