# Organisational Structure
## Project owner
Dr James McEntee
## Clinical leads
Dr James McEntee - AICU Senior Clinical Design Fellow, 2023 Digital Horizon Fellow
Dr Alice Sisson - AICU Consultant, Service Director for Theatres and ICU
## Divisional triumvirate sign off
Pending
The project has been agreed as part of CW+ Horizon Fellowship at divisional level 06/2023
## Training lead
Dr James McEntee
Subdivision of training will be based on existing local leads for services e.g. education, projects, induction
## DCIO name 
TBC

---
# Project Structure

## Title
**ICU Single Point of Knowledge (ICU-SPOK)**
Started 01/06/2023
Planned Care - Adult ICU
Requestor - Dr James McEntee
DCIO - tbc
DCNIO - tbc
## Purpose
To centralise and improve access to knowledge within ICU
To create an integrated system of knowledge creation and sharing
To reduce administrative burden for clinicians, through automation
To prepare our knowledge base future integrations
## Background
ICU is a complex environment with up to 18 doctors rotating every 3, 4 or 6 months. At least half of these doctors will never have worked in ICU before. We also have a broad team of nurses, AHPs, therapists and other staff. To work most effectively as a team, we need to work from a shared understanding of standard practice. With constant workforce flux, a growing department, and an increasingly complex clinical workload, working from a shared standard becomes increasingly difficult.
## Problem
The knowledge sharing issues can be characterised as:
1. division of knowledge
2. inaccessibility of knowledge
3. no portable knowledge framework
### Division of knowledge
Knowledge in the ICU is divided, and not openly accessible
Guidelines exist in digital form in many locations:
	trust intranet
	trust shared drive
	Box.com (funded locally)
	WhatsApp group shared media
	Cerner eTraining app
	pilot ICU website

There are also paper guidelines in the:
	Hub office
	Pharmacy folder
	Research folders
	Equipment room
	Multiple whiteboards/noticeboards

The division of knowledge leads to ignorance of existing  guidelines, guidelines that are out of date, and duplicated work.
### Inaccessibility of knowledge
A divided knowledge base means that most staff are unaware of guidelines. With no unified, searchable repository and a huge knowledge base, guidelines are often missed and have frequently not been reviewed in years. 
Much of the knowledge in ICU is also not suited to the formal trust guideline template e.g. a local induction timetable, and so exists only within a shared drive, email thread or as 'institutional knowledge'. 
The inaccessibility of knowledge leads to poor data storage and review practice. The diversity of formats (PDF, email, images, Word documents) prevents intra-operability such that work must be duplicated and manually transcribed between formats.
### No portable knowledge framework
Most departments have a significant 'institutional knowledge' and local culture that is maintained through personal memory and conversations. The success of this is wholly reliant on staff retention and much of that knowledge is lost due to the rotational workforce. 
We currently have no solution to document this culture/knowledge or for new information to integrated in the department. This leads to cultural inertia and resistance to new, improved practice.
	It's easy to think of quality improvement work that stops when a staff member leaves
With no framework to capture this knowledge, it is usually lost or locked in a non-transferrable format. This lack of 'portability' prevents conversion from institutional knowledge to formally agreed practice. 

---
# Solution

## A modern, open source, microservice architecture
This encompasses:
	digital and paper-to-digital knowledge base
	project management
	onboarding
	communication
	integration/automation
	teaching
	CRUD interface (create-read-update-destroy)
	static website/dashboard

Microservice architecture is a concept that has overtaken historical monolithic development. This approach underpins modern digital services like Netflix. Using the best suited, open source software for each task rather than one companies suite of software.

For specific service details please see the [Architecture Decision Record](https://github.com/drmcentee/ChelseaICU-adr/) on the project's GitHub.
## Setup
Airtable and the chelseaicu.com domain has already been funded via a CW+ SCBI grant. This has delivered a significant time cost saving as detailed below.
These are now mature systems within the department and have become business as usual.
Containerised deployment via a cloud hosted virtual machine (VM) will allow this project to be piloted. DigitalOcean has been chosen as it provides a balance of operability and cost. It has become an industry standard, entrypoint for cloud service with a track record of reliability.
Ultimately this could be transitioned to a trust based server, given the minimal hardware requirements.

## Maintenance
Domain - £10/yr
VM - £230/yr
Airtable - £200 ($240)/yr (this could be replaced once the ICU-SPOK system has matured)
S3 compatible bucket (storage)- £60/year
Assorted support services e.g. SMTP, Twilio, Elastisearch £100/yr (includes scope for unknown unknowns)
TOTAL - £600/yr

Currently sysadmin time is covered within the CW+ Fellowship time for Dr McEntee. This would need to be allocated within Dr McEntee's job role or outsourced after the roll out of the project. However, it will still be more cost effective than current practice - see below.
These costs could be reduced significantly (sysadmin fees aside) if the system were trust hosted.

Within the structure of the project, there is scope for teaching resources to be offered out to external candidates for a fee. For example, 25 candidates paying £30 each would cover the project with overheads for expansion. This is well within the scope of the established FOCC course alone.

---
## Implication
The principle benefits would be 
- Increased patient safety through adherence to guidelines
- Improved information governance through review and automated re-review of guidelines
- Reduced administrative workload for clinicians
- Deeper integration of rotation team members within the ICU team
### Cost saving
By way of reference, the current Airtable teaching project has reduced consultant administrative time significantly. When considering only the time relating to generating teaching reports - this changed from 8hours to 1.5hours x 7 events/year:

Previously - 56hrs at £100/hr = £5600
Currently - 10.5hrs at £100hr + £200/yr = £1250 (£200/yr for Airtable)

This equates to £4350 saved on one element of teaching administration alone. However, this project will reduce administration time for:
	Local induction
	Teaching (in addition to the current processes)
	Project and quality improvement
	Nursing teaching (Foundation of Critical Care course)
### Transferrable
Since this project is open-source, fully documented, largely containerised and significantly built on text based deployment, it can be rolled out cross-site/cross-network with minimal architectural change.
Similarly it builds a foundation for regional critical care teaching, establishing Chelsea as a centre for critical care education for both doctors and nurses.
### Regional Service guideline sharing
As a centre for burns critical care and HIV critical care, this project will allow secure sharing of guidelines to other trusts that fall within our service area. Currently, the only option for this is downloading and emailing files - requiring administrative time and a minimally documented chain of sharing.
This project provides an option for information sharing based on NHS.net email domain authentication. This allows staff to point to a shared repository and ensure a restricted access log with only NHS staff able to access it.
### Improved information governance 
A spot audit of current guidelines for TENS (a specialist service we provide) showed that all guidelines had not been reviewed since 2011.
The automation allowed by this project would allow issues like this to be flagged.

--- 
# Next steps

## Alpha Release
Feedback from local department leads, nurses, junior doctors and AHPs
## Motion towards approval
Feedback from the board to work towards full approval
If no current objections then progression with the project and re-review after final release
## Stakeholder map for cross site deployment
Once the pilot project has launched, this project aims to move cross site
Since there are significant differences between the two ICUs, the project needs a stakeholder review to assess if it is of benefit to the WMUH site.
# Additional material to support this work
## Trust Internet Policy Review
Currently blocks Slack.com which is used for authentication and as the communication backbone
A request has been submitted but no response received
## Consideration of local deployment
Costs could be improved if this was deployed within trust architecture
## Roll out plan
Work is ongoing towards roll out of the project 
However, a roll out plan is needed to fully embed the project within departmental culture
This will most likely leverage current pain points that have been identified for staff and target key decision makers in the team. 
Currently leads for all the issues raised within the Architecture Decision Record have been identified.
## Downtime plan
DigitalOcean has a impressive track record of uptime. However, it also allows for backups which can be deployed in the event of an outage.
The service architecture is built on GitHub hosted yaml files and so re-deployment in the event of catastrophic failure is possible.
However, a more realistic scenario is of high server load causing issues. As such Kubernetes or other scalable architecture needs to be considered after release of v1.0 of the project.
