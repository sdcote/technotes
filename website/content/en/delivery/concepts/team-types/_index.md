---
title: Team Types
description: >-
    Not all teams deliver value in the same way. Practices that work
    well for one type of team may not work well for others. Therefore, 
    it is essential to understand the different models of value
    delivery.
weight: 3
---

One of the most common mistakes seen in delivery teams today is trying to use delivery practices for software development on a team that does not (only) deliver software. As development teams take on different responsibilities, the traditional Scrum, Kanban, Extreme Programming (XP), Lean, and other software development methodologies fail to manage other types of work and value delivery.

Not all teams are the same—in fact, no two teams are the same—but there are some basic team types we have seen over the years. This section will cover the six basic team types.

## Product Team

Some teams meet the classical development model. These “code and compile” teams generally write source code and compile it into deployment artifacts. The deployment artifacts are then deployed into an execution environment, where they deliver value to the stakeholders.

When people think of development teams, this type of team usually comes to mind. This is the type of team all the blog posts, podcasts, and videos cover. Unfortunately, all those good ideas don’t apply well to the other team types.


## Packaged Application Team

There are teams that do not develop the artifacts deployed into execution environments but configure them to meet the needs of the stakeholders. This model involves development teams configuring deployed applications, not creating them. Organizations that purchase licenses to SaaS applications like SAP, Salesforce, ServiceNow, Jira, and others often need delivery teams to customize the deployments to meet the organization’s unique needs.

Packaged application teams do not usually deploy their applications. Instead, they make configuration changes, package those changes, and deploy them to the appropriate execution environments. These teams’ primary artifacts are configuration changes. For example, in ServiceNow, delivery teams create artifacts called “update sets.”

Well, there are many good practices these teams can adopt to make their lives easier. Some are well-known practices modified slightly to meet the needs of a packaged application team.

## Tools Team

Some teams assemble tools, data, and configurations to meet their users' needs. Tools teams tend to deploy tool instances to support user demands. Contrast this with applications teams that only configure deployed applications. 

These teams use packaged applications to implement integrations between systems, using tools like MuleSoft, Boomi, IBM Integrator, and webMethods. They do more than manage configurations; they create entire solutions that are deployed into their users’ execution environments.

Again, many good practices can be applied to this team’s delivery stream. They need to be tailored to meet the unique needs of this type of team.

Data analytics teams tend to create data sets deployed into execution environments. You might be on a tools team if you are a data scientist or deliver machine learning models.

## Operations Team

Operations teams configure and maintain execution environments. They tend to deal with change and configuration management, ensuring applications are deployed correctly, execute reliably, and remain available. Operations teams do not always deliver deployable artifacts; they perform tasks at their users' requests.

These teams tend to receive requests from IT Service Management (ITSM) systems, which track the operational state of enterprise systems and generate operations requests in response to configuration and change management systems, preventative maintenance, and incidents.

## Services Team

Services teams, a.k.a. Shared Services teams, are any team that responds to requests for service. Services like consultation, design, training, administration, and troubleshooting might be generic. Services teams support requests that fall outside IT operations.

Again, these teams do not consistently deliver artifacts but perform tasks supporting user requests. When they provide artifacts, they are usually unique and user-specific.

## Hybrid Team

Lately, an increasing number of teams are delivering value using multiple modes. It is becoming challenging to encounter a team that fits nicely into one classification. Teams are getting demand requests from various sources.

This causes confusion among some teams when they try to apply a methodology to their delivery process. For example, Scrum does not support Services and Operations teams well. Since teams deliver value differently, they find adopting one method to fit their needs difficult. This is why adopting individual practices is better than entire methodologies. Selecting the particular practices related to the team's delivery model results in a customized delivery workflow.

### DevOps

A "DevOps" team is an example of a hybrid team. Modern teams are becoming responsible for the entire application delivery. Source code is compiled, tested, and deployed into execution environments, where it is then monitored and managed. This combines traditional development methodologies with traditional operations models.

If a hybrid team tries to operate as a scrum team, it will have problems managing operations. This is often because the team has two sources of work: the product backlog and operational service queues. The ITSM system may send them incidents and service requests. Hybrid teams can have multiple sources of work and need practices that help them deliver value across all sources.

"DevSecOps" can add to the confusion for teams as Security methodologies are continuously evolving, requiring teams to coordinate multiple methods and sources of work (customer demand), adding to workflow overhead to value delivery. 

