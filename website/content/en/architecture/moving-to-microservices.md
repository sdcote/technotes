---
title: Moving to Microservices
description: >-
     Breaking monoliths can be difficult, particularly with legacy applications. It is possible
     though. Here is what was found to work for several large companies. 
weight: 200
---

{{< alert color="warning" title="Work In Progress" >}}This page contains fundamental truths relating to systems design and where the concept of architecture relates to that process. This page needs to be formatted into a logical unit.{{< /alert >}}

To convert an existing team or application to microservices, start with creating a Two Pizza Team which contains at least one member from the original application team. This team will initially be responsible for creating and exposing services to external components.

Another question solved by this approach is, "How do we start becoming agile?

How?

Try breaking the application into three basic layers:

Presentation - Web & CLI - Web Developers work here and deploy web apps

Processing - Services/Methods - Backend Developers live here (often is composed of multiple 2P teams)

Persistence - Data Base (Relational, Document, Queue, Table, Key-Value, etc.)

Salt new teams with members from the existing team. Normally there is one lead web developer which might go to the Presentation team and one Database lead perfect for the Persistence team.

See also "Remove the V from MVC" for thoughts on MVC issues.

# Rolling Refactor

Start with persistence. It often takes code out of the Processing domain and makes processing simpler. 

By starting with Persistence, the team can engineer a set of services that the Processing Layer can use to handle data persistence for the application. This will involve significant changes in both layers. Persistence changes can begin rolling out in a matter of weeks. Migration persistence to services will be a long-term project often covering the life of the application.

Next, start developing services the Presentation layer can use. This will involve major changes to the Presentation architecture, increasingly relying on AJAX calls. This is a significant amount of effort for Web Developers. At some point, the Presentation layer will require complete refactoring (e.g. Angular) to make the best use of services.

It is risky to try changing Persistence and Presentation at the same time. This is because the Processing domain will require an enormous amount of change, resulting in the Processing teams becoming the bottleneck. The amount of change in the Processing domain will also introduce errors and the teams try to keep up with the changes in the presentation and persistence teams.
