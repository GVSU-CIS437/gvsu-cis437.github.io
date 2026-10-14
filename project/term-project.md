# Term Project

The term project is an opportunity to apply the cloud computing concepts and services we have discussed in class by designing and implementing a working cloud application.

Because we are beginning the project around the middle of the semester, this is intended to be a **half-semester project**. Your goal is not to build a huge application. Instead, focus on creating a **working prototype with a clear cloud architecture** that meaningfully integrates multiple cloud services.

Project teams may consist of **1 to 4 students**.

The scope of the project should be appropriate for the size of your team. A larger team is expected to complete a somewhat more substantial project than an individual student.

---

## Project Goal

Your overall task is to design and implement a working cloud application that meaningfully integrates **at least four cloud services**.

The four services should work together as part of one application architecture. Simply enabling four unrelated cloud services does not satisfy the project requirement.

A relatively simple application with a thoughtful cloud architecture is better than a very large application that makes only limited use of cloud services.

Your project should demonstrate that you understand:

- why the selected cloud services are appropriate,
- how the services communicate or interact,
- how the application is deployed in the cloud, and
- how cloud computing improves the design or operation of the application.

---

## Core Requirements

Your project must:

1. Implement a working cloud-based application or prototype.
2. Meaningfully integrate **at least four cloud services**.
3. Include at least one service that provides **application execution or computing**.
4. Include at least one service that provides **data storage or persistence**.
5. Include an **architecture diagram** showing the major application components and how they communicate.
6. Explain the role of each cloud service used in the project.
7. Be demonstrated during the final project presentation.
8. Include documentation that allows another person to understand and run the project.

You may use Google Cloud, AWS, Azure, or another cloud platform with instructor approval.

Because we have been working primarily with Google Cloud and course credits are available, Google Cloud will likely be the easiest option for most teams.

---

## What Counts as a Cloud Service?

Examples of services that may count toward the four-service requirement include:

- Compute Engine
- App Engine
- Cloud Run
- Cloud Run functions
- Cloud Storage
- Firestore
- Cloud SQL
- Pub/Sub
- Cloud Load Balancing
- Other managed cloud services or APIs that play a meaningful role in your application

This list is not exhaustive.

Supporting services and administrative tools normally **do not count** toward the four required cloud services. Examples include:

- Cloud Shell
- IAM
- Billing
- Basic VPC configuration
- Basic firewall rules
- Logging or monitoring used only for administration

You should still use these supporting services when appropriate. For example, your application should use appropriate IAM permissions and firewall rules even though those do not normally count toward the four-service requirement.

If you are unsure whether a particular service counts, please ask before submitting your proposal.

---

## Architecture Diagram

Your project must include an architecture diagram.

The diagram should show:

- the major cloud services used,
- the main application components,
- how users interact with the application, and
- how data or requests move between the services.

For example, a simple architecture might look like:

```text
User
  |
  v
Cloud Run
  |
  +------> Firestore
  |
  +------> Cloud Storage
  |
  +------> Pub/Sub
```
Your architecture may be simpler or more complex depending on your project.

You will include an initial architecture diagram in your proposal and an updated final version with your final project submission.

---

## Project Timeline

| Milestone | Target Time | What to Submit / Prepare |
|---|---|---|
| **Project Proposal** | **Week 8** | Project title, team members, project description, proposed cloud services, and initial architecture diagram |
| **Project Progress Check** | **Week 12** | Brief update on completed work, working cloud services, architecture changes, current challenges, and remaining tasks |
| **Final Presentation & Demo** | **Week 15** | Short presentation explaining the project and cloud architecture, followed by a demonstration of the working application |
| **Final Project Report & Submission** | **Week 15** | README/report, final architecture diagram, screenshots, source code, team-member contributions, and other required project files |

> Specific due dates and presentation times will be posted on Blackboard/course schedule.

Do not wait until the final weeks to begin integrating your cloud services. Cloud configuration and service integration often take longer than expected.

---

## Project Milestones

### 1. Project Proposal

Each team will submit a short project proposal.

The proposal should include:

- Project title
- Team member names
- Brief description of the problem or application
- Intended users
- At least four proposed cloud services
- A brief explanation of the role of each service
- An initial architecture diagram
- Expected project scope and major features

The purpose of the proposal is to make sure the project is appropriately scoped and that the selected cloud services form a meaningful architecture.

Only **one proposal per team** is required.

---

### 2. Progress Check

During the second half of the semester, teams will provide a brief project progress update.

The update should identify:

- What has been completed
- Which cloud services are currently working
- Any changes to the original architecture
- Problems or challenges encountered
- Remaining work

The purpose of the progress check is to make sure that teams are making steady progress and to identify problems early.

---

### 3. Final Presentation and Demonstration

During the final week of class, each team will give a short presentation and demonstration of the project.

Your presentation should explain:

- What problem your project addresses
- Your cloud architecture
- Which cloud services you used
- Why you selected those services
- How the services interact
- What you learned while developing the project

You should also demonstrate the working application.

The demonstration is important. A project that exists only in slides or screenshots does not fully satisfy the project requirements.

---

### 4. Final Project Submission

Only **one final submission per team** is required.

Your final submission should include:

1. A `README` file that explains:
   - What the project does
   - Which cloud services are used
   - How the cloud services interact
   - How to set up, deploy, and run the application

2. Your final architecture diagram.

3. Screenshots showing the working application and important cloud components.

4. Well-commented source code for anything your team developed.

5. A short description of each team member's primary contributions.

6. Any other files necessary to understand or reproduce the project.

Make sure that all team members' names are clearly included in the submission.

---

## Project Ideas

You may choose any project topic, subject to instructor approval and appropriate scope.

Possible examples include:

- Cloud-based file or photo management application
- Weather or environmental data dashboard
- Collaborative notes or task-management application
- Online quiz or flashcard application
- IoT data collection and visualization system
- Event-driven data processing application
- AI-enabled web application
- Image analysis or classification application
- Translation application
- Scheduling application
- Cloud-hosted shopping or inventory application
- Scalable web application using managed instance groups and load balancing

These are only examples. You are encouraged to propose your own idea.

Try to choose something that interests you and that you would be proud to include in your portfolio.

---

## Project Scope

Keep the project achievable.

You have approximately half of the semester to complete the project, so avoid selecting an idea that requires building a very large application from scratch.

For example, you do not need to build a complete commercial application. A smaller working prototype that clearly demonstrates good cloud architecture is sufficient.

Focus on:

- cloud service integration,
- architecture,
- deployment,
- reliability,
- scalability where appropriate, and
- a working demonstration.

Do not spend most of your time building features that are unrelated to cloud computing.

---

## Using Existing Code, Tutorials, and AI Tools

You may use:

- Open-source libraries
- Frameworks
- Tutorials
- Google Cloud documentation and examples
- Codelabs or similar learning materials
- Starter code
- Generative AI tools

However, you must **understand the project that you submit**.

You may not simply copy an existing project or tutorial and submit it as your own.

If you begin with an existing example, tutorial, or starter project, you must:

1. Clearly cite the original source.
2. Significantly extend or modify it.
3. Integrate your own cloud architecture and project requirements.
4. Be able to explain how the application and cloud services work.

If you use generative AI to help create code, documentation, or other substantial project content, acknowledge that use in your project documentation.

During the final presentation, any team member may be asked to explain part of the architecture or implementation.

---

## Project Tips

- **Start early.** Do not wait until the final week to integrate your cloud services.
- Choose a project that is realistic for your team's experience and available time.
- Build and test one component at a time.
- Integrate services gradually instead of trying to build the entire system at once.
- Keep your architecture diagram updated as your project changes.
- Use Git or another version-control system to protect your work.
- Be proud of what you’ve worked on - ideally this will be part of your project portfolio that you can show off to future employers. That being said, given this is on the cloud it will probably be taken offline after class is over, given that you would have to start paying for it otherwise. As such, make backups or, at minimum, take screenshots!
- Cite tutorials, starter projects, libraries, and other resources that you use.
- Test your application before the final demonstration.
- Be prepared to explain why you selected each cloud service.
- **Watch your cloud costs.** Stop or delete resources that you are not using.
- After the course is finished, remove cloud resources that may continue generating charges.

---

## Team Responsibilities

All team members are expected to contribute meaningfully to the project.

Teams should divide responsibilities, but everyone should understand the overall architecture of the project.

The final submission must include a brief description of each team member's primary contributions.

If there is a serious imbalance in contributions, individual project grades may be adjusted.

---

## Team Member Issues

Working successfully as a team is part of the project experience.

If problems occur:

1. Communicate with your teammates early.
2. Discuss responsibilities and expectations clearly.
3. Do not wait until the final week to address a problem.
4. If your team cannot resolve an issue, contact me as soon as possible.

I can help with project scope, technical problems, or team issues, but it is much easier to help when problems are raised early.

---

## Most Important Advice

Do not think of this project as:

> "How can I use four cloud services?"

Instead, think:

> "What application do I want to build, and how can cloud services work together to support it?"

The goal is to create a **working application with a meaningful cloud architecture**, not simply to collect service names.






