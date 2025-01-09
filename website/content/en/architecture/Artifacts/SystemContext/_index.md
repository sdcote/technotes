---
title: System Context
description: Understanding the relationship of the architected system in relationship with other systems and actors is critical for collective understanding of the problem domain.
weight: 2
---
{{< alert title="Note" color="success">}}This page is a collection of concepts and has not been formatted into a finished page.{{< /alert >}}

This is not a very big deliverable, but it is important for the sake of conveying the scope of the project and identifying integration points.

This is normally just a circle representing the system with lines associating the system to other entities.

The system context model is usually a diagram which looks like a wheel with the system under consideration in the center.

Each of the systems on the diagram is described. It purpose, owners, business value and anything else which can assist the designers in making technical decisions.

Each of the lines are described as this is the description of the integration required.

Research for this diagram often uncovers integrations which only a few people in the organization know.

Do not model indirect relationships unless there is a good reason.

## System Descriptions
As the systems are identified, it is very helpful to record the owners of the applications and technical points of contact. Later in the project, when there are questions, this list of very helpful on only in design of the system, but during implementation and operations. It acts as the map of the business landscape enabling you to contact the right people at the right time.

When you have a decision which affects other systems, the System Context Model descriptions are a good place to get email addresses of Subject Matter Experts, Application Owners, Operations Leads and management. If you are working in a regulated industry (finance, public utilities) data may cross organizational boundaries and be subject to special audit.

## Dependencies
Each source system is a potential data dependency. You may find that timings of data flows will have an impact on how your system operates. 

For example, you may get batch data from another system at 3 in the morning and that data is required by a dependent system at 4. That only gives you 1 hour to process that data. Is it enough time? What if data doubles? What if the source system is late with the data?

## Example Discovery
While talking about a well-know integration, this exchange happened:

Them: "So we generate the asset list for you and place it in the export directory."

Me: "And that includes all the assets for your business unit?"

Them: "Yeah, except for printers and monitors. You get that list of our assets each month from Karen". 

Me: "Where does she get them?"

Them: "Well, they are tracked in some monitoring system Finance wrote that gets it data from order entry and receiving. She usually spends the last few days in the accounting period generating that list and emails a spreadsheet for Chris to import."

## Case Study Example
We are a solutions provider with the goal of creating a highly reusable Data Acquisition and Processing platform. We don't have specific systems to place in our systems context, but we can characterize the systems based on our experience and in discussions with potential clients.

We know there will be devices in the environment and that they will be the source of events and metrics. They will either communicate with us directly or through an intermediary system (a.k.a. Head-End).

We expect there will be systems needing access to the data managed by our system. The question is how to we make that data available? For now, the how is not as important as what; what data is required by the external system. We will assume that all events and metrics we managed will be available to external systems.

## Takeaway
The System Context (Model) is a valuable tool in the discovery of the environment in which the system exists. It literally illustrates the size and complexity of the project is one simple diagram. It is useful in not only discovery discussions, but having a record for the project of potential dependencies and key points of contact for each of the systems.

Just the act of documenting the system context diagram results in exchanges that lead to the discovery of little known systems.

Documentation may be useless, but documenting is priceless.