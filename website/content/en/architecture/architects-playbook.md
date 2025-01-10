---
title: The Architects Playbook
description: >-
     Gathering a common understanding of the subject system quickly is critical 
     to the efficient execution of any project. This is my standard playbook for 
     engaging all new clients and projects as an architect.
weight: 200

---
As a consultant, I work with various clients and contribute to the development of different systems. Most of my work involves enhancing or troubleshooting existing systems. When taking on the role of an architect, it is crucial for me to understand not only the requested changes but also the environment in which the target system will operate.

A key factor in my success has been quickly grasping the system's intricacies. By gathering information and organizing it in easily accessible formats, I can focus on essential aspects and effectively communicate goals, objectives, and expectations.

Throughout my career, creating documentation ranging from high-level concepts to detailed models has enabled me to provide prompt feedback to clients and establish alignment among stakeholders and delivery teams within hours of starting a project.

Below are the steps I follow in each architecture engagement with my clients.

## 1. Documentation Standards

Determine what the client uses to generate documentation. This includes what office suite to be used.

Determine the preferred graphic format. SVG tools like Inkscape are my preferred tool, but the client may be limited in what formats are readable. Some use Microsoft Visio, others might use LucidChart. In any case, be sure to establish a standard format and begin working on that technology.

Determine what document repository strategy the client uses. This might be a Wiki framework like Confluence or a repository like Microsoft SharePoint. In cases where there is no repository, seek to create one. It is best to place all documentation in one location so information is easy to locate. At least, with one location, all searches can start in one place and link to other locations as necessary.

If there are no repository standards, consider creating a repository with a static site generator like Hugo and use cloud provider BLOB storage services to host the sites. GCP buckets are a quick and easy way to establish secure file-sharing services. If the client does not allow the cloud to your project, ask for a VM and install an on-prem repository.

Create a project page in the document repository

Create an architecture folder under the project page.

Ensure the documents are accessible by everyone on the project and email a link to everyone on the project at this point.

## 2. System Qualities

It is critical to begin discussions with key stakeholders and establish non-functional requirements in the form of a prioritized list of system qualities.

Create a system qualities document in the architecture folder in the document repository.

Use the project kick-off meetings to communicate the need for this list. It will take several days to get everyone engaged and contributing to this list so the request for this list of qualities must be raised early. Send a link to the systems qualities document in meeting invites and ask the participants to view the document before the meeting.

The list should contain only 3 columns:
- Rank
- Quality Name
- Quality Description

Once the prioritized System Qualities List has been created, it is time to start asking for quality scenarios. These are optional, but useful in generating automated quality tests.

Quality scenarios can be created at any time during the project.

## 3. System Context Model

Start gathering information for a system context model. Meet with the project manager and begin collecting a list of contacts for all of the connected systems.

Create a system context document in the architecture folder in the document repository.

Use the Statement of Work (SOW) to begin gathering information for the model. It should contain information about the requested system.

Each system in the model should contain the following information:
- Name
- Architecture Contact (Who has the strategic details for this system)
- Technical Contact (Who has the technical details for this system)
- Operations Contact (who know how this system operates)
- Product Owner/Manager
- List of all data sent to the system
- List of all data received from the system

Schedule an initial discovery session with the project manager, product owner, and any other team member available to begin discovery. The goal is to seed the context model with information and to determine what more detailed system context discovery sessions are necessary. Send links to the systems qualities document and the system context model in meeting invites and ask the participants to view the documents before the meeting. Start with one hour.

This is the time to also start creating an integration catalog. This is just a spreadsheet that tracks the details for each line in the system context. For now, all that is required for each line is the following information:
- Integration Name
- Origination system name
- Destination system name
- Technical Contact (Who has the technical details for this interface)
- Operations Contact (who know how this interface operates)

Once the system context model has stabilized and all the stakeholders have agreed to its accuracy, the Integration Catalog can be filled out with the details.

## 4. Integration Catalog

As the System Context is being created, integrations with external entities are being identified. As each external entity is discovered catalog relationships between each system.

While the system context model may only have a single line associating the two systems, many integrations may exist between them. Identify all data being sent to and received from the subject system. 

Each integration entry in the catalog should contain the following information:
- Integration Name
- Origination system name
- Destination system name
- Direction (import, export)
- Type (batch, message, stream, request/response)
- Data (describe the data being transferred)
- Format (JSON, XML, Binary, CSV, FFL)
- Encoding (UTF8, ASCII, Unicode)
- Schedule (describe when and how often data is transferred)
- Origination Technical Contact (Who has the technical details creating the data for this interface)
- Destination Technical Contact (Who has the technical details consuming the data for this interface)
- Operations Contact (who know how this interface operates)

## 5. Decision Log

The architecture decision log is created when there is a decision to be made for the new system.

The log can be started when an existing decision has been previously made for the system. In this case, the details of the decision should be captured. This will result in a discussion where the decision-makers will be asked for details about the decision.

When logging previously made decisions, it is often discovered that a careful trade-off analysis was not performed and decision-makers may get defensive. The goal is to log what data there is about the decision and record it in the log. Previously made decisions do not have to be complete.

## 6. Component Model

As architecturally significant components are identifiers, they should be placed in a component model. This mode would contain at least a name and a description of the function of the component.

While this can be a simple component diagram, diagrams can be difficult to maintain. Do not worry about diagramming, just log the name and details of components identified to be important to the system.

Components need not be classes or physical objects in the system.

## 7. Sequence Models

If there is confusion about the behavior of the system, start generating sequence diagrams using the component model as the source of entities.

Any new components discovered during sequence model discussions should be placed in the component model.

As discussions continue regarding designs, ask the designers to walk through use case scenarios and document how components interact.

## 8. Deployment Model

At some point in the design of the system, physical deployments will be discussed. These discussions should be used to generate a physical model of where components are deployed in the system.

## 9. Failure Mode Effect Analysis

Once the deployment model is started, failure mode effect analysis (FMEA) discussions can begin.

Start identifying and rating every failure mode the team can identify.

Immediately raise risk issues for the highest failure modes and request they be addressed.

