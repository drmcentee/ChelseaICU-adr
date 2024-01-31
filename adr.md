# Key Services
## Dashboard
### Background
Ease of navigation is essential to the project. While a static webpage could be used, this would require rebuilding in the event of failure and is not human readable in its raw form, making documentation/transferability harder. Therefore a dashboard which can be easily configured, backed up and provide easy navigation is required as the landing page for the staff side of the website.
### Decision
[Dashy](https://dashy.to/)
### Reasoning
Heimdall, Homer, and Homarr were considered. However, Dashy provided better file and GUI based configuration as well as a suite of prebuilt/documented security options for login. Overall, it had the best visual appeal.
### Conclusion
Dashy provides a resilient and robustly functioning landing page for the website.

## Wiki
### Background
The base idea for the upgraded website was knowledge storage and communication. While most guidelines exist in PDF form, this is not space efficient, machine readable, well suited to searching and requires specific software to read. By contrast, Markdown can be converted to PDFs if required with a variety of templates, is human readable in its raw state, can be converted to HTML for web viewing and is well suited to machine reading/AI integration. As such, a Wiki which can store markdown is needed as the core service for documentation. 

### Decision
[Outline](https://www.getoutline.com/)
### Reasoning
WikiJS is the main contender here. However, the following criteria were deemed important:
1. Easy to edit (WYSIWIG)
2. Easy to move (Markdown)
3. PDF export
4. Slack login
5. Slack integration
6. Support for diagrams
7. Integration for video etc

PDF export is currently in beta testing for WikiJS. 
Bookstack was also considered and had good authentication/security. However, the 'book' style interface was less visually appealing.
Outline has easy export to PDF, markdown and HTML, text to diagram via Mermaid and integration with Airtable, GitHub, Gsuite, YouTube and more.

### Conclusion
Outline provides the most complete solution for knowledge transfer based on the criteria at the time of decision. Future versions of WikiJS >v3 should be considered if change is needed.


## Paper documentation storage 
### Background
While a markdown based wiki is the overall aim, it is inevitable that some documents will be better suited to PDF storage, such as complex diagrams. Also, there will be a significant period of time where existing documents will need to be stored, transcribed and then archived/deleted. As such, a digital 'paper guideline' solution is needed.

### Decision
[PaperlessNGX](https://github.com/paperless-ngx/paperless-ngx/tree/main/docker/compose)
### Reasoning
NextCloud and PaperlessNGX are the most popular choices. 
Paperless is lighter weight and specific to document storage. It also has functionality to side by side transpose PDF to text/markdown
NextCloud seems more suited to a GoogleDrive replacement.
### Conclusion
PaperlessNGX is ideally suited to document storage and has undergone extensive development since its original Paperless release. Since the overall project aim is to move away from paper based guidelines, this software my eventually become obsolete/better replaced with a object storage service.

## Employee Onboarding
### Background
Significant time is spent onboarding new team members. While a guideline could be written for this, it is more efficient to use a service to automate this process, allow it to be adjusted as needed and provide a means to integrate new starters with Slack. A local service is needed as trust HR do not fulfil the needs of the department or have sufficient resources to do this.

### Decision
 [ChiefOnboarding](https://github.com/chiefonboarding/ChiefOnboarding)

### Reasoning
Laudspeaker was also considered. While it was visually more attractive, it is still in alpha release and documentation of all but the basic features is lacking. 
### Conclusion
There were few, open source options for onboarding services. ChiefOnboarding seems to fit the criteria but should be reviewed for change if it does not work well in practice. 

## Teaching
### Background
There is a large teaching program in the department but from the doctors and the nurses' FOCC course. Development of this program to allow outside parties to attend could provide financially input to the department/allow this project to self fund in the long term.
A solution for hosting eLearning that allows payment is needed. The trust system is not specific enough to the needs of the department and is visually outdated.

### Decision
[Moodle](https://moodle.org/)
### Reasoning
OpenEdx seemed to be the better option. However, Moodle is more widely used, has better documentation and is more suited to small to medium classes (vs univeristy size for OpenEdx). 
### Conclusion
Moodle seemed the most holistically suited to the task but could perhaps be replaced if uptake is increased.

## Form to PDF
[Docassemble](https://docassemble.org/deploy.html)
## Comms/Auth
Slack
widely used
plugins
AI automation
Markdown suitable

## Project Management
[Plane](https://github.com/makeplane/plane)

?could this be replaced by Github? - maybe not since it required login to allow a private repository

## CRUD
Looking for a form that will send to a Postgres DB
and / and includes
A dashboard platform

https://www.appsmith.com/

https://www.tooljet.com/

https://refine.dev/

https://budibase.com/

https://dashibase.com/

https://www.lowdefy.com/

https://github.com/dashpresshq/dashpress

https://www.getmotoradmin.com/

https://pocketbase.io/

---
# Support Services
## Updating
 [Watchtower](https://github.com/containrrr/watchtower) - 'industry' standard

---
# Concepts
## Markdown
Transferrable
Suited to Git
	This allows Issues, Milestones, Projects
	Suited to large scale projects
	Barebones but fully featured
	Free

## Internally open source
Allow everyone to see +/- do everything
Reduces admin overhead
	No waiting for someone to approve
	Editing/creating can happen when needed 
Authentication allows things to be tracked, versions allow rollback if needed
Encourages engagement
Can be audited by pull requests etc

## Git
Change history is baked in
Transferrable
Future proof (has been around since Linux started)
Integrated Issues, Milestones, Projects
Find and replace
Automations baked in 
Style guidelines 

### Slack
Industry standard communication
Plays well with other services and hence automation
Can act as a login service for apps - offloads storage of data to a track proven service
Segregates work chat to a work chat app - WhatsApp for personal

## Infrastructure as code
Docker compose and other services should be configured via text/automation where possible. This allows a system to be spun up with minimal manual input.

---
# Stretch Ideas
## Authentication server
Offload authentication to NHS email
